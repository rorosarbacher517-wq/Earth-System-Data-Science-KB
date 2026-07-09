# 知识体系总图

## 一句话定位

本知识库围绕“遥感-气象-生态碳通量-时空数据科学”建立个人知识体系，以我的 HLS + ERA5/气象 + EC 通量塔 + footprint-aware modeling 研究为主干，同时连接科研、工程、政策、产业和职业发展。

## 总体链条

```text
理论
  -> 认识
  -> 数据与技术
  -> 方法
  -> 政策法规
  -> 应用场景
  -> 项目案例
  -> 岗位映射
```

这条链条的含义是：

- 理论告诉我“为什么这个问题重要、变量之间可能有什么机制”。
- 认识帮助我形成判断，而不是只搬运论文观点。
- 数据与技术告诉我“可观测的世界是什么样”。
- 方法告诉我“如何把数据变成证据”。
- 政策法规告诉我“社会为什么需要这些证据”。
- 应用场景告诉我“知识如何进入真实产品、行业和治理”。
- 项目案例把抽象知识落到我做过的事情上。
- 岗位映射把能力翻译给外部世界。

## 我的核心主干

我的主干研究可以概括为：

> 用高分辨率遥感、气象驱动、通量塔观测和动态 footprint 约束，解决 EC 通量观测与遥感像元之间的 observation-support mismatch，从而改进 NEE、GPP、RECO 等碳通量估计，并解释这种改进在空间异质性、时间状态和生态过程边界上的条件。

围绕这个主干，知识库需要持续吸收七类知识：

1. 碳循环、生态生理和陆气交换理论。
2. 遥感观测、HLS/Landsat/Sentinel/MODIS 数据和植被指数。
3. ERA5/ERA5-Land、VPD、辐射、温度、土壤水分等气象变量。
4. EC/FLUXNET/AmeriFlux、footprint、通量分解和质量控制。
5. 时空匹配、尺度转换、空间代表性和泄漏控制。
6. 统计学习、机器学习、Transformer、解释性和不确定性。
7. 双碳、MRV、碳市场、生态监测、ESG、数字能源和空间智能应用。

## 企业、社会、国家、世界需求的连接

| 视角 | 需求 | 知识库对应模块 |
|---|---|---|
| 我 | 建立系统知识、补齐短板、沉淀项目经验 | 全库，尤其 `02_understanding/`、`04_methods/`、`07_projects_and_cases/` |
| 企业 | 数据产品、算法模型、行业解决方案、可交付系统 | `03_data_and_technology/`、`04_methods/`、`06_applications/`、`08_career_mapping/` |
| 社会 | 生态环境监测、气候风险、农业和城市治理 | `05_policy_and_regulation/`、`06_applications/` |
| 国家 | 双碳、生态文明、自然资源监测、数据治理 | `05_policy_and_regulation/`、`06_applications/` |
| 世界 | 气候变化、碳循环不确定性、全球可持续发展 | `01_theory/`、`02_understanding/`、`06_applications/` |

## 第一轮优先补全主题

1. 碳循环与通量基础：NEE、GPP、RECO、NPP、碳源/碳汇。
2. 遥感数据体系：HLS、Landsat、Sentinel、MODIS、植被指数、SIF。
3. 气象驱动体系：ERA5、ERA5-Land、VPD、辐射、温度、水分。
4. EC 观测与 footprint：通量塔、源区、representativeness、support mismatch。
5. 时空数据方法：站点-像元匹配、时间聚合、空间/时间泄漏。
6. 建模方法：逐步回归、随机森林、XGBoost、Transformer、site-level CV。
7. 解释和验证：变量重要性、PDP、SHAP、阈值、稳健性、不确定性。
8. 政策应用：双碳、MRV、碳汇核算、碳市场、ESG。

