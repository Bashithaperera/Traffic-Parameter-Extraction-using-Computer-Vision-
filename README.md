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

## ✅ Results

Below is a single frame of a inference tested traffic footage. The vehicle count is visualized iwhtin the detection zone while the individual vehicle stopped delay times on the right side along with the assigned unique tracking ids of the corresponding vehicle.

![11](https://github.com/user-attachments/assets/75ef9fa9-2318-43cf-b393-12b4d215053f)


