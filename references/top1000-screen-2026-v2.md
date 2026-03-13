# 2026-03 Top1000 全市场筛选 v2
## 基于框架 v1.7 + 评分卡 v2 + 市场温度执行门 v1（identity-aware 重跑）

> **这不是一个被真钱验证过的投资系统。它是一个经过双周期内部检验、擅长排错、能约束执行冲动的 alpha 研究与纪律框架。**
>
> 本系统适用于 alpha 仓位的排错与筛选，不适用于核心仓位（BTC / ETH）的配置决策。

可验证输入：
- `data/cmc_historical_2026-03-12_top1000_filtered.csv`
- `data/top1000_screen_identity_mapping_2023_2026_v1.csv`
- `references/crypto-strong-coin-framework-v1.7.md`
- `references/rules-scorecard-design-v2.md`
- `references/market-temperature-execution-gate-v1.md`

最终候选明细：
- `data/top1000_screen_2026_v2_candidates.csv`

---

## 一、这次 v2 到底修了什么？

v1 最大的问题不是框架方向，而是：
> **跨年路径不能只按 symbol 直接拼。**

v2 已修正：
- 同符号不同资产（collision）
  - `MNT`：Mantle / Mr Mint
  - `STRK`：Starknet / Strike
  - `TON`：Toncoin / Tokamak
  - `DOGE`：Dogecoin / Department Of Government Efficiency
  - `TRUMP`：OFFICIAL TRUMP / MAGA
- 同资产改名 / 换 ticker（continuity）
  - `XAUt ← XAUT`
  - `POL ← MATIC`
  - `RENDER ← RNDR`
  - `KAIA ← KLAY`
  - `SYRUP ← MPL`
  - `SKY ← MKR`
  - `ZBCN ← ZBC`

所以这次 v2 的含义是：
> **先把资产身份修对，再谈正式筛选结果。**

---

## 二、当前市场温度

可验证文件：`references/market-temperature-execution-gate-v1.md`

- BTC 收盘（2026-03-13 UTC）：`71190.40`
- 200D MA：`94335.58`
- 偏离：`-24.53%`
- 温度档位：**下行 / 横盘弱势**
- 默认执行动作：**只跟踪**

结论：
> **以下所有正向结论的执行级别统一为“只跟踪”。不存在当前可执行的正式建仓信号。**

---

## 三、第一轮：机械预筛（identity-aware）

筛选宇宙：
- `2026-03-12 top1000 filtered`：`862`

按框架 v1.7 的 Step 1 口径（修正为 identity-aware）重算：

### 路径 A：有历史爬升（全量增长池口径）
- `31` 个

### 路径 B：2023 top500 外 -> 2026 top150 的新上位
- `58` 个

### 合并去重后
- `89` 个预筛候选

说明：
- v1 PDF 的 `31 / ~55 / 90` 量级大体没崩
- 真正需要修的是组成成分，而不是第一轮规模感

---

## 四、第二轮到第四轮：Hard fail → 事实层 → 规律层

这三轮重跑后的正式结果，不再沿用 v1 的 symbol-only 路径。  
v2 只保留：
- 路径连续
- 身份清楚
- Hard fail 不触发
- 事实层与规律层仍站得住

最终留下：
- **18 个正式候选**

可验证文件：
- `data/top1000_screen_2026_v2_candidates.csv`

---

## 五、最终 retained list（18）

### A. 高优先级（4）
| 项目 | 代码 | 路径 | 2026 rank | 当前评级 | 说明 |
|---|---|---|---:|---|---|
| Hyperliquid | `HYPE` | 路径B | `8` | 高优先级 | 产品驱动极强，扣掉高位折扣后仍保留高优先级 |
| Canton | `CC` | 路径B | `14` | 高优先级（需验证） | 机构区块链基础设施，新发现，主线很强但历史太短 |
| Morpho | `MORPHO` | 路径B | `52` | 高优先级锚点 | 当前最稳的 DeFi 借贷基础设施正例之一 |
| Aerodrome Finance | `AERO` | 路径B | `90` | 高优先级锚点 | Base 流动性基础设施，位置清楚 |

