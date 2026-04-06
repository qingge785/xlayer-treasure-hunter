# X Layer Treasure Hunter（X Layer 宝藏竞技场猎人）

把 OKX X Layer 上的 Uniswap DeFi 机会变成冒险寻宝游戏的创意 Agent Skill  
**OKX Build-X Hackathon Skills Arena 参赛作品**

## 项目简介
X Layer Treasure Hunter 是一个**游戏化 + 实用型**的可复用 Agent Skill。

它实时监控 X Layer Uniswap 流动性池和新机会，将高收益场景包装成不同等级的“宝箱”（N / R / SR / SSR / 传说级），用生动冒险竞技场风格与用户互动。

新增安全扫描、智能钱信号、投资组合个性化推荐，并采用**异步分步执行模式**，有效解决长时间无反馈问题，支持安全、稳定地进行链上操作。

## 架构概述
- **核心 Skill**：SKILL.md 定义猎人角色、宝箱评估逻辑、战绩系统和异步分步机制
- **链上身份**：使用独立的 **Agentic Wallet** 作为链上执行身份
- **依赖 Skill**：
  - `okx/onchainos-skills`（Wallet 查询、Token Discovery、Market Data、DEX Swap、交易广播、安全扫描等）
  - `uniswap/uniswap-ai`（Swap 路径优化、流动性深度分析、APY 估算）

## Agentic Wallet（链上身份）
- **钱包地址**： `0x34ad070cdd36aab490d55d30d3e361b69c13c87e24`
- **用途**：作为 Treasure Hunter 的链上执行身份，用于演示宝箱开箱（Swap / LP 操作）

## 增强功能（v1.3.0）

### 1. 安全扫描模块
- 使用 `okx-security` 进行代币风险、合约风险、钓鱼检测、授权管理扫描
- 汇报时增加 **安全评级**（安全 / 中风险 / 高风险）及具体风险提示

### 2. 智能钱跟踪与信号
- 调用 `okx-dex-signal` 和 `okx-dex-trenches`
- 检测 Whale、Smart Money、KOL 信号及早期 Pump 动态
- 帮助发现“热门宝箱”和“早期猎物”

### 3. 投资组合分析与个性化建议
- 使用 `okx-wallet-portfolio` 和 `okx-agentic-wallet`
- 分析用户当前持仓，计算宝箱匹配度并给出个性化入场建议

### 4. 异步分步执行模式（性能核心优化）
- 采用分步执行 + 进度持久化机制
- 支持“开始深度猎宝 → 下一步 → 当前进度 → 生成完整报告”等指令
- 每步控制在 30-60 秒以内，有效避免长时间无反馈
- 默认快速模式（轻量查询），深度模式需用户主动触发并分步进行

## 运作机制
1. 巡逻 X Layer Uniswap 池 → 发现潜在宝箱
2. 进行安全扫描、智能钱信号检测、投资组合匹配
3. 结合 Uniswap AI 计算详细 APY、流动性与滑点
4. 以冒险风格汇报宝箱信息（含稀有度 + 安全评级 + 信号强度 + 个性化建议）
5. 用户确认后通过 Onchain OS 执行交易（必须二次确认）
6. 记录战利品并更新战绩榜

## 项目在 X Layer 生态中的定位
本 Skill 以游戏化方式降低 X Layer DeFi 使用门槛，让用户在有趣的“寻宝”过程中安全参与 Yield Farming 和流动性提供，同时充分展示 Onchain OS Skill 在 X Layer 上的强大执行能力。

## 团队成员
- qingge（Solo Developer）

## 安装方式
```bash
npx skills add qingge785/xlayer-treasure-hunter
