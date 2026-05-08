# Public Trading Signal History

## Overview

This repository publicly tracks the trading-signal history of an experimental AI-assisted equity screening system.

The purpose of this repository is to create a transparent, time-stamped record of how the system performs when used prospectively. Instead of only reporting retrospective backtests, this repository records signals, watchlists, and trade-management notes over time.

The underlying algorithm is proprietary and not disclosed in this public repository.

## What This Repository Shows

This repository may include:

- dated signal reports;
- entry candidate lists;
- watchlist candidates;
- open-position review notes;
- trade-management status;
- closed-trade summaries;
- simple performance summaries over time.

The repository is intended to document the history of the system’s real-time or near-real-time output.

## What This Repository Does Not Show

This repository does **not** disclose:

- proprietary model architecture;
- feature-engineering details;
- raw model internals;
- private training data;
- embeddings or retrieval internals;
- full scoring formulas;
- source code for the core algorithm;
- any confidential or commercially sensitive implementation details.

The public reports are intentionally simplified so that the trading history can be reviewed without exposing the intellectual property behind the system.

## Trading Philosophy

The system is used as a ranking and screening tool.

At a high level, the workflow is:

1. Refresh recent market data.
2. Generate prediction-ready data using a point-in-time-safe pipeline.
3. Run saved prediction models.
4. Rank current stock candidates.
5. Identify high-confidence candidates.
6. Review open positions against simple trade-management rules.
7. Produce a human-readable report.

The system does **not** automatically place trades. Human review remains part of the process.

## Entry Logic

The system ranks eligible stocks by model confidence.

In general:

- the highest-ranked candidates may be considered for possible entry;
- lower-ranked candidates may be placed on a watchlist;
- candidates without sufficient confidence or agreement are ignored.

Public reports may use simplified labels such as:

- `ENTRY CANDIDATE`
- `WATCHLIST`
- `IGNORE`

The exact ranking algorithm and model-agreement logic are proprietary and are not disclosed publicly.

## Position Review Logic

Open positions are reviewed periodically.

The system may produce simple review labels such as:

- `HOLD`
- `REVIEW`
- `STRONG REVIEW`
- `CONSIDER EXIT`
- `SELL - TARGET`
- `SELL - STOP`
- `SELL - TIME`

At a high level, review decisions may consider:

- current return;
- holding period;
- whether the stock remains highly ranked;
- whether the signal has weakened;
- whether the position has reached a target, stop, or time limit.

A stock falling in rank does not automatically mean it must be sold. Rank deterioration is generally treated as a review signal, while price target, stop-loss, and maximum holding period are treated as stronger trade-management rules.

## Time-Stamped Record

This repository is designed to remain true to time.

Because updates are committed to Git, readers can inspect the commit history to see when reports were added or modified.

The goal is to avoid hindsight bias by maintaining a chronological public record.

Readers should evaluate the repository history directly rather than relying only on later summaries.

## Important Limitations

This is an experimental research and commercialization project.

Performance may be affected by:

- market regime changes;
- liquidity and execution quality;
- bid-ask spreads;
- slippage;
- delayed manual execution;
- transaction costs;
- data quality;
- model drift;
- corporate actions;
- survivorship issues;
- human discretion in trade selection.

Past performance does not guarantee future results.

The presence of a signal does not mean a trade will be profitable.

## No Investment Advice

Nothing in this repository is financial, investment, legal, tax, or trading advice.

The information is provided for research transparency and commercial demonstration only.

No reader should buy, sell, short, or hold any security based solely on the contents of this repository.

Anyone making investment decisions should conduct their own research and consult qualified professionals as appropriate.

## No Client Relationship

This repository does not create an adviser-client, fiduciary, broker, or investment-management relationship.

The project owner is not offering individualized investment advice through this repository.

The public reports are not tailored to any individual investor’s objectives, risk tolerance, financial situation, or constraints.

## Commercial Interest

The underlying system is proprietary.

We are open to discussions regarding:

- acquisition;
- licensing;
- research collaboration;
- commercial partnership;
- integration into a larger investment-research platform;
- evaluation by qualified institutional or strategic partners.

Interested parties may contact the project owner for private discussion.

The public repository is intended to demonstrate process transparency while preserving the proprietary algorithm.

## Suggested Evaluation Criteria

Interested readers or potential partners may evaluate the public record based on:

- whether signals were posted before outcomes were known;
- consistency of the reporting process;
- hit rate over time;
- realized trade outcomes;
- drawdowns;
- turnover;
- robustness across market conditions;
- whether performance survives transaction-cost assumptions;
- whether positive results persist beyond the initial observation period.

## Disclaimer

This project is experimental.

Trading securities involves risk, including the possible loss of principal.

No representation is made that any account, user, investor, or strategy will achieve profits or losses similar to those shown in this repository.

All public results should be interpreted as research records, not as investment recommendations or performance guarantees.