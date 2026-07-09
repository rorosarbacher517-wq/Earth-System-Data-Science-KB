# 使用的方法

## Observation Operator

核心思想：

```text
tower_flux(t) = sum_i footprint_weight_i(t) * pixel_flux_i(t)
```

这里 `pixel_flux_i(t)` 是模型学习出的潜在像元级通量场，`footprint_weight_i(t)` 来自源区物理约束。Footprint 不是普通 predictor，而是把像元级输出映射到塔尺度监督标签的观测算子。

## Same-backbone Comparison

为了证明收益来自 footprint-aware spatial support，而不是模型容量，需要保持：

- 相同输入数据。
- 相同 Transformer backbone。
- 相同 loss、normalization、training protocol。
- 相同 site-level validation split。
- 只改变 spatial aggregation operator。

## Site-level Cross-validation

同一个站点的所有样本必须进入同一 fold。这样可以降低站点泄漏，避免模型通过站点特征记忆得到过乐观指标。

## 分量解释

GPP、NEE、RECO 应分别解释：

- GPP 更直接受光学可观测冠层状态和辐射影响。
- NEE 是 GPP 与 RECO 共同结果，解释更复杂。
- RECO 包含地下碳库、温湿滞后和非光学控制，footprint-aware HLS 对它的帮助可能较弱。

