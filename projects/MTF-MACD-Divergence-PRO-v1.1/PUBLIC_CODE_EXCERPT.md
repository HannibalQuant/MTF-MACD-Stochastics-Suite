# Public Code Excerpt

This excerpt is intentionally incomplete. It demonstrates coding style and MTF safety conventions without publishing the proprietary divergence engine.

```pine
//@version=6
indicator("MTF MACD Divergence PRO", shorttitle="MTFMDIV", overlay=false)

string tfMode = input.string("Auto", "Timeframe mode", options=["Auto", "Manual"])
int chartTfSec = timeframe.in_seconds()

// Public architectural example only.
// The production implementation resolves TF2/TF3 from a guarded
// same-or-higher timeframe ladder and validates Manual mode.

f_confirmedValue(float value) =>
    value[1]

// Production code requests a confirmed tuple from each enabled timeframe
// and applies explicit consensus/event logic after the request boundary.
```

Not included publicly:

- divergence classification rules
- pivot pairing / span logic
- internal filters
- consensus implementation
- full alert payload generation
- complete indicator source
