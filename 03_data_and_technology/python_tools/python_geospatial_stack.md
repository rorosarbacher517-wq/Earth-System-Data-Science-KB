# Python 地理空间与时空数据工具栈

## 核心工具

| 工具 | 用途 | 我需要掌握的重点 |
|---|---|---|
| `pandas` | 表格、站点元数据、指标汇总 | groupby、merge、时间索引、缺失值 |
| `numpy` | 数组计算 | mask、广播、向量化、nan 处理 |
| `xarray` | 多维时空数据 | NetCDF/Zarr、维度命名、按时间/空间切片 |
| `rasterio` | 栅格读写 | CRS、transform、window、mask、profile |
| `geopandas` | 矢量数据 | CRS、spatial join、buffer、overlay |
| `shapely` | 几何计算 | polygon、intersection、area、distance |
| `pyproj` | 坐标转换 | WGS84、UTM、等面积投影 |
| `scikit-learn` | 传统机器学习 | CV、metrics、pipeline、feature importance |
| `pytorch` | 深度学习 | tensor、mask、batch、GPU、loss |
| `matplotlib` / `cartopy` | 图表和地图 | 多面板图、投影、色标、图例 |

## 项目结构建议

```text
project/
  configs/
  data/
    raw/
    interim/
    processed/
  scripts/
  src/
  notebooks/
  outputs/
  docs/
```

## 可复现原则

1. 所有路径和参数进入配置文件。
2. 中间数据保留 manifest：输入、输出、时间、脚本版本。
3. 每个处理阶段输出 QC 表。
4. 模型训练记录 random seed、fold、normalizer 和指标。
5. 图件生成脚本与数据版本绑定。

## 我的短板补强

- 更系统地掌握 `xarray` + `zarr` 的大规模时空数据处理。
- 学会将 notebook 中的探索流程沉淀为可重复脚本。
- 建立项目级日志和错误恢复机制。

