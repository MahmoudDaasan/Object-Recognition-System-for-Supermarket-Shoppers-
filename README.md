# AI Cart System

## Overview
This AI Cart System is designed to recognize supermarket items using the YOLOv4 algorithm. The project aims to streamline the shopping experience by automatically identifying items placed in a shopping cart, facilitating a quicker checkout process.

## Files in the Repository

- `Train_YoloV3_Multiple.ipynb`: Jupyter notebook for training the YOLOv3 model on multiple supermarket items. This notebook includes detailed steps from data preprocessing to training the model.
- `yolo_object_detection.py`: Python script for performing real-time object detection using the trained YOLOv4 model. This script processes video input to identify and classify items.

## Getting Started

### Prerequisites

- Python 3.6 or higher
- Dependencies: opencv-python, numpy, matplotlib (Install using `pip install -r requirements.txt`)
- Pre-trained YOLOv4 weights (Download and place in the project directory)

### Setup

1. Clone this repository to your local machine.
2. Install the required Python dependencies.
3. Download the pre-trained YOLOv4 weights and place them in the project directory.

### Running the Object Detection

To run the object detection script, execute the following command in your terminal:

```shell
python yolo_object_detection.py
