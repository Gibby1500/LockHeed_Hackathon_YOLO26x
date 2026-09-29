# LockHeed_Hackathon_YOLO26x

Local review copy based on the Lockheed Martin Hackathon notebook and the supplied
`00_starter_notebook_fixed_26x (3).ipynb`. The notebook is preserved byte-for-byte,
including its authorship, code, configuration, and saved outputs.

## YOLO26x configuration

- Pretrained starting weights: `yolo26x.pt` (downloaded by Ultralytics on first use if absent).
- Training/evaluation image size: 640; batch size: 4; epochs: 100; seed: 42.
- Task: plastic-bag detection from KITTI-format annotations.
- Official test execution remains disabled (`RUN_OFFICIAL_TEST = False`).


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
