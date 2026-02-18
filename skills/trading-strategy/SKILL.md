# Trading Strategy Skill

Multi-agent trading strategy framework with risk management and post-trade analysis.

## Core Concepts

### Strategy Evaluation Pipeline
```
User Idea → Technical Check → Risk Assessment → Execute → Post-Mortem
```

### Risk Hard-Locks
- **1-2% Rule**: Max position size = 2% of portfolio
- **Trend Alignment**: Only trade with higher-timeframe trend
- **Stop Loss**: Mandatory on every trade

## Sub-Agent Roles

### GLM5 (Strategy Validator)
- Deep technical analysis
- Chart pattern validation
- Multi-timeframe trend alignment
- Risk/reward calculation

### MiniMax (Quick Scanner)
- Market sentiment snapshot
- News/social momentum
- Quick risk check
- Opportunity ranking

## Strategy Debate Protocol

When user proposes trade idea:

1. **My Role**: Present synthesized analysis
2. **Format**: "Technicals show [X], but given your view on [Y], recommend [Z]"
3. **Always include**: Entry, stop, target, size (%), conviction level

Example:
```
User: "I think ETH will pump on ETF news"
Me: "Technicals agree (broke $2400 resistance), momentum positive. 
     Recommend: Long at $2420, stop $2380 (1.6%), target $2550.
     Size: 1.5% portfolio. Conviction: Medium-High.
     Execute? [Yes] [Adjust] [Cancel]"
```

## Post-Trade Analysis

Every closed trade triggers:

1. **Expected vs Actual**: Compare forecast to outcome
2. **Decision Audit**: What signaled entry/exit?
3. **Strategy Score Update**: Tag as +1/-1 for pattern
4. **Pattern Deprecation**: 3 losses = bench strategy

## Commands

- `/trade [asset] [direction] [reason]` - Propose trade
- `/journal` - View recent trades with scores
- `/strategies` - See active vs benched strategies
- `/risk` - Current exposure summary

## Memory Keys

- `trades:YYYYMMDD` - Daily trade log
- `strategy_scores` - Strategy performance tracking
- `portfolio:risk` - Current exposure and limits
