# 🏋️ FormCorrect — Pose-Based Exercise Form Correctness Detector

FormCorrect is a lightweight pipeline for detecting **exercise form correctness** using human pose estimation models such as **MediaPipe** or **OpenPose**.  
The system extracts body keypoints, computes angles & alignment, applies **rule-based posture evaluation**, and generates **frame-wise or window-based feedback** for common fitness exercises (e.g., bicep curl, lateral raise).

This project is aimed at demonstrating understanding of pose tracking, geometric reasoning, and real-time feedback systems.  
**Deadline: 8 December 2025**

---

## 📌 **Features**
- ✔ Uses **MediaPipe** or **OpenPose** for pose keypoint detection  
- ✔ Extracts **time-series** keypoints from video  
- ✔ Smoothing options (Moving Average / Savitzky-Golay)  
- ✔ Rule-based correctness logic for each exercise  
- ✔ Frame-wise + window-based feedback  
- ✔ Visual overlays (optional)  
- ✔ **MLflow integration** for experiment tracking  

---

## 📽 **Demo Output Example**

### Frame-wise Feedback (JSON)
```json
{
  "frame": 132,
  "timestamp": 4.10,
  "angles": { "left_elbow": 45.2, "torso_angle": 12.8 },
  "rules": {
    "elbow_angle": "OK",
    "back_symmetry": "WARN"
  },
  "feedback": [
    "Good curl depth.",
    "Slight back lean — maintain neutral spine."
  ]
}
