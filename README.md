# Multi-Model-Object-Detection using YOLOv5, YOLOv8, AND Detectron2

The objective is to detect vehicles in a street scene, generate bounding boxes, and compare the performance of these models in terms of accuracy, inference speed, and detection quality.

Project Overview

This project implements object detection on video data using three different deep learning models:

YOLOv5 – Applied for initial inference and bounding box detection.
YOLOv8 – Used for model training and fine-tuning on a custom dataset.
Detectron2 – Implemented for an alternative approach to object detection.

Dataset and Video Processing

A street scene video is used as the input data.
The video is split into frames before running inference.
Each model processes the frames, detects objects, and draws bounding boxes.
The processed frames are recompiled into a final output video.

Object Detection Workflow
1.Video Preprocessing:
Convert the input video into image frames.
Resize and normalize the images for model inference.
2.YOLOv5 Inference:
Pre-trained YOLOv5s model is loaded for detection.
Vehicles such as cars, buses, and trucks are identified and labeled.
Bounding boxes are drawn around detected objects.
3.YOLOv8 Model Training:
A custom dataset is used for training YOLOv8.
The dataset is structured in COCO format and stored in a ZIP file.
YOLOv8 is fine-tuned for 25 epochs using a pre-trained model (yolov8s.pt).
The confusion matrix and validation loss graphs are generated.
4.Detectron2 Training and Inference:
The COCO-format dataset is registered in Detectron2.
A Faster R-CNN model is trained using the Detectron2 model zoo.
The model is fine-tuned on six object classes.
Bounding box predictions are generated on test images.
5.Post-Processing:
The detected frames from YOLOv5, YOLOv8, and Detectron2 are compiled into output videos.
The results from the three models are compared in terms of accuracy and visualization.

Results:
The before and after inference videos are compared:
Before: Raw input video.
After: Processed videos with bounding boxes around detected vehicles.
Performance metrics such as:
Inference speed,
Detection accuracy,
Model confidence scores are analyzed,
Training performance is visualized using confusion matrices and validation loss curves.
