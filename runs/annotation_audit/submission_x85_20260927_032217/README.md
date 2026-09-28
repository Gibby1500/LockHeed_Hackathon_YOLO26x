# Validation annotation audit (for organizer review)

Examples of high-confidence false positives and missed bags on the **validation** split. No label file was modified and the official test set was not used.

Colours: green = labelled bag, blue = model prediction kept at the threshold, red = the false positive in question (with its confidence), magenta = the missed labelled bag. Right panel = enlarged crop.

`suggested_category` is produced by simple geometric rules (see `basis`); it is a starting point, **not a verdict**. Fill `reviewed_category` in `audit_examples.csv` after looking at each image.

| run | checkpoint | threshold | kind | model error | suspected missing annotation | questionable ground-truth box | ambiguous object |
|---|---|---|---|---|---|---|---|
| submission_640 | best.pt | 0.7460 | false_positive | 7 | 0 | 0 | 0 |
| submission_640 | best.pt | 0.7460 | missed_bag | 396 | 0 | 1 | 0 |

Counts cover every error at the threshold; `examples/` holds the selected subset (30 images): the most confident false positives, bags never detected at any confidence, and missed bags spread across sizes.
