# Mantis1.0 URDF Model

<div align="center">

<img src="img/LOGO.png" alt="BlueWorm Logo" width="600"/>

[🌟 English](README_EN.md) | [🌏 中文](README.md)

</div>

This repository provides the urdf file of Mantis1.0, designed by BlueWorm EAI Tech.

| <img src="img/mantis_v1_mujoco.png" alt="mujoco preview" width="250"> | <img src="img/comming_soon.png" alt="real robot preview" width="250"> | <img src="img/mantis_v1_rviz.png" alt="rviz preview" width="250"> |
|:--:|:--:|:--:|
| **mujoco preview** | **real robot preview** | **rviz preview** |


## Core Features

Mantis 1.0 URDF includes：
- Omnidirectional Chassis + Lifting Torso: 3D workspace coverage
- 7DOF Dual-Arm: human-like workspace
- Parallel-Jaw Gripper：adaptive + force feedback

## Quick Start

Launch the following command to visualize the robot and move the joints:
```shell
ros2 launch lanchong_description display.launch
```
