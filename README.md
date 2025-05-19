# 🚗 Vehicle Tracking and Counting with YOLOv8 and Supervision

This project demonstrates how to use the **YOLOv8 object detection model** in combination with the **Supervision** library to track and count vehicles in a video. The system identifies moving vehicles, tracks their trajectories, and counts how many cross a defined virtual line.

---

## 🎯 Objectives

- Detect and track multiple types of vehicles in real-time using YOLOv8  
- Define a virtual counting line and count vehicles as they cross it  
- Visualize tracking IDs and live counts on video  
- Save the result as a new annotated video

---

## 🧠 Technologies Used

| Tool/Library    | Purpose                        |
|-----------------|--------------------------------|
| [YOLOv8](https://github.com/ultralytics/ultralytics) | Object detection model |
| [Supervision](https://github.com/roboflow/supervision) | Line counting, tracking, annotation |
| [OpenCV](https://opencv.org/) | Video processing & rendering |
| Python + Jupyter Notebook | Implementation in `.ipynb` format |

---

## 📁 Files

| File                             | Description                                 |
|----------------------------------|---------------------------------------------|
| `Track_and_count_vehicles_with_yolov8_and_supervison.ipynb` | Main notebook (detection + tracking) |
| `vehicles.mp4`                   | Original input video                        |
| `result.mp4`                     | Output video with tracking & counting       |

> 🧠 **Note:**  
> The YOLOv8 model weights (`yolov8x.pt`) are **not included** due to GitHub size limits.  
> You can download it automatically from Ultralytics using the code below:

```python
from ultralytics import YOLO
model = YOLO('yolov8x.pt')  # Downloads automatically if not present
```
---
📽 Demo

[![Watch Demo](https://img.youtube.com/vi/3Qm_A4X525I/0.jpg)](https://www.youtube.com/watch?v=3Qm_A4X525I)

This video demonstrates the real-time vehicle detection, tracking, and line-based counting system using YOLOv8 and Supervision.

---

🧪 How It Works
- Load yolov8x.pt model using Ultralytics
- Process frames from vehicles.mp4
- Detect vehicles and assign tracking IDs
- Count vehicles crossing a virtual line
- Overlay results on video and save to result.mp4

---

▶️ Getting Started
1. Clone this repo
2. Install dependencies:
   ```bash
     pip install ultralytics supervision opencv-python
    ```
3. Run the notebook:
     ```bash
      jupyter notebook Track_and_count_vehicles_with_yolov8_and_supervison.ipynb
     ```
4. Adjust the counting line or vehicle classes if needed

---
📌 Notes
Uses yolov8x for high-accuracy detection; replace with yolov8m.pt or yolov8n.pt for faster performance if needed

Works well with pre-recorded footage; also adaptable to live camera feeds
