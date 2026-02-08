# solidstate-lidar-slam

面向固态面阵激光雷达的 LIO/LVIO/SLAM 统一适配与评测基线仓库，重点覆盖小角度短距雷达与退化场景鲁棒性问题。  
An adapter and benchmark baseline repository for solid-state LiDAR across LIO/LVIO/SLAM, with emphasis on small-FoV short-range sensing and degenerate-scene robustness.

## 项目简介

本仓库聚焦固态面阵激光雷达在多类里程计与建图算法中的统一接入、配置规范和效果对比。  
当前阶段仓库框架已建立，适配代码将逐步开放（持续补充模块实现、配置模板与实验记录）。

## 当前已适配算法

- FAST-LIO2
- FAST-LIVO2
- Coin-LIO
- Direct-LIO
- Voxel-SLAM
- VoxelMap

| Algorithm | Category (LIO/LVIO/SLAM) | Status | Notes |
| --- | --- | --- | --- |
| FAST-LIO2 | LIO | Adapted internally | Open-source module release in progress |
| FAST-LIVO2 | LVIO | Adapted internally | Open-source module release in progress |
| Coin-LIO | LIO | Adapted internally | Open-source module release in progress |
| Direct-LIO | LIO | Adapted internally | Open-source module release in progress |
| Voxel-SLAM | SLAM | Adapted internally | Open-source module release in progress |
| VoxelMap | SLAM | Adapted internally | Open-source module release in progress |

## 重点问题：小角度短距与退化场景

本仓库重点组织以下退化场景方案，入口位于 `docs/degenerate-scenarios/`：

- Low-Texture
- Repetitive Geometry
- Narrow FoV
- Dynamic Interference

## 仓库结构

```text
.
|-- README.md
|-- LICENSE
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

## 快速开始

1. 克隆仓库并进入目录。  
2. 按算法模块查看后续开放的适配代码与配置说明。  
3. 使用 `docs/degenerate-scenarios/` 的分类文档选择对应退化场景处理策略。  

## 路线图

- 发布各算法模块的最小可运行适配代码与配置基线。
- 补充小角度短距雷达的参数建议与评测协议。
- 完善退化场景测试集组织和结果对比模板。

## 引用与致谢

若本仓库对你的研究或工程有帮助，欢迎 Star 并在后续引用信息发布后使用标准格式引用。  
感谢 FAST-LIO2、FAST-LIVO2、Coin-LIO、Direct-LIO、Voxel-SLAM、VoxelMap 等相关工作与社区贡献。

## Overview (EN)

This repository standardizes integration, configuration conventions, and evaluation for solid-state LiDAR across multiple odometry and mapping pipelines.  
The repository skeleton is ready, and adapter code will be open-sourced progressively (with module implementations, config templates, and experiment records added iteratively).

## Currently Integrated Algorithms

- FAST-LIO2
- FAST-LIVO2
- Coin-LIO
- Direct-LIO
- Voxel-SLAM
- VoxelMap

| Algorithm | Category (LIO/LVIO/SLAM) | Status | Notes |
| --- | --- | --- | --- |
| FAST-LIO2 | LIO | Adapted internally | Open-source module release in progress |
| FAST-LIVO2 | LVIO | Adapted internally | Open-source module release in progress |
| Coin-LIO | LIO | Adapted internally | Open-source module release in progress |
| Direct-LIO | LIO | Adapted internally | Open-source module release in progress |
| Voxel-SLAM | SLAM | Adapted internally | Open-source module release in progress |
| VoxelMap | SLAM | Adapted internally | Open-source module release in progress |

## Focus: Small-FoV Short-Range and Degenerate Scenarios

Degenerate-scene handling is organized under `docs/degenerate-scenarios/` with the following taxonomy:

- Low-Texture
- Repetitive Geometry
- Narrow FoV
- Dynamic Interference

## Repository Layout

```text
.
|-- README.md
|-- LICENSE
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

## Quick Start

1. Clone the repository and enter the project folder.  
2. Check each algorithm module for progressively released adapter code and configs.  
3. Use the taxonomy in `docs/degenerate-scenarios/` to select handling strategies for specific degenerate conditions.

## Roadmap

- Release minimum runnable adapter modules and baseline configs for each algorithm.
- Add parameter recommendations and evaluation protocols for small-FoV short-range LiDAR.
- Complete degenerate-scene dataset organization and benchmark reporting templates.

## Citation and Acknowledgement

If this repository is useful for your research or production work, please star it and cite it once citation metadata is published.  
We acknowledge the upstream works and communities around FAST-LIO2, FAST-LIVO2, Coin-LIO, Direct-LIO, Voxel-SLAM, and VoxelMap.
