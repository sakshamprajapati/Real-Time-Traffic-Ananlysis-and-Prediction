# Smart Adaptive Traffic Management System

## Real-Time Traffic Analysis and Prediction

This project implements a smart traffic management system that uses real-time vehicle detection to adjust traffic signal timings dynamically. It leverages computer vision techniques using the YOLOv4 model for vehicle detection and Python for processing and controlling the traffic signals.

## Prerequisites

Before you begin, ensure you have the following prerequisites:

- Python 3.6 or higher installed on your system.
- OpenCV library installed: `pip install opencv-python`
- YOLOv4 pre-trained model files:
  - [yolov4.cfg](https://github.com/kiyoshiiriemon/yolov4_darknet/blob/master/cfg/yolov4.cfg)
  - [yolov4.weights](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights)

## Installation

1. Clone or download the project repository to your local machine.
2. Place the YOLOv4 pre-trained model files (`yolov4.cfg`, `yolov4.weights`) in the project directory.

## Usage

### Vehicle Detection

Run the `vehicle_detection.py` script to detect vehicles in an image:

```bash
python vehicle_detection.py
```

The script will read the image from the specified path (`data/imtest2.jpeg`) and display the image with detected vehicles outlined in green rectangles.

### Traffic Signal Adjustment

Run the `green_time_signal.py` script to adjust the green signal time based on the vehicle count:

```bash
python green_time_signal.py
```

The script reads the vehicle count from the `vehicle_count.txt` file (ensure the file is in the same directory). It calculates the adjusted green signal time and displays the result.

### Real-Time Image Capture

Run the `cctv_image_capture.py` script to capture images from a CCTV camera at regular intervals:

```bash
python cctv_image_capture.py
```

The script captures images from the camera specified by `camera_index` and saves them with a timestamp in the filename.

## Customization

You can further customize the project by adjusting the base green time, vehicle multiplier, and other parameters in the `green_time_signal.py` script. Additionally, you can explore advanced YOLO model versions and incorporate real-time video streams for vehicle detection.
