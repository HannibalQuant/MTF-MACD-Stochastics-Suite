# MTF Stochastics PRO v1

Closed-source Pine Script v6 indicator focused on adaptive multi-timeframe Stochastic analysis.

## Capabilities

- %K / %D oscillator analysis
- overbought / oversold reversal events
- centerline momentum events
- optional %K / %D directional alignment
- Auto / Manual timeframe modes
- adaptive timeframe stack
- confirmed requested-timeframe values
- selectable consensus family: Reversal / Momentum / Either
- configurable confirmation window
- individual timeframe signal controls
- MTF consensus labels
- dashboard
- TradingView alert conditions
- JSON alert payloads

## Timeframe behavior

Auto mode follows the active chart interval. Examples:

| Chart | TF1 | TF2 | TF3 |
|---|---|---|---|
| 15m | 15m | 1H | 4H |
| 1H | 1H | 4H | 1D |
| 2H | 2H | 4H | 1D |
| 4H | 4H | 1D | 1W |
| 1D | 1D | 1W | 1M |

Manual mode deliberately rejects lower-than-chart requests rather than silently changing semantics.

## Non-repainting design

The production implementation uses confirmed requested-timeframe data so developing HTF candles are not presented as settled historical signals.

The full Stochastic signal engine, consensus implementation, timeframe resolver, alert builder, and Pine source remain private.

## Validation

- TradingView compile/runtime: passed
- BTCUSDT 1H runtime check: passed
- oscillator rendering: passed
- adaptive timeframe dashboard: passed
- MTF bullish / bearish consensus labels: passed

## Public sample

A limited code excerpt is available in [PUBLIC_CODE_EXCERPT.md](PUBLIC_CODE_EXCERPT.md).

**Full Pine source: private.**
