# 量化金融高讨论度论文 Top 100

> 整理日期:2026-09-02
>
> 来源范围:arXiv (q-fin)、SSRN、NBER、顶级期刊(JF / JFE / RFS / Econometrica / Quantitative Finance 等),以及 Quantpedia、Alpha Architect、AQR、Quantocracy、Wilmott、QuantConnect 等量化社区反复讨论、复现的论文。
>
> **"讨论度"衡量口径**:以 Google Scholar 引用量级为主(数值为约数,截至 2025 年前后的量级,非精确值),辅以 SSRN 下载量、GitHub 复现热度、社区讨论(Quantpedia 收录 / Alpha Architect 解读 / 论坛热帖)。近两年的新论文引用尚少,以社区热度为准。
>
> 链接说明:优先给出 arXiv / 原文直链;其余给 Google Scholar 检索链接(点开第一条通常即原文,可看到实时引用数与全部版本)。

---

## 一、奠基经典:组合理论与资产定价(1–10)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 1 | [Portfolio Selection](https://scholar.google.com/scholar?q=%22Portfolio+Selection%22+Markowitz+1952) | Markowitz, 1952 | Journal of Finance | 5万+ 引用 | 现代组合理论(MPT)起点,均值-方差框架 |
| 2 | [Capital Asset Prices: A Theory of Market Equilibrium](https://scholar.google.com/scholar?q=%22Capital+Asset+Prices%22+Sharpe+1964) | Sharpe, 1964 | Journal of Finance | 3万+ 引用 | CAPM,β 的来源 |
| 3 | [Efficient Capital Markets: A Review of Theory and Empirical Work](https://scholar.google.com/scholar?q=%22Efficient+Capital+Markets%22+Fama+1970) | Fama, 1970 | Journal of Finance | 4万+ 引用 | 有效市场假说(EMH) |
| 4 | [The Pricing of Options and Corporate Liabilities](https://scholar.google.com/scholar?q=%22The+Pricing+of+Options+and+Corporate+Liabilities%22+Black+Scholes) | Black & Scholes, 1973 | Journal of Political Economy | 5万+ 引用 | BS 期权定价公式 |
| 5 | [Theory of Rational Option Pricing](https://scholar.google.com/scholar?q=%22Theory+of+Rational+Option+Pricing%22+Merton+1973) | Merton, 1973 | Bell Journal of Economics | 2万+ 引用 | 与 BS 并列的期权定价基石 |
| 6 | [The Arbitrage Theory of Capital Asset Pricing](https://scholar.google.com/scholar?q=%22The+Arbitrage+Theory+of+Capital+Asset+Pricing%22+Ross+1976) | Ross, 1976 | Journal of Economic Theory | 1万+ 引用 | APT 套利定价理论,多因子模型的理论根基 |
| 7 | [A New Interpretation of Information Rate](https://scholar.google.com/scholar?q=%22A+New+Interpretation+of+Information+Rate%22+Kelly+1956) | Kelly, 1956 | Bell System Technical Journal | 4,000+ 引用 | Kelly 公式,仓位管理的理论源头 |
| 8 | [Does the Stock Market Overreact?](https://scholar.google.com/scholar?q=%22Does+the+Stock+Market+Overreact%22+De+Bondt+Thaler) | De Bondt & Thaler, 1985 | Journal of Finance | 1万+ 引用 | 反转效应,行为金融开山作之一 |
| 9 | [Common Risk Factors in the Returns on Stocks and Bonds](https://scholar.google.com/scholar?q=%22Common+risk+factors+in+the+returns+on+stocks+and+bonds%22+Fama+French) | Fama & French, 1993 | Journal of Financial Economics | 4万+ 引用 | 三因子模型,因子投资的原点 |
| 10 | [Returns to Buying Winners and Selling Losers](https://scholar.google.com/scholar?q=%22Returns+to+Buying+Winners+and+Selling+Losers%22+Jegadeesh+Titman) | Jegadeesh & Titman, 1993 | Journal of Finance | 1.5万+ 引用 | 动量效应的实证起点 |

## 二、因子动物园与异象研究(11–22)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 11 | [On Persistence in Mutual Fund Performance](https://scholar.google.com/scholar?q=%22On+Persistence+in+Mutual+Fund+Performance%22+Carhart) | Carhart, 1997 | Journal of Finance | 2万+ 引用 | 四因子模型(加动量) |
| 12 | [A Five-Factor Asset Pricing Model](https://scholar.google.com/scholar?q=%22A+five-factor+asset+pricing+model%22+Fama+French) | Fama & French, 2015 | Journal of Financial Economics | 1万+ 引用 | 五因子模型(加盈利、投资) |
| 13 | [Presidential Address: Discount Rates](https://scholar.google.com/scholar?q=%22Presidential+Address+Discount+Rates%22+Cochrane) | Cochrane, 2011 | Journal of Finance | 5,000+ 引用 | "因子动物园(factor zoo)"一词的出处 |
| 14 | [… and the Cross-Section of Expected Returns](https://scholar.google.com/scholar?q=%22and+the+Cross-Section+of+Expected+Returns%22+Harvey+Liu+Zhu) | Harvey, Liu & Zhu, 2016 | Review of Financial Studies | 3,000+ 引用 | 316 个因子的多重检验,提出 t>3 标准,争论极大 |
| 15 | [Digesting Anomalies: An Investment Approach](https://scholar.google.com/scholar?q=%22Digesting+Anomalies%22+Hou+Xue+Zhang) | Hou, Xue & Zhang, 2015 | Review of Financial Studies | 3,000+ 引用 | q-因子模型,与 FF5 正面竞争 |
| 16 | [Replicating Anomalies](https://scholar.google.com/scholar?q=%22Replicating+Anomalies%22+Hou+Xue+Zhang) | Hou, Xue & Zhang, 2020 | Review of Financial Studies | 1,500+ 引用 | 复现 452 个异象,大半失效,轰动学界 |
| 17 | [Does Academic Research Destroy Stock Return Predictability?](https://scholar.google.com/scholar?q=%22Does+Academic+Research+Destroy+Stock+Return+Predictability%22) | McLean & Pontiff, 2016 | Journal of Finance | 2,000+ 引用 | 论文发表后异象收益衰减 |
| 18 | [Is There a Replication Crisis in Finance?](https://scholar.google.com/scholar?q=%22Is+There+a+Replication+Crisis+in+Finance%22+Jensen+Kelly+Pedersen) | Jensen, Kelly & Pedersen, 2023 | Journal of Finance | 近年热点 | 用贝叶斯方法反驳"复现危机",与 #14/#16 对垒 |
| 19 | [Value and Momentum Everywhere](https://scholar.google.com/scholar?q=%22Value+and+Momentum+Everywhere%22+Asness) | Asness, Moskowitz & Pedersen, 2013 | Journal of Finance | 3,000+ 引用 | AQR 名作,跨资产的价值+动量 |
| 20 | [Betting Against Beta](https://scholar.google.com/scholar?q=%22Betting+Against+Beta%22+Frazzini+Pedersen) | Frazzini & Pedersen, 2014 | Journal of Financial Economics | 2,500+ 引用 | BAB 因子,低β异象 |
| 21 | [Quality Minus Junk](https://scholar.google.com/scholar?q=%22Quality+Minus+Junk%22+Asness+Frazzini+Pedersen) | Asness, Frazzini & Pedersen, 2019 | Review of Accounting Studies | 1,500+ 引用 | 质量因子 QMJ,SSRN 长期热门下载 |
| 22 | [The Other Side of Value: The Gross Profitability Premium](https://scholar.google.com/scholar?q=%22The+Other+Side+of+Value%22+Novy-Marx) | Novy-Marx, 2013 | Journal of Financial Economics | 2,500+ 引用 | 毛利率因子 |

## 三、经典策略研究:动量、低波、配对、Alpha 库(23–30)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 23 | [Time Series Momentum](https://scholar.google.com/scholar?q=%22Time+Series+Momentum%22+Moskowitz+Ooi+Pedersen) | Moskowitz, Ooi & Pedersen, 2012 | Journal of Financial Economics | 2,500+ 引用 | 时序动量/趋势跟踪,CTA 策略理论支柱 |
| 24 | [The Cross-Section of Volatility and Expected Returns](https://scholar.google.com/scholar?q=%22The+Cross-Section+of+Volatility+and+Expected+Returns%22+Ang) | Ang, Hodrick, Xing & Zhang, 2006 | Journal of Finance | 4,500+ 引用 | 特质波动率之谜 |
| 25 | [Benchmarks as Limits to Arbitrage: Understanding the Low-Volatility Anomaly](https://scholar.google.com/scholar?q=%22Benchmarks+as+Limits+to+Arbitrage%22+Baker+Bradley+Wurgler) | Baker, Bradley & Wurgler, 2011 | Financial Analysts Journal | 1,200+ 引用 | 低波动异象的经典解释 |
| 26 | [A Quantitative Approach to Tactical Asset Allocation](https://scholar.google.com/scholar?q=%22A+Quantitative+Approach+to+Tactical+Asset+Allocation%22+Faber) | Faber, 2007 | Journal of Wealth Management / SSRN | SSRN 下载量历史前列 | 200 日均线择时,散户与博客圈讨论度极高 |
| 27 | [Pairs Trading: Performance of a Relative-Value Arbitrage Rule](https://scholar.google.com/scholar?q=%22Pairs+Trading+Performance+of+a+Relative-Value+Arbitrage+Rule%22) | Gatev, Goetzmann & Rouwenhorst, 2006 | Review of Financial Studies | 2,000+ 引用 | 配对交易学术奠基 |
| 28 | [Statistical Arbitrage in the US Equities Market](https://scholar.google.com/scholar?q=%22Statistical+Arbitrage+in+the+US+Equities+Market%22+Avellaneda+Lee) | Avellaneda & Lee, 2010 | Quantitative Finance | 900+ 引用 | PCA/ETF 残差统计套利标准范式 |
| 29 | [101 Formulaic Alphas](https://arxiv.org/abs/1601.00991) | Kakushadze, 2016 | Wilmott / arXiv | 社区讨论度极高 | WorldQuant 公开的 101 个因子表达式,复现项目遍地 |
| 30 | [A Comprehensive Look at the Empirical Performance of Equity Premium Prediction](https://scholar.google.com/scholar?q=%22A+Comprehensive+Look+at+the+Empirical+Performance+of+Equity+Premium+Prediction%22) | Welch & Goyal, 2008 | Review of Financial Studies | 4,500+ 引用 | 收益可预测性研究的"照妖镜"基准 |

## 四、机器学习 × 资产定价(31–40)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 31 | [Empirical Asset Pricing via Machine Learning](https://scholar.google.com/scholar?q=%22Empirical+Asset+Pricing+via+Machine+Learning%22+Gu+Kelly+Xiu) | Gu, Kelly & Xiu, 2020 | Review of Financial Studies | 4,000+ 引用 | ML 资产定价第一名片,近十年讨论度最高的实证论文之一 |
| 32 | [Characteristics Are Covariances: A Unified Model of Risk and Return](https://scholar.google.com/scholar?q=%22Characteristics+are+covariances%22+Kelly+Pruitt+Su) | Kelly, Pruitt & Su, 2019 | Journal of Financial Economics | 1,200+ 引用 | IPCA 工具性主成分分析 |
| 33 | [Taming the Factor Zoo: A Test of New Factors](https://scholar.google.com/scholar?q=%22Taming+the+Factor+Zoo%22+Feng+Giglio+Xiu) | Feng, Giglio & Xiu, 2020 | Journal of Finance | 1,200+ 引用 | 新因子边际贡献的系统检验 |
| 34 | [Shrinking the Cross-Section](https://scholar.google.com/scholar?q=%22Shrinking+the+Cross-Section%22+Kozak+Nagel+Santosh) | Kozak, Nagel & Santosh, 2020 | Journal of Financial Economics | 1,200+ 引用 | 贝叶斯收缩构造 SDF |
| 35 | [Dissecting Characteristics Nonparametrically](https://scholar.google.com/scholar?q=%22Dissecting+Characteristics+Nonparametrically%22) | Freyberger, Neuhierl & Weber, 2020 | Review of Financial Studies | 900+ 引用 | 非参数方法筛选有效特征 |
| 36 | [Deep Learning in Asset Pricing](https://scholar.google.com/scholar?q=%22Deep+Learning+in+Asset+Pricing%22+Chen+Pelger+Zhu) | Chen, Pelger & Zhu, 2024 | Management Science | 900+ 引用 | GAN + 无套利条件估计 SDF |
| 37 | [The Virtue of Complexity in Return Prediction](https://scholar.google.com/scholar?q=%22The+Virtue+of+Complexity+in+Return+Prediction%22+Kelly) | Kelly, Malamud & Zhou, 2024 | Journal of Finance | 近年最大论战之一 | "越复杂越好"结论引发 Nagel 等多篇反驳,讨论持续 |
| 38 | [Financial Machine Learning](https://scholar.google.com/scholar?q=%22Financial+Machine+Learning%22+Kelly+Xiu+survey) | Kelly & Xiu, 2023 | Foundations and Trends in Finance / SSRN | 引用增长极快 | 金融 ML 领域权威综述 |
| 39 | [(Re-)Imag(in)ing Price Trends](https://scholar.google.com/scholar?q=%22Re-Imag%28in%29ing+Price+Trends%22+Jiang+Kelly+Xiu) | Jiang, Kelly & Xiu, 2023 | Journal of Finance | 近年热点 | CNN 直接"看 K 线图"预测收益,社区复现极多 |
| 40 | [Predicting Returns with Text Data](https://scholar.google.com/scholar?q=%22Predicting+Returns+with+Text+Data%22+Ke+Kelly+Xiu) | Ke, Kelly & Xiu, 2019 | NBER / SSRN | 500+ 引用 | SESTM 监督情绪提取 |

## 五、深度学习预测与统计套利(41–47)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 41 | [Deep Learning with LSTM Networks for Financial Market Predictions](https://scholar.google.com/scholar?q=%22Deep+learning+with+long+short-term+memory+networks+for+financial+market+predictions%22) | Fischer & Krauss, 2018 | European Journal of Operational Research | 3,000+ 引用 | LSTM 选股的标准参考 |
| 42 | [Deep Neural Networks, Gradient-Boosted Trees, Random Forests: Statistical Arbitrage on the S&P 500](https://scholar.google.com/scholar?q=%22Deep+neural+networks%2C+gradient-boosted+trees%2C+random+forests%22+Krauss) | Krauss, Do & Huck, 2017 | European Journal of Operational Research | 1,500+ 引用 | 三大 ML 模型统计套利横评 |
| 43 | [Financial Time Series Forecasting with Deep Learning: A Systematic Literature Review](https://scholar.google.com/scholar?q=%22Financial+time+series+forecasting+with+deep+learning%22+Sezer) | Sezer, Gudelek & Ozbayoglu, 2020 | Applied Soft Computing | 2,000+ 引用 | 2005–2019 深度学习金融预测综述 |
| 44 | [A Deep Learning Framework for Financial Time Series Using Stacked Autoencoders and LSTM](https://scholar.google.com/scholar?q=%22A+deep+learning+framework+for+financial+time+series+using+stacked+autoencoders+and+long-short+term+memory%22) | Bao, Yue & Rao, 2017 | PLOS ONE | 2,000+ 引用 | WSAE-LSTM,被复现和引用极多 |
| 45 | [DeepLOB: Deep Convolutional Neural Networks for Limit Order Books](https://arxiv.org/abs/1808.03668) | Zhang, Zohren & Roberts, 2019 | IEEE Trans. Signal Processing / arXiv | 1,200+ 引用 | 限价单簿深度学习标杆 |
| 46 | [Universal Features of Price Formation in Financial Markets](https://arxiv.org/abs/1803.06917) | Sirignano & Cont, 2019 | Quantitative Finance / arXiv | 700+ 引用 | 大规模 LOB 数据揭示价格形成的普适性 |
| 47 | [Deep Learning for Event-Driven Stock Prediction](https://scholar.google.com/scholar?q=%22Deep+Learning+for+Event-Driven+Stock+Prediction%22+Ding) | Ding, Zhang, Liu & Duan, 2015 | IJCAI | 1,500+ 引用 | 事件驱动 + 深度学习早期代表作 |

## 六、强化学习与深度对冲(48–52)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 48 | [Learning to Trade via Direct Reinforcement](https://scholar.google.com/scholar?q=%22Learning+to+Trade+via+Direct+Reinforcement%22+Moody+Saffell) | Moody & Saffell, 2001 | IEEE Trans. Neural Networks | 1,500+ 引用 | RL 交易的开山之作 |
| 49 | [Deep Direct Reinforcement Learning for Financial Signal Representation and Trading](https://scholar.google.com/scholar?q=%22Deep+Direct+Reinforcement+Learning+for+Financial+Signal+Representation+and+Trading%22) | Deng et al., 2016 | IEEE Trans. Neural Networks and Learning Systems | 1,500+ 引用 | 深度 RL 交易早期高引论文 |
| 50 | [A Deep Reinforcement Learning Framework for the Financial Portfolio Management Problem](https://arxiv.org/abs/1706.10059) | Jiang, Xu & Liang, 2017 | arXiv | 1,500+ 引用,GitHub 复现极多 | 加密货币组合管理 RL 框架 |
| 51 | [Deep Hedging](https://arxiv.org/abs/1802.03042) | Buehler, Gonon, Teichmann & Wood, 2019 | Quantitative Finance / arXiv | 1,200+ 引用 | 用神经网络做对冲,衍生品圈近年最热方向 |
| 52 | [FinRL: A Deep Reinforcement Learning Library for Automated Stock Trading](https://arxiv.org/abs/2011.09607) | Liu et al., 2020 | NeurIPS Workshop / arXiv | GitHub 万星级 | 开源 RL 交易框架,社区讨论度极高 |

## 七、LLM × 金融(近两年最热)(53–60)

> 本版块已单独深挖扩展为 50+ 篇的专题文档:[deep-dive-llm-finance.md](./deep-dive-llm-finance.md)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 53 | [BloombergGPT: A Large Language Model for Finance](https://arxiv.org/abs/2303.17564) | Wu et al., 2023 | arXiv | 1,500+ 引用,媒体刷屏 | 首个大规模金融专用 LLM |
| 54 | [FinBERT: Financial Sentiment Analysis with Pre-trained Language Models](https://arxiv.org/abs/1908.10063) | Araci, 2019 | arXiv | 1,500+ 引用 | 金融情绪分析事实标准模型 |
| 55 | [FinGPT: Open-Source Financial Large Language Models](https://arxiv.org/abs/2306.06031) | Yang, Liu & Wang, 2023 | arXiv | GitHub 1.5万+ 星 | 开源金融 LLM 生态 |
| 56 | [Can ChatGPT Forecast Stock Price Movements?](https://scholar.google.com/scholar?q=%22Can+ChatGPT+Forecast+Stock+Price+Movements%22+Lopez-Lira) | Lopez-Lira & Tang, 2023 | SSRN | SSRN 现象级下载 | ChatGPT 读新闻标题预测涨跌,出圈之作 |
| 57 | [TradingAgents: Multi-Agents LLM Financial Trading Framework](https://arxiv.org/abs/2412.20138) | Xiao et al., 2024 | arXiv | GitHub 数万星 | 多智能体模拟交易团队,2025 年最火开源项目之一 |
| 58 | [FinMem: A Performance-Enhanced LLM Trading Agent with Layered Memory](https://arxiv.org/abs/2311.13743) | Yu et al., 2023 | arXiv / IEEE Trans. Big Data | 热点 | 带分层记忆的 LLM 交易智能体 |
| 59 | [FinCon: A Synthesized LLM Multi-Agent System with Conceptual Verbal Reinforcement](https://scholar.google.com/scholar?q=%22FinCon%22+LLM+multi-agent+financial) | Yu et al., 2024 | NeurIPS 2024 | 热点 | 多智能体 + 语言强化的投资决策系统 |
| 60 | [QuantAgent: Seeking Holy Grail in Trading by Self-Improving LLM](https://arxiv.org/abs/2402.03755) | Wang et al., 2024 | arXiv | 热点 | 自我迭代的量化研究智能体 |

## 八、市场微观结构与高频交易(61–70)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 61 | [Continuous Auctions and Insider Trading](https://scholar.google.com/scholar?q=%22Continuous+Auctions+and+Insider+Trading%22+Kyle) | Kyle, 1985 | Econometrica | 1.5万+ 引用 | Kyle 模型,微观结构理论基石 |
| 62 | [Bid, Ask and Transaction Prices in a Specialist Market](https://scholar.google.com/scholar?q=%22Bid%2C+ask+and+transaction+prices+in+a+specialist+market%22+Glosten+Milgrom) | Glosten & Milgrom, 1985 | Journal of Financial Economics | 1万+ 引用 | 信息不对称下的买卖价差 |
| 63 | [Illiquidity and Stock Returns](https://scholar.google.com/scholar?q=%22Illiquidity+and+stock+returns%22+Amihud+2002) | Amihud, 2002 | Journal of Financial Markets | 1.2万+ 引用 | Amihud 非流动性指标 |
| 64 | [Measuring the Information Content of Stock Trades](https://scholar.google.com/scholar?q=%22Measuring+the+Information+Content+of+Stock+Trades%22+Hasbrouck) | Hasbrouck, 1991 | Journal of Finance | 3,000+ 引用 | 交易信息含量的 VAR 分解 |
| 65 | [Optimal Execution of Portfolio Transactions](https://scholar.google.com/scholar?q=%22Optimal+Execution+of+Portfolio+Transactions%22+Almgren+Chriss) | Almgren & Chriss, 2001 | Journal of Risk | 2,500+ 引用 | 算法执行(冲击成本-风险权衡)基石 |
| 66 | [High-Frequency Trading in a Limit Order Book](https://scholar.google.com/scholar?q=%22High-frequency+trading+in+a+limit+order+book%22+Avellaneda+Stoikov) | Avellaneda & Stoikov, 2008 | Quantitative Finance | 1,200+ 引用 | 做市商报价模型标配,加密做市圈人手一份 |
| 67 | [Empirical Properties of Asset Returns: Stylized Facts and Statistical Issues](https://scholar.google.com/scholar?q=%22Empirical+properties+of+asset+returns%22+Cont+2001) | Cont, 2001 | Quantitative Finance | 5,000+ 引用 | 收益率典型事实(肥尾、波动聚集等)权威总结 |
| 68 | [Does Algorithmic Trading Improve Liquidity?](https://scholar.google.com/scholar?q=%22Does+Algorithmic+Trading+Improve+Liquidity%22+Hendershott) | Hendershott, Jones & Menkveld, 2011 | Journal of Finance | 2,500+ 引用 | 算法交易与流动性的经典实证 |
| 69 | [The High-Frequency Trading Arms Race](https://scholar.google.com/scholar?q=%22The+High-Frequency+Trading+Arms+Race%22+Budish) | Budish, Cramton & Shim, 2015 | Quarterly Journal of Economics | 1,500+ 引用 | HFT 军备竞赛与频繁批量拍卖,政策讨论极多 |
| 70 | [How Markets Slowly Digest Changes in Supply and Demand](https://scholar.google.com/scholar?q=%22How+markets+slowly+digest+changes+in+supply+and+demand%22+Bouchaud) | Bouchaud, Farmer & Lillo, 2009 | Handbook of Financial Markets | 800+ 引用 | 订单流冲击与价格形成,econophysics 名篇 |

## 九、波动率建模与衍生品定价(71–80)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 71 | [Autoregressive Conditional Heteroscedasticity (ARCH)](https://scholar.google.com/scholar?q=%22Autoregressive+Conditional+Heteroscedasticity+with+Estimates%22+Engle) | Engle, 1982 | Econometrica | 3万+ 引用 | ARCH,诺奖成果 |
| 72 | [Generalized Autoregressive Conditional Heteroskedasticity (GARCH)](https://scholar.google.com/scholar?q=%22Generalized+autoregressive+conditional+heteroskedasticity%22+Bollerslev) | Bollerslev, 1986 | Journal of Econometrics | 3万+ 引用 | GARCH,波动率建模默认起点 |
| 73 | [A Closed-Form Solution for Options with Stochastic Volatility](https://scholar.google.com/scholar?q=%22A+Closed-Form+Solution+for+Options+with+Stochastic+Volatility%22+Heston) | Heston, 1993 | Review of Financial Studies | 1万+ 引用 | Heston 模型 |
| 74 | [Pricing with a Smile](https://scholar.google.com/scholar?q=%22Pricing+with+a+smile%22+Dupire+1994) | Dupire, 1994 | Risk Magazine | 3,000+ 引用 | 局部波动率模型 |
| 75 | [Managing Smile Risk (SABR)](https://scholar.google.com/scholar?q=%22Managing+Smile+Risk%22+Hagan) | Hagan, Kumar, Lesniewski & Woodward, 2002 | Wilmott Magazine | 2,500+ 引用 | SABR 模型,利率期权市场标准 |
| 76 | [Option Valuation Using the Fast Fourier Transform](https://scholar.google.com/scholar?q=%22Option+valuation+using+the+fast+Fourier+transform%22+Carr+Madan) | Carr & Madan, 1999 | Journal of Computational Finance | 3,000+ 引用 | FFT 定价方法 |
| 77 | [Modeling and Forecasting Realized Volatility](https://scholar.google.com/scholar?q=%22Modeling+and+Forecasting+Realized+Volatility%22+Andersen+Bollerslev+Diebold+Labys) | Andersen, Bollerslev, Diebold & Labys, 2003 | Econometrica | 5,000+ 引用 | 已实现波动率框架 |
| 78 | [A Simple Approximate Long-Memory Model of Realized Volatility (HAR)](https://scholar.google.com/scholar?q=%22A+Simple+Approximate+Long-Memory+Model+of+Realized+Volatility%22+Corsi) | Corsi, 2009 | Journal of Financial Econometrics | 3,000+ 引用 | HAR-RV,波动率预测最常用基准 |
| 79 | [Volatility Is Rough](https://arxiv.org/abs/1410.3394) | Gatheral, Jaisson & Rosenbaum, 2018 | Quantitative Finance / arXiv | 1,500+ 引用 | 粗糙波动率,近十年衍生品定价最热潮流 |
| 80 | [Valuing American Options by Simulation: A Simple Least-Squares Approach](https://scholar.google.com/scholar?q=%22Valuing+American+Options+by+Simulation%22+Longstaff+Schwartz) | Longstaff & Schwartz, 2001 | Review of Financial Studies | 5,000+ 引用 | LSM 蒙特卡洛,美式期权定价标准算法 |

## 十、组合优化、风险管理与回测方法论(81–90)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 81 | [Global Portfolio Optimization](https://scholar.google.com/scholar?q=%22Global+Portfolio+Optimization%22+Black+Litterman) | Black & Litterman, 1992 | Financial Analysts Journal | 4,000+ 引用 | Black-Litterman 模型 |
| 82 | [Honey, I Shrunk the Sample Covariance Matrix](https://scholar.google.com/scholar?q=%22Honey%2C+I+Shrunk+the+Sample+Covariance+Matrix%22) | Ledoit & Wolf, 2004 | Journal of Portfolio Management | 2,000+ 引用 | 协方差收缩估计,工程实践必引 |
| 83 | [Optimal Versus Naive Diversification: How Inefficient Is the 1/N Strategy?](https://scholar.google.com/scholar?q=%22Optimal+Versus+Naive+Diversification%22+DeMiguel) | DeMiguel, Garlappi & Uppal, 2009 | Review of Financial Studies | 4,000+ 引用 | 1/N 打败优化组合,争议与讨论巨大 |
| 84 | [Optimization of Conditional Value-at-Risk](https://scholar.google.com/scholar?q=%22Optimization+of+Conditional+Value-at-Risk%22+Rockafellar+Uryasev) | Rockafellar & Uryasev, 2000 | Journal of Risk | 1万+ 引用 | CVaR 优化 |
| 85 | [Coherent Measures of Risk](https://scholar.google.com/scholar?q=%22Coherent+Measures+of+Risk%22+Artzner) | Artzner, Delbaen, Eber & Heath, 1999 | Mathematical Finance | 1.2万+ 引用 | 一致性风险度量公理体系 |
| 86 | [Pseudo-Mathematics and Financial Charlatanism](https://scholar.google.com/scholar?q=%22Pseudo-Mathematics+and+Financial+Charlatanism%22) | Bailey, Borwein, López de Prado & Zhu, 2014 | Notices of the AMS | 论战名篇 | 抨击回测过拟合,业界大讨论 |
| 87 | [The Properties of Equally Weighted Risk Contribution Portfolios](https://scholar.google.com/scholar?q=%22The+properties+of+equally+weighted+risk+contribution+portfolios%22) | Maillard, Roncalli & Teiletche, 2010 | Journal of Portfolio Management | 1,000+ 引用 | 风险平价(ERC)理论化 |
| 88 | [Building Diversified Portfolios that Outperform Out-of-Sample (HRP)](https://scholar.google.com/scholar?q=%22Building+Diversified+Portfolios+that+Outperform+Out+of+Sample%22) | López de Prado, 2016 | Journal of Portfolio Management | 社区实现极多 | 层次风险平价 HRP,开源库标配 |
| 89 | [The Deflated Sharpe Ratio](https://scholar.google.com/scholar?q=%22The+Deflated+Sharpe+Ratio%22+Bailey+Lopez+de+Prado) | Bailey & López de Prado, 2014 | Journal of Portfolio Management | 回测方法论必读 | 修正多重测试后的夏普比 |
| 90 | [Backtesting](https://scholar.google.com/scholar?q=%22Backtesting%22+Harvey+Liu+2015+haircut+Sharpe) | Harvey & Liu, 2015 | Journal of Portfolio Management | 回测方法论必读 | 多重检验下的夏普比"打折" |

## 十一、文本挖掘、情绪与另类数据(91–96)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 91 | [Giving Content to Investor Sentiment: The Role of Media in the Stock Market](https://scholar.google.com/scholar?q=%22Giving+Content+to+Investor+Sentiment%22+Tetlock) | Tetlock, 2007 | Journal of Finance | 6,000+ 引用 | 媒体文本情绪与股市,文本金融开山 |
| 92 | [When Is a Liability Not a Liability? Textual Analysis, Dictionaries, and 10-Ks](https://scholar.google.com/scholar?q=%22When+Is+a+Liability+Not+a+Liability%22+Loughran+McDonald) | Loughran & McDonald, 2011 | Journal of Finance | 6,000+ 引用 | LM 金融情绪词典,NLP 金融标配 |
| 93 | [Twitter Mood Predicts the Stock Market](https://scholar.google.com/scholar?q=%22Twitter+mood+predicts+the+stock+market%22+Bollen) | Bollen, Mao & Zeng, 2011 | Journal of Computational Science | 7,000+ 引用 | 现象级出圈论文,社交媒体情绪预测 |
| 94 | [In Search of Attention](https://scholar.google.com/scholar?q=%22In+Search+of+Attention%22+Da+Engelberg+Gao) | Da, Engelberg & Gao, 2011 | Journal of Finance | 3,500+ 引用 | Google 搜索量度量投资者关注度 |
| 95 | [Quantifying Trading Behavior in Financial Markets Using Google Trends](https://scholar.google.com/scholar?q=%22Quantifying+Trading+Behavior+in+Financial+Markets+Using+Google+Trends%22) | Preis, Moat & Stanley, 2013 | Scientific Reports | 1,500+ 引用 | Google Trends 择时,媒体讨论极广 |
| 96 | [Text as Data](https://scholar.google.com/scholar?q=%22Text+as+Data%22+Gentzkow+Kelly+Taddy) | Gentzkow, Kelly & Taddy, 2019 | Journal of Economic Literature | 2,000+ 引用 | 经济金融文本方法论权威综述 |

## 十二、加密资产(97–100)

| # | 论文 | 作者 / 年份 | 发表 | 讨论度 | 备注 |
|---|------|------------|------|--------|------|
| 97 | [Bitcoin: A Peer-to-Peer Electronic Cash System](https://bitcoin.org/bitcoin.pdf) | Nakamoto, 2008 | 白皮书 | 3万+ 引用 | 讨论度无需解释 |
| 98 | [Risks and Returns of Cryptocurrency](https://scholar.google.com/scholar?q=%22Risks+and+Returns+of+Cryptocurrency%22+Liu+Tsyvinski) | Liu & Tsyvinski, 2021 | Review of Financial Studies | 1,500+ 引用 | 加密资产收益风险的首篇顶刊系统研究 |
| 99 | [Trading and Arbitrage in Cryptocurrency Markets](https://scholar.google.com/scholar?q=%22Trading+and+arbitrage+in+cryptocurrency+markets%22+Makarov+Schoar) | Makarov & Schoar, 2020 | Journal of Financial Economics | 1,200+ 引用 | 跨交易所价差("泡菜溢价")研究 |
| 100 | [Common Risk Factors in Cryptocurrency](https://scholar.google.com/scholar?q=%22Common+Risk+Factors+in+Cryptocurrency%22+Liu+Tsyvinski+Wu) | Liu, Tsyvinski & Wu, 2022 | Journal of Finance | 800+ 引用 | 加密市场三因子(市场/规模/动量) |

---

## 附:2024–2026 社区正在热议的新论文(未计入 100 篇)

**Quantpedia Awards 2025 获奖论文**(量化社区年度评选,均可在 SSRN 找到):

- Harvey, Mazzoleni & Melone — *The Unintended Consequences of Rebalancing*(第一名,再平衡的市场冲击)
- Baltussen, Da & Soebhag — *End-of-Day Reversal*(日内尾盘反转)
- Beckmeyer, Filippou, Zhou & Zhou — *Intraday Option Reversals*
- Zarattini, Aziz & Barbon — *Beat the Market: An Effective Intraday Momentum Strategy for S&P 500 ETF (SPY)*(2024 年 SSRN 爆款)
- Azevedo, Riedersberger & Velikov — *The Aggregated Equity Risk Premium*

**arXiv q-fin 上的 LLM 智能体热点**:

- [Automate Strategy Finding with LLM in Quant Investment](https://arxiv.org/abs/2409.06289)(2024)
- Trading-R1: Financial Trading with LLM Reasoning via RL(2025)
- QuantAgents: Multi-Agent Financial System via Simulated Trading(2025)

## 使用建议

- **入门路线**:第一、二部分(奠基 + 因子)→ 第十部分(回测方法论,先学会不骗自己)→ 感兴趣的方向。
- **找实现**:#29 (101 Alphas)、#45 (DeepLOB)、#50–52 (RL)、#55/#57 (FinGPT/TradingAgents)、#88 (HRP) 在 GitHub 上均有大量开源复现。
- **查原文**:引用数为约数;点击 Google Scholar 链接可看到实时引用数,并通过 "All versions" 找到 SSRN/arXiv 免费版本。
