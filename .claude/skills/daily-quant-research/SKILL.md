---
name: daily-quant-research
description: 每日量化研究扫描:检索至少 10 篇未收录的新研究(NQ/股指期货日内交易、LLM 挖因子、LLM×金融、因子建模、波动率与微观结构),去重后写入 research/daily/ 当日简报,更新已收录清单并推送到 master。触发词:每日研究简报、daily research digest、跑一下今天的 research、daily quant research。
---

# Daily Quant Research(每日量化研究扫描)

**目标**:每次运行产出一份当日简报 `research/daily/YYYY-MM-DD.md`(日期用美东时间),包含 **至少 10 篇此前未收录**的相关研究。

**环境约束**:本环境直连 arXiv/SSRN/Semantic Scholar API 会被网络策略拦截(403),**只能用 WebSearch 工具检索**,不要浪费时间 curl 这些站点。

## 主题范围(按优先级)

1. **NQ / 股指期货日内交易**:日内动量、开盘区间突破(ORB)、隔夜效应、0DTE、宏观公告、订单流/微观结构
2. **LLM 挖因子**:alpha mining、因子生成 agent、因子评测
3. **LLM × 金融其他**:交易智能体、金融 LLM、评测基准、前视偏差
4. **因子建模与组合**:因子合成、股票预测模型、组合优化、回测方法论
5. **波动率**:波动预测、VRP、期权与期货联动

## 流程(严格按序执行)

### 1. 准备
- `git pull origin master`,确认在 master 且干净。
- 读取 `research/daily/seen.md`(历史已收录清单)。

### 2. 检索(WebSearch,至少 6 组查询)
优先找**最近 7 天**发布/上线的;不足再放宽到 30 天。查询模板(把 <当前月份/年份> 换成实际值):

- `arXiv q-fin new paper <月份 年份> trading futures intraday`
- `SSRN new working paper <年份> intraday momentum index futures`
- `0DTE options new research paper <月份 年份>`
- `LLM alpha mining factor generation arXiv <月份 年份>`
- `LLM trading agent new paper arXiv <月份 年份>`
- `market microstructure order flow imbalance paper <年份>`
- `Quantpedia new strategy article <月份 年份>`
- `Alpha Architect research review <月份 年份>`

若仍不足 10 篇新条目,追加更多查询(变换关键词:volatility forecasting、machine learning asset pricing、overnight returns、FOMC announcement drift 等),**最多 15 组**;仍不足则如实在简报中说明缺口,宁缺毋滥。

### 3. 筛选(两道闸门,逐篇过)
- **相关性**:属于上述 5 个主题之一;纯宏观评论、新闻、营销文不收。
- **新颖性**:标题不在 `research/daily/seen.md` 中,且 `grep -ri "<标题关键词>" research/` 无命中(排除 daily/ 自身除外的知识库文档也算已收录)。

### 4. 写当日简报 `research/daily/YYYY-MM-DD.md`
格式:

```markdown
# 每日量化研究简报 YYYY-MM-DD

> 运行时间(美东):…;检索查询数:…;新收录:N 篇

## 今日要点(3 条以内)
- …(最值得读的 1–3 篇,一句话说为什么)

## 新研究清单
### 1. <标题>(链接)
- 作者 / 来源 / 日期:…
- 摘要:2–4 句,说清方法与结论
- 主题:[NQ日内 | LLM挖因子 | LLM金融 | 因子建模 | 波动率]
- 可操作性:A(有可复现规则/代码)/ B(思路可借鉴)/ C(仅供了解)
…(至少 10 篇)
```

### 5. 更新登记
- `research/daily/seen.md` 末尾逐行追加:`YYYY-MM-DD | <标题> | <链接>`
- `research/daily/README.md` 索引表加一行(日期、篇数、一句话主题概括)。
- (可选)某篇与知识库模块高度相关且质量高 → 在对应 `01-papers.md`/清单文档补一行。

### 6. 提交推送
```bash
git add research/ && git commit -m "Daily quant research digest YYYY-MM-DD"
git push origin master   # 被拒则 git pull --rebase origin master 后重试,最多 4 次
```
提交信息末尾按当前会话的 attribution 规则附 Co-Authored-By 尾注。

### 7. 汇报
向用户汇报:今日要点、新收录篇数、简报文件路径。若当天检索质量差(新文少),如实说明。

## 质量红线

- 不虚构论文、作者或链接;每条链接必须来自检索结果。
- 同一论文的 arXiv/SSRN/期刊多个版本算一篇。
- 摘要基于检索摘要/描述撰写,不臆测结论;不确定的信息标注"待核实"。
