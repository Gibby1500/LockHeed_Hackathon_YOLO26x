# evaluate run

- status: **OK**, runtime 25.7 s, figures rendered: 1
- notebook: `00_starter_notebook_fixed.ipynb` sha256 `87ab086d8db787507045ee3a67e64420446d7e4270157fc36540d5509902df2d`
- code_tree_sha256: `5b7c2be416d2ce96c7e0783bb552ce09e34afe47ef21234f3a272e9fccc49bb8`
- versions: python 3.14.6, torch 2.13.0+cu132, ultralytics 8.4.163, GPU NVIDIA GeForce RTX 3070 Laptop GPU

## Key notebook output
```
RUN_MODE = 'evaluate'   RUN_NAME = 'evaluate_yolo26s_640_20260926_020213'
evaluate mode: training-data conversion skipped
mode: evaluate | GPU: NVIDIA GeForce RTX 3070 Laptop GPU | model: C:\Users\diego\OneDrive\Documents\GitHub\Lockheed-Hackathon\uprm-hackathon-2026\weights\yolo26n.pt
epochs: 0 | train batch: 8 | train fraction: 1.0 | evaluated val images: 199
evaluate mode: no training run is configured
evaluate mode: training skipped
validation mAP@50 (plastic_bag), all 199 evaluated val images: 0.1079  (0.10785218649967149)
validation mAP@50 (plastic_bag), starter-notebook loader (drop_last=True): 0.1087  (0.10872369615191763)
inference settings: {'nms_kwarg': 'nms', 'nms_value': None, 'end2end_head': False, 'imgsz': 640, 'conf': 0.001, 'iou': 0.7, 'max_det': 300, 'augment': False, 'device': '0'}
No training history available (evaluate mode without the checkpoint's results.csv).
  at conf >= 0.3: bags found 9/537, missed bags 528, false positives 38
RUN_OFFICIAL_TEST is False - official test data not downloaded.
RUN_OFFICIAL_TEST is False - no test loader.
RUN_OFFICIAL_TEST is False - official test set not scored.
```
