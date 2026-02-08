# Third-Party License Mapping

Last verified: 2026-02-08

This repository tracks adaptation work across multiple upstream projects. When source code is adapted from an upstream project, the corresponding module must keep upstream copyright notices and comply with upstream license terms.

| Algorithm Label in This Repo | Upstream Repository | Observed Upstream License Signal | Notes |
| --- | --- | --- | --- |
| FAST-LIO2 | <https://github.com/hku-mars/FAST_LIO> | GPL-2.0 (`LICENSE`) | Core upstream for FAST-LIO2 adaptation lineage. |
| FAST-LIVO2 | <https://github.com/hku-mars/FAST-LIVO2> | GPL-2.0 (`LICENSE`) | Direct upstream repository. |
| COIN-LIO | <https://github.com/ethz-asl/COIN-LIO> | BSD-3-Clause + embedded GPLv2 notice (`LICENSE`) | Upstream LICENSE states BSD-3-Clause for added code and includes GPLv2 text due FAST-LIO2 base. |
| Direct-LIO | <https://github.com/vectr-ucla/direct_lidar_inertial_odometry> | MIT (`LICENSE`) | Used as Direct-LIO reference implementation in this repository. |
| Voxel-SLAM | <https://github.com/hku-mars/Voxel-SLAM> | GPL-2.0 (`LICENSE`) | Direct upstream repository. |
| VoxelMap | <https://github.com/hku-mars/VoxelMap> | GPLv2 statement in upstream README (`README.md`, section "License") | No root LICENSE file detected in upstream repository at verification time. |

## Compliance Policy

- Repository-level license is GPL-2.0.
- Module-level adapted source files must retain required upstream notices.
- If future upstream license terms change, this file and module notices must be updated before release.
