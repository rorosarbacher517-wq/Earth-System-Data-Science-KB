# 时空数据类型：raster、vector、point、time series

## 为什么要区分数据类型

遥感碳通量研究同时处理多种数据结构。只有清楚每类数据的空间/时间含义，才能避免错误匹配和错误解释。

## 主要数据类型

| 类型 | 示例 | 典型操作 | 风险 |
|---|---|---|---|
| Raster | HLS 反射率、NDVI、土地覆盖 | 重投影、裁剪、重采样、窗口统计 | NoData、投影、分辨率不一致 |
| Vector | 站点位置、行政边界、生态区 | 空间 join、buffer、overlay | 坐标系、边界精度 |
| Point observation | EC tower、气象站 | 最近邻、缓冲区、源区匹配 | 点位不等于观测范围 |
| Time series | 半小时通量、ERA5 小时变量、HLS 时序 | 插值、聚合、滞后窗口、异常值 | 时区、缺测、时间泄漏 |
| Tensor sample | HLS patch + 48 half-hour forcing | 模型训练、batch、mask | 维度、归一化和缺测处理复杂 |

## 项目中的典型数据结构

```text
HLS:       site-day-patch, 30 m raster grid
ERA5:      site-day-time, hourly/half-hour forcing
EC flux:   site-day-time, NEE/GPP/RECO target
FFP:       site-day-time-pixel, footprint weights
Metadata:  site-level static attributes
```

## 常见错误

1. 把 EC tower 当成一个点值，而不是动态 source-area 观测。
2. 把 ERA5 网格误解成局地 30 m 气象差异。
3. 将 HLS 缺测像元直接填 0，造成虚假地表信号。
4. 在随机划分样本后再做归一化，造成站点泄漏。
5. 忽略时区差异，把遥感、气象和通量错位匹配。

## 我的工作原则

每次构建样本前，先写清楚：

- 每个变量的空间支持是什么；
- 每个变量的时间支持是什么；
- 标签和输入是否代表同一个观测支持；
- 缺测、QC 和归一化在哪里处理；
- 训练/测试划分是否发生泄漏。

