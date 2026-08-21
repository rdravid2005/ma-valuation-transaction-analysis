# Discounted Cash Flow Analysis

**Company:** Cognex Corporation  
**Valuation method:** Unlevered DCF using the Gordon Growth method  
**Forecast period:** FY2026E-FY2030E  
**Discounting convention:** Mid-year  
**Selected operating case:** Base

## Methodology

The DCF values Cognex's standalone operations before acquisition financing or synergies. Forecast unlevered free cash flow is linked directly from the operating model and calculated as:

```text
NOPAT
+ Depreciation and amortization
− Capital expenditures
− Increase in operating net working capital
= Unlevered free cash flow
```

UFCF is discounted at Cognex's weighted average cost of capital. Because Cognex has no funded debt, its WACC is effectively its cost of equity. Cost of equity is calculated using CAPM:

```text
Cost of equity = Risk-free rate + Adjusted beta × Equity risk premium
```

Terminal value is calculated using the Gordon Growth formula:

```text
Terminal value = Final-year UFCF × (1 + terminal growth) ÷ (WACC − terminal growth)
```

## Selected assumptions

| Assumption | Selected value | Rationale |
|---|---:|---|
| Risk-free rate | 4.7% | Rounded ten-year U.S. Treasury yield |
| Observed beta | 1.50x | Five-year market beta |
| Adjusted beta | 1.34x | Observed beta adjusted toward 1.0 |
| Equity risk premium | 5.0% | Kroll recommended U.S. ERP |
| WACC | 11.4% | CAPM-derived cost of equity; no debt weighting |
| Terminal growth | 2.5% | Long-term nominal growth below WACC |
| Cash and investments | $755.0 million | Cognex balance at July 5, 2026 |
| Debt | $0.0 million | Cognex reported no funded debt |
| Share count | 168.2 million | Latest basic shares used as a provisional diluted proxy |

## Base-case results

| Output | Value |
|---|---:|
| Present value of forecast UFCF | $1,097.4 million |
| Present value of terminal value | $2,486.3 million |
| Enterprise value | $3,583.7 million |
| Equity value | $4,338.7 million |
| Implied value per share | $25.79 |
| Terminal value / enterprise value | 69.4% |
| Implied terminal EV / EBITDA | 8.4x |

The implied per-share sensitivity range is approximately $20.83-$35.78 across WACC values of 9.4%-13.4% and terminal-growth rates of 1.5%-3.5%.

## Interpretation

The DCF produces a conservative standalone valuation because Cognex's equity value is highly sensitive to its discount rate and terminal assumptions. The terminal value represents approximately 69% of enterprise value, which is significant but not unusual for a high-margin, low-capital-intensity business.

The result should not be interpreted as the final offer price. A buyer must also consider unaffected trading price, public-company trading multiples, precedent transaction premiums and multiples, strategic value, synergies, and transaction feasibility. If market-based methods imply materially higher values, the difference will reveal how much future growth and strategic value the market is capitalizing beyond this DCF.

## Limitations and items to refine

- The beta is a direct observed beta adjusted toward 1.0. A peer-derived unlevered and relevered beta should be considered after the comparable-company set is complete.
- Latest basic shares are used as a provisional diluted-share proxy. Options and restricted equity will be refined using the treasury-stock method before final publication.
- The primary terminal-value method is Gordon Growth. An exit-multiple cross-check will be incorporated after trading comparable companies are complete.
- The model uses full-year forecasts and a mid-year convention rather than a detailed stub-period calculation.
- The DCF excludes acquisition synergies, financing effects, and an acquisition premium.

## Sources

Key inputs are supported by S-022 and S-029 through S-031 in the [sources register](../01_research/sources.md).
