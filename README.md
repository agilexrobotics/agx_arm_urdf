# AgileX 机械臂 URDF 模型

[English](./README_EN.md)

本仓库包含 AgileX 系列机械臂的 URDF / Xacro 模型文件及对应的 3D 网格（mesh）资源，供 ROS2 可视化、仿真和运动规划使用。

> 本仓库作为 [agx_arm_ros](https://github.com/agilexrobotics/agx_arm_ros) 的子模块使用，完整的 ROS2 驱动、启动与控制说明请参阅主仓库。

---

## 支持的型号

| 型号 | 目录 | 基础 URDF | 夹爪 Xacro | 灵巧手 Xacro |
|------|------|-----------|------------|--------------|
| Piper | `piper/` | `piper_description.urdf` | `piper_with_gripper_description.xacro` | `piper_with_left_revo2_description.xacro` / `piper_with_right_revo2_description.xacro` |
| Piper H | `piper_h/` | `piper_h_description.urdf` | `piper_h_with_gripper_description.xacro` | `piper_h_with_left_revo2_description.xacro` / `piper_h_with_right_revo2_description.xacro` |
| Piper L | `piper_l/` | `piper_l_description.urdf` | `piper_l_with_gripper_description.xacro` | `piper_l_with_left_revo2_description.xacro` / `piper_l_with_right_revo2_description.xacro` |
| Piper X | `piper_x/` | `piper_x_description.urdf` | `piper_x_with_gripper_description.xacro` | `piper_x_with_left_revo2_description.xacro` / `piper_x_with_right_revo2_description.xacro` |
| Nero | `nero/` | `nero_description.urdf` | `nero_with_gripper_description.xacro` | `nero_with_left_revo2_description.xacro` / `nero_with_right_revo2_description.xacro` |
| Revo2 灵巧手 | `revo2/` | `revo2_left_hand.urdf` / `revo2_right_hand.urdf` | — | — |

---

## 目录结构

```
agx_arm_urdf/
├── piper/
│   ├── meshes/dae/    # 3D 网格文件（.dae）
│   └── urdf/          # URDF / Xacro 文件
├── piper_h/
│   ├── meshes/dae/
│   └── urdf/
├── piper_l/
│   ├── meshes/dae/
│   └── urdf/
├── piper_x/
│   ├── meshes/dae/
│   └── urdf/
├── nero/
│   ├── meshes/dae/
│   └── urdf/
└── revo2/
    ├── meshes/dae/
    └── urdf/
```

---

## 使用方式

本仓库通常不需要单独克隆，请通过 [agx_arm_ros](https://github.com/agilexrobotics/agx_arm_ros) 主仓库获取：

```bash
git clone -b ros2 --recurse-submodules https://github.com/agilexrobotics/agx_arm_ros.git
```

在 ROS2 中加载模型进行可视化：

```bash
ros2 launch agx_arm_description display.launch.py arm_type:=piper
```

更多用法请参阅 [agx_arm_ros 文档](https://github.com/agilexrobotics/agx_arm_ros)。

---

## 许可证

本项目基于 [MIT License](./LICENSE) 发布。
