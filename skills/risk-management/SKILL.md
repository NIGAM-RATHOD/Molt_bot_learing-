# Risk Management Skill

Portfolio risk framework with hard constraints and dynamic sizing.

## Hard Locks (Non-Negotiable)

### Position Sizing
```
Max Position = MIN(2% of Equity, Kelly Criterion/2)

For $100,000 portfolio:
- Max single trade: $2,000
- If conviction low: $500-1,000
- If high conviction: $2,000 (still capped)
```

### Portfolio Exposure
- Max 50% in crypto (adjustable by user)
- Max 30% in single sector
- Max 20% correlated positions

### Loss Limits
- Daily: -5% max (stop trading)
- Weekly: -10% max (review strategy)
- Per trade: -2% max (hard stop)

## Dynamic Sizing Formula

```
Position Size = Base Risk × Conviction × Volatility Adjust

Where:
- Base Risk = 1% of equity
- Conviction = 0.5x (low), 1x (med), 2x (high)
- Vol Adjust = ATR(14) / ATR(50) (trending=more, chop=less)
```

## Correlation Matrix

Track major assets:
```
BTC-ETH: +0.85 (high)
BTC-SOL: +0.75 (high)
BTC-GOLD: +0.15 (low)
BTC-SPX: +0.35 (medium, rising)
```

## Risk Checks Before Entry

Every trade must pass:
- [ ] Size ≤ 2% equity
- [ ] Stop defined and -2% max loss
- [ ] Correlation check (not doubling down)
- [ ] Trend alignment
- [ ] Daily loss limit not hit

## Post-Trade Risk Update

After each trade:
1. Update portfolio heat map
2. Check sector concentration
3. Recalculate available risk budget
4. Adjust future sizing if needed

## Commands

- `/exposure` - Current portfolio heat map
- `/risk [trade]` - Pre-trade risk check
- `/limits` - Current loss budgets
- `/adjust [setting]` - Modify constraints

## Emergency Protocols

If daily loss limit hit:
1. Stop all new entries
2. Close speculative positions
3. Notify user with P&L breakdown
4. Require manual override to resume
