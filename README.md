# Mantis v2.0 URDF 模型

<div align="center">

<img src="img/LOGO.png" alt="BlueWorm Logo" width="600"/>

[🌟 English](README_EN.md) | [🌏 中文](README.md)

</div>

本仓库提供蓝虫具身 Mantis v2.0 机器人的统一机器人描述格式（URDF）文件。

| <img src="img/mantis_v1_mujoco.png" alt="mujoco preview" width="250"> | <img src="img/comming_soon.png" alt="real robot preview" width="250"> | <img src="img/mantis_v1_rviz.png" alt="rviz preview" width="250"> |
|:--:|:--:|:--:|
| **mujoco 预览** | **真机预览** | **rviz 预览** |

## 核心特性

Mantis v2.0 URDF 模型包含：
- **全向舵轮底盘+升降躯干**：实现灵活的移动与大范围高度调节。
- **2自由度头部系统**：新增 Neck_Joint (Yaw) 和 Head_Joint (Pitch)，支持视觉传感器的主动感知。
- **7自由度高性能双臂**：优化的动力学参数，更接近人体运动范围。
- **自适应夹爪**：集成力反馈的齿轮齿条双指夹爪。
- **完整传感器定义**：包含 LiDAR、IMU 等核心传感器的位姿定义。

## 快速开始

启动可视化 launch 文件：
```shell
ros2 launch mantis_description display.launch.py
```
