# 工具栈与复现路径

## 1. 核心工具

| 工具 | 用途 | 备注 |
|------|------|------|
| [Qlib](https://github.com/microsoft/qlib) | 全流程:Alpha158/Alpha360 因子集、model zoo、滚动训练、TopkDropout 组合回测 | 首选底座;`examples/benchmarks/` 里每个模型都附统一指标 |
| [LightGBM](https://github.com/microsoft/LightGBM) | 因子合成默认模型 | 表格数据之王;`lambdarank` 可做排序损失 |
| [cvxpy](https://github.com/cvxpy/cvxpy) | 约束组合优化 | 二次规划 + L1 换手惩罚,几十行写完完整版优化器 |
| [riskfolio-lib](https://github.com/dcajasn/Riskfolio-Lib) | 组合优化/风险预算库 | HRP、风险平价、CVaR 优化开箱即用 |
| [alphalens-reloaded](https://github.com/stefan-jansen/alphalens-reloaded) | 因子级分析(IC、分层、换手) | 与上游挖因子管道共用 |
| [empyrical-reloaded](https://github.com/stefan-jansen/empyrical-reloaded) | 组合级指标(IR、回撤等) | 轻量 |

## 2. Qlib 快速复现(从零到组合回测,半天)

```bash
pip install pyqlib lightgbm
python scripts/get_data.py qlib_data --target_dir ~/.qlib/qlib_data/cn_data --region cn
# 跑官方 benchmark:Alpha158 因子集 + LightGBM + TopkDropout 回测
cd examples && qrun benchmarks/LightGBM/workflow_config_lightgbm_Alpha158.yaml
```

产出即包含:预测 IC/ICIR、TopK 组合的超额年化/IR/换手。**这套输出就是你所有后续改动的对照组。**

替换自己的因子:把挖出的因子写成 Qlib 表达式加进 handler 的字段列表,或实现自定义 `DataHandler` 喂 DataFrame。

## 3. 进阶模型复现

- **DoubleAdapt / MASTER / TRA / HIST**:均有官方或社区实现,入口见 [stock-top-papers](https://github.com/marcuswang6/stock-top-papers) 与 Qlib `examples/benchmarks/` 目录;先在相同数据划分下对齐它们论文里的 baseline,再谈自己的改进。
- 对比原则:同一因子集、同一滚动划分、同一组合规则,只换模型;论文里动辄 20% 的提升在对齐后常缩水到 1–3%。

## 4. 风险模型的现实选择

| 方案 | 成本 | 说明 |
|------|------|------|
| 自建简版 | 免费 | 用市值/行业/动量/波动等 8–10 个风格因子截面回归,自估因子协方差;精度够研究用 |
| 商用 Barra(MSCI)/ 迅投·东方金工等 | 付费 | 实盘机构标准;研究阶段不必 |
| Qlib 内置暴露计算 + 收缩协方差 | 免费 | Ledoit-Wolf 收缩(sklearn `LedoitWolf`)直接可用 |

## 5. 一体化替代:RD-Agent(Q)

上游已在用 [RD-Agent](https://github.com/microsoft/RD-Agent) 的话,它的 quant 场景本身就包含"因子 + 模型"联合迭代(模型侧也是 Qlib 训练),可以把本库的验收标准(02-methods 第⑤节)配置成它的反馈指标,让整条流水线自动跑。
