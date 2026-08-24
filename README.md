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

### 1. 准备环境

当前包按 ROS 2 的 `ament_cmake` 工作空间组织。需要安装 ROS 2、RViz2、`robot_state_publisher`、`joint_state_publisher_gui` 和 `xacro`。

以 ROS 2 Humble 为例：

```bash
sudo apt install \
  ros-humble-rviz2 \
  ros-humble-robot-state-publisher \
  ros-humble-joint-state-publisher-gui \
  ros-humble-xacro
```

### 2. 编译

```bash
mkdir -p /path/to/mantis_ws/src
cd /path/to/mantis_ws/src
git clone https://github.com/BlueWorm-EAI-Tech/mantis_description.git

cd /path/to/mantis_ws
colcon build --symlink-install --packages-select lanchong_description
source install/setup.bash
```

仓库名是 `mantis_description`，ROS 2 包名暂时保留为 `lanchong_description`。

### 3. 在 RViz2 中查看

```shell
ros2 launch lanchong_description display.launch
```

启动后可使用 `joint_state_publisher_gui` 调整关节并在 RViz2 中查看模型。使用自定义 URDF 时可传入绝对路径：

```bash
ros2 launch lanchong_description display.launch \
  model:=/absolute/path/to/model.urdf
```

## 文件说明

| 路径 | 内容 |
| --- | --- |
| `urdf/lanchong_description.urdf` | 默认 Mantis 1.0 URDF |
| `urdf_full/` | 完整模型的源文件资料 |
| `meshes/`、`meshes_full/` | 可视化和碰撞网格 |
| `launch/display.launch.py` | RViz2 显示入口 |
| `rviz/lanchong_description.rviz` | 默认 RViz2 配置 |
| `config/joint_names_lanchong_description.yaml` | 关节名称配置 |

## 当前范围

- 本仓库当前面向 Mantis 1.0 模型；其他机器人版本应使用对应的 URDF 和网格资料。
- RViz2 能够显示模型只说明文件可以加载，不代表关节方向、零位、限位和真机控制已经验收。
- 修改 URDF 后，应检查网格路径、关节树、左右臂方向、碰撞模型和 RViz2 显示，再交给控制项目使用。

## 问题反馈

请在 [GitHub Issues](https://github.com/BlueWorm-EAI-Tech/mantis_description/issues) 中说明 ROS 2 版本、使用的 URDF、启动命令和报错信息。
