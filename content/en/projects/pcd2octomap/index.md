---
title: "PCD to OctoMap"
description: "A ROS utility for converting PCD point clouds to OctoMap files, with support for PointXYZ, PointXYZRGB, and PointXYZRGBA."
translationKey: pcd2octomap
weight: 3
category: "Map representation"
source: "https://github.com/siyiovo/pcd2octomap"
tags:
  - ROS
  - PCL
  - OctoMap
---

## Overview

This ROS package converts PCD files to OctoMap `.bt` or `.ot` formats. The repository documents support for `pcl::PointXYZ`, `pcl::PointXYZRGB`, and `pcl::PointXYZRGBA` point types.

## Configurable parameters

- Octree resolution through `octree_resolution`, defaulting to `0.05` in the repository.
- Voxel filter size through `voxel_grid_leaf_size`, defaulting to `0.05`.
- Map pose parameters for adjusting map rotation.

## Project notes

These details are based on the public repository README. Dataset details, conversion timings, and integration context can be added later.