### B. 观察级（14）
| 项目 | 代码 | 路径 | 2026 rank | 当前评级 | 说明 |
|---|---|---|---:|---|---|
| Jupiter | `JUP` | 路径B | `65` | 观察级（由高优先级降级） | `#51 -> #65`，排名恶化是硬事实 |
| Jito | `JTO` | 路径B | `148` | 观察级（由高优先级讨论降级） | `#81 -> #148`，已不能继续维持前评级 |
| Sui | `SUI` | 路径B | `19` | 观察级 | 新链生态仍成立，但已在高位区间 |
| Tether Gold | `XAUt` | 路径A | `24` | 观察级 | 视为 `XAUT` 连续体，黄金锚定路径清楚 |
| PAX Gold | `PAXG` | 路径A | `27` | 观察级 | 黄金锚定方向仍清楚 |
| Bitget Token | `BGB` | 路径A | `38` | 观察级 | 平台币正例，但 2025→2026 已回落 |
| Ondo | `ONDO` | 路径B | `42` | 观察级 | RWA 龙头之一，但高位折扣后不再维持更高评级 |
| Ethena | `ENA` | 路径B | `47` | 观察级（供给红灯） | 产品线成立，但供给压力仍在 |
| Bittensor | `TAO` | 路径B | `31` | 观察级 | AI 主线强，但高位横盘已久 |
| Mantle | `MNT` | 路径B | `30` | 观察级 | identity 修正后路径为 `#41 -> #33 -> #30` |
| Sky | `SKY` | 路径A | `34` | 观察级（identity fix） | 视为 Maker 连续体，不能再用“身份不清”排除 |
| Maple Finance | `SYRUP` | 路径B | `100` | 观察级（待 Hard fail 核实） | 视为 Maple 连续体，路径成立但仍需继续核查风险 |
| Render | `RENDER` | 路径A | `48` | 观察级 | 视为 RNDR 连续体，创新先行型资产进入分层阶段 |
| Artificial Superintelligence Alliance | `FET` | 路径A | `77` | 观察级 | AI 主线仍在，但相对高点回落明显 |

---

## 六、这次 v2 确认了什么？

### 1) JTO 和 JUP 的降级是对的
可验证路径：
- `JTO`：`2025 #81 -> 2026 #148`
- `JUP`：`2025 #51 -> 2026 #65`

这两个降级现在是 identity-aware 后仍成立的硬结论。

### 2) KMNO 不在正式 retained list 里
原因很简单：
- 当前 `2026 rank = 249`
- 已经不在全市场预筛的主战场范围

### 3) HYPE 和 CC 是这轮最重要的新增/强化结果
- `HYPE`：当前最强 DeFi/交易基础设施样本之一
- `CC`：当前最值得补研究的新机构基础设施样本之一

### 4) 规律 4B 仍在兑现
以下路径仍然支持“创新先行型资产进入分层淘汰”：
- `ARB #45 -> #47 -> #63`
- `TIA #42 -> #39 -> #92`
- `SEI #52 -> #67 -> #74`
- `PI #9 -> #26`
- `STRK（Starknet）#63 -> #100 -> #113`

---

## 七、这次 v2 撤回了什么？

### 1) MNT 的异常反弹叙事
撤回原因：
- 原先把 `Mr Mint #596` 错拼成了 `Mantle`

修正后应读为：
- `Mantle #41 -> #33 -> #30`

### 2) SKY 的“身份不清”硬排除
撤回原因：
- `SKY` 是 `MKR / Maker` 连续体
- 不是“突然冒出来的信息黑箱”

### 3) 任何依赖 symbol-only 历史路径得出的最终评级
都不应再直接引用为正式结果。

---

## 八、最短结论

> **在 identity-aware 修正后，2026 全市场筛选的正式 retained list 为 18 个，其中真正的高优先级只剩 4 个：MORPHO、AERO、HYPE、CC；JTO 与 JUP 均确认降级，KMNO 被移出正式候选；但由于 BTC 仍明显低于 200D MA，当前所有候选的执行级别统一仍是“只跟踪”。**
