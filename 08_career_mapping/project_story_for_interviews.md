# 面试项目讲述：HLS-footprint 碳通量项目

## 30 秒版本

我做过一个多源时空数据融合项目，目标是用 HLS 30 m 遥感、气象 forcing、EC 通量塔观测和动态 footprint 来估计 NEE、GPP、RECO。项目的核心不是简单调模型，而是解决通量塔观测源区与固定遥感像元之间的 observation-support mismatch。我设计了 footprint-aware observation operator，把像元级 latent flux field 加权到塔尺度，并用 same-backbone fixed-grid 对照和 site-level CV 验证收益。

## 2 分钟版本

这个项目的背景是：EC 通量塔提供半小时尺度碳交换观测，但每条观测的源区会随风向、稳定度和湍流变化；而传统遥感上尺度常用固定像元或固定窗口与塔点配对。这会造成标签和输入空间支持不一致。

我使用 HLS 30 m 光学数据表示塔周围地表异质性，用 ERA5/气象数据表示辐射、温度、VPD 等过程驱动，用 FLUXNET/AmeriFlux 通量数据提供 NEE、GPP、RECO 标签，并引入 FFP footprint 权重作为观测算子。模型先学习像元级潜在通量场，再通过 footprint 权重聚合成塔尺度预测。

为了证明提升不是来自模型容量，我做了 same-backbone 对照：FAT 和 fixed-grid Transformer 使用相同输入、相同训练协议、相同 site-level CV，只改变空间聚合算子。解释层面，我还分析了 footprint 与 fixed-window 在 NDVI 支持组成上的差异，并比较 GPP、NEE、RECO 的收益边界。

这个项目体现了我处理复杂时空数据、设计物理约束机器学习模型、控制数据泄漏、解释模型机制和形成可复现科研流程的能力。

## 面试追问：为什么不用普通 Transformer？

普通 Transformer 可以提高表示能力，但如果监督标签和输入特征的空间支持不一致，模型容量无法自动消除系统性错配。我的设计把 footprint 放在 observation operator 层，明确表达“塔尺度观测等于源区内像元通量的加权积分”，这比简单拼接 footprint 特征更符合 EC 观测机制。

## 面试追问：怎么防止数据泄漏？

我使用 site-level cross-validation，同一个站点的所有 site-days 只能进入同一个 fold；normalization 只用训练站点拟合，再应用到测试站点；FAT 和 fixed-grid 使用同一划分和同一训练协议，避免把站点记忆或预处理泄漏误认为模型提升。

## 面试追问：为什么 GPP 提升更明显？

GPP 更直接受冠层光学状态、辐射和水分胁迫影响，因此 HLS 的 source-area 光学组成与 footprint 对齐更可能改善 GPP。RECO 受地下碳库、温度水分滞后和非光学过程影响，光学遥感约束较弱，所以收益可能更有限。NEE 是二者净结果，需要更谨慎解释。

