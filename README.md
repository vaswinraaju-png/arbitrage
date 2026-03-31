# Vortex Arb — Funding Rate Arbitrage Bot

Binance Spot + Perp delta-neutral funding rate arbitrage.
Top 10 USDT pairs. Runs every hour.

## Setup
1. Clone repo
2. Create .env from .env.example
3. pip install -r requirements.txt
4. python main.py

## Structure
- config.py         → all settings
- funding_monitor.py → live rate scanner
- signal_engine.py  → entry/exit logic
- executor.py       → order placement
- tracker.py        → PnL logging
- main.py           → bot runner
```

**1.5 Create .env.example — safe template to commit**
```
# Copy this to .env and fill in your values
# NEVER commit the actual .env file

BINANCE_API_KEY=your_api_key_here
BINANCE_SECRET=your_secret_here
CAPITAL_PER_PAIR=500
ENTRY_THRESHOLD=0.0001
EXIT_THRESHOLD=0.00005
