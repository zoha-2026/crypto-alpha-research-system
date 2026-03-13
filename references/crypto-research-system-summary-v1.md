# Crypto 研究系统总览摘要 v1
## 截至 v1.7 的数据、回测、规律、执行层与边界收口

> **这不是一个被真钱验证过的投资系统。它是一个经过双周期内部检验、擅长排错、能约束执行冲动的 alpha 研究与纪律框架。**

---

## 一、当前冻结基线

### 主框架
- `references/crypto-strong-coin-framework-v1.7.md`

### 规律总表
- `references/rules-change-table-v1.7.md`

### 评分卡设计
- `references/rules-scorecard-design-v2.md`

### 边界声明
- `references/system-limits-and-biases-v1.md`

### 验证协议
- `references/paper-portfolio-validation-protocol-v1.md`

### 系统索引
- `references/research-system-index-v1.7.md`

---

## 二、数据资产现状

### 8 年 top1000 快照（统一 3 月 12 日）
可验证文件：`data/cmc_historical_YYYY-03-12_top1000_filtered.csv`

| 年份 | 过滤后保留条数 |
|---|---:|
| 2019 | `993` |
| 2020 | `989` |
| 2021 | `970` |
| 2022 | `957` |
| 2023 | `953` |
| 2024 | `953` |
| 2025 | `955` |
| 2026 | `862` |

说明：
- 统一排除了：稳定币、wrapped 资产、staked 衍生币
- `2026` 条数明显更低，是因为后期 wrapped / bridged / staked 资产数量显著增多

---

## 三、Step 4 当前标准化候选池

可验证文件：`data/rules_scorecard_filled_examples_v2.csv`

### 当前标准化条目数
- `13`

### 当前分层
- 高优先级锚点：`2`
- 高优先级：`1`
- 高优先级讨论 / 强观察级：`1`
- 各类观察级合计：`6`
- 暂不成立：`2`
- 预跟踪中优先级最高：`1`

### 代表性当前候选
- 高优先级锚点：`MORPHO`、`AERO`
- 高优先级：`JUP`
- 高优先级讨论 / 强观察级：`JTO`
- 观察级（独立候选）：`KMNO`
- 观察级：`GT`、`CFG`、`SYRUP`、`ENA`、`BABY`
- 暂不成立：`VANA`、`DRIFT`
- 预跟踪：`Symbiotic`

---

## 四、两轮回测结果（当前最关键的量化证据）

## 窗口 A：2024→2026
可验证文件：
- `data/rules_scorecard_backtest_2024_2026_v2.csv`
- `references/rules-scorecard-backtest-report-v2.md`

### 全样本（32）
- TP=`9`
- FP=`3`
- TN=`8`
- FN=`12`
- 命中率：`53.1%`

### 仅限 2024 可见市场样本（22）
- TP=`9`
- FP=`3`
- TN=`6`
- FN=`4`
- 命中率：`68.2%`
- Precision：`75.0%`

### 解读
- 对 **2024 当时已在可见市场里的样本**，评分卡有一定区分力
- 对 **offscreen / pre-TGE / 当时未上市新物种**，明显无力

---

## 窗口 B：2022→2024
可验证文件：
- `data/rules_scorecard_backtest_2022_2024_v1.csv`
- `references/rules-scorecard-backtest-report-2022-2024-v2.md`

### 全样本（38）
- TP=`2`
- FP=`12`
- TN=`24`
- FN=`0`
- 命中率：`68.4%`
- Precision：`14.3%`

### 解读
- 这个窗口的高命中率，**主要来自 TN 堆积**
- 它说明评分卡在弱市 / 横盘市里更像是：
  - **排错成功**
  - 而不是 **选优成功**

---

## 五、从两轮回测得出的最终定位

### 评分卡最强能力
> **排错能力 > 选优能力 > 新物种发现能力**

### 更精确的周期化表述
- **排错能力**：跨周期更稳定
- **选优能力**：上行周期更有效，下行/横盘周期明显变差
- **新物种发现能力**：当前仍弱

### 关键结论
> **评分卡不是单独的买入工具。它更像是 alpha 仓位里的排错与筛选工具。**

