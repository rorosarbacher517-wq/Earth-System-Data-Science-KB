# 知识体系总图

## 一句话定位

本知识库围绕“遥感、气象、生态碳通量与时空数据科学”建立长期知识体系，以 HLS、ERA5/气象、EC 通量塔和 footprint-aware modeling 为主干，连接理论学习、数据技术、方法沉淀、政策理解、应用分析和项目复盘。

## 总体链条

```text
理论
  -> 认识
  -> 数据与技术
  -> 方法
  -> 政策法规
  -> 应用场景
  -> 项目案例
  -> 知识迁移
```

这条链条的含义是：

- 理论说明变量、机制和假设的来源。
- 认识帮助形成对尺度、边界、不确定性和证据强度的判断。
- 数据与技术说明可观测世界的结构和工具。
- 方法说明如何把数据转化为可检验的证据。
- 政策法规说明知识进入社会治理和碳管理体系的制度背景。
- 应用场景说明知识如何服务真实环境问题。
- 项目案例把抽象知识落实到具体研究流程。
- 知识迁移帮助把一个研究中的经验推广到相邻问题。

## 主干研究问题

> 如何使用高分辨率遥感、气象驱动、通量塔观测和动态 footprint 约束，识别并减弱 EC 通量观测与遥感像元之间的 observation-support mismatch，从而改进 NEE、GPP、RECO 等碳通量估计，并理解这种改进在空间异质性、时间状态和生态过程边界上的条件？

围绕这个主干，知识库持续吸收七类知识：

1. 碳循环、生态生理和陆气交换理论。
2. 遥感观测、HLS/Landsat/Sentinel/MODIS 数据和植被指数。
3. ERA5/ERA5-Land、VPD、辐射、温度、土壤水分等气象变量。
4. EC/FLUXNET/AmeriFlux、footprint、通量分解和质量控制。
5. 时空匹配、尺度转换、空间代表性和泄漏控制。
6. 统计学习、机器学习、Transformer、解释性和不确定性。
7. 双碳、MRV、碳市场、生态监测、ESG、气候风险和空间智能应用。

## 多层需求的连接

| 视角 | 关注问题 | 知识库对应模块 |
|---|---|---|
| 个人学习 | 建立系统知识、补齐短板、沉淀项目经验 | 全库，尤其 `02_understanding/`、`04_methods/`、`07_projects_and_cases/` |
| 科学研究 | 理解机制、构建证据、控制不确定性 | `01_theory/`、`02_understanding/`、`04_methods/` |
| 工程实现 | 组织数据、复现流程、扩展计算 | `03_data_and_technology/`、`04_methods/`、`resources/` |
| 社会治理 | 生态环境监测、气候风险、农业和城市治理 | `05_policy_and_regulation/`、`06_applications/` |
| 国家战略 | 双碳、生态文明、自然资源监测、数据治理 | `05_policy_and_regulation/`、`06_applications/` |
| 全球议题 | 气候变化、碳循环不确定性、可持续发展 | `01_theory/`、`05_policy_and_regulation/`、`06_applications/` |

## 第一轮优先补全主题

1. 碳循环与通量基础：NEE、GPP、RECO、NPP、碳源/碳汇。
2. 遥感数据体系：HLS、Landsat、Sentinel、MODIS、植被指数、SIF。
3. 气象驱动体系：ERA5、ERA5-Land、VPD、辐射、温度、水分。
4. EC 观测与 footprint：通量塔、源区、representativeness、support mismatch。
5. 时空数据方法：站点-像元匹配、时间聚合、空间/时间泄漏。
6. 建模方法：逐步回归、随机森林、XGBoost、Transformer、site-level CV。
7. 解释和验证：变量重要性、PDP、SHAP、阈值、稳健性、不确定性。
8. 政策应用：双碳、MRV、碳汇核算、碳市场、ESG。

