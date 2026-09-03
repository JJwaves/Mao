# 论文全景:因子挖掘自动化(2016–2026)

> 按方法家族分组。★ = 该家族里优先读的代表作。链接为 arXiv/GitHub 直链(已检索验证),个别为 Google Scholar 检索链接。

## 0. 前 LLM 时代:符号搜索基线(理解 LLM 方法必须先懂的对照组)

| 论文 / 项目 | 年份 | 方法 | 要点 |
|------------|------|------|------|
| ★ [101 Formulaic Alphas](https://arxiv.org/abs/1601.00991) | 2016 | 人工 | WorldQuant 公开的 101 个因子表达式,定义了整个领域的"表达式语法"与数据词表 |
| [gplearn 遗传规划路线](https://scholar.google.com/scholar?q=genetic+programming+alpha+factor+mining+stock) | 2017– | 遗传规划 | 各券商金工报告与开源实现的传统主力,LLM 论文的常用 baseline |
| ★ [AlphaGen: Generating Synergistic Formulaic Alpha Collections via RL](https://arxiv.org/abs/2306.12964) | 2023 (KDD) | 强化学习 | 里程碑:不优化单因子 IC,而以**下游组合模型的整体表现**为奖励,直接挖"协同因子集";[GitHub](https://github.com/RL-MLDM/alphagen/)(含 alphagen_llm 模块) |
| [RiskMiner: Risk-Seeking MCTS](https://arxiv.org/abs/2402.07080) | 2024 | MCTS | 蒙特卡洛树搜索 + 风险寻求策略挖公式因子 |
| [QuantFactor REINFORCE](https://arxiv.org/abs/2409.05144) | 2024 | 强化学习 | 方差有界 REINFORCE 替代 PPO,解决训练不稳定 |
| [AlphaQCM: Distributional RL](https://openreview.net/pdf?id=3sXMHlhBSs) | 2024 | 分布 RL | 用分布强化学习刻画因子奖励的不确定性 |
| [AlphaForge: Mine and Dynamically Combine Formulaic Alphas](https://scholar.google.com/scholar?q=%22AlphaForge%22+formulaic+alpha+factors+mine+dynamically+combine) | 2024 | 生成+动态组合 | 挖掘与动态加权组合分离的两段式框架 |

## 1. LLM 交互式/生成式挖因子(第一波,2023–2024)

| 论文 | 年份 | 要点 |
|------|------|------|
| ★ [Alpha-GPT: Human-AI Interactive Alpha Mining](https://arxiv.org/abs/2308.00016) | 2023 | 开创"人机交互挖因子"范式:自然语言交易想法 → LLM 翻译为因子表达式 → 回测反馈 → 对话式迭代 |
| [Alpha-GPT 2.0: Human-in-the-Loop AI for Quantitative Investment](https://scholar.google.com/scholar?q=%22Alpha-GPT+2.0%22+quantitative+investment) | 2024 | 扩展到整条投研流水线(因子→建模→分析)的人机协同 |
| [Chain-of-Alpha](https://arxiv.org/abs/2508.06312) | 2025 | 双链架构:因子生成链 + 因子优化链,主打简单高效的全自动挖掘 |
| [FAMA: LLM Alpha Mining with Chain-of-Experience](https://scholar.google.com/scholar?q=FAMA+LLM+alpha+mining+chain-of-experience) | 2024 | 引入"经验链":跨股票共享挖掘经验、记住成功案例,被后续 agent 工作广泛引用 |
| [Automate Strategy Finding with LLM in Quant Investment](https://arxiv.org/abs/2409.06289) | 2024 | 多智能体挖因子 + 多模态数据 + 动态加权组合,Quantpedia 做过专题解读 |

## 2. Agent 化闭环:自进化挖因子智能体(第二波,2025–2026 主流)

| 论文 | 年份 | 要点 |
|------|------|------|
| ★ [AlphaAgent: Regularized Exploration to Counteract Alpha Decay](https://arxiv.org/abs/2502.16789) | 2025 (KDD) | 直面因子衰减:AST 相似度查重(防复述已知因子)+ 假设-因子语义对齐 + 复杂度约束(防过拟合),三大正则化设计成为后续标配 |
| [QuantaAlpha: An Evolutionary Framework for LLM-Driven Alpha Mining](https://arxiv.org/pdf/2602.07085) | 2026 | LLM + 进化算法:变异/交叉在表达式空间进行,LLM 提供语义引导;[GitHub](https://github.com/QuantaAlpha/QuantaAlpha) |
| [AlphaPROBE: Principled Retrieval and On-graph Biased Evolution](https://arxiv.org/pdf/2602.11917) | 2026 | 检索历史挖掘轨迹 + 图上有偏进化 |
| [FactorMiner: Self-Evolving Agent with Skills and Experience Memory](https://arxiv.org/html/2602.14670v1) | 2026 | 技能库 + 经验记忆的自进化因子挖掘 agent |
| [FactorEngine: Program-level Knowledge-Infused Factor Mining](https://arxiv.org/pdf/2603.16365) | 2026 | 把领域知识注入到程序(代码)级因子生成 |
| [AlphaLogics: Market Logic-Driven Multi-Agent Alpha Generation](https://arxiv.org/pdf/2603.20247) | 2026 | 强调因子的市场逻辑可解释性,多智能体分工生成 |
| [AlphaMemo: Structured Search-Process Memory](https://arxiv.org/pdf/2606.20625) | 2026 | 结构化记录"父因子→子因子"编辑轨迹,用历史搜索过程指导新搜索 |
| [EFS: Evolutionary Factor Searching for Sparse Portfolio Optimization](https://arxiv.org/pdf/2507.17211) | 2025 | LLM 进化搜索直接服务于稀疏组合优化目标 |

## 3. 全流程自动化投研(因子 + 模型协同)

| 论文 / 项目 | 年份 | 要点 |
|------------|------|------|
| ★ [R&D-Agent(Q): Multi-Agent Framework for Data-Centric Factors and Model Joint Optimization](https://arxiv.org/abs/2505.15155) | 2025 | CMU + 微软亚研 + 牛津:Research(假设生成)/ Development(Co-STEER 代码生成)双阶段 + 多臂老虎机调度;宣称比经典因子库少用 70% 因子、年化收益翻倍;[GitHub](https://github.com/microsoft/RD-Agent),对接 Qlib,**工程化程度最高的开源实现** |
| [QRAFTI: Agentic Framework for Empirical Research in Quantitative Finance](https://arxiv.org/pdf/2604.18500) | 2026 | 把"实证研究"整个流程 agent 化(不止挖因子) |

## 4. 因子筛选与评测(去伪存真层)

| 论文 | 年份 | 要点 |
|------|------|------|
| ★ [AlphaEval: Evaluation Framework for Formula Alpha Mining](https://arxiv.org/pdf/2508.13174) | 2025 | 专门评"挖出来的因子"质量的多维框架(预测力、稳定性、多样性、可解释性等),挖因子系统的标准验收工具 |
| [Alpha-R1: Alpha Screening with LLM Reasoning via RL](https://arxiv.org/pdf/2512.23515) | 2025 | 用 RL 训练的推理模型做因子筛选(而非生成) |
| [AlphaForgeBench: Benchmarking End-to-End Trading Strategy Design](https://arxiv.org/pdf/2602.18481) | 2026 | 端到端"设计策略"能力的基准测试 |
| [A Survey on LLM-based Alpha Mining](https://link.springer.com/article/10.1631/FITEE.2500386) | 2025 | 该子领域的正式学术综述,建立分类学 |

## 阅读顺序建议

1. [101 Formulaic Alphas](https://arxiv.org/abs/1601.00991) — 建立"因子表达式"的语感(1 小时)
2. [AlphaGen](https://arxiv.org/abs/2306.12964) — 理解"优化组合增量而非单因子"这个关键思想
3. [Alpha-GPT](https://arxiv.org/abs/2308.00016) — LLM 进场的起点
4. [AlphaAgent](https://arxiv.org/abs/2502.16789) — 三大正则化,理解行业痛点
5. [R&D-Agent(Q)](https://arxiv.org/abs/2505.15155) — 当前工程化天花板
6. [AlphaEval](https://arxiv.org/pdf/2508.13174) — 学会验收
