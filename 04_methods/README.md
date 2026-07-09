# 04 方法层

方法层回答：我如何把数据变成证据？

这是知识库的“工具箱”和“作战手册”。每个方法笔记都应该说明适用场景、输入输出、原理、步骤、风险和在我的项目中的使用方式。

## 子模块

| 子模块 | 方法主题 |
|---|---|
| `preprocessing/` | 数据清洗、质量控制、缺失值、重采样、合成 |
| `spatiotemporal_matching/` | 站点-像元匹配、footprint 加权、时间同步、尺度转换 |
| `feature_engineering/` | 植被指数、气象聚合、时间特征、异质性指标 |
| `modeling/` | 回归、随机森林、XGBoost、Transformer、多任务建模 |
| `interpretation/` | 变量重要性、PDP、SHAP、机制解释 |
| `validation/` | site-level CV、空间/时间泄漏控制、不确定性和稳健性 |
| `visualization/` | 地图、多面板图、响应曲线、模型诊断图 |

## 我的核心方法链

```text
数据获取
  -> QC 和时空同步
  -> HLS/气象/通量/footprint 样本构建
  -> 特征工程和尺度匹配
  -> 模型训练
  -> site-level 验证
  -> 支持组成诊断
  -> 解释性和稳健性分析
  -> 图表和结论表达
```

## 第一轮重点方法

1. Footprint-weighted aggregation。
2. Site-level cross-validation。
3. HLS 云掩膜和有效像元检查。
4. VPD、辐射、温度、水分变量构建。
5. Same-backbone ablation。
6. 支持组成差异诊断。
7. GPP/NEE/RECO 分量差异解释。

