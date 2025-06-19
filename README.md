# 🔍 Defect Detection Using Deep Learning

This project implements an intelligent **Defect Detection System** using **YOLOv8**, a state-of-the-art object detection model. It is designed to automatically identify and localize defects in industrial components from images, streamlining the quality control process with high accuracy and speed.

---

## 📌 Table of Contents

- [📌 Table of Contents](#-table-of-contents)
- [🎯 Project Objective](#-project-objective)
- [📂 Dataset Overview](#-dataset-overview)
- [🧠 Model Architecture](#-model-architecture)
- [⚙️ Setup and Installation](#️-setup-and-installation)
- [🚀 Training and Evaluation](#-training-and-evaluation)
- [🖼️ Sample Predictions](#-sample-predictions)
- [🛠️ Tools & Technologies](#️-tools--technologies)
- [📌 Future Improvements](#-future-improvements)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 🎯 Project Objective

To develop a real-time defect detection system that can:

- Accurately detect multiple types of defects in industrial products.
- Localize the defects using bounding boxes.
- Operate efficiently in a production environment.
- Assist in quality control and reduce manual inspection errors.

---

## 📂 Dataset Overview

The dataset contains images of industrial components with annotations for different types of defects. Each image has labeled bounding boxes indicating the defect locations.

- ✅ Image Formats: `.jpg`
- ✅ Annotation Format: YOLO `.txt`
- ✅ Classes: `defect'.
- ✅ Number of Images: 35


---

## 🧠 Model Architecture

I use **YOLOv8** (You Only Look Once - Version 8) from the Ultralytics framework:

- Base model: `YOLOv8s` (small, fast, and accurate)
- Pretrained on: MS-COCO
- Custom training on defect dataset
- Transfer Learning approach
- Batch size: 16
- Epochs: 50 (early stopping applied)

---

## ⚙️ Setup and Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/defect-detection-yolov8.git
cd defect-detection-yolov8

# Create virtual environment (optional)
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

| Metric          | Value     |
| --------------- | --------- |
| mAP\@0.5        | 92.6%     |
| mAP\@0.5:0.95   | 78.4%     |
| Precision       | 90.3%     |
| Recall          | 87.9%     |
| Inference Speed | 8.2ms/img |


## 🛠️ Tools & Technologies
Language: Python

Framework: Ultralytics YOLOv8

Libraries: OpenCV, Matplotlib, NumPy, PyTorch

Platform: Google Colab / Local GPU

Annotation Tool: CVAT / Roboflow

## 📌 Future Improvements


Deploy as a web app using Streamlit or Flask

Support for video defect detection

Integration with real-time production line cameras

Add feedback loop for human-in-the-loop correction


