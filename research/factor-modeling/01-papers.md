# 论文与模型全景:从因子到组合

> ★ = 优先读。arXiv/ACM/GitHub 链接经检索验证;经典文献用 Google Scholar 检索链接(点开第一条即原文)。

## 1. 学术基石(为什么这样做)

| 论文 | 年份 | 要点 |
|------|------|------|
| ★ [Empirical Asset Pricing via Machine Learning](https://scholar.google.com/scholar?q=%22Empirical+Asset+Pricing+via+Machine+Learning%22+Gu+Kelly+Xiu) | 2020 | 系统横评 OLS→惩罚回归→树→神经网络:非线性与交互项有真实增量,浅层 NN 足够;方法论模板 |
| [Autoencoder Asset Pricing Models](https://scholar.google.com/scholar?q=%22Autoencoder+asset+pricing+models%22+Gu+Kelly+Xiu) | 2021 | 用自编码器同时学因子载荷与因子收益 |
| [Characteristics Are Covariances (IPCA)](https://scholar.google.com/scholar?q=%22Characteristics+are+covariances%22+Kelly+Pruitt+Su) | 2019 | 特征驱动的条件因子模型,线性可解释路线的天花板 |
| [Financial Machine Learning(综述)](https://scholar.google.com/scholar?q=%22Financial+Machine+Learning%22+Kelly+Xiu) | 2023 | 建模环节所有选择(标签、损失、验证协议)的权威讨论 |
| [Forecasting Stock Return Distributions with Quantile NNs](https://arxiv.org/pdf/2408.07497) | 2024 | 预测收益**分布**而非点估计,直接服务风险管理 |

## 2. 工业界模型演进(Qlib model zoo 谱系)

| 模型 | 年份/出处 | 解决什么 |
|------|----------|---------|
| ★ LightGBM/XGBoost | 2016–17 | 表格因子数据的默认冠军:快、稳、抗噪;至今仍是最难打败的 baseline |
| ALSTM / GRU 系 | 2018–19 | 引入时序结构,吃原始量价序列 |
| [TRA: Temporal Routing Adaptor](https://scholar.google.com/scholar?q=%22Temporal+Routing+Adaptor%22+stock+KDD) | KDD 2021 | 多交易模式路由:不同股票/时期走不同预测头 |
| [HIST: 概念图模型](https://scholar.google.com/scholar?q=HIST+stock+trend+forecasting+concept+graph) | 2021 | 引入股票-概念(行业/主题)图共享信息 |
| ★ [DoubleAdapt: Meta-learning for Incremental Learning](https://dl.acm.org/doi/pdf/10.1145/3580305.3599315) | KDD 2023 | **概念漂移**的标准解法:数据适配器+模型适配器,滚动增量更新 |
| ★ [MASTER: Market-Guided Stock Transformer](https://scholar.google.com/scholar?q=MASTER+Market-Guided+Stock+Transformer+AAAI) | AAAI 2024 | 市场状态门控的股票 Transformer,截面+时序+市场信息三合一,近年最常被复现的 SOTA |
| [MDGNN: Multi-Relational Dynamic GNN](https://ojs.aaai.org/index.php/AAAI/article/view/29381/30608) | AAAI 2024 | 多关系动态图:同时建模多种股票关联及其演化 |
| [DGDNN: Decoupled Graph Diffusion NN](https://arxiv.org/pdf/2401.01846) | 2024 | 从数据自动学股票图结构而非人工指定 |
| [EP-GAT: Energy-based Parallel Graph Attention](https://arxiv.org/pdf/2507.08184) | 2025 | 能量视角构建动态股票图 |
| [TGNS: Transformer-based GNN](https://dl.acm.org/doi/10.1016/j.ins.2025.122555) | 2025 | 概念注意力 + 股票注意力双模块 |
| [H3M-SSMoEs: Hypergraph + LLM Reasoning + MoE](https://arxiv.org/pdf/2510.25091) | 2025 | 超图多模态 + LLM 推理 + 风格分组专家,代表"重模型"前沿 |
| [ACT: Anti-Crosstalk Learning](https://arxiv.org/pdf/2604.20204) | 2026 | 截面排序中的时序解耦与结构净化 |

**谱系规律**:每一代都在给"每只股票独立预测"补信息——时序(LSTM)→ 关联(图)→ 市场状态(MASTER)→ 漂移适应(DoubleAdapt)。但在干净的因子输入上,**LightGBM 至今难被显著打败**;复杂模型的增量主要来自吃原始序列与关联结构。

## 3. 因子合成与集成

| 论文 | 年份 | 要点 |
|------|------|------|
| [ML Enhanced Multi-Factor Trading with Bias Correction](https://arxiv.org/pdf/2507.07107) | 2025 | 截面组合优化 + 偏差校正的完整多因子管道 |
| [Combined ML for Stock Selection with Dynamic Weighting](https://arxiv.org/pdf/2508.18592) | 2025 | 多模型动态加权集成选股 |

## 4. 组合优化、风险模型与成本(把预测变成持仓)

| 论文 | 年份 | 要点 |
|------|------|------|
| ★ [Barra 风险模型(CNE5/CNE6/USE4 手册)](https://scholar.google.com/scholar?q=Barra+China+equity+model+CNE5+risk+model) | — | 结构化风险模型的工业标准:风格+行业+国家因子分解,组合优化的约束基础 |
| [60 Years of Portfolio Optimization(综述)](https://scholar.google.com/scholar?q=%2260+Years+of+Portfolio+Optimization%22+Kolm) | 2014 | 均值-方差之后所有改良路线的地图 |
| ★ [Dynamic Trading with Predictable Returns and Transaction Costs](https://scholar.google.com/scholar?q=%22Dynamic+Trading+with+Predictable+Returns+and+Transaction+Costs%22+Garleanu+Pedersen) | 2013 | 有成本时的最优交易:向目标组合"部分调仓"(aim portfolio),换手控制的理论基础 |
| ★ [Trading Costs](https://scholar.google.com/scholar?q=%22Trading+Costs%22+Frazzini+Israel+Moskowitz) | 2018 | AQR 用 1.7 万亿美元真实执行数据测量冲击成本:因子策略实际容量远大于学术悲观估计,讨论度极高 |
| [Honey, I Shrunk the Sample Covariance Matrix](https://scholar.google.com/scholar?q=%22Honey%2C+I+Shrunk+the+Sample+Covariance+Matrix%22) | 2004 | 协方差收缩,任何优化器的必备输入 |
| [Building Diversified Portfolios (HRP)](https://scholar.google.com/scholar?q=%22Building+Diversified+Portfolios+that+Outperform+Out+of+Sample%22) | 2016 | 免协方差求逆的层次配权 |

## 5. 持续追新

- [stock-top-papers](https://github.com/marcuswang6/stock-top-papers):顶会(KDD/AAAI/NeurIPS/IJCAI)股票预测论文合集,按年份整理,追 SOTA 用
- [Qlib examples/benchmarks](https://github.com/microsoft/qlib/tree/main/examples/benchmarks):模型 zoo 附统一回测指标,新模型是否真有增量一看便知

## 阅读顺序建议

1. Gu-Kelly-Xiu 2020 —— 建立"哪类模型对因子数据有效"的先验
2. Qlib benchmarks 页 —— 看工业界同一数据上各模型的真实差距(通常比论文声称的小)
3. DoubleAdapt —— 理解概念漂移这个 A 股建模第一杀手
4. Gârleanu-Pedersen + Trading Costs —— 理解为什么组合层的成本处理决定实盘成败
