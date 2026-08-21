# Model Architecture

## Objective

The Excel model will separate sources, assumptions, calculations, and outputs so that another analyst can audit the work without relying on the model's author.

## Planned worksheet order

| Order | Tab | Purpose | Principal inputs | Principal outputs |
|---:|---|---|---|---|
| 1 | Cover | Navigation, model status, version, conventions, and high-level outputs | Version and analysis-date inputs | Navigation and model-status indicator |
| 2 | Control | Scenario selection and global transaction assumptions | Case, valuation date, close date, units, and tax settings | Active model controls |
| 3 | Sources | Source IDs, documents, dates, URLs, and model uses | SEC and investor-relations references | Auditable source map |
| 4 | ROK Historical | Rockwell historical financial statements and KPIs | Reported filings and source IDs | Buyer historical financial profile |
| 5 | CGNX Historical | Cognex historical financial statements and KPIs | Reported filings and source IDs | Target historical financial profile |
| 6 | CGNX Operating Model | Target revenue, margin, working-capital, capex, and cash-flow forecast | Historical results and forecast assumptions | Five-year target forecast |
| 7 | ROK Forecast | Selected buyer forecast metrics needed for transaction analysis | Historical results and forecast assumptions | Buyer net income, EPS, cash, debt, and shares |
| 8 | DCF | Standalone intrinsic valuation of Cognex | Forecast UFCF, WACC, and terminal-value assumptions | Enterprise, equity, and per-share value |
| 9 | Trading Comps | Public-company benchmarking and implied valuation | Market data and peer financials | Selected trading-multiple ranges |
| 10 | Precedent Transactions | Acquisition multiples and premiums | Comparable deal data | Selected precedent ranges |
| 11 | Valuation Summary | Synthesis of valuation methodologies | DCF, comps, precedents, and trading range | Football field and offer-price framework |
| 12 | Sources & Uses | Purchase price and transaction funding | Offer price, diluted shares, debt, cash, fees, and consideration | Sources, uses, and financing need |
| 13 | Purchase Accounting | Goodwill and intangible-asset analysis | Purchase price and balance-sheet adjustments | Goodwill, amortization, and tax effects |
| 14 | Accretion Dilution | Pro forma earnings impact | Buyer/target earnings, financing, purchase accounting, and synergies | Pro forma EPS and accretion/dilution |
| 15 | Synergies | Cost/revenue synergies, timing, and implementation costs | Operational assumptions | Run-rate and realized after-tax synergies |
| 16 | Sensitivities | Key valuation and transaction sensitivities | WACC, terminal value, price, financing, and synergies | Valuation and EPS sensitivity tables |
| 17 | Checks | Model integrity and reconciliation tests | Outputs from all calculation tabs | Central pass/fail model status |

## Information flow

```text
Primary sources
      ↓
Historical financials
      ↓
Operating assumptions and forecasts
      ↓
Standalone valuation
      ↓
Offer price and financing
      ↓
Purchase accounting and synergies
      ↓
Accretion/dilution, sensitivities, and recommendation
```

## Design principles

- Historical data will be entered once and referenced elsewhere.
- Forecasts will be driven by visible assumptions rather than hardcoded outputs.
- No offer price will be selected before standalone valuation is complete.
- Revenue and cost synergies will be modeled separately.
- Sources and uses must balance.
- The equity-value bridge, purchase accounting, and pro forma EPS must reconcile.
- Every material output will have a visible check.
