# Footprint-weighted aggregation

## 解决什么问题

解决 EC 通量塔观测源区与遥感像元/固定窗口之间的空间支持不一致问题。

## 输入

- 像元级 latent flux field。
- 每个半小时的 footprint 权重。
- EC 塔尺度通量观测。
- HLS 像元网格和有效像元 mask。

## 输出

塔尺度预测值：NEE、GPP、RECO。

## 核心原理

EC 通量观测可以近似理解为源区内地表通量的加权积分。若模型输出的是像元级潜在通量，则可用 footprint 权重将其聚合到塔尺度，与 EC 标签对齐。

```text
y_hat_tower = W_footprint @ y_pixel
```

## 适用场景

- EC tower 与高分辨率遥感融合。
- 地表异质性明显。
- 动态 footprint 与固定窗口组成差异较大。
- 模型需要解释空间支持和观测机制。

## 不适用或需谨慎

- Footprint 输入变量质量差。
- HLS 有效像元比例过低。
- 目标过程主要受地下、滞后或非光学过程控制。
- 研究区域地表极均一，动态 footprint 与固定窗口差异很小。

## 我的项目案例

在 FAT 框架中，footprint 权重不是额外 predictor，而是 observation operator。它决定像元级 latent flux field 如何映射到塔尺度监督信号。

