# MTF MACD & Stochastics Suite

Public showcase for two Pine Script v6 multi-timeframe indicators built around confirmed-bar execution, non-repainting higher-timeframe requests, adaptive timeframe handling, alerts, and TradingView runtime validation.

> **Source policy:** this repository is intentionally a showcase. Full production Pine source and internal reference implementations are private. Public files document capabilities, engineering decisions, validation evidence, and limited non-sensitive excerpts only.

## Included indicators

### 1. MTF MACD Divergence PRO v1.1

A multi-timeframe MACD divergence indicator featuring:

- regular bullish / bearish divergence
- hidden bullish / bearish divergence
- adaptive Auto / Manual timeframe modes
- confirmed higher-timeframe data
- pivot-confirmed divergence logic
- configurable MTF confirmation window
- dashboard
- TradingView alerts
- optional JSON alert payloads
- runtime validation across multiple chart intervals

[Open project overview →](projects/MTF-MACD-Divergence-PRO-v1.1/README.md)

### 2. MTF Stochastics PRO v1

A multi-timeframe Stochastic indicator featuring:

- %K / %D oscillator analysis
- overbought / oversold reversal events
- centerline momentum events
- optional %K / %D directional alignment
- adaptive Auto / Manual timeframe modes
- selectable MTF consensus logic
- dashboard
- TradingView alerts
- optional JSON alert payloads
- runtime validation on TradingView

[Open project overview →](projects/MTF-Stochastics-PRO-v1/README.md)

## Engineering focus

- Pine Script v6
- `request.security()` / MTF architecture
- confirmed-bar execution semantics
- non-repainting HTF request design
- no-lookahead discipline
- adaptive timeframe resolution
- signal debouncing / event pulses
- MTF confirmation windows
- defensive validation
- alerts and webhook-ready payload design
- TradingView runtime verification

## Runtime status

| Indicator | TradingView runtime | Public source |
|---|---|---|
| MTF MACD Divergence PRO v1.1 | Passed | Closed source |
| MTF Stochastics PRO v1 | Passed | Closed source |

## Source availability

The complete Pine implementations are **not published in this repository**. Full source can be reviewed privately for legitimate project discussions when appropriate.

See [SOURCE_POLICY.md](SOURCE_POLICY.md).

## Purpose

This repository demonstrates relevant Pine Script engineering work for advanced TradingView projects involving multi-timeframe oscillators, divergence detection, non-repainting logic, alerts, and production-oriented indicator design.

No profitability claims are made. These are engineering demonstrations, not financial advice.
