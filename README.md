# 个人地球系统数据科学知识库

这个知识库以“遥感、气象、生态碳通量与时空数据科学”为主干，用来长期沉淀理论、概念、数据、方法、政策、应用、项目经验和阅读资料。它的核心目的不是展示话术，而是帮助我建立可持续生长的知识体系。

## 主干问题

如何利用 HLS/Landsat/Sentinel/MODIS 等遥感数据、ERA5/ERA5-Land 等气象数据、FLUXNET/AmeriFlux 等通量观测数据，以及统计建模、机器学习、深度学习和时空数据工程方法，理解并量化陆地生态系统中的 NEE、GPP、RECO 等碳通量过程？

## 知识体系

本库按“理论、认识、数据与技术、方法、政策法规、应用、项目案例、知识迁移”组织。

| 模块 | 作用 | 核心问题 |
|---|---|---|
| `00_knowledge_framework/` | 管理知识库的总规则 | 如何持续积累、归类、核验和复盘知识 |
| `01_theory/` | 底层理论 | 这个领域的概念、机制和基本假设是什么 |
| `02_understanding/` | 个人认识 | 如何形成对问题边界、尺度和不确定性的判断 |
| `03_data_and_technology/` | 数据与技术 | 有哪些可观测数据、工具和计算平台 |
| `04_methods/` | 方法库 | 如何处理、建模、验证、解释和表达 |
| `05_policy_and_regulation/` | 政策法规 | 碳、生态、气候和数据治理的制度背景是什么 |
| `06_applications/` | 应用场景 | 这些知识如何服务碳监测、生态评估和气候风险分析 |
| `07_projects_and_cases/` | 项目案例 | 如何从实际研究中沉淀可复用经验 |
| `08_knowledge_transfer/` | 知识迁移 | 如何把知识连接到相邻学科、工程系统和现实问题 |
| `resources/` | 资料资产 | 参考文献、政策源、数据源、术语和学习路线 |

## 已填充的核心内容

### 理论层

- [碳通量核心概念：NEE、GPP、RECO、NPP](01_theory/carbon_cycle/carbon_flux_core_concepts.md)
- [光学遥感与植被碳过程](01_theory/remote_sensing/optical_remote_sensing_for_vegetation.md)
- [气象因子对碳通量的控制](01_theory/meteorology_climate/meteorological_controls_on_carbon_flux.md)
- [观测支持、尺度与代表性](01_theory/spatiotemporal_science/observation_support_and_scale.md)
- [预测、解释与因果的边界](01_theory/statistics_ml/prediction_explanation_causality.md)

### 数据与方法层

- [时空数据类型](03_data_and_technology/geospatial_data/spatiotemporal_data_types.md)
- [Python 地理空间与时空数据工具栈](03_data_and_technology/python_tools/python_geospatial_stack.md)
- [HLS 质量控制与有效像元检查](04_methods/preprocessing/hls_quality_control.md)
- [气象特征工程](04_methods/feature_engineering/meteorological_feature_engineering.md)
- [Footprint-aware Transformer 建模策略](04_methods/modeling/footprint_aware_transformer.md)
- [支持组成差异诊断](04_methods/interpretation/support_composition_diagnosis.md)
- [泄漏控制与稳健性检查清单](04_methods/validation/leakage_and_robustness_checklist.md)

### 政策与应用层

- [中国双碳政策背景](05_policy_and_regulation/carbon_neutrality/china_dual_carbon_policy_context.md)
- [MRV 与碳监测](05_policy_and_regulation/carbon_accounting/mrv_and_carbon_monitoring.md)
- [碳监测与 MRV 产品图谱](06_applications/carbon_monitoring_mrv/carbon_monitoring_product_map.md)
- [数字能源与碳管理](06_applications/digital_energy/digital_energy_and_carbon_management.md)
- [生态系统气候风险评估](06_applications/climate_risk/ecosystem_climate_risk_assessment.md)
- [ESG 与环境数据系统](06_applications/esg_sustainability/esg_environmental_data_system.md)

### 知识迁移与资料资产

- [跨领域应用图谱](08_knowledge_transfer/cross_domain_application_map.md)
- [HLS-footprint 碳通量项目解释](08_knowledge_transfer/project_explanation_for_learning.md)
- [知识能力矩阵](08_knowledge_transfer/knowledge_capability_matrix.md)
- [来源与证据索引](00_knowledge_framework/06_sources_and_evidence_index.md)
- [核心参考文献 BibTeX](resources/references/core_references.bib)
- [权威数据源清单](resources/data_sources/authoritative_data_sources.csv)
- [政策与标准来源清单](resources/policy_sources/policy_and_standard_sources.csv)
- [核心术语表](resources/glossary/core_terms.md)
- [学习路线图](resources/learning_paths/earth_system_data_science_path.md)

## 资料归档原则

1. 数据、政策、论文和报告都要记录来源、时间、URL、许可或使用边界。
2. 公开仓库优先存放元数据、阅读笔记、引用文件和公开资料链接；受版权或许可限制的 PDF 不直接上传。
3. 每篇论文进入知识库时，需要写清研究问题、数据、方法、发现、局限和可复用内容。
4. 每个方法笔记需要说明适用场景、不适用场景、输入、输出、验证方式和常见错误。
5. 项目案例只作为知识沉淀，不作为宣传材料；重点记录问题定义、证据链、方法边界和可迁移经验。

