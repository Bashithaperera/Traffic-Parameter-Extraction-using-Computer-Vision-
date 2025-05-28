# 🚦 Vision-Based Traffic Parameter Extraction for Adaptive Traffic Control

This project implements a computer vision system to identify key traffic parameters such as "vehicle stopped delay time" and "vehicle count" from video feeds at intersections. The extracted data can be used to simulate or inform adaptive traffic control systems, helping reduce congestion and optimize traffic flow.

---

## 📌 Project Overview
Conventional traffic light systems rely on fixed timing, which often fails to adapt to real-time traffic conditions. This project utilizes a trained YOLOv8 object detection model combined with the ByteTrack tracking algorithm to:
- Detect and track vehicles in a defined zone
- Identify the vehcile motion status (stopped or in-motion)
- Counting the number of stationary vehicles inside teh detection zone (based on percentage area overlap)
- Measure individual vehicle stopped delay times (how long they remain stationary in real-time)
- Log traffic behavior data for potential adaptive signal control

---

## 🧠 Key Features

- 🚗 Real-time vehicle detection and tracking using YOLOv8 + ByteTrack
- ⏱️ Vehicle stoppage detection and delay time calculation
- 🎥 Visual output with bounding boxes and delay information
- 📊 Exportable logs for traffic analysis or as input to adaptively control traffic lights 

---

## 🛠️ Dependencies

The core dependencies for inference are listed in `requirements.txt`:

```txt
supervision==0.25.1
ultralytics==8.3.11
opencv-python==4.10.0.84
numpy==1.23.2
shapely==2.0.6
