# Object Recognition System for Supermarket Shoppers 

## Overview
This Object Recognition System for Supermarket Shoppers  is designed to recognize supermarket items using the YOLOv3 algorithm. The project aims to streamline the shopping experience by automatically identifying items placed in a shopping cart, facilitating a quicker checkout process.

## Files in the Repository

- `Train_YoloV3_Multiple.ipynb`: Jupyter notebook for training the YOLOv3 model on multiple supermarket items. This notebook includes detailed steps from data preprocessing to training the model.
- `yolo_object_detection.py`: Python script for performing real-time object detection using the trained YOLOv4 model. This script processes video input to identify and classify items.

## Getting Started

### Prerequisites

- Python 3.6 or higher
- Dependencies: opencv-python, numpy, matplotlib (Install using `pip install -r requirements.txt`)
- Pre-trained YOLOv3 weights (Download and place in the project directory)

### Setup

1. Clone this repository to your local machine.
2. Install the required Python dependencies.
3. Download the pre-trained YOLOv3 weights or custom ttrain your weights and place them in the project directory.

## Detailed Guide for `Train_YoloV3_Multiple.ipynb`

This notebook is your step-by-step guide to training the YOLOv3 model on multiple classes of supermarket items. It is structured to take you through the entire process of training, from setting up your dataset to the final model training.

### Adjusting for Extra Classes

When adding extra classes to your model, there are specific sections within the notebook that require your attention:

1. **Dataset Preparation**: Ensure your dataset includes labeled images for all the classes you intend to train the model on. The labeling format should be compatible with YOLOv3 requirements.

2. **Configuration Files**: Adjust the `.cfg` file for YOLOv3 to include the number of classes you are training for. This involves changing the `classes` parameter in each of the `[yolo]` layers and the `filters` parameter in the preceding `[convolutional]` layers. The formula to calculate the `filters` value is `(classes + 5)*3`.

3. **Class Names File**: Update the `obj.names` file to include the names of the new classes you're adding. Ensure that the order of class names matches the labels in your dataset.

4. **Training Parameters**: Depending on the complexity and the number of classes, you might need to adjust the training parameters such as learning rate, batch size, and number of iterations to ensure optimal training performance.

5. **Model Evaluation**: After training, evaluate the model's performance on a test set that includes examples of the new classes. Adjust the training parameters as necessary based on the evaluation results.

### Final Steps

After making these adjustments, proceed with the training process as outlined in the notebook. Monitor the training process closely to ensure that the model is learning effectively. Post-training, thoroughly test the model with real-world data to validate its accuracy and reliability.

### Running the Object Detection

To run the object detection script, execute the following command in your terminal:

```shell
python yolo_object_detection.py
