#### baseline完成了什么工作？有什么效果？

baseline是赛事方提供一个基础的baseline的改动版，仍然利用等变扩散模型(EDM)来生成分子结构，但减少了训练时间和成本，以方便新手越过这道门槛。

Baseline提供了一个端到端的分子生成框架，能够直接生成3D分子结构，而非仅限于分子图[^1]或SMILES表示[^2]

[^1]: 类似于这种的2d表示 ![](000-attachments/Pasted%20image%2020250423210720.png)

[^2]: SMILES（Simplified Molecular Input Line Entry System，简化分子线性输入规范）。一种用ASCII字符串明确描述分子结构的规范。SMILES通过一串字符来描述一个三维化学结构，它将化学结构转化成一个生成树，并采用纵向优先遍历树算法。SMILES字符串可以被大多数分子编辑软件导入并转换成二维图形或分子的三维模型。
