# Strategy

The strategy repository is the orchestration and decision layer for the trading platform. It owns the full pipeline from ingesting normalized market and options data, through feature engineering, filtering, scoring, and portfolio decision-making, to producing trade intents and eventually execution.

Each stage is implemented as a modular component behind stable interfaces so data sources, signal models, filters, scoring methods, and execution adapters can be swapped independently without changing the rest of the system.

The core design goal is a contract-driven, replayable pipeline where research, backtesting, and live trading all run on the same staged architecture with different module implementations.
