# LockHeed_Hackathon_YOLO26x

Local review copy based on Joshua-Rivera/Lockheed-Hackathon and the supplied
`00_starter_notebook_fixed_26x (3).ipynb`. The notebook is preserved byte-for-byte,
including its authorship, code, configuration, and saved outputs.

## YOLO26x configuration

- Pretrained starting weights: `yolo26x.pt` (downloaded by Ultralytics on first use if absent).
- Training/evaluation image size: 640; batch size: 4; epochs: 100; seed: 42.
- Task: plastic-bag detection from KITTI-format annotations.
- Official test execution remains disabled (`RUN_OFFICIAL_TEST = False`).

## Contents and provenance

- `event_materials/00_starter_notebook_fixed_26x.ipynb`: your supplied notebook.
- `event_materials/img/`: accompanying illustrations from Joshua's checkout.
- `data/`: available KITTI-format dataset from that checkout.
- `yolo_data/`: its existing converted dataset. The notebook refreshes data.yaml for this machine when preparing training.
- `models/`, `weights/`, `runs/`: available historical weights, outputs, logs, and executed notebooks copied from Joshua's checkout. These include other model sizes and smoke tests; they are not claimed as results from this YOLO26x notebook.
- `models/imported_downloads/`: `best (1).pt` and `best_p95.pt` from Downloads. Both contain YOLO26x metadata and run name `full_cmpX_yolo26x_train640_eval640_b4_ep100_20260926_214457`, which appears in the supplied notebook outputs. Metadata was inspected without loading/executing the checkpoints. They are not automatically selected for evaluation or training.
- `docs/artifact_manifest.csv`: source path, size, and SHA-256 for every copied file.

Datasets, model weights, and training outputs are included and are not ignored.
Git LFS attributes cover checkpoints and binary image/archive assets for a future commit.
The pretrained `yolo26x.pt` was not found among the copied assets; no download was run.
Existing logs and notebook outputs may reference their original machine's paths.

## Setup and use

From this repository root, in PowerShell:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python -m jupyterlab event_materials/00_starter_notebook_fixed_26x.ipynb
```

Use a CUDA-capable PyTorch environment for training. Dependency pins are inherited
from the source notebook/project; installation and GPU execution have not been tested
in this review copy. Review the configuration cell before running the notebook:
its default `RUN_MODE = "full"` starts 100 epochs when the training cells are executed.
For evaluation, set `RUN_MODE = "evaluate"` and choose a confirmed checkpoint via
`EVAL_CHECKPOINT`. Existing saved outputs are historical, not newly generated validation.

## Review status

The user approved the initial local commit, including datasets, weights, and outputs.
No GitHub remote has been configured; publishing remains a separate step requiring
approval. No training, package installation, or official test download was performed
during preparation.
