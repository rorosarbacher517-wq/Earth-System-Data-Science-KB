# Footprint-aware Transformer 建模策略

## 问题定义

目标不是简单预测站点通量，而是学习一个能与 EC 观测机制对齐的模型：

```text
HLS patch + meteorology + time
  -> latent pixel-level flux field
  -> footprint observation operator
  -> tower-scale NEE/GPP/RECO prediction
```

## 输入

- HLS patch：空间网格上的光学特征。
- 气象时间序列：48 个半小时的 forcing。
- 时间变量：DOY、hour、season、sensor。
- Footprint 权重：每个半小时的源区空间权重。

## 输出

- 塔尺度 NEE、GPP、RECO 预测。
- 可选：像元级 latent flux field，用于机制可视化。

## 模型设计逻辑

1. HLS branch 编码空间光学特征。
2. 气象和时间 embedding 表征过程驱动。
3. Temporal self-attention 学习日内响应。
4. MLP 输出像元级 latent flux。
5. Footprint operator 将像元级输出聚合到塔尺度。

## 为什么 footprint 不只是 predictor

如果把 footprint 当作一个普通特征，模型只知道“这个时刻有某些权重信息”，但不一定遵守 EC 观测的空间积分结构。

将 footprint 放在输出聚合层，相当于明确告诉模型：

```text
塔观测 = 源区内像元通量的加权积分
```

这比简单拼接特征更符合物理观测机制。

## 验证设计

必须与 fixed-grid Transformer 做 same-backbone comparison：

- 相同输入。
- 相同架构。
- 相同训练协议。
- 相同 site-level folds。
- 只改变 aggregation operator。

这样才能把差异主要归因于 observation-support alignment。

