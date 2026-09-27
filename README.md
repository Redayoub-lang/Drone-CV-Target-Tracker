# Drone CV Target Tracker Engine

![Python 3](https://img.shields.io/badge/Language-Python%203.10-blue)
![Computer Vision](https://img.shields.io/badge/Domain-Computer%20Vision%20%26%20Target%20Tracking-orange)
![Developer](https://img.shields.io/badge/Developer-Ayoub%20Lahmar-brightgreen)

A robust computer vision target tracking pipeline designed for UAV autonomous gimbal control and visual servoing. Combines real-time object detection with a Discrete Kalman Filter to estimate target trajectories, handle brief visual occlusions, and stabilize control loops during high-speed aerial maneuvers.

Implemented by **Ayoub Lahmar** ([@Redayoub-lang](https://github.com/Redayoub-lang)).

## 📐 Mathematical Formulation

The dynamic target state vector \(\mathbf{x}_k = [x, y, v_x, v_y]^T\) and measurement vector \(\mathbf{z}_k = [z_x, z_y]^T\) are modeled via a Discrete Kalman Filter:

$$
\mathbf{x}_k = \mathbf{F} \mathbf{x}_{k-1} + \mathbf{w}_k, \quad \mathbf{w}_k \sim \mathcal{N}(0, \mathbf{Q})
$$

$$
\mathbf{z}_k = \mathbf{H} \mathbf{x}_k + \mathbf{v}_k, \quad \mathbf{v}_k \sim \mathcal{N}(0, \mathbf{R})
$$

Where \(\mathbf{F}\) is the state transition matrix, \(\mathbf{H}\) is the observation matrix, and \(\mathbf{w}_k, \mathbf{v}_k\) represent Gaussian process and measurement noise distributions.

## 💻 Build & Run

```bash
python target_tracker.py
🎯 Relevance to My Goals at Jiangsu University
Building upon my diploma in Software Engineering (DTS), this project demonstrates my competence in Computer Vision, Image Processing Pipelines, and Automated Object Detection. At Jiangsu University, I plan to extend these capabilities towards AI-driven autonomous UAV visual navigation systems.

📜 License
This project is open-source under the MIT License.
