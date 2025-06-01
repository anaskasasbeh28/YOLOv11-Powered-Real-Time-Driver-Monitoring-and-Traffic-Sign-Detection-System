# 🚗 YOLOv11-Powered Real-Time Driver Monitoring and Traffic Sign Detection System

## 🧠 Overview

This project presents a real-time AI system designed to enhance **road safety** using advanced object detection with **YOLOv11**. It integrates two core modules:

- **Traffic Sign Detection (TSD)**: Detects signs such as stop, speed limits, and traffic lights.
- **Driver Monitoring System (DMS)**: Detects unsafe driver behaviors like phone use, drowsiness, or not wearing a seatbelt.

Both models run **in real-time** with integrated **Text-to-Speech (TTS)** feedback, providing instant voice alerts to reduce accidents and promote safer driving.

---

## 🎯 Project Goals

- Improve driver awareness of road signs and safe behavior.
- Provide immediate alerts for unsafe driving or missed traffic signs.
- Reduce accident risk through proactive AI monitoring and feedback.

---

## 🚧 Road Safety Challenges Addressed

| Problem | Solution |
|--------|----------|
| **Drivers miss traffic signs** due to distraction or poor weather. | AI detects signs in real-time and gives voice alerts. |
| **Unsafe behaviors** (e.g., using phone, drowsiness) go undetected. | DMS detects and alerts for dangerous behaviors instantly. |
| **No real-time correction** with traditional systems. | Our system gives **instant feedback** to influence behavior immediately. |

---

## 🧠 Key Features

- 🔍 **YOLOv11 for Object Detection**
- 🧑‍💻 **Two independent models**: TSD and DMS
- 🎙️ **Text-to-Speech (TTS)** for real-time vocal alerts
- 📸 **Live camera support** for real-world testing
- 📈 **High performance** across real driving scenarios

---

## 📂 Datasets Used

### 🛑 Traffic Sign Detection (TSD)
- **Images**: 4,977  
- **Classes**: 15 (e.g., Stop, Speed Limits, Traffic Lights)
- **Split**:
  - Train: 71%
  - Validation: 16%
  - Test: 13%

### 👁️ Driver Monitoring System (DMS)
- **Images**: 9,884  
- **Classes**: 5  
  - Open Eyes  
  - Closed Eyes  
  - Seatbelt  
  - Phone Usage  
  - Cigarette Smoking  
- **Split**:
  - Train: 60%
  - Validation: 24%
  - Test: 16%

---

## 🔁 Data Augmentation Techniques

- Color Jitter  
- Rotation (up to 10°)  
- Translation (15%)  
- Shear (0.2 rad)  
- Horizontal & Vertical Flip  
- Mosaic & MixUp blending

---

## 📊 Performance Metrics

| Model | mAP@0.5 | Notes |
|-------|---------|-------|
| **Traffic Sign Detection** | **0.97** | High accuracy across all sign types |
| **Driver Monitoring System** | **0.92** | Robust in detecting unsafe behaviors |

- **Training**: 100 epochs  
- **IoU Threshold**: 0.6  
- **Confidence Threshold**: 0.25

✅ **Outperformed YOLOv11** in real-world webcam testing.

---

## 🎙️ Text-to-Speech (TTS) Integration

We integrated `pyttsx3` for real-time **vocal alerts**:

- "Attention: Stop sign ahead."
- "Red light detected."
- "Warning: Phone usage while driving."
- "Seatbelt not detected."

This enhances user experience and encourages immediate corrective actions.

---

## ⚙️ Real-Time Testing

- Jupyter Notebook implementation using `OpenCV`
- Webcam-based live detection (`webcam_test.py`)
- Smooth and efficient real-time feedback

---

## 🔧 Training Pipeline

- Trained both models on **Google Colab TPU** (free tier)
- Code is modular and ready for fine-tuning or extension

---

## 📽️ Demo Videos

- [🚦 Traffic Sign Detection Demo](https://www.youtube.com/watch?v=eQ1tMq20L7M)
- [🧍‍♂️ Driver Behavior Monitoring Demo](https://www.youtube.com/watch?v=JKUsf6RV1CU)

---


## 💡 Future Work

- Improve TTS dynamic updates (e.g., language switch, urgency levels)

- Add support for gesture detection (e.g., hands off the wheel)

- Optimize models for embedded deployment (e.g., Raspberry Pi)

- Localize alerts for Arabic drivers and regional signs

---

## 📌 Tech Stack

- YOLOv11

- Python + OpenCV

- TTS (pyttsx3)

- Google Colab (TPU)

- Kaggle Datasets

- Jupyter Notebooks


---


## 🚀 Getting Started

### 🧬 Clone the Repository
```bash
git clone https://github.com/your-username/YOLOv11-Driver-Monitoring-TSD.git
cd YOLOv11-Driver-Monitoring-TSD
