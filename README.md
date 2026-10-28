# YOLOv8-Based Object Detection

## Project Overview
This project explores object detection using YOLOv8 to identify three object classes: bottles, cans, and cups. It combines a public dataset with personally collected and annotated images to study model training and evaluation.

## Objectives
- Detect bottles, cans, and cups in images.
- Train an object detection model using YOLOv8.
- Evaluate model performance using precision, recall, and mean Average Precision (mAP).
- Analyze prediction errors and compare experimental configurations.

## Technologies
- Python
- Ultralytics YOLOv8
- PyTorch
- OpenCV
- Roboflow
- Google Colab

## Dataset
The project uses a public bottles-and-cups dataset and a personal image dataset. Personal images are annotated using bounding boxes for the three target classes.

## Experiments
The notebook includes a baseline training workflow and a second experiment with Mosaic augmentation disabled. Results should be added after both experiments complete successfully.

## Repository Contents
- `YOLOv8_Object_Detection.ipynb` — training and evaluation notebook.
- `README.md` — project documentation.
- `dataset_annotation_audit.txt` — dataset annotation statistics, if included.

## Notes
The notebook requires valid dataset access and configuration before execution. Evaluation results should be reported only after the corresponding experiments have completed.

## Author
Sumasri

GitHub: https://github.com/Sumasri-16
