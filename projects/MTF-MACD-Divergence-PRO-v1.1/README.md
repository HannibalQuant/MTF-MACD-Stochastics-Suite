# MTF MACD Divergence PRO v1.1

Closed-source Pine Script v6 indicator focused on multi-timeframe MACD divergence detection.

## Capabilities

- regular bullish divergence
- regular bearish divergence
- hidden bullish divergence
- hidden bearish divergence
- pivot-confirmed divergence detection
- adaptive timeframe stack
- Auto / Manual timeframe modes
- confirmed higher-timeframe values
- MTF confirmation window
- individual timeframe signal controls
- consensus labels
- dashboard
- TradingView alert conditions
- JSON alert payloads

## Timeframe behavior

Auto mode adapts to the active chart interval. Examples:

| Chart | TF1 | TF2 | TF3 |
|---|---|---|---|
| 15m | 15m | 1H | 4H |
| 1H | 1H | 4H | 1D |
| 2H | 2H | 4H | 1D |
| 4H | 4H | 1D | 1W |
| 1D | 1D | 1W | 1M |

Manual mode is fail-closed for lower-than-chart requests.

## Non-repainting design

The implementation uses confirmed requested-timeframe values and avoids treating a developing higher-timeframe candle as final historical information.

The public repository intentionally does not expose the complete divergence engine, pivot pairing logic, filters, alert payload builder, or full Pine source.

## Validation

- TradingView compile/runtime: passed
- multiple chart intervals: passed
- adaptive timeframe behavior: passed
- historical confirmed-bar design: implemented

## Public sample

A limited code excerpt is available in [PUBLIC_CODE_EXCERPT.md](PUBLIC_CODE_EXCERPT.md).

**Full Pine source: private.**
