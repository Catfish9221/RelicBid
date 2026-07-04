# 遗链竞拍 RelicBid

> On-chain sealed-bid auction game — Bid on forgotten blockchain wallets, unbox the truth.

[English](#english) | [中文](#中文)

---

## 中文

### 什么是遗链竞拍

区块链上存在大量被遗忘或密钥丢失的钱包，里面可能躺着从 ICO 狂潮到 DeFi Summer 各个时代的遗留资产。

遗链竞拍将这个真实存在的链上现象做成了一个竞拍博弈游戏。被打捞出的废弃钱包作为密封拍品，供玩家竞拍。

### 玩法

- **4 人暗标竞拍**：你和 3 个对手同时对一个密封钱包出价，互相看不到对方的出价
- **5 轮博弈**：每轮系统释放新线索，你需要在信息不完整的情况下做出出价决策
- **扫描道具**：花钱购买扫描道具获取钱包内物品的局部信息（颜色分布、格数占比），但永远无法在开箱前知道全貌
- **角色技能**：3 个角色各有独特的信息获取能力，影响你的估值策略
- **开箱揭示**：竞拍赢家打开钱包，物品逐件从迷雾中浮现，那一刻才知道赚还是亏
- **回收销毁**：开出的物品可以选择官方回收（物品销毁，换取代币），形成通缩经济

### 关键设计

**格子 ≠ 价值**：大件物品可能一文不值（12 格的报废矿机主板），小件物品可能价值连城（1 格的中本聪钱包密钥）。格子大小只代表物理尺寸，不代表价值——和三角洲行动中的非洲之心一个道理。

**种子验证**：每个钱包由唯一的 TxHash 种子生成。同一种子永远产出相同内容，任何人可输入种子复盘验证。

**赢家诅咒**：4 人竞争天然推高出价。出价最高的人往往是高估最多的人——这是拍卖理论中的经典现象，也是游戏经济的内在平衡机制。

### 试玩

```
双击 index.html 即可在浏览器中体验
```

支持中英文切换（右上角按钮）。

### 截图

角色选择 → 密封竞拍 → 扫描侦察 → 暗标出价 → 开箱揭示 → 盈亏结算

### 物品体系

| 颜色   | 格子范围 | 价值区间         | 示例             |
| ------ | -------- | ---------------- | ---------------- |
| ⚪ 白色 | 1-4      | 50-200 R         | 🗑️ Rug Pull 残渣  |
| 🟢 绿色 | 1-4      | 300-600 R        | 🪙 测试网纪念币   |
| 🔵 蓝色 | 1-8      | 1,600-3,500 R    | 🏅 早期矿工徽章   |
| 🟣 紫色 | 1-4      | 6,200-11,000 R   | 🧬 MEV 策略密卷   |
| 🟡 金色 | 1-4      | 22,000-35,000 R  | ✍️ 以太坊创世签名 |
| 🔴 红色 | 1-12     | 68,000-320,000 R | 💎 中本聪钱包密钥 |

### 技术说明

- 纯前端实现，单个 HTML 文件，无需服务器
- 确定性伪随机数生成器（Mulberry32），种子 = TxHash
- 2D 背包放置算法（物品在 10×10 格子中随机排列）
- 中英文国际化（i18n）

---

## English

### What is RelicBid

Blockchains are full of forgotten wallets — keys lost, owners gone, assets left behind from every era: ICO booms, DeFi Summer, NFT waves, meme seasons.

RelicBid turns this real on-chain phenomenon into an auction game. Recovered abandoned wallets are sealed and put up for bidding.

### Gameplay

- **4-player sealed-bid auction**: You and 3 opponents bid on the same sealed wallet. No one can see each other's bids.
- **5 rounds**: Each round reveals new clues. You must decide how much to bid with incomplete information.
- **Scanners**: Spend tokens to scan parts of the wallet — see color distribution and grid occupation — but never the full picture before unboxing.
- **Character skills**: 3 characters with unique intel abilities that shape your valuation strategy.
- **Unboxing**: The winner opens the wallet. Items emerge from the fog one by one. Only then do you know if you profited or lost.
- **Recycle & burn**: Unwanted items can be recycled (burned for tokens), creating a deflationary economy.

### Key Design Principles

**Grid size ≠ value**: A 12-grid scrapped motherboard may be worthless. A 1-grid Satoshi wallet key may be priceless. Just like the Heart of Africa in Delta Force.

**Seed verification**: Each wallet is generated from a unique TxHash seed. Same seed always produces the same contents. Anyone can replay and verify.

**Winner's curse**: 4-player competition naturally inflates bids. The highest bidder is often the one who overestimated the most — a classic auction theory phenomenon that serves as the game's built-in economic balancer.

### Try it

```
Open index.html in any browser
```

Supports English/Chinese toggle (top-right button).

### Item Tiers

| Color    | Grid Range | Value Range      | Example                      |
| -------- | ---------- | ---------------- | ---------------------------- |
| ⚪ White  | 1-4        | 50-200 R         | 🗑️ Rug Pull Debris            |
| 🟢 Green  | 1-4        | 300-600 R        | 🪙 Testnet Coin               |
| 🔵 Blue   | 1-8        | 1,600-3,500 R    | 🏅 Early Miner Badge          |
| 🟣 Purple | 1-4        | 6,200-11,000 R   | 🧬 MEV Strategy Scroll        |
| 🟡 Gold   | 1-4        | 22,000-35,000 R  | ✍️ Ethereum Genesis Signature |
| 🔴 Red    | 1-12       | 68,000-320,000 R | 💎 Satoshi Wallet Key         |

---

## License

MIT
