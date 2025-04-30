.
├── README.md
├── __pycache__
│   ├── train_test.cpython-310.pyc
│   └── utils.cpython-310.pyc
├── configs
│   ├── __pycache__
│   │   └── datasets_config.cpython-310.pyc
│   ├── datasets_config.py
│   └── qm9_config.yaml
├── data
│   ├── competition
│   │   ├── competition_smiles.pickle
│   │   ├── test.npz
│   │   ├── train.npz
│   │   └── valid.npz
│   ├── competition_smiles.pickle
│   ├── test.npz
│   ├── train.npz
│   └── valid.npz
├── egnn
│   ├── __pycache__
│   │   ├── egnn_new.cpython-310.pyc
│   │   └── models.cpython-310.pyc
│   ├── egnn.py
│   ├── egnn_new.py
│   └── models.py
├── equivariant_diffusion
│   ├── __init__.py
│   ├── __pycache__
│   │   ├── __init__.cpython-310.pyc
│   │   ├── en_diffusion.cpython-310.pyc
│   │   └── utils.cpython-310.pyc
│   ├── distributions.py
│   ├── en_diffusion.py
│   ├── overview.png
│   ├── training.png
│   └── utils.py
├── main.py
├── main.py_bak_20250417_2205
├── output.txt
├── outputs
│   ├── edm_competition
│   │   ├── args.pickle
│   │   ├── generative_model.npy
│   │   ├── generative_model_ema.npy
│   │   └── optim.npy
│   ├── edm_competition_resume
│   └── edm_competition_resume_20250420_110918
│       ├── args.pickle
│       ├── args_0.pickle
│       ├── ......
│       ├── args_5.pickle
│       ├── eval
│       │   ├── analyzed_molecules
│       │   │   ├── molecule_000.xyz
│       │   │   ├── molecule_001.xyz
│       │   │   ├── molecule_002.xyz
│       │   │   ├── ......
│       │   │   └── molecule_9999.xyz
│       │   └── data.pkl
│       ├── generative_model.npy
│       ├── generative_model_0.npy
│       ├── ......
│       ├── generative_model_5.npy
│       ├── generative_model_ema.npy
│       ├── generative_model_ema_0.npy
│       ├── ......
│       ├── generative_model_ema_5.npy
│       ├── optim.npy
│       ├── optim_0.npy
│       ├── ......
│       └── optim_5.npy
├── qm9
│   ├── __init__.py
│   ├── __pycache__
│   │   ├── __init__.cpython-310.pyc
│   │   ├── analyze.cpython-310.pyc
│   │   ├── bond_analyze.cpython-310.pyc
│   │   ├── dataset.cpython-310.pyc
│   │   ├── losses.cpython-310.pyc
│   │   ├── models.cpython-310.pyc
│   │   ├── rdkit_functions.cpython-310.pyc
│   │   ├── sampling.cpython-310.pyc
│   │   ├── utils.cpython-310.pyc
│   │   └── visualizer.cpython-310.pyc
│   ├── analyze.py
│   ├── bond_analyze.py
│   ├── data
│   │   ├── __init__.py
│   │   ├── __pycache__
│   │   │   ├── __init__.cpython-310.pyc
│   │   │   ├── __init__.cpython-312.pyc
│   │   │   ├── args.cpython-310.pyc
│   │   │   ├── args.cpython-312.pyc
│   │   │   ├── collate.cpython-310.pyc
│   │   │   ├── collate.cpython-312.pyc
│   │   │   ├── dataset_class.cpython-310.pyc
│   │   │   ├── dataset_class.cpython-312.pyc
│   │   │   ├── utils.cpython-310.pyc
│   │   │   └── utils.cpython-312.pyc
│   │   ├── args.py
│   │   ├── collate.py
│   │   ├── dataset_class.py
│   │   ├── prepare
│   │   │   ├── __init__.py
│   │   │   ├── __pycache__
│   │   │   │   ├── __init__.cpython-310.pyc
│   │   │   │   ├── __init__.cpython-312.pyc
│   │   │   │   ├── download.cpython-310.pyc
│   │   │   │   ├── download.cpython-312.pyc
│   │   │   │   ├── md17.cpython-310.pyc
│   │   │   │   ├── md17.cpython-312.pyc
│   │   │   │   ├── process.cpython-310.pyc
│   │   │   │   ├── process.cpython-312.pyc
│   │   │   │   ├── qm9.cpython-310.pyc
│   │   │   │   ├── qm9.cpython-312.pyc
│   │   │   │   ├── utils.cpython-310.pyc
│   │   │   │   └── utils.cpython-312.pyc
│   │   │   ├── download.py
│   │   │   ├── md17.py
│   │   │   ├── process.py
│   │   │   ├── qm9.py
│   │   │   └── utils.py
│   │   └── utils.py
│   ├── dataset.py
│   ├── losses.py
│   ├── models.py
│   ├── property_prediction
│   │   ├── README.md
│   │   ├── __init__.py
│   │   ├── main_qm9_prop.py
│   │   ├── models
│   │   │   ├── __init__.py
│   │   │   └── gcl.py
│   │   ├── models_property.py
│   │   └── prop_utils.py
│   ├── rdkit_functions.py
│   ├── sampling.py
│   ├── utils.py
│   └── visualizer.py
├── requirements.txt
├── sample.py
├── sample.sh
├── train.sh
├── train_test.py
├── use_tutorial.md
├── utils.py
└── wandb
    ├── debug-internal.log -> offline-run-20250420_110917-be6jp2t0/logs/debug-internal.log
    ├── debug.log -> offline-run-20250420_110917-be6jp2t0/logs/debug.log
    ├── latest-run -> offline-run-20250420_110917-be6jp2t0
    ├── offline-run-20250417_211722-ygayhibi
    │   ├── files
    │   │   ├── output.log
    │   │   ├── requirements.txt -> /root/sais_third_material_baseline/requirements.txt
    │   │   └── wandb-metadata.json
    │   ├── logs
    │   │   ├── debug-core.log -> /root/.cache/wandb/logs/core-debug-20250417_211722.log
    │   │   ├── debug-internal.log
    │   │   └── debug.log
    │   ├── run-ygayhibi.wandb
    │   └── tmp
    │       └── code
    ├── offline-run-20250417_211954-f3g3tokr
    │   ├── files
    │   │   ├── output.log
    │   │   ├── requirements.txt -> /root/sais_third_material_baseline/requirements.txt
    │   │   └── wandb-metadata.json
    │   ├── logs
    │   │   ├── debug-core.log -> /root/.cache/wandb/logs/core-debug-20250417_211954.log
    │   │   ├── debug-internal.log
    │   │   └── debug.log
    │   ├── run-f3g3tokr.wandb
    │   └── tmp
    │       └── code
    ├── offline-run-20250417_212442-m8naect5
    │   ├── files
    │   │   ├── output.log
    │   │   ├── requirements.txt -> /root/sais_third_material_baseline/requirements.txt
    │   │   └── wandb-metadata.json
    │   ├── logs
    │   │   ├── debug-core.log -> /root/.cache/wandb/logs/core-debug-20250417_212442.log
    │   │   ├── debug-internal.log
    │   │   └── debug.log
    │   ├── run-m8naect5.wandb
    │   └── tmp
    │       └── code
    ├── offline-run-20250417_212936-mffiuw4q
    │   ├── files
    │   │   ├── output.log
    │   │   ├── requirements.txt -> /root/sais_third_material_baseline/requirements.txt
    │   │   └── wandb-metadata.json
    │   ├── logs
    │   │   ├── debug-core.log -> /root/.cache/wandb/logs/core-debug-20250417_212936.log
    │   │   ├── debug-internal.log
    │   │   └── debug.log
    │   ├── run-mffiuw4q.wandb
    │   └── tmp
    │       └── code
    ├── offline-run-20250417_213358-jzqv9757
    │   ├── files
    │   │   ├── output.log
    │   │   ├── requirements.txt -> /root/sais_third_material_baseline/requirements.txt
    │   │   └── wandb-metadata.json
    │   ├── logs
    │   │   ├── debug-core.log -> /root/.cache/wandb/logs/core-debug-20250417_213358.log
    │   │   ├── debug-internal.log
    │   │   └── debug.log
    │   ├── run-jzqv9757.wandb
    │   └── tmp
    │       └── code
    ├── offline-run-20250417_220800-w8jjpdav
    │   ├── files
    │   │   ├── output.log
    │   │   ├── requirements.txt -> /root/sais_third_material_baseline/requirements.txt
    │   │   └── wandb-metadata.json
    │   ├── logs
    │   │   ├── debug-core.log -> /root/.cache/wandb/logs/core-debug-20250417_220800.log
    │   │   ├── debug-internal.log
    │   │   └── debug.log
    │   ├── run-w8jjpdav.wandb
    │   └── tmp
    │       └── code
    └── offline-run-20250420_110917-be6jp2t0
        ├── files
        │   ├── output.log
        │   ├── requirements.txt -> /root/sais_third_material_baseline/requirements.txt
        │   └── wandb-metadata.json
        ├── logs
        │   ├── debug-core.log -> /root/.cache/wandb/logs/core-debug-20250420_110917.log
        │   ├── debug-internal.log
        │   └── debug.log
        ├── run-be6jp2t0.wandb
        └── tmp
            └── code

60 directories, 10178 files
