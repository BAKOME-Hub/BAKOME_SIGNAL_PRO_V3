# 📡 BAKOME SIGNAL PRO V3 – Ultimate SMC/PA/OF/ICT/MTF Indicator for MT5

## All‑in‑one professional trading signal generator with adaptive scoring, news filter, and real‑time dashboard

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![MQL5](https://img.shields.io/badge/MQL5-Indicator-005F99)](https://www.mql5.com)
[![Platform](https://img.shields.io/badge/Platform-MT5-blue)](https://www.metatrader5.com)

---

## 🔥 Key Features

| Feature | Description |
|---------|-------------|
| **Multi‑Strategy Scoring** | Combines SMC (Order Blocks, FVG, Liquidity Sweeps), PA (Engulfing, Pin Bar), OF (Order Flow), ICT (Kill Zones), and MTF (H4/H1/M15) |
| **Adaptive AI Score** | Dynamically adjusts score based on ADX strength, ATR volatility ratio, and statistical win probability |
| **News Filter** | Blocks signals before/after high‑impact news (NFP, FOMC, CPI, Rate Decisions) – fully customisable calendar |
| **Session & Kill Zones** | London, New York, London Kill Zone (8‑9h), NY Kill Zone (15‑16h) |
| **Real‑Time Dashboard** | Displays MTF alignment, ADX, spread, session, news status, weekly/daily levels, and suggested lot size |
| **ATR‑based SL/TP** | Automatic stop loss and take profit levels (3 targets) with Fib and ATR projections |
| **Non‑Repainting Arrows** | Buy (green), Sell (red), Reversal Bull (aqua), Reversal Bear (orange) – signals appear on closed bars |
| **Alert System** | Popup, sound, and push notifications – one alert per bar to avoid spam |
| **High Performance** | Global indicator handles, pre‑copied buffers, no memory leaks – compiles with zero errors/warnings |

---

## 🛠️ Installation

1. **Download** `BAKOME_SIGNAL_PRO_V3.mq5` from this repository.
2. **Place** the file in `MQL5/Indicators/` folder.
3. **Compile** (F7) in MetaEditor – **no errors, no warnings**.
4. **Attach** to any chart (M5 recommended).
5. Adjust input parameters according to your trading style.

---

## ⚙️ Input Parameters (key groups)

| Group | Parameter | Default | Description |
|-------|-----------|---------|-------------|
| **Signal** | `ScoreMin` | 3 | Minimum score (1‑9) required for a signal |
| | `ArrowGap` | 8 | Gap between arrow and price (points) |
| **SMC** | `OB_Look`, `FVG_Look`, `Liq_Look` | 20,15,15 | Lookback bars for Order Blocks, FVG, Liquidity Sweeps |
| **Indicators** | `EMA_Trend` | 50 | EMA period for trend confirmation |
| | `ATR_Per`, `ADX_Per` | 14,14 | ATR and ADX periods |
| **HTF** | `UseHTF`, `BlockConflict` | true, true | Higher timeframe (H4/H1) trend alignment |
| **News** | `UseCalendar` | true | Enables news filter |
| **Sessions** | `UseSessions`, `London_Start/End`, `NY_Start/End` | true, 7‑12,13‑18 | Trading session windows |
| **Protection** | `SpreadMax` | 3.0 | Maximum spread in points |
| **Projections** | `ShowFibo`, `ShowATRProj` | true, true | Shows Fibonacci and ATR projection levels |
| **General** | `EnableAdaptiveScore` | true | Enables AI‑style adaptive scoring |

---

## 📊 How It Works

1. **Multi‑timeframe trend** – H4, H1, M15 EMAs determine the master trend.
2. **Score calculation** – Each confirmed pattern (OB, FVG, Sweep, Engulfing, Pin Bar, Order Flow, MACD, Bulls/Bears, D1 bonus) adds 1 point.
3. **Adaptive adjustment** – The raw score is boosted if ADX > 30, ATR ratio > 1.2, or win probability > 60%.
4. **Filters** – News block, session, spread, ATR spike, and Judas Swing (fake move) remove low‑quality signals.
5. **Signal execution** – When `finalScore >= ScoreMin`, a directional arrow is plotted, and SL/TP levels are drawn.
6. **Dashboard** – Shows real‑time market state (phase, MTF alignment, ADX, spread, news, weekly/daily levels, suggested lot size).

---

## 💡 Tips

- Use on **M5** for scalping; higher timeframes for swing trading.
- For prop firms, set `RiskPercent` to 0.5‑1.0 and enable daily loss protection (via external EA).
- Test the news filter with your broker’s calendar – adjust `PauseBefore/PauseAfter` as needed.
- Combine with support/resistance zones for extra confluence.

---

## 💰 Crypto Donations (Support Open Source)

If this indicator helps you trade, consider supporting its development:

| Network | Address |
|---------|---------|
| **Bitcoin (BTC)** | `bc1qhtjp3qpqru4vuqd355dfcn46mqjrlpdfmngk6u0` |
| **Ethereum (ETH)** | `0x2fD73626714d9e37EA464109F8eCeA2CA5401062` |
| **Solana (SOL)** | `3CfhghA7hSNPBbd1RME5rRDm5UUeesTq9NKTcyzZdkz4` |
| **USDT (TRC20)** | `THkLdiKsmscJFwBPA4tpWeAn1xVw7DTKxq` |

👉 [Sponsor on Drips](https://app.drips.network/projects/BAKOME-Hub/BAKOME_SIGNAL_PRO_V3)

---

## 📜 License

**MIT** – free for personal and commercial use. No hidden fees, no paywalls.

---

## 👑 Author

**Bakome Fabrice Kitoko** – Goma, Democratic Republic of Congo 🇨🇩  
[GitHub](https://github.com/BAKOME-Hub) | [Email](mailto:fabienbakome@gmail.com)

---

<p align="center">
  <img src="https://img.shields.io/badge/SMC-PA--OF--ICT-blue?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Adaptive-Score-00FF88?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Open%20Source-MIT-green?style=for-the-badge"/>
</p>
