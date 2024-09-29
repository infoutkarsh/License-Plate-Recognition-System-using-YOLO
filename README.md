# License Plate Recognition System using YOLO & OCR

## Project Overview
This project implements a **License Plate Recognition System** that uses **YOLO (You Only Look Once)** for detecting vehicle license plates in images or videos and **OCR (Optical Character Recognition)** to extract alphanumeric characters from the detected plates. The system is designed to work in **real-time**, offering high accuracy and efficiency, making it suitable for applications like **traffic monitoring**, **automated toll systems**, and **parking management**.

## Features
- **Real-time License Plate Detection**: Utilizes the YOLOv4 model to detect license plates in images or video streams.
- **Optical Character Recognition (OCR)**: Extracts alphanumeric characters from detected plates for further processing.
- **High Accuracy**: Achieves around **88.38% accuracy** in both detection and character recognition.
- **Scalable**: Can be applied to multiple use cases, such as smart city applications and automated vehicle identification.

## Installation

1. **Install dependencies**:
   Ensure you have Python installed and then run:
   ```bash
   pip install -r requirements.txt
   ```

2. **Download the YOLOv4 weights**:
   - You can download the pre-trained YOLOv4 weights [here](https://github.com/AlexeyAB/darknet#pre-trained-models).

3. **Set up OCR**:
   - Install `Tesseract OCR`. You can follow instructions [here](https://github.com/tesseract-ocr/tesseract).

4. **Run the system**:
   Use the following command to run the detection system:
   ```bash
   python detect_plate.py --input video.mp4
   ```

## Usage
- **Input**: The system takes an image or video stream as input.
- **Output**: It returns the license plate detected and the extracted alphanumeric characters.

### Example
```bash
python detect_plate.py --input car_image.jpg
```
The output will display the recognized license plate:
```
Detected Plate: MH12DE1433
```

## Project Structure
- `detect_plate.py`: Main script to run the license plate detection and recognition.
- `yolo_utils.py`: Contains utility functions for loading the YOLO model and handling detections.
- `ocr_utils.py`: Functions to handle Optical Character Recognition (OCR) using Tesseract.
- `requirements.txt`: List of Python libraries required to run the project.

## Dependencies
- **YOLOv4** for object detection
- **Tesseract OCR** for optical character recognition
- **OpenCV** for image processing
- **Python** with libraries: numpy, pytesseract, opencv-python, etc.

## Applications
- **Traffic Monitoring**: Track and log vehicles in real-time.
- **Automated Toll Systems**: Automatically identify and process vehicle information.
- **Parking Management**: Track vehicle entry and exit for automated parking systems.
