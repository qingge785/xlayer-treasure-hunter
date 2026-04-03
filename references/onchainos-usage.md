# Onchain OS Skill 使用指南（X Layer Treasure Hunter）

本 Skill 主要依赖 **okx/onchainos-skills** 实现链上功能。以下是核心模块使用说明（基于官方仓库 https://github.com/okx/onchainos-skills）。

## 已集成的核心模块

| 模块                        | 功能描述                              | 在本 Skill 中的用途                     | 调用时机                  |
|-----------------------------|---------------------------------------|-----------------------------------------|---------------------------|
| okx-agentic-wallet          | 钱包余额、组合 PnL、交易历史         | 查询用户/Agentic Wallet 资产            | 每次巡逻或开箱前          |
| Token Discovery             | 搜索代币、信息、集群分析             | 发现新流动性池或热门代币                | 巡逻 X Layer Uniswap 时   |
| Market Data                 | 实时价格、深度、K线、交易量           | 计算 APY、评估流动性深度                | 宝箱评估阶段              |
| DEX Swap                    | Swap 执行、路径优化                   | 执行“开箱”（Swap 入场/出场）            | 用户确认后                |
| Transaction Broadcasting    | 交易签名与广播                        | 将 Swap 交易广播到 X Layer              | 执行交易最后一步          |

## 优先网络
- 默认优先 **X Layer**（OKX L2）
- 支持测试网（用于安全测试）和主网

## 安全使用规则
- 仅在用户明确说“开箱”、“执行”、“确认交易”等词时才调用 DEX Swap / Broadcasting。
- 执行前必须输出完整报告（预计收益、Gas 估算、风险）。
- 推荐使用独立的 **Agentic Wallet** 作为执行身份，避免直接操作用户主钱包。

## 安装依赖
确保用户已安装：
```bash
npx skills add okx/onchainos-skills
