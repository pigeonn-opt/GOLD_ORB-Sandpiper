# GOLD_ORB-Sandpiper
### Overview

GOLD_ORB Sandpiper is an enhanced version of the original GOLD_ORB EA, adding time-based trading filters for more precise trade timing control.

### Key Enhancements

#### Time Filters

Two new input parameters have been added to control when the EA can execute trades:

- **BlockedWeekDays** = `"3"` - Blocks trading on specific days of the week (1=Monday, 7=Sunday). Multiple days can be specified with commas, e.g., `"3,5"` blocks Wednesday and Friday.

- **BlockedHours** = `"5,11"` - Blocks trading during specific hours (server time, 0-23). Multiple hours can be specified with commas, e.g., `"5,11"` blocks trading at 5:00 AM and 11:00 AM.

### Why These Filters?

These filters are particularly useful for:
- Avoiding low-liquidity periods
- Skipping high-impact news releases
- Aligning with your preferred trading sessions
- Reducing noise during non-optimal market hours

### Installation

1. Download the EA files
2. Place in your MetaTrader 5 `Experts` folder
3. Compile the EA (F7)
4. Attach to a chart and configure parameters

### Credits
Based on the original GOLD_ORB EA by yulz008 https://github.com/yulz008/GOLD_ORB/tree/main/GOLD_ORB
