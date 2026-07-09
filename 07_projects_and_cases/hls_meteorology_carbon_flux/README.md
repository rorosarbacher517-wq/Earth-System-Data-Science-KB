# HLS-气象-footprint 碳通量研究

## 项目定位

这是当前知识库的主干案例。它把遥感、气象、生态碳循环、通量塔观测、动态 footprint、时空数据科学和机器学习建模连接在一起。

## 一句话概括

本项目尝试解决 EC 通量塔观测与高分辨率遥感像元之间的 observation-support mismatch：模型先基于 HLS 30 m 光学场和气象驱动学习潜在像元级通量场，再用动态 footprint 权重作为 observation operator 聚合到塔尺度，以估计 NEE、GPP 和 RECO。

## 科学问题

1. 固定像元或固定窗口是否足以代表 EC 通量观测的动态源区？
2. Footprint-aware spatial aggregation 是否能改善碳通量估计？
3. 这种改善是否取决于空间异质性、物候状态、日内状态和气象条件？
4. GPP、NEE、RECO 的收益为什么不同？
5. 模型提升来自 footprint 对齐，还是来自模型容量、输入变量或数据划分？

## 项目证据链

```text
EC 观测源区动态
  -> 固定像元/窗口存在支持错配
  -> HLS 30 m 放大异质性表达和错配敏感性
  -> FFP footprint 提供物理约束权重
  -> FAT 使用 footprint 作为 observation operator
  -> same-backbone fixed-grid comparison 检验收益来源
  -> site-level CV 控制泄漏
  -> GPP/NEE/RECO 分量差异解释机制边界
```

## 使用的数据

| 数据 | 作用 |
|---|---|
| HLS 30 m 光学数据 | 表征 source-area 内的地表和植被异质性 |
| ERA5/ERA5-Land 或站点气象 | 提供辐射、温度、水分、大气需求等背景 forcing |
| FLUXNET/AmeriFlux EC 数据 | 提供 NEE、GPP、RECO 目标变量 |
| Footprint/FFP 权重 | 表征每个半小时通量观测的动态空间支持 |
| 站点元数据/土地覆盖/气候区 | 支持分层分析、解释和验证 |

## 使用的方法

| 方法 | 作用 |
|---|---|
| QC 和数据同步 | 保证遥感、气象、通量和 footprint 时间一致 |
| Footprint-weighted aggregation | 将像元级 latent flux field 聚合到塔尺度 |
| Transformer temporal modeling | 表征 48 个半小时内的日内响应 |
| Same-backbone ablation | 分离 footprint operator 和模型容量的影响 |
| Site-level CV | 避免站点泄漏和伪重复 |
| 支持组成诊断 | 判断 fixed window 与 dynamic footprint 的 NDVI/组成差异 |
| 分量解释 | 解释 GPP、NEE、RECO 对光学约束和气象驱动的不同响应 |

## 对知识库的连接

- 理论层：碳循环、生态生理、遥感观测、footprint、时空尺度。
- 认识层：support mismatch、机制与相关性、模型容量与观测算子。
- 数据技术层：HLS、ERA5、EC flux、FFP、Python/GIS/深度学习。
- 方法层：时空匹配、建模、解释、验证、可视化。
- 政策法规层：碳监测、MRV、生态碳汇、双碳。
- 应用层：碳汇评估、遥感碳监测、AI for Earth、数字能源。
- 知识迁移层：遥感产品验证、时空数据融合、AI for Earth、碳监测和生态风险分析。

## 后续需要沉淀

1. 把现有代码流程整理成 `data_pipeline.md`。
2. 把模型结构和 observation operator 整理成 `modeling_strategy.md`。
3. 把结果图、审稿逻辑和稳健性分析整理成 `results_and_limitations.md`。
4. 把可迁移经验整理成 `reusable_experience.md`。
