# 核心术语表

## NEE

- 中文：净生态系统交换
- 英文：Net Ecosystem Exchange
- 简释：生态系统与大气之间 CO2 的净交换量。
- 注意：不同数据集可能有不同符号约定，使用前必须确认正负方向。

## GPP

- 中文：总初级生产力
- 英文：Gross Primary Productivity
- 简释：植物光合作用固定的总碳量。
- 相关数据：EC 通量分解、遥感植被指数、SIF、NIRv。

## RECO

- 中文：生态系统呼吸
- 英文：Ecosystem Respiration
- 简释：植物和微生物呼吸释放的 CO2 总量。
- 注意：受温度、土壤水分、底物供应和滞后过程影响。

## Footprint

- 中文：通量源区
- 英文：Flux footprint
- 简释：某一时刻 EC 通量观测所代表的上风向源区及其权重分布。
- 相关方法：FFP、footprint-weighted aggregation。

## Observation Support

- 中文：观测支持
- 英文：Observation support
- 简释：一个观测值在空间和时间上代表的范围。
- 重要性：遥感像元、EC 通量、ERA5 网格和样地点的观测支持不同。

## Support Mismatch

- 中文：观测支持错配
- 英文：Support mismatch
- 简释：输入特征、监督标签或验证数据代表的空间/时间范围不一致。
- 项目关联：HLS fixed-window 与 EC dynamic footprint 的不一致。

## VPD

- 中文：饱和水汽压差
- 英文：Vapor Pressure Deficit
- 简释：空气干燥程度指标，反映大气对水分的需求。
- 生态意义：高 VPD 常导致气孔关闭，限制 GPP。

## Site-level Cross-validation

- 中文：站点级交叉验证
- 英文：Site-level cross-validation
- 简释：同一站点的所有样本进入同一个 fold，用于减少站点泄漏。

## MRV

- 中文：监测、报告与核查
- 英文：Monitoring, Reporting and Verification
- 简释：碳管理和气候治理中保证数据可信的机制。

