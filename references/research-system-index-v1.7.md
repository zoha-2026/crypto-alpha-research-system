# 研究系统总目录 v1.7
## 三段式研究框架 v1.7 的文件导航

> **这不是一个被真钱验证过的投资系统。它是一个经过双周期内部检验、擅长排错、能约束执行冲动的 alpha 研究与纪律框架。**

这套系统现在服务的是一条完整决策链：

> **资本交叉比对 → 评分卡 → 市场温度**
>
> 发现 → 筛选 → 执行

同时底层研究主线仍然是：

> **先找过去三年的强势币，再提炼规律，最后映射当前候选，并通过执行门决定是否动作。**

---

# 零、先看边界（优先级最高）

## 0) 使用边界与已知偏差
- `references/system-limits-and-biases-v1.md`

作用：
- 把系统最危险的 8 条边界与偏差放到最前面
- 明确：
  - Step 1 是相对强弱采样器，不是绝对价值指标
  - 当前回测不是对整个市场的前瞻选股验证
  - 系统最强的是排错与纪律，不是整体资产配置
  - 系统适用于 **alpha 仓位**，不适用于 **BTC / ETH 核心仓位** 的配置决策

---

# 一、核心框架

## 1) 框架定稿（当前主框架）
- `references/crypto-strong-coin-framework-v1.7.md`

作用：
- 定义整个研究方法
- 包括 Step 1 ~ Step 4 的逻辑
- 已吸收：
  - 评分卡 v2 修订
  - 市场温度执行门
  - 跨周期验证后的结构性规律
  - Hard fail 第 7 条（反身性闭环飞轮）

## 2) 规律总览（当前总表）
- `references/rules-change-table-v1.7.md`

作用：
- 汇总原有规律的修改与当前表述
- 标出：
  - 结构性规律（跨周期验证）
  - 周期特异规律
  - 新增 Hard fail / 风险模式

---

# 二、五步正式产出

## 3) Step 1 — 历史强势币筛选
- `step1_formal_v1.5.xlsx`

作用：
- 用三年排名变化筛出历史强势币
- 输出全量增长池与优先研究池

补充数据文件（原主周期）：
- `data/cmc_historical_2023-03-12_top500_filtered.csv`
- `data/cmc_historical_2023-03-12_top500_excluded.csv`
- `data/cmc_historical_2023-03-12_top500_raw.json`

## 4) Step 2 + Step 3 — 归因与规律提炼
- `step2_attribution_v1.5.xlsx`

作用：
- 对优先池样本做 7 维归因
- 提炼规律与模板

## 5) Step 4 — 当前潜力币映射
- `step4_potential_mapping_v1.5.xlsx`

作用：
- 用规律、模板、事实层、判断层、Hard fail
- 筛出当前潜力币

## 6) Step 5 — 行动清单
- `references/step5-action-checklist-v1.5.md`

作用：
- 把 Step 4 结果转成可执行盯盘规则
- 每个币包含：
  - 关键观测指标
  - 升级触发条件
  - 降级 / 排除触发条件

---

# 三、执行层（v1.7 新增完成）

## 7) 市场温度执行门
- `references/market-temperature-execution-gate-v1.md`

作用：
- 把“评分卡正向结果”与“是否执行”分开
- 用 **BTC vs 200D MA** 的三档规则，决定：
  - 可执行
  - 轻仓验证
  - 只跟踪

## 8) 执行卡（当前候选）
- `references/execution-cards-jto-kmno-morpho-aero-jup-v1.md`

作用：
- 把发现层 / 评分层 / 执行层合并成一页式动作卡
- 明确“现在该做什么”与“何时允许升级”

---

# 四、跨周期验证（v1.7 新增完成）

## 9) 2019→2022 Step 1 样本
- `data/step1_historical_2019_2022_v1.csv`

## 10) 2019→2022 独立规律清单
- `references/step2_3_rules_2019_2022_v1.md`

## 11) 跨周期交叉比对
- `references/rules_cross_cycle_comparison_v1.md`

作用：
- 用 `2019→2022` 重新独立跑 Step 1 / Step 2 / Step 3
- 和 `2023→2026` 的现有规则系统做交叉比对
- 确认哪些规律可以升级为：
  - **结构性规律（跨周期验证）**
- 暴露出：
  - **反身性闭环飞轮 Hard fail** 这一新盲区

---

# 五、维护与背景材料

## 12) 更新流程说明
- `references/update-workflow-v1.5.md`

作用：
- 规定以后怎么低成本维护这套系统
- 默认先刷 Step 5，不重跑全流程
- 只有在必要时才回溯到 Step 1 / Step 4 / Step 3

## 13) 增强层补注清单
- `references/enhanced-layer-footnotes-v1.5.md`

## 14) 全部规律整合正文（历史主正文）
- `all-rules-consolidated-v1.5.pdf`

## 15) 增强层洞察备忘
- `references/enhanced-layer-insights-v1.5.md`

## 16) 增强层完整发现汇总
- `references/enhanced-layer-full-findings-v1.5.md`

## 17) Step 3 规律修正补丁
- `references/step3-rules-patch-v1.5.md`

## 18) 纸面组合验证协议
- `references/paper-portfolio-validation-protocol-v1.md`

作用：
- 规定未来如何用真正前瞻、带基准、带成本、冻结规则的方式验证这套系统
- 把验证对象明确限定为：**alpha 仓位**，不是核心仓位配置
- 回答“系统到底有没有真实增量价值”这个最关键的问题

---

# 六、默认阅读顺序

如果你第一次打开现在这套系统，推荐顺序：

1. `references/system-limits-and-biases-v1.md`
2. `references/crypto-strong-coin-framework-v1.7.md`
3. `references/rules-change-table-v1.7.md`
4. `references/paper-portfolio-validation-protocol-v1.md`
5. `references/market-temperature-execution-gate-v1.md`
6. `references/execution-cards-jto-kmno-morpho-aero-jup-v1.md`
7. `references/rules_cross_cycle_comparison_v1.md`

如果你只是日常维护，直接看：

1. `references/execution-cards-jto-kmno-morpho-aero-jup-v1.md`
2. `references/market-temperature-execution-gate-v1.md`
3. `references/update-workflow-v1.5.md`

---

# 七、一句话版

> **v1.7 之后，这套系统已经不是单纯的研究框架，而是带有“发现 → 筛选 → 执行”闭环，并经过双周期交叉验证的决策系统。**
