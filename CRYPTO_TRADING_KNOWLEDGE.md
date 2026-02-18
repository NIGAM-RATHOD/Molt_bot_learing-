# Crypto Trading Knowledge Base

Compiled from research. Demo trading only — no real execution.

---

## 1. Cryptocurrency Fundamentals

### What is Cryptocurrency?
Digital currency designed to work through a computer network without central authority (government/bank). Uses blockchain technology with consensus mechanisms:

- **Proof of Work (PoW)**: Miners solve puzzles (Bitcoin, early Ethereum)
- **Proof of Stake (PoS)**: Validators stake coins (Ethereum 2.0, Solana, Cardano)

### Key Assets
| Asset | Symbol | Type | Market Position |
|-------|--------|------|-----------------|
| Bitcoin | BTC | Store of value, "digital gold" | #1 by market cap |
| Ethereum | ETH | Smart contract platform | #2, DeFi backbone |
| Solana | SOL | High-speed L1 | #5-10 range |
| Stablecoins | USDC, USDT | Pegged to $1 | Bridge between fiat/crypto |

### Market Structure
- **Spot**: Buy/sell actual coins
- **Futures/Perpetuals**: Derivatives with leverage
- **DeFi**: Decentralized exchanges, yield farming, lending
- **CEX**: Centralized exchanges (Binance, Coinbase, etc.)

---

## 2. Trading Styles

### Day Trading
- Buy and sell same day
- Closes positions before market close
- Uses leverage (margin)
- Pattern day trader rule: 4+ day trades in 5 days → $25k min required (US stocks)
- Crypto markets: 24/7, no PDT rule
- Requires fast execution, high risk

### Swing Trading
- Holds 2 days to several weeks
- Captures larger price moves
- Less stressful than day trading
- Uses technical analysis primarily

### Position Trading / HODLing
- Holds months to years
- Based on fundamentals/narrative
- "HODL" = Hold On for Dear Life
- Dollar-cost averaging (DCA) popular method

### Scalping
- Very short term (seconds to minutes)
- Tiny profits, high volume
- Requires discipline and fast execution

---

## 3. Technical Analysis Essentials

### Core Principle
Price reflects all available information. Study past price/volume to forecast future direction.

### Chart Patterns

**Reversal Patterns:**
- Head and Shoulders → Bearish reversal
- Double Top → Bearish reversal
- Double Bottom → Bullish reversal
- Cup and Handle → Bullish continuation

**Continuation Patterns:**
- Flags and Pennants → Brief pause in trend
- Wedges → Breakout direction matters
- Triangles → Ascending, descending, symmetrical

### Support & Resistance
- **Support**: Price level where buying pressure stops declines
- **Resistance**: Price level where selling pressure stops rallies
- **Breakout**: Price moves through S/R with volume = trade signal

### Key Indicators

| Indicator | Purpose | Signal |
|-----------|---------|--------|
| Moving Average (MA) | Trend direction | Price above MA = uptrend |
| RSI (Relative Strength Index) | Momentum/overbought | >70 overbought, <30 oversold |
| MACD | Trend/momentum | Bullish when line crosses above signal |
| Volume | Confirmation | High volume = valid breakout |
| ATR (Average True Range) | Volatility | Higher = more volatile |
| Bollinger Bands | Volatility/mean reversion | Touch upper/lower band = potential reversal |

### Candlestick Patterns
- **Doji**: Indecision, potential reversal
- **Hammer**: Bullish at bottom
- **Shooting Star**: Bearish at top
- **Engulfing**: Strong reversal signal
- **Morning/Evening Star**: 3-candle reversal patterns

---

## 4. Risk Management (Critical)

### Position Sizing Formula
```
Position Size = (Account Risk $) / (Entry - Stop Loss)

Example:
- Account: $10,000
- Risk per trade: 1% = $100
- Entry: $100
- Stop: $95 (5% risk on position)
- Position Size = $100 / $100-$95 = $100 / $5 = 20 shares
- Capital deployed = 20 × $100 = $2,000 (20% of account)
- Risk = $100 (1% of account) ✓
```

### Hard Rules (Non-Negotiable)
1. **Max Risk Per Trade**: 1-2% of account
2. **Stop Loss**: Mandatory on every trade
3. **Risk/Reward**: Minimum 1:2 (risk $1 to make $2)
4. **Daily Loss Limit**: -3% to -5% max, then stop
5. **Max Exposure**: Never risk more than 5-10% total across all positions

