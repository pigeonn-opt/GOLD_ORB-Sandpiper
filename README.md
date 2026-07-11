# Neural Sandpiper

### Overview

GOLD_ORB Sandpiper is an enhanced version of the original GOLD_ORB EA, adding advanced risk management features and signal filtering for improved trade quality and reduced drawdown.

---

### Key Enhancements

#### 1. Time Filters

Two input parameters control when the EA can execute trades:

- **BlockedWeekDays** = `"3"` - Blocks trading on specific days (1=Monday, 7=Sunday). Multiple days with commas, e.g., `"3,5"` blocks Wednesday and Friday.

- **BlockedHours** = `"5,11"` - Blocks trading during specific hours (server time, 0-23). Multiple hours with commas, e.g., `"5,11"` blocks trading at 5:00 AM and 11:00 AM.

#### 2. Break-Even Stop Loss

When profit reaches 50 points, stop loss moves to entry price + 5 points lock-in profit, protecting capital before trailing stop activates.

#### 3. Dynamic ATR-Based Stop Loss

Stop loss and take profit adjust based on market volatility using ATR(14), adapting to changing market conditions rather than using fixed values.

#### 4. Signal Quality Filter

Enhanced `GetBuySellSignal()` with three-layer filtering:

- Breakthrough strength > 30% of range width
- Price position relative to 100-period MA
- Candle body ratio > 50% (reducing false breakout signals)

#### 5. Multi-Timeframe Trend Confirmation

H4 200-period MA confirms major trend direction before executing trades, reducing counter-trend entries.

---

### Why These Enhancements?

- Avoid low-liquidity periods and high-impact news
- Reduce false breakouts during choppy markets
- Align trades with major trend direction
- Protect profits early with break-even stops

---

### Installation

1. Download the EA files
2. Place in your MetaTrader 5 `Experts` folder
3. Compile the EA (F7)
4. Attach to a chart and configure parameters

---

### Credits

Based on the original [GOLD_ORB EA](https://github.com/yulz008/GOLD_ORB/tree/main/GOLD_ORB) by yulz008.
