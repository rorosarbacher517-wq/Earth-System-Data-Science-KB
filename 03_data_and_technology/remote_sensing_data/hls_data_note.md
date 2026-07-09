# HLS 数据笔记

## 是什么

HLS 是 Harmonized Landsat and Sentinel-2 的缩写，目标是将 Landsat 和 Sentinel-2 的观测协调成更高时间频率、可分析的地表反射率产品。

## 为什么对我重要

我的研究使用 HLS 30 m 光学数据来表征 EC 通量塔周围的地表异质性。HLS 的价值不只是分辨率高，而是它能在相对高频次上追踪植被状态、物候和地表组成变化。

## 需要掌握

1. L30 和 S30 产品差异。
2. 波段含义和植被指数计算。
3. 云、阴影、雪和质量标记。
4. Landsat 与 Sentinel-2 的光谱 harmonization。
5. 30 m 像元与 EC footprint 的空间支持匹配问题。
6. HLS 数据访问、批量下载和重建流程。

## 与主干项目的关系

HLS 在项目中是可被 footprint 加权的空间场。它不是单点 predictor，而是 source-area 内每个像元的光学状态集合。模型应先学习像元级 latent flux field，再通过 footprint observation operator 聚合到塔尺度。

