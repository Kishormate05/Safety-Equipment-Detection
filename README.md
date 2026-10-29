# 🦺 Safety Equipment Detection Using YOLOv8

## 📌 Project Overview

**Safety Equipment Detection Using YOLOv8** is a computer vision project that detects safety helmets and vests worn by individuals in real time. It uses the YOLOv8 object detection model and OpenCV to process webcam feeds and video inputs.

The system helps identify safety equipment compliance in construction sites, factories, and other industrial environments.

## 🚀 Features

- 🔍 Detects safety helmets and vests.
- 👷 Classifies safety compliance into SAFE, PARTIAL, and UNSAFE.
- 🎨 Displays color-coded bounding boxes for different safety statuses.
- 📹 Supports real-time webcam and video input.
- 🧠 Supports training on custom annotated datasets.
- ⚡ Uses YOLOv8 for efficient object detection.

## 🛠️ Technologies Used

- Python
- YOLOv8 (Ultralytics)
- OpenCV
- NumPy
- Computer Vision
- Deep Learning

## 📁 Project Structure

```text
Safety-Equipment-Detection/
│
├── safety_detection.py
├── train.py
├── yolov8n.pt
│
└── Q1/
    ├── data.yaml
    └── runs/
        └── detect/
            └── vest_helmet_final/
                └── weights/
                    └── best.pt
│
└── README.md
```

*Note: The folder structure above represents the expected project setup. Include the trained weights and dataset configuration if available.*

## 📦 Installation

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd Safety-Equipment-Detection
```

### 2. Install Dependencies

Make sure Python 3 is installed, then run:

```bash
pip install ultralytics opencv-python numpy
```

## 🧠 Model Training

Ensure that your dataset is annotated correctly and that `Q1/data.yaml` contains the correct dataset paths and class names.

Run the training script:

```bash
python train.py
```

After successful training, the best model weights should be available at:

```text
Q1/runs/detect/vest_helmet_final/weights/best.pt
```

The actual output directory depends on the configuration in `train.py`.

## ▶️ Running Detection

Open `safety_detection.py` and verify that the model path is configured correctly:

```python
MODEL_PATH = "Q1/runs/detect/vest_helmet_final/weights/best.pt"
```

Start the detection system:

```bash
python safety_detection.py
```

The webcam opens by default when `cv2.VideoCapture(0)` is used.

**Press `q` to exit the detection window.**

## 🎨 Safety Classification

| Status | Description | Bounding Box Color |
|---|---|---|
| SAFE | Helmet and vest detected | Green |
| PARTIAL | Only one required safety item detected | Cyan or Yellow |
| UNSAFE | No required safety equipment detected | Red |

The classification logic depends on the detected classes and must be configured in `safety_detection.py`.

## 🏷️ Dataset Classes

The original project uses the following YOLO class mapping:

| Class ID | Class Name |
|---|---|
| 0 | No Vest |
| 1 | Helmet |
| 2 | Vest |

Ensure that the class IDs, names, and detection logic match your actual dataset annotations and trained model.

## 📸 Output Preview

Add screenshots or a short video of the working detection system here.

Example:

- Helmet detection
- Vest detection
- SAFE classification
- PARTIAL classification
- UNSAFE classification

## 🌍 Applications

- Construction site safety monitoring
- Industrial workplace surveillance
- Factory safety compliance
- Personal protective equipment (PPE) detection
- Computer vision and deep learning applications

## 🔮 Future Scope

- Integration with CCTV cameras.
- Automated alerts for safety violations.
- Safety compliance reports and analytics.
- Integration with real-time monitoring dashboards.
- Improved detection accuracy using larger datasets.

## 👨‍💻 About Me

**Kishor Dadarao Mate**

Final-Year B.Tech Student  
Artificial Intelligence and Data Science

Interested in Data Science, Machine Learning, Deep Learning, and Computer Vision.


## 🤝 Contributing

Contributions, suggestions, and improvements are welcome. Feel free to fork this repository and submit a pull request.

## 📄 License

This project is intended for educational and research purposes. Add an appropriate open-source license if you plan to distribute the project.

---


