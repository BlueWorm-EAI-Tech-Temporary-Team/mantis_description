# Mantis1.0 URDF 模型

<div align="center">

<img src="img/LOGO.png" alt="BlueWorm Logo" width="600"/>

[🌟 English](README_EN.md) | [🌏 中文](README.md)

</div>

本仓库提供蓝虫具身 Mantis1.0 机器人的统一机器人描述格式（URDF）文件。

| <img src="img/mantis_v1_mujoco.png" alt="mujoco preview" width="250"> | <img src="img/comming_soon.png" alt="real robot preview" width="250"> | <img src="img/mantis_v1_rviz.png" alt="rviz preview" width="250"> |
|:--:|:--:|:--:|
| **mujoco 预览** | **真机预览** | **rviz 预览** |

## 核心特性

Mantis 1.0 URDF 模型包含：
- 舵轮底盘+升降滑台式躯干：实现三维工作空间覆盖
- 七自由度双臂：模拟人体工作空间
- 齿轮齿条双指夹爪：自适应力反馈夹持

## 快速开始

启动可视化 launch 文件：
```shell
ros2 launch lanchong_description display.launch
```
