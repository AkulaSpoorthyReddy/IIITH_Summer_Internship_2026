\# YOLO Car Detection Project



\## Overview



This task implements a custom car detection pipeline using YOLOv8. The workflow includes dataset preparation, image annotation, dataset structuring, model training, and prediction testing.



\## Project Structure



```text

car\_detection\_project/

│

├── images/

│   ├── train/

│   └── val/

│

├── labels/

│   ├── train/

│   └── val/

│

```



\## Task Workflow



\### 1. Dataset Preparation



\* Extracted frames from video dataset.

\* Organized images into training and validation sets.

\* Structured dataset in YOLO format.



\### 2. Image Annotation



\* Annotated cars using Label Studio.

\* Exported annotations in YOLO format.

\* Generated label files corresponding to each image.



\### 3. Dataset Configuration



Created `data.yaml` containing:



\* Dataset path

\* Train and validation image paths

\* Class names



\### 4. Model Training



Trained YOLOv8 models on the custom dataset.



Training command used:



```bash

yolo detect train model=yolov8n.pt data=data.yaml epochs=30

```



\## Prediction



Tested the trained model on validation images.



Prediction command:



```bash

yolo predict model=runs/detect/train-7/weights/best.pt source=car\_dataset/images/val

```



\## Results



\* Successfully detected cars on custom images.

\* Generated prediction outputs with bounding boxes.

\* Training metrics showed strong precision and recall values.



\## Tools and Technologies



\* Python

\* YOLOv8

\* Label Studio

\* OpenCV

\* PyTorch



\## Output



Prediction results are stored in:



```text

runs/detect/predict/

```



Training outputs are stored in:



```text

runs/detect/train-7/

```



\## Conclusion



The task demonstrates the complete workflow for custom object detection using YOLOv8, including annotation, dataset preparation, training, and prediction on custom car images.



