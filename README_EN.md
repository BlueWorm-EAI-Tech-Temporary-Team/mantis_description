# Mantis v2.0 URDF Model

<div align="center">

<img src="img/LOGO.png" alt="BlueWorm Logo" width="600"/>

[🌟 English](README_EN.md) | [🌏 中文](README.md)

</div>

This repository provides the URDF files for Mantis v2.0, designed by BlueWorm EAI Tech.

| <img src="img/mantis_v1_mujoco.png" alt="mujoco preview" width="250"> | <img src="img/comming_soon.png" alt="real robot preview" width="250"> | <img src="img/mantis_v1_rviz.png" alt="rviz preview" width="250"> |
|:--:|:--:|:--:|
| **mujoco preview** | **real robot preview** | **rviz preview** |

## Core Features

Mantis v2.0 URDF includes:
- **Omnidirectional Chassis + Lifting Torso**: Flexible mobility and wide-range height adjustment.
- **2-DOF Head System**: Newly added Neck_Joint (Yaw) and Head_Joint (Pitch) for active perception.
- **7-DOF High-Performance Dual-Arms**: Optimized dynamic parameters with a human-like workspace.
- **Adaptive Grippers**: Rack-and-pinion parallel-jaw grippers with integrated force feedback.
- **Full Sensor Definitions**: Precise pose definitions for core sensors including LiDAR and IMU.

## Quick Start

Launch the following command to visualize the robot and move the joints:
```shell
ros2 launch mantis_description display.launch.py
```
