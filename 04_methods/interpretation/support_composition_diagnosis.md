# 支持组成差异诊断

## 解决什么问题

模型提升是否真的与 footprint/fixed-window 的支持差异有关？支持组成差异诊断用于回答这个问题。

## 核心思路

比较动态 footprint 源区与固定窗口在 HLS 光学场上的组成差异，例如 NDVI、EVI、NIRv、土地覆盖比例或异质性指标。

如果 footprint-aware 模型的收益在支持组成差异大的样本或站点中更明显，就支持 observation-support mismatch 是重要约束。

## 可能指标

| 指标 | 含义 |
|---|---|
| footprint-weighted NDVI | 动态源区加权平均 NDVI |
| fixed-window NDVI | 固定窗口平均 NDVI |
| delta NDVI | 二者差异 |
| land-cover composition difference | 源区与窗口土地覆盖比例差异 |
| NDVI heterogeneity | 源区内 NDVI 标准差或分位差 |
| footprint entropy | 源区权重集中或分散程度 |

## 分析方式

1. 计算每个 site-day 或 half-hour 的支持组成差异。
2. 计算 FAT 相对 fixed-grid 的误差改善。
3. 按支持差异分组或分位数分析。
4. 检查不同通量分量是否一致。
5. 与生态类型、物候和气象状态交叉分析。

## 解释边界

支持组成差异与模型收益相关，并不自动证明唯一因果机制。还需要 same-backbone ablation、site-level CV 和生态合理性共同支撑。

