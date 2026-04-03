
# X Layer Treasure Hunter（X Layer 宝藏竞技场）

把 OKX X Layer 上的 Uniswap DeFi 机会变成冒险寻宝游戏的创意 Agent Skill  

## 项目简介
X Layer Treasure Hunter 是一个游戏化的可复用 Agent Skill。  
它实时监控 X Layer Uniswap 流动性池和新机会，将高收益场景包装成“宝箱”（N/R/SR/SSR/传说级），用生动冒险风格与用户互动，并通过 Onchain OS Skill 安全执行交易。

## 架构概述
- **核心 Skill**：SKILL.md 定义猎人角色、宝箱评估逻辑、战绩系统
- **链上身份**：使用独立的 **Agentic Wallet"（TreasureHunter-Agent）作为链上执行身份
- **依赖 Skill**：
  - okx/onchainos-skills（Wallet 查询、Token Discovery、Market Data、DEX Swap、交易广播）
  - uniswap/uniswap-ai（Swap 路径优化、流动性分析）

## Agentic Wallet（链上身份）
- 钱包地址：`0x...`（请填写你的演示地址）
- 用途：作为 Treasure Hunter 的链上执行身份，用于演示宝箱开箱（Swap / LP 操作）

（如果有多个 Agent，请在这里列出各自角色，例如：
- Scout Agent：负责发现新池
- Appraiser Agent：评估宝箱价值
- Executor Agent：执行交易）

## Onchain OS Skill & Uniswap Skill 使用情况
- **Onchain OS Skill**：用于实时市场数据、代币发现、钱包余额查询、DEX Swap 执行和交易广播（重点在 X Layer 网络）
- **Uniswap AI Skill**：用于最佳 Swap 路径计算、流动性深度分析和 APY 估算
- 本 Skill 充分集成了两者核心模块，支持端到端从发现 → 评估 → 执行的闭环

## 运作机制
1. 巡逻 X Layer Uniswap 池 → 发现潜在宝箱
2. 结合 Uniswap AI + Onchain OS 评估稀有度和真实收益
3. 以冒险风格汇报给用户
4. 用户确认后通过 Onchain OS 执行交易（必须二次确认）
5. 记录战利品并生成战绩榜

## 项目在 X Layer 生态中的定位
本 Skill 让普通用户以游戏化方式参与 X Layer DeFi，降低 DeFi 使用门槛，同时展示 Onchain OS 在 X Layer 上的强大执行能力。适合 Yield Farming、流动性提供等场景。

## 团队成员
- Your Name（Solo Developer）

## 安装方式
```bash
npx skills add 你的用户名/xlayer-treasure-hunter
