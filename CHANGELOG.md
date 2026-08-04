# Portfolio Manager — What's New

The latest updates to Portfolio Manager, in plain language. Newest first.

## 3.4.1 — Preview

> 🧪 **This is a preview build.** You're seeing it because **Receive preview updates** is on in Settings → Updates. Preview builds land earlier and get more polish before the stable release. Turn the setting off any time to drop back to the latest stable on the next update check.

The biggest step since 3.3.1 — a smarter Home, backtesting across **multiple brokers**, and an AI setup that runs your backtests *and* reads the results in a single click.

<p align="center">
  <img src="pictures/preview_home.PNG" alt="Portfolio Manager — the new Home" width="820"/>
  <br/><em>The new Home — guided MetaTrader 5 setup, live workers, and one-glance access to every tool.</em>
</p>

### 🏦 Backtest across multiple brokers

Different brokers mean different symbols, spreads, and fills — now Portfolio Manager can drive them all. Register a broker from inside the app, choose which one runs each strategy, and see exactly where every result came from.

- **Register brokers in-app.** Add a broker terminal without leaving Portfolio Manager — the app logs it in, discovers its symbols, and adds it to your list for you.
- **Choose the broker per run.** The Backtest Queue and Portfolio Builder gain a broker column, so you decide where each strategy is tested — and the Queue names the broker a task actually ran on.
- **Switch your master terminal** in a click. Multi-broker stays safely off until you opt in — turn it on in **Settings → Experimental Features**, with your master terminal running in portable mode. It adds a **Brokers** page and a per-run broker column so you always see where a result came from.

<p align="center">
  <img src="pictures/multi_broker.PNG" alt="Multi-broker registration" width="820"/>
  <br/><em>Register and switch brokers from inside the app — no manual terminal juggling.</em>
</p>

### 🤖 Your AI assistant can now run the backtests *and* read the results

Portfolio Manager runs MetaTrader 5 backtests for an assistant; StrategyLens turns finished reports into numbers. Wiring the two together used to be a fiddly manual job that quietly broke whenever they disagreed about where reports live. Now it's one step — an explosive combination once they're pointed at the same folder.

- **One-click AI Combo.** Settings → MCP Server produces a ready-made configuration with **both** servers — Portfolio Manager to run the tests, StrategyLens to analyse them — already pointed at the same reports folder. Paste it into your assistant, restart it, done.
- **An AI reports folder you control.** Name where reports land when the assistant doesn't specify one — it defaults to a sensible place in your Documents, and **Reset** never moves or deletes a single report.
- **Each product still stands alone.** Nothing here makes one depend on the other. The combo is an offer, and declining it costs you nothing.

<p align="center">
  <img src="pictures/new_settings.PNG" alt="Settings — the MCP AI Combo card" width="820"/>
  <br/><em>Settings → MCP Server — copy one configuration and your assistant gains both hands and eyes.</em>
</p>

### 🧭 A guided MetaTrader 5 setup

First run is no longer guesswork. Portfolio Manager finds your MT5 terminals, tells you which ones will actually work, and stops you saving a folder it can't use.

- **A "Connect MetaTrader 5" card** on Home walks you through pointing the app at a working terminal.
- **A terminal picker with verdicts** — every detected install shows a clear can-use / can't-use badge, and why.
- **Path validation before save** — if a folder isn't writable or isn't a real MT5 data folder, the app says so up front instead of failing silently mid-backtest later.

### 🧩 Multi-strategy portfolios & Dynamic Risk profiles

The Portfolio Builder composes one portfolio from **several strategies at once** — each with its own EA, symbol, timeframe, and risk profile — and carries them all the way through Backtest → Balance → Calibrate → Review as a single book.

- **Dynamic Risk Settings (DRS) profiles** define how a strategy is risked — fixed lots or percent-of-balance — and reuse across strategies, with their own sidebar home and an explicit **"Any" timeframe**.
- **The Risk Balancer** walks each strategy to the risk that fits your portfolio drawdown target, with per-strategy retry and a warm-start probe library so re-runs need fewer backtests.
- **Review the portfolio as one account** — merged drawdown, Sharpe, profit factor, and each strategy's contribution.

<p align="center">
  <img src="pictures/drs_profiles.PNG" alt="Dynamic Risk Settings profiles" width="820"/>
  <br/><em>Dynamic Risk Settings profiles — define risk once, reuse it across every strategy.</em>
</p>

### ✨ Smoother, safer day-to-day

- **Nothing lost on the way out.** A clear **Save / Discard / Cancel** prompt when you leave a page with unsaved changes — and **Cancel** really means stay.
- **Queues survive restarts.** Finished results are recovered for tasks that were mid-run when the app last closed, and the "kill running terminals" prompt now has a real **Cancel**.
- **In-app help, expanded.** New topics for connecting your AI assistant, multi-broker requirements, symbol discovery, and the combined MT5 check.

### Upgrade

Nothing to do — your workspaces, settings, license, and existing reports carry over. If you build a multi-strategy portfolio on this preview and later roll back to a stable build, that older build may not be able to read the newer workspace, so **back up your workspaces before testing** if you might want to roll back. Connecting StrategyLens to your assistant needs Node 20 or later on the machine that launches it.

---

## 3.3.1 — Current stable release

Highlights of Portfolio Manager today:

- **Parallel backtesting.** Test many strategies at once across your MetaTrader 5 terminals, so large runs finish far faster.
- **Portfolio Builder.** A guided, step-by-step wizard that assembles your strategies into a balanced portfolio.
- **Strategy Scaler & Calculator.** Size your positions and preview a portfolio's risk and return before you commit.
- **Built-in Backtester.** Run and review strategy tests without leaving the app.

*From here on, each update is listed above with what's new.*

---

*Portfolio Manager is a tool by [TrendSurfers](https://trendsurfers.io). Get the latest version from [Releases](../../releases).*
