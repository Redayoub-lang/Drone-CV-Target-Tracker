# Autonomous Drone Visual Target Tracker & HUD Estimator

![Python 3.x](https://img.shields.io/badge/Language-Python%203-blue.svg)
![OpenCV](https://img.shields.io/badge/Library-OpenCV%204.x-green.svg)
![Domain](https://img.shields.io/badge/Domain-Computer%20Vision%20%26%20Robotics-orange.svg)
![Developer](https://img.shields.io/badge/Developer-Ayoub%20Lahmar-brightgreen.svg)

A real-time Computer Vision (CV) target tracking system designed for autonomous drone landing and visual servoing. Built using **Python** and **OpenCV**, this module detects objects in HSV color space, extracts frame centroid displacement vectors, and streams real-time navigation telemetry over a simulated Heads-Up Display (HUD).

Developed by **Ayoub Lahmar** ([@Redayoub-lang](https://github.com/Redayoub-lang)) as part of my technical portfolio for application to the **Bachelor’s in Computer Science & Technology** program at **Jiangsu University (JSU)**.
🚀 System Architecture & CapabilitiesReal-Time HSV Segmentation: Filters camera input using dynamic Hue-Saturation-Value boundaries to isolate targets under changing lighting conditions.Visual Servoing Offset Estimation: Computes Pixel-Displacement Error vectors relative to the camera center, providing correction inputs for drone Yaw and Pitch PID controllers.Adaptive Contouring & Noise Cancellation: Applies Morphological operations (Erosion & Dilation) to prevent false positives from background sensor noise.Flight HUD Overlay: Streams active target locking status, bounding box coordinates, error displacement, and FPS processing rates directly on the live feed.📐 Displacement Mathematics$$\Delta X = X_{target} - X_{center}$$$$\Delta Y = Y_{center} - Y_{target}$$Where $(X_{center}, Y_{center})$ represents the optical center of the camera frame, used to send flight correction commands to the flight controller.
💻 How to RunPrerequisitesPython 3.8+OpenCV (opencv-python)NumPy (numpy)Installation & Execution
# Clone the repository
git clone [https://github.com/Redayoub-lang/Drone-CV-Target-Tracker.git](https://github.com/Redayoub-lang/Drone-CV-Target-Tracker.git)
cd Drone-CV-Target-Tracker

# Install dependencies
pip install opencv-python numpy

# Run Tracker
python tracker.py
🎯 Relevance to My Goals at Jiangsu University
Building upon my diploma in Software Engineering (DTS), this project demonstrates my competence in Computer Vision, Image Processing Pipelines, and Automated Object Detection. At Jiangsu University, I plan to extend these capabilities towards AI-driven autonomous UAV visual navigation systems.

📜 License
This project is open-source under the MIT License.