### The Kelly Criterion
```
Kelly % = W - [(1-W) / R]
Where:
- W = Win rate (probability of winning)
- R = Win/Loss ratio (avg win / avg loss)

Practical: Use "Half Kelly" or "Quarter Kelly" to reduce volatility
```

### Correlation Risk
- BTC and ETH highly correlated (~0.85)
- Holding both = concentrated risk
- Diversify across uncorrelated assets or strategies

---

## 5. Trading Psychology

### Common Biases
- **Confirmation Bias**: Seeking info that supports your trade
- **Anchoring**: Fixating on entry price (irrational)
- **Loss Aversion**: Holding losers too long, taking profits too early
- **Recency Bias**: Overweighting recent trades
- **Overconfidence**: Wining streak → bigger trades → blowup

### Mental Framework
- **Process Over Outcome**: Good trade = followed rules, regardless of result
- ** expectancy = (Win% × Avg Win) - (Loss% × Avg Loss)**
- Edge exists in probability, not guarantees

---

## 6. Crypto-Specific Risks

| Risk Type | Description | Mitigation |
|-----------|-------------|------------|
| Volatility | 5-20% daily swings common | Size down, wider stops |
| Exchange Risk | Hacks, insolvency | Use reputable CEX, self-custody for long-term |
| Liquidity Risk | Low volume = slippage | Trade top 50 coins, check depth |
| Regulatory News | Sudden government action | Stay informed, reduce exposure before events |
| Stablecoin Depeg | USDT/USDC losing $1 peg | Diversify stables, check redemption mechanisms |
| Meme Coins | Pump and dumps, rug pulls | Avoid without deep research |

---

## 7. Market Sentiment Tools

### On-Chain Metrics
- Exchange inflows/outflows
- Wallet accumulation (whales)
- Network activity
- Hash rate trends (BTC)

### Derivatives Data
- Funding rates (high = longs pay shorts)
- Open Interest (total contracts open)
- Liquidations (forced closures)
- Options skew (sentiment indicator)

### Social Signals
- Google Trends
- Twitter/X sentiment
- Reddit mentions
- Fear & Greed Index

---

## 8. Demo Trading Best Practices

### Setup
1. **Virtual Capital**: $10,000 or $100,000 for realistic math
2. **Same Rules**: Apply all risk management rules
3. **Journal Every Trade**: Entry, exit, reasoning, emotion
4. **Track Metrics**: Win rate, avg gain/loss, max drawdown

### Goals
- Master strategy before real money
- Build discipline and habits
- Test adjustments without cost
- Build confidence through consistency

### Demo vs. Real Difference
- Demo: No emotional attachment → better decisions
- Real: Emotions amplify mistakes
- Must bridge the gap through journaling and reflection

---

## 9. Trading Plan Template

```
STRATEGY: [Name]
TIMEFRAME: [e.g., 4H, Daily]
ASSETS: [BTC, ETH, etc.]

ENTRY RULES:
- Condition 1: [e.g., Price above 20 MA]
- Condition 2: [e.g., RSI < 70]
- Confirmation: [e.g., Volume spike]

EXIT RULES:
- Stop Loss: [Risk %, technical level]
- Take Profit 1: [R/R 1:1.5]
- Take Profit 2: [R/R 1:3]

POSITION SIZE:
- Risk per trade: 1%
- Max positions open: 3

FILTERS (No Trade If):
- Major news event within 2 hours
- Low volume (< average)
- Correlated asset already in position

REVIEW SCHEDULE:
- Daily: Journal trades
- Weekly: Strategy performance
- Monthly: Adjust rules based on data
```

---

## 10. Quick Reference: Before Every Trade

**Checklist:**
- [ ] Entry signal meets strategy criteria
- [ ] Stop loss defined (not mental)
- [ ] Position size calculated (risk ≤ 2%)
- [ ] Risk/Reward minimum 1:2
- [ ] No conflicting positions
- [ ] Market conditions appropriate
- [ ] Emotional state neutral

**Ask:**
1. What is my edge here?
2. What invalidates this trade?
3. At what point am I wrong?
4. Is this FOMO or part of my plan?

---

*Demo trading only. Ready