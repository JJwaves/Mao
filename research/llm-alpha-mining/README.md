# LLM 挖因子(LLM-based Alpha Mining)知识库

> 更新日期:2026-09-03。本文件夹是一个自包含的知识库,可在任何 Claude Code 窗口/会话中直接调用:
> 让 Claude 读取本文件夹(`research/llm-alpha-mining/`)即可获得该领域的论文全景、方法论和可执行的实操流程。
>
> **注意**:本文件夹当前在分支 `claude/quant-finance-research-sites-9mv8gk` 上。在其他窗口使用时,先让 Claude 切到该分支(`git fetch origin claude/quant-finance-research-sites-9mv8gk && git checkout claude/quant-finance-research-sites-9mv8gk`),或将该分支合并进 master。

## 文件索引

| 文件 | 内容 | 什么时候读 |
|------|------|-----------|
| [01-papers.md](./01-papers.md) | 论文全景:30+ 篇论文按方法家族分组,附链接与一句话要点 | 想了解某类方法有哪些工作、找参考文献 |
| [02-methods.md](./02-methods.md) | 方法拆解:任务形式化、表达式语法、六大方法族对比、防过拟合/防衰减机制、评测协议 | 想理解原理、设计自己的挖因子系统 |
| [03-tooling.md](./03-tooling.md) | 开源工具栈与数据源:Qlib、alphagen、RD-Agent 等,以及推荐的复现路径 | 准备动手搭环境 |
| [04-playbook.md](./04-playbook.md) | 实操手册:在一个 Claude Code 会话里跑一轮"假设→因子→回测→迭代"的完整流程,含提示词模板和验收清单 | 直接开工挖因子 |

## 一句话认识这个领域

**LLM 挖因子 = 用大模型加速"市场假设 → 因子表达式 → 回测验证 → 迭代改进"的研究循环。** LLM 不直接预测价格(那条路有严重的前视偏差问题,见 [../deep-dive-llm-finance.md](../deep-dive-llm-finance.md) 第 2 节),而是替代人类研究员生成和改进公式化因子;因子本身仍然经过传统量化回测检验,因此这是 LLM 在量化中最务实、离实盘最近的落地方向。

## 领域三大痛点(所有系统设计都围绕它们)

1. **复述而非发现**:LLM 训练语料里全是经典因子(Alpha101、学术论文),裸用 prompt 挖出来的大概率是"换皮动量/反转"。→ 解法:AST 查重、原创性约束(AlphaAgent)。
2. **过拟合与多重检验**:一晚上生成一万个因子,总有几个回测好看。→ 解法:复杂度约束、样本外验证、Deflated Sharpe / Harvey-Liu 折减、AlphaEval 多维评测。
3. **同质化与衰减**:挖出的因子彼此高度相关、与已知因子库重合,上线即衰减。→ 解法:以组合增量(而非单因子 IC)为优化目标(AlphaGen 的核心思想)、相关性惩罚、衰减监测。

## 快速上手路径

- **只想看懂**:读 02-methods.md 的方法族对比表 + 01-papers.md 挑 3 篇(AlphaGen → AlphaAgent → RD-Agent(Q))。
- **想跑起来**:读 03-tooling.md,先跑通 Qlib + alphagen baseline,再上 RD-Agent。
- **想让 Claude 直接挖**:把 04-playbook.md 丢给任意 Claude 会话,照流程执行。
