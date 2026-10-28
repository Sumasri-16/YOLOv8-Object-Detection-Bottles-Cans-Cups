# YOLOv8s Object Detection: Bottles, Cans and Cups

## Overview
This project explores object detection with Ultralytics YOLOv8s for three classes: `bottle`, `can`, and `cup`. It uses the Roboflow Bottles and Cups Detection dataset and a small set of personally captured images annotated in CVAT.

## Dataset
- Roboflow dataset version: 27
- Roboflow train images: 11,268
- Roboflow validation images: 1,071
- Roboflow test images: 535
- Personal images: 43
- Existing personal bounding boxes: 50 (24 bottles, 4 cans, 22 cups)

The personal annotations are below the assignment target of 150 boxes. This limitation is disclosed rather than hidden.

## Model and training setup
- Model: YOLOv8s pretrained weights
- Image size: 512
- Batch size: 16
- Seed: 257058
- Baseline training: 46 epochs
- Confidence threshold used for evaluation: 0.28

## Original baseline results
The following are the results recorded in the original notebook for the Roboflow test split:

| Metric | Result |
|---|---:|
| Precision | 0.9785 |
| Recall | 0.9488 |
| F1-score | 0.9634 |
| mAP@0.5 | 0.9586 |
| mAP@0.5:0.95 | 0.8552 |

These values describe the original baseline evaluation. They are not results from the corrected workflow notebook.

## Classes
| Class | Test images | Instances | Precision | Recall | mAP@0.5 |
|---|---:|---:|---:|---:|---:|
| Bottle | 163 | 188 | 0.984 | 0.973 | 0.971 |
| Can | 155 | 223 | 0.958 | 0.928 | 0.940 |
| Cup | 123 | 164 | 0.994 | 0.945 | 0.964 |

## Limitations and next steps
- The personal annotations currently total 50 bounding boxes, below the 150-box target.
- The original personal test split overlapped with training images, so its reported perfect precision and recall should not be treated as an independent test result.
- Experiment 2 was interrupted before completion in the available logs.
- The corrected workflow notebook prepares a clean personal train/validation/test split and code for two experiments and error analysis. The corrected experiments must be run before reporting their results.

## Files in this repository
- `YOLO_Assignment5_Corrected_Workflow.ipynb` — corrected workflow notebook (run in Google Colab).
- `YOLOv8s_Lab_Assignment5_Report.pdf` — original report documenting the baseline and limitations.
- `YOLO_Assignment5_Annotation_Audit.txt` — audit of the existing personal annotations.
- `results/` — optional folder for selected prediction images and exported result tables after you generate them.

## Dataset and attribution
The Roboflow dataset used in the original work is identified as Bottles and Cups Detection, version 27, with CC BY 4.0 noted in the original report. Check the dataset page for the correct attribution details and follow its license terms if redistributing any dataset material.

## Reproducibility
The corrected workflow requires Google Colab, Ultralytics, and access to the Roboflow dataset. Do not commit API keys, private credentials, the full dataset, or large model weight files to this repository.
