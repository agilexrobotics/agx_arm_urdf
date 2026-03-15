# AgileX Robotic Arm URDF Models

[中文](./README.md)

This repository contains URDF / Xacro model files and 3D mesh resources for AgileX series robotic arms, used for ROS2 visualization, simulation, and motion planning.

> This repository is used as a submodule of [agx_arm_ros](https://github.com/agilexrobotics/agx_arm_ros). For complete ROS2 driver, launch, and control instructions, please refer to the main repository.

---

## Supported Models

| Model | Directory | Base URDF | Gripper Xacro | Dexterous Hand Xacro |
|-------|-----------|-----------|---------------|----------------------|
| Piper | `piper/` | `piper_description.urdf` | `piper_with_gripper_description.xacro` | `piper_with_left_revo2_description.xacro` / `piper_with_right_revo2_description.xacro` |
| Piper H | `piper_h/` | `piper_h_description.urdf` | `piper_h_with_gripper_description.xacro` | `piper_h_with_left_revo2_description.xacro` / `piper_h_with_right_revo2_description.xacro` |
| Piper L | `piper_l/` | `piper_l_description.urdf` | `piper_l_with_gripper_description.xacro` | `piper_l_with_left_revo2_description.xacro` / `piper_l_with_right_revo2_description.xacro` |
| Piper X | `piper_x/` | `piper_x_description.urdf` | `piper_x_with_gripper_description.xacro` | `piper_x_with_left_revo2_description.xacro` / `piper_x_with_right_revo2_description.xacro` |
| Nero | `nero/` | `nero_description.urdf` | `nero_with_gripper_description.xacro` | `nero_with_left_revo2_description.xacro` / `nero_with_right_revo2_description.xacro` |
| Revo2 Hand | `revo2/` | `revo2_left_hand.urdf` / `revo2_right_hand.urdf` | — | — |

---

## Directory Structure

```
agx_arm_urdf/
├── piper/
│   ├── meshes/dae/    # 3D mesh files (.dae)
│   └── urdf/          # URDF / Xacro files
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

## Usage

This repository is typically not cloned separately. Use the [agx_arm_ros](https://github.com/agilexrobotics/agx_arm_ros) main repository instead:

```bash
git clone -b ros2 --recurse-submodules https://github.com/agilexrobotics/agx_arm_ros.git
```

To visualize the model in ROS2:

```bash
ros2 launch agx_arm_description display.launch.py arm_type:=piper
```

For more details, see the [agx_arm_ros documentation](https://github.com/agilexrobotics/agx_arm_ros).

---

## License

This project is released under the [MIT License](./LICENSE).
