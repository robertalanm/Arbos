# Arbos

![Arbos](arbos.jpg)

<p align="center">
  Welcome! Arbos is simply a <a href="https://ghuntley.com/loop/">Ralph-loop</a> combined with a Telegram bot.<br>
  That's all you need to do just about anything.
</p>

# The Design

```
                         (prompt.md + goal.md + state.md)
                       ┌─────────────────────────┐
                       ▼                         │
  ┌──────────┐     ┌───────┐                     │
  │ Telegram │◄───►│ Agent │─────────────────────┘
  └──────────┘     └───────┘
```

## Requirements

- [Telegram Bot token](https://core.telegram.org/bots#how-do-i-create-a-bot)
- [Chutes API key](https://chutes.ai)

## Getting started

```sh
curl -fsSL https://raw.githubusercontent.com/unconst/Arbos/main/run.sh | bash
```

## Usage

Arbos runs a loop which passes `GOAL.md` to a coding agent. 
To run Arbos just tell the agent what you want `GOAL.md` to be.

Example prompt:
```
R = you = an autonomous research agent with capital, data, and compute

Goal: design and evolve a system S that discovers profitable strategies in changing environments.

Initial State:
C = { $10k Hyperliquid capital, Coinglass derivatives data (funding, OI, liquidations, leverage), compute on Basilica/Targon/Lium }
S₀ = continuous adaptive trading system with:
    M ≈ 50 models per asset
    online training on fresh data
    evolutionary model search (mutate/replace weak models)
    strict walk-forward validation + online Sharpe filtering
    horizon ensembles H = {1h,4h,8h,12h,24h}
    consensus gating for signals
    layered risk controls (position limits, vol sizing, stops, drawdown protection)
    features from derivatives positioning signals + price
    exploration of modern time-series foundation models

Your loop consists of the following:
loop t = 1..∞
    S_t = design_or_modify(S_{t-1})
    O_t = run(S_t)         # train models, evaluate, ensemble, trade
    P_t = measure(O_t)     # Sharpe, PnL, drawdown, regime behavior
    Δ_t = reflect(P_t)     # find weaknesses in models, signals, validation, risk
    S_{t+1} = improve(S_t, Δ_t)
end

Dont stop. Be proactive.
```

---

MIT 

