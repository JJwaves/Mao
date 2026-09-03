# NQ(纳指 E-mini 期货)交易研究 Top 100

> 整理日期:2026-09-03。面向**交易 NQ/MNQ(E-mini Nasdaq-100 期货)**的研究清单:指数期货的大部分学术研究直接用 ES/NQ 数据完成,本清单按"对 NQ 交易者的可用性"组织成 10 个版块。
>
> 讨论度为 Google Scholar 引用量级(约数)或社区热度;链接:SSRN/arXiv 直链(已验证)+ Google Scholar 检索链接(点开第一条即原文)。与 [top100-quant-papers.md](./top100-quant-papers.md) 重复的少数必读经典(约 8 篇)保留,以保证本清单自包含。

---

## 一、指数期货定价、期现关系与价格发现(1–10)

NQ 与现货(NDX/QQQ)谁先动、基差怎么定价——这是理解这个品种的地基。

| # | 论文 | 作者/年份 | 讨论度 | 对 NQ 交易的启示 |
|---|------|----------|--------|-----------------|
| 1 | [The Pricing of Stock Index Futures](https://scholar.google.com/scholar?q=%22The+Pricing+of+Stock+Index+Futures%22+Cornell+French) | Cornell & French, 1983 | 1,000+ | 持有成本模型:基差 = 利率 − 股息,NQ 定价的第一性原理 |
| 2 | [Index-Futures Arbitrage and the Behavior of Stock Index Futures Prices](https://scholar.google.com/scholar?q=%22Index-Futures+Arbitrage+and+the+Behavior+of+Stock+Index+Futures+Prices%22) | MacKinlay & Ramaswamy, 1988 | 1,000+ | 期现套利如何把期货钉在公允价值附近 |
| 3 | [The Temporal Price Relationship between S&P 500 Futures and the S&P 500 Index](https://scholar.google.com/scholar?q=Kawaller+Koch+%22temporal+price+relationship%22+futures) | Kawaller, Koch & Koch, 1987 | 1,500+ | 期货领先现货 20–45 分钟的早期证据 |
| 4 | [The Dynamics of Stock Index and Stock Index Futures Returns](https://scholar.google.com/scholar?q=%22The+Dynamics+of+Stock+Index+and+Stock+Index+Futures+Returns%22+Stoll+Whaley) | Stoll & Whaley, 1990 | 2,000+ | 期货-现货互动的标准计量框架 |
| 5 | [A Further Analysis of the Lead-Lag Relationship](https://scholar.google.com/scholar?q=Chan+1992+%22lead-lag%22+futures+cash+index) | Chan, 1992 | 1,500+ | 好消息/坏消息、宽跌/宽涨时领先关系如何变化 |
| 6 | [Intraday Price Formation in U.S. Equity Index Markets](https://scholar.google.com/scholar?q=%22Intraday+Price+Formation+in+US+Equity+Index+Markets%22+Hasbrouck) | Hasbrouck, 2003 | 1,000+ | **直接研究 E-mini NQ**:价格发现主要发生在 E-mini 期货,不在 ETF/现货 |
| 7 | [One Security, Many Markets: Determining the Contributions to Price Discovery](https://scholar.google.com/scholar?q=%22One+Security%2C+Many+Markets%22+Hasbrouck+1995) | Hasbrouck, 1995 | 3,000+ | 信息份额(information share)方法论,期现价格发现度量的标准工具 |
| 8 | [Trading Costs and the Relative Rates of Price Discovery](https://scholar.google.com/scholar?q=%22Trading+costs+and+the+relative+rates+of+price+discovery%22+Fleming+Ostdiek+Whaley) | Fleming, Ostdiek & Whaley, 1996 | 1,000+ | 为什么期货领先:交易成本最低的场所先反映信息 |
| 9 | [Wavelet-Based Methods for High-Frequency Lead-Lag Analysis](https://arxiv.org/pdf/1612.01232) | Hayashi & Koike, 2016 | 方法论 | 高频领先-滞后的现代测量方法 |
| 10 | [High Frequency Lead/Lag Relationships — Empirical Facts](https://scholar.google.com/scholar?q=Huth+Abergel+%22high+frequency+lead%2Flag%22) | Huth & Abergel, 2014 | 300+ | 高频尺度上领先关系的实证规律(已缩短到秒级) |

## 二、日内模式:动量、反转与开盘区间(11–22)

NQ 日内交易者最直接可用的一块文献。

| # | 论文 | 作者/年份 | 讨论度 | 对 NQ 交易的启示 |
|---|------|----------|--------|-----------------|
| 11 | [A Theory of Intraday Patterns: Volume and Price Variability](https://scholar.google.com/scholar?q=%22A+Theory+of+Intraday+Patterns%22+Admati+Pfleiderer) | Admati & Pfleiderer, 1988 | 4,000+ | 为什么成交量和波动集中在开盘收盘:知情与流动性交易者的聚集博弈 |
| 12 | [An Investigation of Transactions Data for NYSE Stocks](https://scholar.google.com/scholar?q=Wood+McInish+Ord+%22transactions+data%22+NYSE) | Wood, McInish & Ord, 1985 | 2,000+ | 日内 U 型(微笑曲线)模式的最早记录 |
| 13 | [A Transaction Data Study of Weekly and Intradaily Patterns](https://scholar.google.com/scholar?q=Harris+1986+%22intradaily+patterns+in+stock+returns%22) | Harris, 1986 | 1,500+ | 日内与周内模式的系统证据 |
| 14 | [Intraday Periodicity and Volatility Persistence in Financial Markets](https://scholar.google.com/scholar?q=%22Intraday+periodicity+and+volatility+persistence%22+Andersen+Bollerslev) | Andersen & Bollerslev, 1997 | 2,500+ | 日内波动周期律的建模标准(做日内策略必须先剔除它) |
| 15 | [Intraday Patterns in the Cross-Section of Stock Returns](https://scholar.google.com/scholar?q=%22Intraday+Patterns+in+the+Cross-section+of+Stock+Returns%22+Heston) | Heston, Korajczyk & Sadka, 2010 | 600+ | 收益率的 30 分钟周期性:同一时段的动量跨日延续 |
| 16 | [Market Intraday Momentum](https://scholar.google.com/scholar?q=%22Market+Intraday+Momentum%22+Gao+Han+Li+Zhou) | Gao, Han, Li & Zhou, 2018 | 500+ | **头半小时预测尾半小时**:日内动量核心论文,ETF/期货均适用 |
| 17 | [Intraday Time Series Momentum: Global Evidence](https://scholar.google.com/scholar?q=%22intraday+time+series+momentum%22+global+evidence) | Li, Sakkas & Urquhart, 2022 | 近年热点 | 日内时序动量在全球指数期货上的样本外验证 |
| 18 | [Can Day Trading Really Be Profitable?(ORB on QQQ)](https://www.semanticscholar.org/paper/Can-Day-Trading-Really-Be-Profitable-Evidence-of-in-Zarattini-Aziz/4d55f526cc56f08662cb8976796cd3b719ef6d2b) | Zarattini & Aziz, 2023 | SSRN 爆款 | 5 分钟开盘区间突破(ORB)策略在 **QQQ/纳指**上的长期正收益证据,杠杆化后即 NQ 玩法 |
| 19 | [A Profitable Day Trading Strategy for the U.S. Equity Market](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4729284) | Zarattini, Barbon & Aziz, 2024 | SSRN 爆款 | ORB 应用于"Stocks in Play"(高相对成交量),Sharpe 2.4、近零 beta |
| 20 | [Beat the Market: An Effective Intraday Momentum Strategy for S&P500 ETF](https://scholar.google.com/scholar?q=Zarattini+Aziz+Barbon+%22intraday+momentum%22+SPY) | Zarattini, Aziz & Barbon, 2024 | Quantpedia Awards 2025 | 日内动量+动态止损的完整可复现规则,直接可移植到 NQ |
| 21 | [End-of-Day Reversal](https://scholar.google.com/scholar?q=%22End-of-Day+Reversal%22+Baltussen+Da) | Baltussen, Da & Soebhag, 2024 | Quantpedia Awards 2025 | 尾盘最后 30 分钟的系统性反转及其与 0DTE/做市对冲的关联 |
| 22 | [The Cross-Section of Intraday and Overnight Returns](https://scholar.google.com/scholar?q=%22The+cross-section+of+intraday+and+overnight+returns%22+Bogousslavsky) | Bogousslavsky, 2021 | 300+ | 哪些异象在日内赚钱、哪些只在隔夜赚钱 |

## 三、隔夜效应与日历规律(23–32)

NQ 全天 23 小时交易,隔夜时段的结构性规律是这个品种独有的 alpha 与风险来源。

| # | 论文 | 作者/年份 | 讨论度 | 对 NQ 交易的启示 |
|---|------|----------|--------|-----------------|
| 23 | [Return Differences between Trading and Non-Trading Hours](https://scholar.google.com/scholar?q=%22Return+Differences+between+Trading+and+Non-trading+Hours%22+Cliff+Cooper+Gulen) | Cliff, Cooper & Gulen, 2008 | 名篇 | 股权风险溢价几乎全部在隔夜实现——日内平均收益≈0 |
| 24 | [A Tug of War: Overnight Versus Intraday Expected Returns](https://scholar.google.com/scholar?q=%22A+Tug+of+War%3A+Overnight+Versus+Intraday+Expected+Returns%22) | Lou, Polk & Skouras, 2019 | 400+ | 隔夜/日内收益的角力:机构与散户客群的分时段博弈 |
| 25 | [The Overnight Drift](https://scholar.google.com/scholar?q=%22The+Overnight+Drift%22+Boyarchenko+Larsen+Whelan) | Boyarchenko, Larsen & Whelan, 2023 | RFS,讨论极高 | **用 ES 期货**:1998–2019 美东 2–3 点(欧洲开盘)的系统性正漂移,归因于做市商库存管理 |
| 26 | [The Disappearing Overnight Drift](https://libertystreeteconomics.newyorkfed.org/2026/07/the-disappearing-overnight-drift/) | NY Fed, 2026 | 最新跟进 | 2021 年后 2–3 点漂移消失——经典规律会衰减的活教材 |
| 27 | [Does Overnight News Explain Overnight Returns?](https://arxiv.org/pdf/2507.04481) | 2025 | arXiv 新作 | 隔夜收益与隔夜新闻的归因分解 |
| 28 | [Overnight Returns of Stock Indexes: Evidence from ETFs and Futures](https://www.sciencedirect.com/science/article/abs/pii/S1059056016301563) | 2016 | 200+ | 指数期货与 ETF 隔夜收益结构的直接对比 |
| 29 | [Overnight Returns and Firm-Specific Investor Sentiment](https://scholar.google.com/scholar?q=%22Overnight+returns+and+firm-specific+investor+sentiment%22+Aboody) | Aboody et al., 2018 | 400+ | 隔夜收益作为情绪代理:高隔夜收益后的短期反转 |
| 30 | [Are Seasonal Anomalies Real? A Ninety-Year Perspective](https://scholar.google.com/scholar?q=%22Are+Seasonal+Anomalies+Real%22+Lakonishok+Smidt) | Lakonishok & Smidt, 1988 | 2,000+ | 月末/月初效应(turn-of-the-month)的长样本证据 |
| 31 | [The Halloween Indicator: Sell in May](https://scholar.google.com/scholar?q=%22The+Halloween+Indicator%22+Bouman+Jacobsen) | Bouman & Jacobsen, 2002 | 1,000+ | "五穷六绝"的全球证据与争论 |
| 32 | [A Monthly Effect in Stock Returns](https://scholar.google.com/scholar?q=%22A+Monthly+Effect+in+Stock+Returns%22+Ariel) | Ariel, 1987 | 800+ | 月内上/下半月收益不对称 |

## 四、宏观公告与事件驱动(33–42)

NQ 对 CPI/FOMC/非农的反应是全市场最烈的;这块文献大多直接用指数期货高频数据。

| # | 论文 | 作者/年份 | 讨论度 | 对 NQ 交易的启示 |
|---|------|----------|--------|-----------------|
| 33 | [The Pre-FOMC Announcement Drift](https://scholar.google.com/scholar?q=%22The+Pre-FOMC+Announcement+Drift%22+Lucca+Moench) | Lucca & Moench, 2015 | 800+ | FOMC 决议前 24 小时的系统性上涨漂移(用 ES 期货度量),事件交易第一名篇 |
| 34 | [How Much Do Investors Care About Macroeconomic Risk?](https://scholar.google.com/scholar?q=Savor+Wilson+%22macroeconomic+risk%22+announcement+days) | Savor & Wilson, 2013 | 700+ | 股市超额收益集中在宏观公告日 |
| 35 | [What Explains the Stock Market's Reaction to Federal Reserve Policy?](https://scholar.google.com/scholar?q=%22What+Explains+the+Stock+Market%27s+Reaction+to+Federal+Reserve+Policy%22) | Bernanke & Kuttner, 2005 | 4,000+ | 意外降息 25bp ≈ 股指 +1%;科技/成长股(纳指)弹性最大 |
| 36 | [Micro Effects of Macro Announcements](https://scholar.google.com/scholar?q=%22Micro+Effects+of+Macro+Announcements%22+Andersen+Bollerslev+Diebold+Vega) | Andersen, Bollerslev, Diebold & Vega, 2003 | 3,000+ | 期货价格对各类宏观数据的逐秒反应函数:坏消息在扩张期反而利多 |
| 37 | [How Markets Process Information: News Releases and Volatility](https://scholar.google.com/scholar?q=Ederington+Lee+%22news+releases+and+volatility%22) | Ederington & Lee, 1993 | 2,000+ | 公告后 1 分钟内完成大部分价格调整,波动抬升持续数小时 |
| 38 | [Stock Returns over the FOMC Cycle](https://scholar.google.com/scholar?q=%22Stock+Returns+over+the+FOMC+Cycle%22+Cieslak) | Cieslak, Morse & Vissing-Jorgensen, 2019 | 600+ | FOMC 周期的偶数周效应 |
| 39 | [Premium for Heightened Uncertainty(公告前溢价)](https://scholar.google.com/scholar?q=Hu+Pan+Wang+Zhu+%22heightened+uncertainty%22+announcement) | Hu, Pan, Wang & Zhu, 2022 | 近年热点 | 公告前风险溢价的一般化:不止 FOMC |
| 40 | [Volume, Volatility, and Public News Announcements](https://scholar.google.com/scholar?q=%22Volume%2C+Volatility%2C+and+Public+News+Announcements%22+Bollerslev) | Bollerslev, Li & Xue, 2018 | 300+ | 用 E-mini 高频数据分解公告日的量-波动关系 |
| 41 | [Price Drift Before U.S. Macroeconomic News](https://scholar.google.com/scholar?q=Kurov+%22price+drift%22+macroeconomic+news+futures) | Kurov et al., 2019 | 300+ | 公告**前**期货已沿正确方向漂移——信息泄漏/知情交易证据 |
| 42 | [Monetary Momentum](https://scholar.google.com/scholar?q=%22Monetary+Momentum%22+Neuhierl+Weber) | Neuhierl & Weber, 2021 | 200+ | 货币政策意外后的延续漂移 |

## 五、趋势跟踪与时序动量(43–50)

NQ 波段/持仓过夜策略的主证据链。

| # | 论文 | 作者/年份 | 讨论度 | 对 NQ 交易的启示 |
|---|------|----------|--------|-----------------|
| 43 | [Time Series Momentum](https://scholar.google.com/scholar?q=%22Time+Series+Momentum%22+Moskowitz+Ooi+Pedersen) | Moskowitz, Ooi & Pedersen, 2012 | 2,500+ | 58 个期货品种(含股指)过去 12 个月符号预测未来 1 个月 |
| 44 | [A Century of Evidence on Trend-Following Investing](https://scholar.google.com/scholar?q=%22A+Century+of+Evidence+on+Trend-Following+Investing%22) | Hurst, Ooi & Pedersen, 2017 | 500+ | 137 年、跨资产的趋势跟踪证据 |
| 45 | [Momentum Strategies in Futures Markets and Trend-Following Funds](https://scholar.google.com/scholar?q=Baltas+Kosowski+%22momentum+strategies+in+futures+markets%22) | Baltas & Kosowski, 2013 | 300+ | CTA 式时序动量的容量与实现细节 |
| 46 | [Which Trend Is Your Friend?](https://scholar.google.com/scholar?q=%22Which+Trend+is+Your+Friend%22+Levine+Pedersen) | Levine & Pedersen, 2016 | 200+ | 各种趋势度量(均线交叉/回看收益)本质等价 |
| 47 | [Momentum Turning Points](https://scholar.google.com/scholar?q=%22Momentum+Turning+Points%22+Garg+Goulding+Harvey) | Garg, Goulding, Harvey & Mazzoleni, 2023 | 近年热点 | 快慢信号冲突期(拐点)是趋势策略亏损集中地,动态混合快慢 |
| 48 | [The Best of Strategies for the Worst of Times](https://scholar.google.com/scholar?q=%22The+Best+of+Strategies+for+the+Worst+of+Times%22+Harvey) | Harvey et al., 2019 | 400+ | 危机中什么有效:趋势跟踪的危机 alpha |
| 49 | [Enhancing Time-Series Momentum Strategies Using Deep Neural Networks](https://scholar.google.com/scholar?q=%22Enhancing+Time+Series+Momentum+Strategies+Using+Deep+Neural+Networks%22) | Lim, Zohren & Roberts, 2019 | 300+ | 深度学习直接输出仓位的时序动量(DMN) |
| 50 | [Trading with the Momentum Transformer](https://scholar.google.com/scholar?q=%22Momentum+Transformer%22+Wood+Zohren+trading) | Wood, Roberts & Zohren, 2022 | 200+ | 注意力机制版时序动量,拐点适应更快 |

## 六、波动率与 0DTE(51–62)

NQ 的波动率生态:VXN、已实现波动、以及 2023 年后彻底改变日内结构的 0DTE 期权。

| # | 论文 | 作者/年份 | 讨论度 | 对 NQ 交易的启示 |
|---|------|----------|--------|-----------------|
| 51 | [The Investor Fear Gauge](https://scholar.google.com/scholar?q=%22The+Investor+Fear+Gauge%22+Whaley) | Whaley, 2000 | 1,500+ | VIX/VXN 作为恐慌指标的原始论文 |
| 52 | [Expected Stock Returns and Variance Risk Premia](https://scholar.google.com/scholar?q=%22Expected+Stock+Returns+and+Variance+Risk+Premia%22+Bollerslev) | Bollerslev, Tauchen & Zhou, 2009 | 2,500+ | 方差风险溢价(IV−RV)预测未来指数收益 |
| 53 | [The VIX, the Variance Premium and Stock Market Volatility](https://scholar.google.com/scholar?q=%22The+VIX%2C+the+variance+premium+and+stock+market+volatility%22+Bekaert+Hoerova) | Bekaert & Hoerova, 2014 | 1,500+ | 把 VIX 分解为风险厌恶与不确定性两部分 |
| 54 | [Volatility-Managed Portfolios](https://scholar.google.com/scholar?q=%22Volatility-Managed+Portfolios%22+Moreira+Muir) | Moreira & Muir, 2017 | 1,000+ | 按波动率倒数调仓位提升 Sharpe——期货杠杆交易的仓位管理直接依据 |
| 55 | [A Simple Approximate Long-Memory Model of Realized Volatility (HAR)](https://scholar.google.com/scholar?q=%22A+Simple+Approximate+Long-Memory+Model+of+Realized+Volatility%22+Corsi) | Corsi, 2009 | 3,000+ | 日/周/月三尺度波动预测,NQ 日内风控的默认模型 |
| 56 | [Modeling and Forecasting Realized Volatility](https://scholar.google.com/scholar?q=%22Modeling+and+Forecasting+Realized+Volatility%22+Andersen+Bollerslev+Diebold+Labys) | Andersen et al., 2003 | 5,000+ | 高频已实现波动率框架 |
| 57 | [Good Volatility, Bad Volatility: Signed Jumps and Persistence](https://scholar.google.com/scholar?q=%22Good+Volatility%2C+Bad+Volatility%22+Patton+Sheppard) | Patton & Sheppard, 2015 | 1,000+ | 下行跳跃才推高未来波动——止损与仓位的不对称依据 |
| 58 | [0DTE Option Pricing](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4503344) | Bandi, Fusari & Renò, 2023–24 | 0DTE 定价开山 | 超短期权定价需要日内跳跃与周期性波动建模 |
| 59 | [Does 0DTE Options Trading Increase Volatility?](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4426358) | Brogaard, Han & Won, 2023–24 | 争论焦点 | 正方:0DTE 交易(散户投机主导)推高日内波动约 9% |
| 60 | [The Market for 0DTE: The Role of Liquidity Providers](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4881008) | Adams, Fontaine & Ornthanalai, 2024 | 争论焦点 | 反方:做市商对冲反而日均压低波动 60–90bp |
| 61 | [0DTE Asset Pricing](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4701401) | Almeida, Freire & Hizmeri, 2024 | 近年热点 | 从 0DTE 提取日内风险中性信息 |
| 62 | [Retail Traders Love 0DTE Options](https://scholar.google.com/scholar?q=%22Retail+Traders+Love+0DTE+Options%22+Beckmeyer) | Beckmeyer, Branger & Gayda, 2023 | SSRN 爆款 | 散户 0DTE 行为画像:平均亏损但交易量爆炸;理解尾盘 gamma 挤压的背景 |

## 七、微观结构、HFT 与订单流(63–76)

这一版块几乎全部用 **E-mini 期货数据**写成——NQ 交易者的"了解你的对手盘"必修课。

| # | 论文 | 作者/年份 | 讨论度 | 对 NQ 交易的启示 |
|---|------|----------|--------|-----------------|
| 63 | [The Flash Crash: High-Frequency Trading in an Electronic Market](https://scholar.google.com/scholar?q=%22The+Flash+Crash%3A+High-Frequency+Trading+in+an+Electronic+Market%22+Kirilenko) | Kirilenko, Kyle, Samadi & Tuzun, 2017 | 1,500+ | 用 E-mini 账户级数据还原 2010.5.6 闪崩:HFT 不引发但会放大 |
| 64 | [Findings Regarding the Market Events of May 6, 2010](https://scholar.google.com/scholar?q=CFTC+SEC+%22May+6%2C+2010%22+report+flash+crash) | CFTC & SEC, 2010 | 官方报告 | 闪崩官方调查:E-mini 卖单算法如何抽干流动性 |
| 65 | [The Microstructure of the Flash Crash](https://scholar.google.com/scholar?q=%22The+Microstructure+of+the+Flash+Crash%22+Easley+Lopez+de+Prado) | Easley, López de Prado & O'Hara, 2011 | 800+ | 订单流毒性(VPIN)视角的闪崩解释 |
| 66 | [Flow Toxicity and Liquidity in a High-Frequency World](https://scholar.google.com/scholar?q=%22Flow+Toxicity+and+Liquidity+in+a+High-frequency+World%22) | Easley, López de Prado & O'Hara, 2012 | 1,200+ | VPIN 指标(用 ES 数据):毒性飙升预警流动性撤退 |
| 67 | [VPIN and the Flash Crash(批评方)](https://scholar.google.com/scholar?q=Andersen+Bondarenko+%22VPIN+and+the+flash+crash%22) | Andersen & Bondarenko, 2014 | 论战 | VPIN 预测力的反驳——完整看两边再决定用不用 |
| 68 | [The High-Frequency Trading Arms Race](https://scholar.google.com/scholar?q=%22The+High-Frequency+Trading+Arms+Race%22+Budish) | Budish, Cramton & Shim, 2015 | 1,500+ | **ES-SPY 套利**:相关性在毫秒尺度崩塌,套利机会恒存;同样适用 NQ-QQQ |
| 69 | [Quantifying the High-Frequency Trading "Arms Race"](https://scholar.google.com/scholar?q=%22Quantifying+the+high-frequency+trading+arms+race%22+Aquilina) | Aquilina, Budish & O'Neill, 2022 | 近年热点 | 用交易所消息数据测量延迟套利的真实规模 |
| 70 | [High-Frequency Trading and Price Discovery](https://scholar.google.com/scholar?q=%22High-Frequency+Trading+and+Price+Discovery%22+Brogaard+Hendershott+Riordan) | Brogaard, Hendershott & Riordan, 2014 | 1,500+ | HFT 整体让价格更快反映信息 |
| 71 | [Risk and Return in High-Frequency Trading](https://scholar.google.com/scholar?q=%22Risk+and+Return+in+High-Frequency+Trading%22+Baron+Brogaard) | Baron, Brogaard, Hagströmer & Kirilenko, 2019 | 400+ | E-mini HFT 公司的真实收益分布:快者恒赚,新进入者难活 |
| 72 | [Do High-Frequency Traders Anticipate Buying and Selling Pressure?](https://scholar.google.com/scholar?q=Hirschey+%22Do+high-frequency+traders+anticipate%22) | Hirschey, 2021 | 300+ | HFT 抢跑大单方向——手动交易者滑点的来源 |
| 73 | [The Price Impact of Order Book Events](https://scholar.google.com/scholar?q=%22The+Price+Impact+of+Order+Book+Events%22+Cont+Kukanov+Stoikov) | Cont, Kukanov & Stoikov, 2014 | 800+ | **订单流不平衡(OFI)**线性驱动短期价格——盘口交易的理论基础 |
| 74 | [Cross-Impact of Order Flow Imbalance](https://scholar.google.com/scholar?q=%22Cross-impact+of+order+flow+imbalance%22+Cont+Cucuringu) | Cont, Cucuringu & Zhang, 2023 | 200+ | 跨资产 OFI(如 ES 的订单流影响 NQ) |
| 75 | [High Frequency Trading and the New Market Makers](https://scholar.google.com/scholar?q=%22High+frequency+trading+and+the+new+market+makers%22+Menkveld) | Menkveld, 2013 | 1,200+ | 现代做市商的库存行为画像 |
| 76 | [The Cost of Latency in High-Frequency Trading](https://scholar.google.com/scholar?q=%22The+Cost+of+Latency%22+Moallemi+Saglam) | Moallemi & Sağlam, 2013 | 300+ | 延迟的货币价值量化 |

## 八、机器学习/深度学习:日内与订单簿(77–86)

| # | 论文 | 作者/年份 | 讨论度 | 对 NQ 交易的启示 |
|---|------|----------|--------|-----------------|
| 77 | [Universal Features of Price Formation in Financial Markets](https://arxiv.org/abs/1803.06917) | Sirignano & Cont, 2019 | 700+ | 用海量 LOB 数据训练的"通用"价格形成模型:规律跨资产迁移 |
| 78 | [DeepLOB: Deep CNN for Limit Order Books](https://arxiv.org/abs/1808.03668) | Zhang, Zohren & Roberts, 2019 | 1,200+ | 订单簿深度学习标杆架构 |
| 79 | [Benchmark Dataset for Mid-Price Forecasting of LOB Data (FI-2010)](https://scholar.google.com/scholar?q=Ntakaris+%22benchmark+dataset%22+limit+order+book+mid-price) | Ntakaris et al., 2018 | 400+ | LOB 预测的公共基准数据集 |
| 80 | [Deep Order Flow Imbalance: Extracting Alpha at High Frequency](https://scholar.google.com/scholar?q=%22Deep+Order+Flow+Imbalance%22+Kolm+Turiel+Westray) | Kolm, Turiel & Westray, 2023 | 近年热点 | 从多档 OFI 提取高频 alpha 的系统实验 |
| 81 | [The Short-Term Predictability of Returns in Order Book Markets](https://scholar.google.com/scholar?q=Lucchese+%22short-term+predictability%22+order+book+deep+learning) | Lucchese, Pakkanen & Veraart, 2024 | 近年热点 | 深度模型在真实 LOB 上可预测性的严格度量 |
| 82 | [LOB-Based Deep Learning Models: A Benchmark Study](https://scholar.google.com/scholar?q=Prata+%22LOB-based+deep+learning%22+benchmark+stock+price+trend) | Prata et al., 2024 | 近年热点 | 15 个 LOB 深度模型公平横评:多数论文声称的优势复现不出 |
| 83 | [Deep Reinforcement Learning for Active High-Frequency Trading](https://scholar.google.com/scholar?q=Briola+%22deep+reinforcement+learning%22+high+frequency+trading) | Briola et al., 2021 | 200+ | RL 直接在日内 tick 数据上学交易 |
| 84 | [Reinforcement Learning for Optimized Trade Execution](https://scholar.google.com/scholar?q=%22Reinforcement+Learning+for+Optimized+Trade+Execution%22+Nevmyvaka+Kearns) | Nevmyvaka, Feng & Kearns, 2006 | 700+ | RL 做执行的开山之作 |
| 85 | [Multi-Horizon Forecasting for Limit Order Books](https://scholar.google.com/scholar?q=Zhang+Zohren+%22multi-horizon+forecasting%22+limit+order+books) | Zhang & Zohren, 2021 | 200+ | 多时间尺度 LOB 预测 |
| 86 | [Algorithmic and High-Frequency Trading(教材)](https://scholar.google.com/scholar?q=Cartea+Jaimungal+Penalva+%22Algorithmic+and+High-Frequency+Trading%22) | Cartea, Jaimungal & Penalva, 2015 | 2,000+ | 日内交易数学的标准教科书(做市、执行、信号) |

## 九、基差、股息与跨品种(87–92)

| # | 论文 | 作者/年份 | 讨论度 | 对 NQ 交易的启示 |
|---|------|----------|--------|-----------------|
| 87 | [Beyond Basis Basics: Liquidity Demand and Deviations from the Law of One Price](https://scholar.google.com/scholar?q=%22Beyond+Basis+Basics%22+Hazelkorn+Moskowitz) | Hazelkorn, Moskowitz & Vasudevan, 2023 | JF,近年热点 | 股指期货基差偏离反映流动性需求方向,本身可预测收益 |
| 88 | [On the Timing and Pricing of Dividends](https://scholar.google.com/scholar?q=%22On+the+Timing+and+Pricing+of+Dividends%22+Binsbergen) | van Binsbergen, Brandt & Koijen, 2012 | 800+ | 股息期限结构:理解 NQ 各到期月定价差异 |
| 89 | [Hedging Performance and Basis Risk in Stock Index Futures](https://scholar.google.com/scholar?q=%22Hedging+Performance+and+Basis+Risk+in+Stock+Index+Futures%22+Figlewski) | Figlewski, 1984 | 800+ | 基差风险与对冲比率 |
| 90 | [The Relationship Between Spot and Futures Prices in Stock Index Futures](https://scholar.google.com/scholar?q=Modest+Sundaresan+%22spot+and+futures+prices%22+stock+index) | Modest & Sundaresan, 1983 | 500+ | 卖空约束下的无套利区间 |
| 91 | [The Limits to Stock Index Arbitrage](https://scholar.google.com/scholar?q=Richie+Daigler+%22stock+index+arbitrage%22+limits) | Richie, Daigler & Gleason, 2008 | 100+ | 期现套利的现实摩擦 |
| 92 | [Do ETFs Increase Volatility?](https://scholar.google.com/scholar?q=%22Do+ETFs+Increase+Volatility%22+Ben-David+Franzoni) | Ben-David, Franzoni & Moussawi, 2018 | 1,000+ | QQQ/ETF 套利活动如何把噪音传导进 NQ 成分股 |

## 十、日内交易实务:盈利证据、技术分析与风控(93–100)

| # | 论文 | 作者/年份 | 讨论度 | 对 NQ 交易的启示 |
|---|------|----------|--------|-----------------|
| 93 | [Optimal Execution of Portfolio Transactions](https://scholar.google.com/scholar?q=%22Optimal+Execution+of+Portfolio+Transactions%22+Almgren+Chriss) | Almgren & Chriss, 2001 | 2,500+ | 拆单执行的冲击-风险权衡 |
| 94 | [The Cross-Section of Speculator Skill: Evidence from Day Trading](https://scholar.google.com/scholar?q=%22The+cross-section+of+speculator+skill%22+Barber+day+trading) | Barber, Lee, Liu & Odean, 2014 | 600+ | 台湾期货全样本:<1% 日内交易者长期稳定盈利,但确实存在 |
| 95 | [Day Trading for a Living?](https://scholar.google.com/scholar?q=%22Day+Trading+for+a+Living%22+Chague) | Chague, De-Losso & Giovannetti, 2020 | SSRN 爆款 | 巴西股指期货日内交易者:坚持越久亏损概率越高——清醒剂 |
| 96 | [The Profitability of Day Traders](https://scholar.google.com/scholar?q=%22The+Profitability+of+Day+Traders%22+Jordan+Diltz) | Jordan & Diltz, 2003 | 200+ | 美国日内交易者盈利分布的早期证据 |
| 97 | [Foundations of Technical Analysis](https://scholar.google.com/scholar?q=%22Foundations+of+Technical+Analysis%22+Lo+Mamaysky+Wang) | Lo, Mamaysky & Wang, 2000 | 2,500+ | 用核回归证明部分图形形态含真实信息——技术分析的学术正名 |
| 98 | [What Do We Know About the Profitability of Technical Analysis?](https://scholar.google.com/scholar?q=%22profitability+of+technical+analysis%22+Park+Irwin+survey) | Park & Irwin, 2007 | 1,000+ | 95 篇技术分析研究的系统综述:期货市场证据强于股票 |
| 99 | [Pseudo-Mathematics and Financial Charlatanism](https://scholar.google.com/scholar?q=%22Pseudo-Mathematics+and+Financial+Charlatanism%22) | Bailey, Borwein, López de Prado & Zhu, 2014 | 论战名篇 | 回测过拟合警告:策略参数越调越好看 ≠ 真实 |
| 100 | [The Kelly Criterion in Blackjack, Sports Betting, and the Stock Market](https://scholar.google.com/scholar?q=%22The+Kelly+Criterion+in+Blackjack+Sports+Betting%22+Thorp) | Thorp, 2006 | 交易员圈必读 | 杠杆品种的仓位数学:全 Kelly 波动巨大,实务用分数 Kelly |

---

## 给 NQ 交易者的阅读路线

- **日内交易者(最短路径,6 篇)**:#16 日内动量 → #18/#20 ORB 与日内动量规则 → #21 尾盘反转 → #59/#60 0DTE 之争 → #73 订单流不平衡
- **隔夜/波段**:#23–26(隔夜漂移兴衰)→ #33(FOMC 漂移)→ #43/#47(时序动量与拐点)→ #54(波动率管理仓位)
- **先泼三盆冷水再上桌**:#94/#95(日内交易者盈利分布)→ #99(回测过拟合)→ #26(经典规律会消失)
- 与本仓库其他模块的衔接:订单流/LOB 建模可直接套用 [llm-alpha-mining/](./llm-alpha-mining/) 与 [factor-modeling/](./factor-modeling/) 的方法论,把"因子"换成日内信号(OFI、区间突破、公告哑变量)即可。
