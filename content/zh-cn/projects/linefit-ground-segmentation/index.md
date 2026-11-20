---
title: "Linefit Ground Segmentation Notes"
description: "围绕激光雷达地面分割算法的代码阅读与学习记录，包含点云投影、直线拟合和分类步骤。"
translationKey: linefit-ground-segmentation
weight: 2
category: "激光雷达点云"
source: "https://github.com/siyiovo/linefit_ground_segmentation_with_details"
tags:
  - LiDAR
  - PCL
  - Ground segmentation
---

## 项目概述

该仓库围绕 Navigation 中的 `linefit_ground_segmentation` 实现整理学习资料。仓库说明将算法概括为将三维点云投影到距离与高度平面，再通过直线拟合和高度判定完成地面分类。

## 资料结构

- 点云投影
- 直线拟合
- 地面与非地面分类
- STL、PCL 与相关论文的阅读指引

## 项目资料

页面描述基于公开仓库 README。代码修改范围、实验数据和个人贡献记录待作者补充。
