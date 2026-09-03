# 工具栈与复现路径

## 1. 回测与数据底座(先有打分器,才谈得上挖因子)

| 工具 | 定位 | 备注 |
|------|------|------|
| [Qlib](https://github.com/microsoft/qlib)(微软) | AI 量化平台:数据、因子表达式引擎、模型、回测全链条 | 事实标准底座;自带表达式引擎(`Ref/Mean/Std/Rank/Corr` 等操作符)可直接算因子 IC;支持 A 股与美股数据 |
| [alphagen](https://github.com/RL-MLDM/alphagen/) | KDD 2023 AlphaGen 官方实现 | 含 `alphagen_qlib`(对接 Qlib 数据)与 **`alphagen_llm`**(LLM 客户端抽象与提示词)——LLM 挖因子最好的起点代码 |
| [gplearn](https://github.com/trevorstephens/gplearn) | 遗传规划库 | 传统 GP 挖因子 baseline,论文对照必备 |
| [WorldQuant BRAIN](https://platform.worldquantbrain.com/) | 在线因子研究平台 | 不开源,但表达式语法与 Alpha101 同源,免费练手、验证想法的好沙盒 |

## 2. LLM 挖因子框架(开源可跑)

| 项目 | 论文 | 上手方式 |
|------|------|---------|
| [RD-Agent](https://github.com/microsoft/RD-Agent)(微软) | [R&D-Agent(Q), arXiv 2505.15155](https://arxiv.org/abs/2505.15155) | `pip install rdagent`;quant 场景 = 因子挖掘 + 模型迭代闭环,对接 Qlib;需要配置 LLM API;**工程成熟度最高,首选** |
| [QuantaAlpha](https://github.com/QuantaAlpha/QuantaAlpha) | [arXiv 2602.07085](https://arxiv.org/pdf/2602.07085) | 进化式 LLM 挖因子流水线 |
| [alphagen 的 LLM 模块](https://github.com/RL-MLDM/alphagen/) | — | 代码量小,适合读懂后改造成自己的 agent loop |

## 3. 数据源

| 市场 | 免费数据 | 说明 |
|------|---------|------|
| A 股 | [Tushare](https://tushare.pro/)、[AkShare](https://github.com/akfamily/akshare)、Qlib 自带的 cn_data | 日频量价 + 基本面;Qlib `scripts/get_data.py` 一键下载 |
| 美股 | [yfinance](https://github.com/ranaroussi/yfinance)、Qlib us_data、[Kenneth French 因子库](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html) | French 库用于基准因子对照 |
| 加密 | 各交易所 REST(ccxt) | 全天候、微观数据易得,适合高频因子实验 |

**提醒**:免费日频数据足够做方法验证;分钟级/逐笔、财报点位对齐(PIT)数据的质量才是实盘因子的真正门槛。

## 4. 推荐复现路径(从零到自建系统,三步)

### Step 1:跑通打分器(1–2 天)
```
pip install pyqlib
python scripts/get_data.py qlib_data --target_dir ~/.qlib/qlib_data/cn_data --region cn
```
用 Qlib 表达式引擎手算 2–3 个 Alpha101 因子的 IC/分层回测,确认数据与指标管道正确。

### Step 2:跑 baseline(2–3 天)
- 克隆 alphagen,复现 RL 挖因子;或用 gplearn 跑 GP 挖因子。
- 记录:合格因子数、平均 IC、因子间相关性——这是后面评价 LLM 方法的对照组。

### Step 3:上 LLM(1 周起)
- 途径 A(省事):部署 RD-Agent 的 quant 场景,观察它的"假设→代码→回测→反馈"循环,改它的提示词与评分标准。
- 途径 B(可控):照 [04-playbook.md](./04-playbook.md) 用 Claude 直接驱动自己的 loop:LLM 只负责生成假设与表达式,打分完全走 Step 1 的管道。

## 5. 成本预算(经验值)

- 一轮完整迭代(假设→5 个因子→回测→反馈)≈ 5k–20k token;一晚上 200 轮 ≈ 数百万 token。
- 结论:**打分器要快**(向量化、缓存)、**LLM 调用要省**(批量生成、失败快筛),否则算力/费用先于 alpha 耗尽。
