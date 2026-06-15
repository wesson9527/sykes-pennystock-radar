# Sykes Pennystock Radar

把 Timothy Sykes 的仙股交易方法论，蒸馏成一个可重复调用的 Agent Skill。

它不负责预测下一只妖股是谁，它负责回答另一件更重要的事：

**这只票，现在到底能不能做。**

详细产品说明见：[中文产品说明](./docs/product-introduction.zh.md)

## 这个项目是干什么的

`Sykes Pennystock Radar` 适合两类场景：

1. 你输入一个 ticker，想知道它现在值不值得买
2. 你想从一批美股小票里，先筛出更有交易价值的候选

它会把 Timothy Sykes 那套“看阶段、看催化剂、看量能、看风险回报”的思路，变成结构化输出。

你最后拿到的不是一堆模糊评价，而是明确判断：

- `Buyable`
- `Watchlist Only`
- `Avoid`

同时会附带：

- 当前所处的 7 步周期阶段
- PREPARE 评分
- 入场 / 失效 / 出场思路
- 更适合追涨、恐慌接多，还是干脆别碰

## 为什么要做这个技能

美股小票最烦的地方，不是它不涨。

而是你永远搞不清楚，它现在到底是：

- 刚启动
- 已经拉完
- 还可以追
- 还是只剩最后一口气

很多票都有故事，也都有截图，也总有人说“这票要飞了”。

问题是，交易不是看故事感，交易看的是：

- 催化剂是不是新的
- 量能是不是异常的
- 流动性够不够
- 阶段对不对
- 风险回报值不值得出手

这个项目的意义，就是把这些判断前置。

## 它的底层逻辑

项目基于 Timothy Sykes 的两层框架：

### 1. 7 步仙股周期

任何一只小票，基本都可以落在这 7 个阶段里：

1. `Pre-Pump` 预泵期
2. `Ramp` 加速期
3. `Supernova` 超新星爆发
4. `Cliff Dive` 悬崖跳水
5. `Dip Buy` 恐慌接多
6. `Dead Pump Bounce` 死泵反弹
7. `Long Kiss Goodnight` 长吻晚安

真正最有交易价值的，往往是：

- `#3 Supernova`
- `#5 Dip Buy`

### 2. PREPARE 评分量表

每个标的都会按 7 个维度打分：

- `P` Pattern / Price
- `R` Reason
- `E` Ease of Entry / Exit
- `P` Past Performance
- `A` Agenda / Timing Window
- `R` Risk / Reward
- `E` Environment

这套技能本质上就是在做一件事：

**把“感觉这票有戏”，变成“为什么能做 / 为什么不能做”的规则化判断。**

## 怎么使用

### 单票判断

输入一个 ticker，比如：

- `ASTC`
- `PAVS`
- `INHD`
- `EDHL`
- `STI`

技能会输出：

1. 当前阶段
2. PREPARE 评分
3. 交易结论
4. 入场思路
5. 失效条件
6. 出场建议

### 小票池扫描

如果接入一批美股小票，它可以按以下顺序筛选：

1. 催化剂新不新
2. 浮动盘紧不紧
3. 成交量异不异常
4. 当前是不是交易窗口
5. 风险回报合不合理
6. 流动性够不够

它更像一个“交易门禁系统”，先帮你把大量不值得看的票挡在门外。

## ASTC 案例

这是一个最典型的结构化输出示例。

当你输入 `"$ASTC"`，技能可以给出这样的判断：

- 形态：进入 `Supernova` 爆发期（模式 #3）✅
- 流动性：日均成交量达标 ✅
- 催化剂：有新闻驱动（合同 / 合作）✅
- 历史表现：过去同类模式下表现一致 ✅
- 风险回报：当前入场点距止损 8%，目标利润 30%+（1:4）✅

结论：

> 符合入场条件。建议小仓位，设 8% 止损，分批止盈。

重点不在于“它一定会涨”，而在于：

- 这单为什么能做
- 如果做，怎么做
- 如果错，怎么退

## 产品图

### 7 步周期图

![7 Step Lifecycle](./assets/7-step-lifecycle.svg)

### PREPARE 评分图

![PREPARE Score](./assets/prepare-score.svg)

### 单票分析图

![Single Ticker Analysis](./assets/single-ticker-analysis.svg)

## 项目定位

这个项目不是荐股工具，也不是预测引擎。

它更接近一个交易过滤器：

- 帮你判断现在是不是出手时机
- 帮你过滤掉不值得做的票
- 帮你把“冲不冲”变成更纪律化的决策

如果只用一句话来概括它：

> 不是看到一只票就买，而是先判断它现在到底走到了哪一段。

## 文档

- [中文产品说明](./docs/product-introduction.zh.md)
- [方法论参考](./references/sykes-framework.md)

## License

MIT
