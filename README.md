# solidstate-lidar-slam

[English](#english) | [中文](#chinese)

> Adapter and benchmark hub for solid-state LiDAR across LIO/LVIO/SLAM, with robust handling for small-FoV short-range and degenerate scenarios.

<a id="english"></a>
## English

### Overview

This repository targets unified adaptation, evaluation, and engineering integration of solid-state LiDAR for LIO/LVIO/SLAM pipelines.

Current status: the repository skeleton is public. Adaptation code will be released progressively module by module.

### Currently Integrated Algorithms

- FAST-LIO2
- FAST-LIVO2
- COIN-LIO
- Direct-LIO
- Voxel-SLAM
- VoxelMap

| Algorithm | Category (LIO/LVIO/SLAM) | Status | Upstream | Upstream License |
| --- | --- | --- | --- | --- |
| FAST-LIO2 | LIO | Adapted internally, release in progress | [hku-mars/FAST_LIO](https://github.com/hku-mars/FAST_LIO) | GPL-2.0 |
| FAST-LIVO2 | LVIO | Adapted internally, release in progress | [hku-mars/FAST-LIVO2](https://github.com/hku-mars/FAST-LIVO2) | GPL-2.0 |
| COIN-LIO | LIO | Adapted internally, release in progress | [ethz-asl/COIN-LIO](https://github.com/ethz-asl/COIN-LIO) | BSD-3-Clause with GPLv2 notice in upstream LICENSE |
| Direct-LIO | LIO | Adapted internally, release in progress | [vectr-ucla/direct_lidar_inertial_odometry](https://github.com/vectr-ucla/direct_lidar_inertial_odometry) | MIT |
| Voxel-SLAM | SLAM | Adapted internally, release in progress | [hku-mars/Voxel-SLAM](https://github.com/hku-mars/Voxel-SLAM) | GPL-2.0 |
| VoxelMap | SLAM | Adapted internally, release in progress | [hku-mars/VoxelMap](https://github.com/hku-mars/VoxelMap) | GPLv2 stated in upstream README |

### Focus: Small-FoV Short-Range and Degenerate Scenarios

Degenerate-scene handling is organized under `docs/degenerate-scenarios/`:

- Low-Texture
- Repetitive Geometry
- Narrow FoV
- Dynamic Interference

### Repository Layout

```text
.
|-- README.md
|-- LICENSE
|-- THIRD_PARTY_LICENSES.md
|-- docs/
|   |-- zh/
|   |-- en/
|   `-- degenerate-scenarios/
|-- modules/
|   |-- fast-lio2/
|   |-- fast-livo2/
|   |-- coin-lio/
|   |-- direct-lio/
|   |-- voxel-slam/
|   `-- voxelmap/
|-- configs/
|-- datasets/
`-- tools/
```

### License Policy

- Repository-level license is `GPL-2.0` (`/LICENSE`) to stay compatible with core upstream GPLv2-based adaptations.
- Third-party algorithm adaptations must follow the corresponding upstream license terms and attribution requirements.
- License mapping and notes are tracked in [`THIRD_PARTY_LICENSES.md`](THIRD_PARTY_LICENSES.md).

### References (Upstream Repositories)

- FAST-LIO2: <https://github.com/hku-mars/FAST_LIO>
- FAST-LIVO2: <https://github.com/hku-mars/FAST-LIVO2>
- COIN-LIO: <https://github.com/ethz-asl/COIN-LIO>
- Direct-LIO: <https://github.com/vectr-ucla/direct_lidar_inertial_odometry>
- Voxel-SLAM: <https://github.com/hku-mars/Voxel-SLAM>
- VoxelMap: <https://github.com/hku-mars/VoxelMap>

### Citation and Acknowledgement

If this repository helps your research or engineering, please star this project and cite the upstream works above.

<a id="chinese"></a>
## 中文

### 项目简介

本仓库聚焦固态面阵激光雷达在 LIO/LVIO/SLAM 算法中的统一适配、评测与工程化集成。

当前阶段：仓库框架已公开，适配代码将按模块逐步开放。

### 当前已适配算法

- FAST-LIO2
- FAST-LIVO2
- COIN-LIO
- Direct-LIO
- Voxel-SLAM
- VoxelMap

| 算法 | 类别 (LIO/LVIO/SLAM) | 状态 | 上游仓库 | 上游许可证 |
| --- | --- | --- | --- | --- |
| FAST-LIO2 | LIO | 已完成适配，代码逐步开放 | [hku-mars/FAST_LIO](https://github.com/hku-mars/FAST_LIO) | GPL-2.0 |
| FAST-LIVO2 | LVIO | 已完成适配，代码逐步开放 | [hku-mars/FAST-LIVO2](https://github.com/hku-mars/FAST-LIVO2) | GPL-2.0 |
| COIN-LIO | LIO | 已完成适配，代码逐步开放 | [ethz-asl/COIN-LIO](https://github.com/ethz-asl/COIN-LIO) | BSD-3-Clause（上游 LICENSE 同时包含 GPLv2 说明） |
| Direct-LIO | LIO | 已完成适配，代码逐步开放 | [vectr-ucla/direct_lidar_inertial_odometry](https://github.com/vectr-ucla/direct_lidar_inertial_odometry) | MIT |
| Voxel-SLAM | SLAM | 已完成适配，代码逐步开放 | [hku-mars/Voxel-SLAM](https://github.com/hku-mars/Voxel-SLAM) | GPL-2.0 |
| VoxelMap | SLAM | 已完成适配，代码逐步开放 | [hku-mars/VoxelMap](https://github.com/hku-mars/VoxelMap) | 上游 README 声明 GPLv2 |

### 重点问题：小角度短距与退化场景

退化场景方案入口：`docs/degenerate-scenarios/`。

- Low-Texture
- Repetitive Geometry
- Narrow FoV
- Dynamic Interference

### 仓库结构

```text
.
|-- README.md
|-- LICENSE
|-- THIRD_PARTY_LICENSES.md
|-- docs/
|   |-- zh/
|   |-- en/
|   `-- degenerate-scenarios/
|-- modules/
|   |-- fast-lio2/
|   |-- fast-livo2/
|   |-- coin-lio/
|   |-- direct-lio/
|   |-- voxel-slam/
|   `-- voxelmap/
|-- configs/
|-- datasets/
`-- tools/
```

### 许可证策略

- 仓库级许可证采用 `GPL-2.0`（见 `/LICENSE`），用于与核心 GPLv2 上游适配保持一致。
- 各算法模块在引入或修改上游代码时，必须遵循对应上游许可证和署名要求。
- 详细映射见 [`THIRD_PARTY_LICENSES.md`](THIRD_PARTY_LICENSES.md)。

### 开源仓库引用

- FAST-LIO2: <https://github.com/hku-mars/FAST_LIO>
- FAST-LIVO2: <https://github.com/hku-mars/FAST-LIVO2>
- COIN-LIO: <https://github.com/ethz-asl/COIN-LIO>
- Direct-LIO: <https://github.com/vectr-ucla/direct_lidar_inertial_odometry>
- Voxel-SLAM: <https://github.com/hku-mars/Voxel-SLAM>
- VoxelMap: <https://github.com/hku-mars/VoxelMap>

### 引用与致谢

如果本仓库对你的研究或工程有帮助，欢迎 Star，并优先引用上述上游工作。
