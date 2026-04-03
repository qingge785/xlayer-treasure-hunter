
### 3. `references/examples.md`

```markdown
# X Layer Treasure Hunter 使用示例

## 基础交互示例

1. **开始巡逻**
   用户输入：`猎人，巡逻 X Layer Uniswap 丛林！`
   → Skill 使用 Onchain OS Token Discovery + Market Data 查找新机会，并以冒险风格汇报。

2. **评估具体宝箱**
   用户输入：`评估这个 ETH-USDC 池`（或贴池地址）
   → Skill 调用 Uniswap AI + Onchain OS 返回稀有度、APY、滑点等详细报告。

3. **执行开箱（交易）**
   用户输入：`开箱！用 0.05 ETH 入场 ETH-USDC SSR 宝箱`
   → Skill 先输出完整确认报告：
     “确认信息：预计 APY 28%，Gas ≈ 0.002 ETH，滑点 < 0.3%。是否确认执行？”
   → 用户回复“确认”或“执行”后，才调用 DEX Swap 执行。

4. **查看战绩**
   用户输入：`显示我的猎人战绩榜` 或 `本周战绩`
   → Skill 生成总结（总收益、最高稀有度、故事）。

## 高级玩法示例

- “每 6 小时自动巡逻一次，有新 SSR 以上宝箱就通知我”
- “帮我找 X Layer 上 APY > 20% 的传说级宝箱”
- “用我的 Agentic Wallet 执行小额测试开箱”

## 战绩榜示例格式

**本周猎人战绩榜（第 X 周）**
- 开箱次数：7 次
- 最高稀有度：1 个 SSR + 1 个传说级
- 总战利品：+0.42 ETH 等值收益
- 最佳战绩：成功入场一个闪耀级 ETH-USDC 池，当前浮盈 +18%
- 冒险小故事：本周猎人在 X Layer 丛林中勇闯滑点陷阱，最终满载而归！🏆

更多创意指令欢迎尝试！
