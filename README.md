# 🚗 Licence Plate Detection using YOLOv8

This project implements a real-time licence plate detection system using YOLOv8, a state-of-the-art object detection model. The model is trained on a custom dataset of Indian licence plates to accurately identify and localize them in images and video streams.

## ✨ Features

*   **YOLOv8 Integration:** Leverages the powerful and efficient YOLOv8 model for object detection.
*   **Custom Dataset Training:** Trained on a specialized dataset focusing on Indian licence plates.
*   **Image and Video Inference:** Capable of performing predictions on both static images and video files.
*   **Accuracy Evaluation:** Includes a basic script for evaluating model performance.

## 🚀 Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

*   Python 3.8+
*   `git`
*   `pip`

### 🛠️ Installation

1.  **Clone the Repository:**
    First, clone the project repository from GitHub.

    ```bash
    git clone https://github.com/Arijit1080/Licence-Plate-Detection-using-YOLO-V8.git
    cd Licence-Plate-Detection-using-YOLO-V8
    ```

2.  **Install Dependencies:**
    Install the required Python packages using `pip`. The `requirements.txt` file contains all necessary libraries including `ultralytics` (for YOLOv8) and `roboflow` (for dataset handling).

    ```bash
    pip install -r requirements.txt
    ```
    You might also need to install `roboflow` separately if it's not fully covered or if you encounter issues.
    ```bash
    pip install roboflow
    ```

## 📊 Dataset

The project utilizes a custom dataset for Indian licence plates, hosted on Roboflow. The dataset is automatically downloaded during the setup phase.

1.  **Roboflow API Key:**
    You'll need a Roboflow API key to download the dataset. Replace `"fAs3pW3f0mZX3Elu8ZnV"` in the `licence_plate_detection_yolo_v8.py` file with your actual API key if the provided one expires or doesn't work.

    ```python
    from roboflow import Roboflow
    rf = Roboflow(api_key="YOUR_ROBOFLOW_API_KEY") # <-- Update this line
    project = rf.workspace("snu-i6ovv").project("license-plate-detector-ogxxg")
    dataset = project.version(2).download("yolov8")
    ```

2.  **Dataset Structure:**
    After downloading, the dataset will be organized in a `yolov8` format within a directory like `License-Plate-Detector-2/`. It will contain `train`, `valid`, and `test` splits, along with a `data.yaml` file that specifies the paths and class names.

## 🏃 Training the Model



## Sample Results


Image 1: 
![alt text](https://github.com/krishnaThoria/vehicle-number-plate-detection/blob/main/img1.jpg)

