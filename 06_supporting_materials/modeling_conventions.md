# Financial Modeling Conventions

## Scope

These conventions apply to the Rockwell Automation / Cognex M&A model unless a specific disclosure or analytical requirement makes an exception necessary.

## Color conventions

| Cell type | Font / fill | Meaning |
|---|---|---|
| User input or assumption | Blue font | Editable hardcode controlled by the analyst |
| Formula | Black font | Calculation within the same worksheet |
| Cross-sheet formula | Green font | Formula linked to another worksheet in the workbook |
| External-workbook link | Red font | External link; generally prohibited in the final model |
| Required update | Yellow fill | Missing or stale input requiring attention |
| Check passed | Green fill | Reconciliation or integrity check passes |
| Check failed | Red fill | Error or unresolved reconciliation difference |

Reported historical values imported from filings will retain a neutral font and carry a source ID; blue is reserved for assumptions the user is expected to change.

## Units and number formats

- Financial statements: USD millions unless otherwise noted
- Shares: millions
- Per-share values: USD per share
- Percentages: one decimal place by default
- Valuation multiples: one decimal place followed by `x`
- Historical periods: `A`; projected periods: `E`
- Zeros: displayed as `-`
- Negative values: parentheses and red font where appropriate

## Sign conventions

- Revenue, profit, assets, and cash inflows are positive.
- Operating expenses may be shown as negative when presented below revenue, but the approach must be consistent within a schedule.
- Debt, cash, and share counts are entered as positive balances.
- Capital expenditures and increases in net working capital are deductions in free cash flow.
- Transaction fees and financing fees are positive uses of funds.
- Accretion is positive; dilution is negative.

## Formula standards

- Do not embed business assumptions as numbers inside formulas.
- Use one copy-across formula pattern for forecast periods where possible.
- Use direct cross-sheet references and avoid external links.
- Avoid volatile functions such as `INDIRECT` and `OFFSET`.
- Use helper rows for complex calculations.
- Use consistent absolute and relative references.
- Sum complete ranges for totals rather than selected individual cells.
- Avoid circular references unless explicitly approved and documented.

## Historical and forecast periods

- Historical analysis will generally cover five fiscal years when consistently available.
- Forecast analysis will generally cover five fiscal years.
- Actual and estimated periods will be visually separated.
- Rockwell and Cognex fiscal calendars will be reviewed before aligning transaction-period earnings.
- Calendarization will be documented wherever fiscal year ends differ from comparable companies.

## Sources and audit trail

- Every material historical figure must have a source ID.
- Full URLs and document metadata belong on the Sources tab and in `01_research/sources.md`.
- Important assumptions must include a source, historical basis, or written rationale.
- Data unavailable from public sources must be labeled as an assumption rather than presented as fact.
- Market data must include an explicit as-of date.

## Required model checks

- Historical statements tie to reported totals.
- Cash flow ending cash ties to the balance sheet where a full cash-flow model is built.
- Debt and diluted-share schedules reconcile.
- DCF free cash flow ties to its components.
- Enterprise value bridges correctly to equity value.
- Sources equal uses.
- Purchase accounting reconciles purchase price to net assets and goodwill.
- Pro forma shares and earnings reconcile to pro forma EPS.
- Sensitivities respond to the intended assumptions.
- Central model status displays `OK` only when all applicable checks pass.
