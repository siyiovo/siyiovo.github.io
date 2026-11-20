---
title: "PCD to OctoMap"
description: "将 PCD 点云转换为 OctoMap 文件的 ROS 工具，支持 PointXYZ、PointXYZRGB 和 PointXYZRGBA 类型。"
translationKey: pcd2octomap
weight: 3
category: "地图表示"
source: "https://github.com/siyiovo/pcd2octomap"
tags:
  - ROS
  - PCL
  - OctoMap
---

## 项目概述

该 ROS 软件包用于将 PCD 文件转换为 OctoMap 的 `.bt` 或 `.ot` 格式。仓库说明列出 `pcl::PointXYZ`、`pcl::PointXYZRGB` 与 `pcl::PointXYZRGBA` 三种点类型。

## 可配置参数

- 八叉树分辨率 `octree_resolution`，仓库默认值为 `0.05`。
- 体素滤波尺寸 `voxel_grid_leaf_size`，仓库默认值为 `0.05`。
- 地图位姿参数可用于调整地图旋转。

## 项目资料

以上信息依据公开仓库 README。实际数据集、转换耗时和集成场景待补充。
