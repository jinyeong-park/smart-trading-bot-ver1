# Smart Trading Bot (STB)

Frontend code: https://github.com/jinyeong-park/smart-trading-bot
Backend code:


Build a complete no-code prototype in LovableDP named "Smart Trading Bot (STB) — v1.0" using the following Product Requirements Document. Produce a working, demonstrable prototype (web dashboard + workflow automation) that supports paper/live trading via Alpaca and historical backtesting via Yahoo Finance. Deliverables: interactive web dashboard, configured workflows/automations, data storage (initial SQLite), mock or real Alpaca connector, alerting (email/SMS), logging & reports, test plan, diagrams, and a deployment checklist.

1) CORE FUNCTIONALITY (MUST)
- Automated trading workflow:
  - Accept user-defined watchlist.
  - Auto-buy when buy rule triggers.
  - Auto-take-profit at +5% from buy price.
  - Auto-stop-loss at -1% from buy price.
  - Restrict trading to market hours.
- Portfolio management:
  - Real-time holdings table (ticker, qty, buy price, current price, P/L).
  - Portfolio value and overall ROI.
- Risk rules:
  - Daily loss limit: $500 (halt trading when reached).
  - Max allocation per symbol: 10% of capital.
  - Max concurrent holdings: 10.
- Logging & reporting:
  - Persist all trades and system events to DB.
  - Daily trade summary report generator.

2) IMPORTANT (SHOULD)
- Real-time monitoring dashboard (charts & tables).
- Alerts: email and SMS for trades, halts, and critical errors.
- Backtesting module:
  - Run strategies on historical data, produce metrics: annualized return, Sharpe ratio, max drawdown.

3) NICE-TO-HAVE (IF FEASIBLE)
- Moving-average & Bollinger Bands strategy templates.
- Volume-based screener.
- Mobile-responsive dashboard and manual override button for emergency stops.

4) TECH CONSTRAINTS & INTEGRATIONS
- Data: Yahoo Finance (historical & intraday). Polling interval ≤1 minute.
- Broker: Alpaca Trading API (or sandbox for demo). Execution latency target ≤5s for demo flows.
- Storage: SQLite for prototype; provide migration notes to PostgreSQL.
- No-code mapping: map backend logic to LovableDP workflows; simulate FastAPI endpoints where necessary.
- Uptime & performance: design for 99.5% uptime in architecture diagram; show retry/backoff for API calls.

5) SECURITY & COMPLIANCE
- Securely store API keys (encrypted fields).
- 2FA for dashboard login.
- Audit logs for every trade and config change.
- Compliance note: include Pattern Day Trading caution and broker TOS check.

6) ACCEPTANCE CRITERIA & KPIs
- Monthly return target (simulated/backtest): 3–5% target.
- Max drawdown ≤10% (backtested).
- System uptime design ≥99.5%.
- Order execution flow completes within demo ≤5s.

7) DELIVERY & MILESTONES
- Phase 1 (4 weeks) — Core:
  Week 1: Data & Alpaca connector setup, DB schema, auth.
  Week 2: Trading workflows (buy/sell/stop-loss/take-profit).
  Week 3: Portfolio UI + risk rules + logging.
  Week 4: Paper-trading test & debugging.
- Phase 2 (2 weeks) — Polish:
  Week 5: Dashboard visuals, alerts, backtesting flows.
  Week 6: Test plan, docs, deployment checklist.

8) WHAT TO PROVIDE AT FINISH
- Live LovableDP prototype (or shareable demo link).
- UI wireframes & workflow diagrams.
- Exportable DB schema + sample data.
- Backtest report sample and one-week paper-trade log.
- Test plan, runbook, and deployment checklist.
- Short user manual: how to add watchlist, set capital, enable live trading, emergency stop.

Please create the prototype in LovableDP, using sandbox Alpaca keys by default. If any integration is unavailable, mock the API responses but keep interfaces pluggable. Provide step-by-step instructions in the project workspace to convert from paper trading to live trading safely.
