# 03 数据与技术层

数据与技术层回答：我用什么数据和工具认识这个问题？

这里存放数据源、数据结构、处理工具、平台、软件包和工程化技术。它与方法层的区别是：本层关注“材料和工具”，方法层关注“如何解决问题”。

## 数据体系

| 数据类型 | 代表数据 | 用途 |
|---|---|---|
| 遥感数据 | HLS、Landsat、Sentinel-2、MODIS、SIF | 表征植被状态、地表异质性、物候和生产力 |
| 气象数据 | ERA5、ERA5-Land、站点气象 | 表征辐射、温度、水分、VPD 和大气需求 |
| 通量观测 | FLUXNET、AmeriFlux、EC tower | 提供 NEE、GPP、RECO 等目标变量 |
| 空间辅助 | 土地覆盖、DEM、站点元数据、气候区 | 分层分析、空间匹配和解释 |
| 政策行业 | 双碳政策、MRV 标准、ESG 报告 | 应用需求和合规背景 |

## 技术工具

- Python: `pandas`, `numpy`, `xarray`, `scikit-learn`, `pytorch`
- 地理空间: `rasterio`, `geopandas`, `shapely`, `pyproj`
- 遥感平台: Google Earth Engine, NASA/USGS 数据平台
- 大数据与工程: Zarr, NetCDF, Slurm, chunk processing, logging, config
- 可视化: Matplotlib, Seaborn, Cartopy, QGIS

## 第一轮重点

1. HLS 数据结构、质量控制和植被指数。
2. ERA5/ERA5-Land 变量含义和尺度限制。
3. FLUXNET/AmeriFlux 变量、QC 和通量分解。
4. FFP footprint 输入变量和权重输出。
5. Python 地理空间处理工具链。

