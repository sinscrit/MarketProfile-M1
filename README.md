[![Stand With Ukraine](https://raw.githubusercontent.com/vshymanskyy/StandWithUkraine/main/badges/StandWithUkraine.svg)](https://github.com/vshymanskyy/StandWithUkraine/blob/main/docs/README.md)
# Market Profile - M1 Fork

Forked from [EarnForex/MarketProfile](https://github.com/EarnForex/MarketProfile). Original indicator by EarnForex.com.

Market Profile shows where the price has spent more time, highlighting important levels that can be used in trading.

![Market Profile - example on intraday sessions of GBP/USD](https://github.com/EarnForex/MarketProfile/blob/master/README%20Images/Market%20Profile%20(Intraday).png)

## What's New: Last_N_Minutes Session Mode

This fork adds a **Last_N_Minutes** rolling session type to the MT4 indicator (`MarketProfile.mq4`), designed for use on **M1 charts**.

Instead of fixed daily/weekly/intraday sessions, it shows a single Market Profile built from the **last N minutes** of price data, rolling forward as new bars arrive.

### How to Use

1. Open an **M1** chart in MetaTrader 4.
2. Attach the indicator and set **Session** = `Last_N_Minutes`.
3. Set **LastNMinutes** = `15` (default) or any duration you prefer.
4. The profile redraws on every tick, always showing the most recent N minutes.

You can also press **Ctrl+9** to switch to this mode at any time.

### Parameters

| Parameter | Default | Description |
|---|---|---|
| `Session` | `Daily` | Set to `Last_N_Minutes` for the rolling window mode |
| `LastNMinutes` | `15` | Duration of the rolling window in minutes |

The chart timeframe must be smaller than `LastNMinutes` (e.g. M1 with 15-minute window = 15 bars).

All other original parameters (colors, value area %, developing POC/VAH/VAL, alerts, rays, etc.) work as normal.

## Original Indicator

Detailed description of the original indicator can be found here:
https://www.earnforex.com/indicators/MarketProfile/

Installation instructions:
https://www.earnforex.com/guides/metatrader-indicators-installation-tutorial/

Last modified: 2026-02-18