---

## 六、跨周期交叉后确认的 4 条结构性规律

可验证文件：
- `references/step2_3_rules_2019_2022_v1.md`
- `references/rules_cross_cycle_comparison_v1.md`
- `references/crypto-strong-coin-framework-v1.7.md`

### 结构性规律 1：高位难续涨
- 2019→2022：高位爬升优先池 = `0`
- 2023→2026：回测 FP 集中在高位项目

### 结构性规律 2：赛道 / 生态命运先于个体胜负
- 先抬的是整条赛道 / 整个生态
- 再发生内部淘汰与分层

### 结构性规律 3：入口 / 基础设施位置比泛叙事更可迁移
- 跨周期更稳定的赢家，多数站在关键入口与基础设施位置上

### 结构性规律 4：创新浪潮会先整体爆发，再快速分层淘汰
- 不管是 DeFi Summer、L1 Summer，还是 ZK / L2 / 技术叙事浪潮
- 第一次爆发后都会迅速进入分层阶段

---

## 七、当前新增的最重要 Hard fail

可验证文件：
- `references/crypto-strong-coin-framework-v1.7.md`
- `references/rules-change-table-v1.7.md`

### Hard fail #7：反身性闭环飞轮
定义：
- 代币需求高度依赖协议自身的收益飞轮、平台资产负债表或内部流动性支撑
- 而不是独立的外生需求

判断问题：
> **如果把代币价格冻结在当前水平，协议核心需求是否还能独立存在？**

如果答案是否：
- 默认亮红灯

这条主要是为：
- `LUNA`
- `FTT`

这类样本补出的新风险识别层。

---

## 八、当前执行层状态

可验证文件：
- `references/market-temperature-execution-gate-v1.md`
- `references/execution-cards-jto-kmno-morpho-aero-jup-v1.md`

### 当前市场温度快照
- BTC 收盘价：`71190.40`
- 200D MA：`94335.58`
- 偏离：`-24.53%`
- 当前判定：**下行 / 横盘弱势**

### 当前执行动作
> **只跟踪**

### 当前执行卡覆盖的 5 个项目
- `MORPHO`
- `AERO`
- `JUP`
- `JTO`
- `KMNO`

### 当前统一结论
- 评分卡评级不变
- 但在当前市场温度下：
  - **没有一个应该直接进入正式建仓**

---

## 九、系统边界（必须前置理解）

可验证文件：`references/system-limits-and-biases-v1.md`

### 8 条已知边界与偏差（压缩版）
1. `rank_delta` 是相对强弱指标，不是绝对投资价值指标
2. 当前回测有样本选择偏差
3. 命中率会掩盖错误结构
4. 结构性规律也不是定律
5. 市场温度门优化的是少犯大错，不是抄底
6. 系统最强的是排错，不是资产配置
7. 内部交叉验证不等于独立验证
8. 8 年数据本质只覆盖两个主要周期

### 一句话使用边界
> **本系统适用于 alpha 仓位的排错与筛选，不适用于核心仓位（BTC / ETH）的配置决策。**

---

## 十、未来如何验证它到底有没有用

可验证文件：`references/paper-portfolio-validation-protocol-v1.md`

### 协议已经冻结的关键点
- live 规则冻结：`12` 个月
- shadow 版本承接所有新想法
- 面向整个可见市场验证，不再先挑赢家样本
- 带 5 个对照组合：
  - Full System Alpha
  - Scorecard Only
  - Naive Alt Basket
  - Cash
  - BTC / ETH Core Context
- 每周评估一次
- 最多 `5` 个持仓
- 等权
- 单边成本：`0.20%`

### 协议要回答的核心问题
> **这套系统在规则冻结之后，能不能为 alpha 仓位提供真实增量价值。**

---

## 十一、当前最诚实的总结

> **这套系统现在最有价值的地方，不是它已经证明自己正确，而是它已经把框架、数据、规律、执行门、边界声明和验证协议全部补齐，并明确知道自己能做什么、不能做什么，以及将来该怎样被真正更难地验证。**
