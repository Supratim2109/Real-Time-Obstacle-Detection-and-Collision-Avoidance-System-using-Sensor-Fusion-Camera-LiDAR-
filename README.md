# 🚗 Real-Time Obstacle Detection & Collision Avoidance System using Sensor Fusion

This project presents a **real-time Advanced Driver Assistance System (ADAS)** built using **sensor fusion of camera and LiDAR data**. It leverages deep learning, spatial calibration, and collision-avoidance decision logic to mimic the perception system of autonomous vehicles.

---

## 🧠 What It Does

- Performs **object detection** in real-time using a YOLOv8 model on live or pre-recorded camera images.
- Associates detected 2D objects with 3D **LiDAR spatial vectors** using sample tokens and calibration parameters.
- Calculates distance to potential obstacles and **assesses collision risk** using threshold-based logic.
- Provides **visual overlays** and **audio alerts** for obstructions detected in the drive path.
- Modular design allows extensibility to incorporate radar, GPS, and control signals.

---

## 🎯 Features

- ✅ Real-time video stream processing
- 🧩 Sensor Fusion: Camera + LiDAR correlation
- 🎥 Object Detection: YOLOv8 pretrained model
- 📏 3D-2D Projection using Calibration Matrix
- 🚨 Risk Assessment: Safe / Warning / Critical levels
- 🔊 Audible and visual alerts for obstruction
- 📍 Based on nuScenes dataset architecture

---

---

## 🔧 Technologies Used

- `Python`, `PyTorch`, `OpenCV`, `NumPy`, `Pygame`
- `Ultralytics YOLOv8` for object detection
- `NuScenes metadata` for camera-LiDAR calibration
- `DBSCAN` for LiDAR object clustering

---

## 🚦 Collision Avoidance Logic

| Distance       | Status   | Action                         |
|----------------|----------|--------------------------------|
| > 15 meters    | ✅ Safe   | No action                      |
| 10–15 meters   | ⚠ Warning | Visual & Audio Alert Triggered |
| < 10 meters    | 🚨 Critical | Emergency Braking / Evasive Maneuver |

---

## 🔍 Example Output

- Bounding boxes with object label and distance (in meters)
- Color-coded risk levels:  
  🔴 Critical | 🟡 Warning | 🟢 Safe

---

## 🛠 How to Run

1. Clone the repository and place sample data in the respective folders.
2. Make sure `alert_sound.mp3` is in the project root.
3. Open and run `assignment.ipynb` to execute all steps:
   - Preprocessing
   - Sensor fusion
   - Decision making
   - Visualization

---

## 📌 Potential Extensions

- Integrate radar sensor data for velocity estimation.
- Use temporal sequence modeling for trajectory prediction.
- Add autonomous actuation hooks (e.g., simulated braking).


## 📚 References

- [nuScenes Dataset](https://www.nuscenes.org/)
- [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
- Real-time sensor calibration principles and ego pose transformations from nuScenes documentation.

---

## ⭐ Star this repo if you found it useful or inspiring!



