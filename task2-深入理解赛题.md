---
tags:
  - DataWhale/春训
  - HW
author: Prince-Ranbow
---

## 1 深入理解baseline方案

### 1.1 baseline完成了什么工作？有什么效果？

baseline是赛事方提供一个基础的baseline的改动版，仍然利用等变扩散模型(EDM)来生成分子结构，但减少了训练时间和成本，以方便新手越过这道门槛。

baseline提供了一个端到端的分子生成框架，能够直接生成3D分子结构（存储为pkl文件格式），而非仅限于分子图[^1]或SMILES表示[^2]。

通过等变神经网络(EGNN)，保证了生成结构的旋转、平移不变性。这对分子性质预测至关重要，因为分子的势能，不会随着分子的位置、角度等而发生变化；而同时，分子内部的相互作用力，又是随着分子的位置、角度等而同步变化的。

使用扩散模型作为生成框架，能够产生多样化且合理的分子构象；同时又支持条件生成，为复赛任务提供了基础


### 1.2 需要了解哪些信息、才能设计出baseline？

分子的设计需要符合一定的条件，比如键能、键长、键角要合适，甚至更进一步，分子生成的结果，需要符合特定的性质（为了药物开发、材料研发等等），这些都是“分子生成的条件”。同时，为了保障生成结果的多样性，需要生成的过程是带有随机性的，以探索更多分子组合的可能性。

- 为了表示分子结构，需要同时考虑原子类型（比如C, H, O, N, F, P, S, Cl, Br等）和3D坐标。
- 为了保证分子结构的合理性，需要符合特定的键能、键长、键角的约束，甚至分子整体性质的约束（比如能量、光谱等）
- 因为其它神经网络，旋转分子意味着将输入旋转，这将导致不同的输出。而对于分子本身，旋转并不会改变分子的势能、旋转会同步改变分子内部的力。同时，分子的性质与其绝对位置和方向无关。为了保证这个“等变性/不变性”，需要构造等变神经网络[^3]

在“发散思维”和“现实情况”的博弈之下，Baseline使用等变扩散模型解决了这些问题：***等变神经网络(EGNN)确保了旋转平移不变性，扩散模型提供了生成多样性，条件生成机制允许控制分子性质***


### 1.3 要如何才能翻译成代码语言？
既然已经看到结果了，那么就学习baseline的各个组件吧~

|                                                               |                                                                               |
| ------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| ![\|178](000-attachments/Pasted%20image%2020250423213320.png) | 进入baseline的目录<br><br>可看到文件架构如图所示<br><br>完整的[tree](tree.md)<br><br>下面将逐一组件进行学习 |

#### 数据处理与加载
QM9是一个包含134k个分子的数据集，为小有机分子提供了相关、一致且全面的量子化学空间的量子化学性质。网上有大量关于这个数据集的介绍。
- [Quantum chemistry structures and properties of 134 kilo molecules](https://figshare.com/collections/Quantum_chemistry_structures_and_properties_of_134_kilo_molecules/978904)
- [QM9 Dataset | Papers With Code](https://paperswithcode.com/dataset/qm9)
```python
# 获取QM9数据集的配置信息
dataset_info = get_dataset_info(args.dataset, args.remove_h)
# 获取原子编码器和解码器
atom_encoder = dataset_info['atom_encoder']
atom_decoder = dataset_info['atom_decoder']
# 加载数据
dataloaders, charge_scale = dataset.retrieve_dataloaders(args)
```

数据处理部分读取QM9分子数据集，并处理成模型可用的格式。包括元素编码、坐标信息等。
`atom_encoder` 和 `atom_decoder` 对应着题目中的生成分子的构成原子为 `['H', 'C', 'N', 'O', 'F','P','S','Cl','Br']`











[^1]: 类似于这种的2d表示 ![](000-attachments/Pasted%20image%2020250423210720.png)

[^2]: SMILES（Simplified Molecular Input Line Entry System，简化分子线性输入规范）。一种用ASCII字符串明确描述分子结构的规范。SMILES通过一串字符来描述一个三维化学结构，它将化学结构转化成一个生成树，并采用纵向优先遍历树算法。SMILES字符串可以被大多数分子编辑软件导入并转换成二维图形或分子的三维模型。

[^3]: 可以参考[Bohrium | AI for Science with Global Scientists](https://bohrium.dp.tech/notebooks/9619364424)
