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

### 1. Prerequisites

This package uses ROS 2 and `ament_cmake`. Install RViz2, `robot_state_publisher`, `joint_state_publisher_gui`, and `xacro`. For ROS 2 Humble:

```bash
sudo apt install \
  ros-humble-rviz2 \
  ros-humble-robot-state-publisher \
  ros-humble-joint-state-publisher-gui \
  ros-humble-xacro
```

### 2. Build

```bash
mkdir -p /path/to/mantis_ws/src
cd /path/to/mantis_ws/src
git clone https://github.com/BlueWorm-EAI-Tech/mantis_description.git

cd /path/to/mantis_ws
colcon build --symlink-install --packages-select lanchong_description
source install/setup.bash
```

The repository is named `mantis_description`; the ROS 2 package currently retains the historical name `lanchong_description`.

### 3. Visualize in RViz2

```shell
ros2 launch lanchong_description display.launch
```

Use the joint-state publisher GUI to move joints in RViz2. To load another URDF, pass an absolute path:

```bash
ros2 launch lanchong_description display.launch \
  model:=/absolute/path/to/model.urdf
```

## Repository Layout

| Path | Contents |
| --- | --- |
| `urdf/lanchong_description.urdf` | Default Mantis 1.0 URDF |
| `urdf_full/` | Full-model source files |
| `meshes/`, `meshes_full/` | Visual and collision meshes |
| `launch/display.launch.py` | RViz2 launch entrypoint |
| `rviz/lanchong_description.rviz` | Default RViz2 configuration |
| `config/joint_names_lanchong_description.yaml` | Joint-name configuration |

## Current Scope

- This repository currently targets the Mantis 1.0 model. Use version-specific assets for other Mantis variants.
- Successful RViz2 display proves that the model loads; it does not qualify joint directions, zero positions, limits, or real-robot control.
- After changing the URDF, check mesh paths, the joint tree, left/right arm directions, collision geometry, and RViz2 rendering before using it in a controller.

## Support

Open a [GitHub Issue](https://github.com/BlueWorm-EAI-Tech/mantis_description/issues) with the ROS 2 version, URDF path, launch command, and error output.
