# Engineering Notes

## Design goals

These indicators were built to demonstrate production-oriented Pine Script v6 engineering for advanced multi-timeframe oscillator work.

### Confirmed-bar semantics

Higher-timeframe requests are designed around confirmed values rather than developing HTF candles. The goal is deterministic historical behavior and avoidance of misleading lookahead effects.

### Adaptive timeframe handling

Auto mode resolves a same-or-higher timeframe stack from the active chart interval. Manual mode is guarded and intentionally fails closed for unsupported lower-than-chart configurations.

### Event normalization

Requested-timeframe states are normalized into chart-bar events before MTF consensus logic. This prevents repeated labels from a single held HTF condition.

### MTF confirmation windows

Signals from different timeframes do not need to occur on the exact same chart bar. A configurable confirmation window allows time-separated evidence to contribute to one consensus state.

### Defensive validation

Inputs and timeframe relationships are validated explicitly. Unsupported combinations fail clearly instead of silently producing ambiguous behavior.

### Alerts

Both projects support TradingView alert conditions and webhook-oriented JSON payload design.

## Source protection

This public repository intentionally stops at architecture-level documentation and small code excerpts. Proprietary signal logic and complete Pine implementations are private.
