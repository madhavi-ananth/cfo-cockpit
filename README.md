# CFO Cockpit — Assuring AI-Generated Board Reporting

**Live dashboard:** https://madhavi-ananth.github.io/cfo-cockpit/

A board-level financial dashboard for Meridian Cloud, Inc., a fictional subscription software business, built with Claude as part of the AI Finance Club's September monthly challenge. **All data is illustrative. No real company or client data is used.**

## Purpose

The exercise was to produce a one-page CFO dashboard from three sources: a 24-month management summary, a monthly trial balance and the FY2026 operating budget. The more relevant question was whether a dashboard produced quickly with AI could be relied upon in front of a board. The design therefore treats data assurance as part of the product, not a separate step.

## What the dashboard covers

- **Overview:** ARR, revenue, margins, net cash and customers, each compared with the prior month, the same month of the prior year and the budget.
- **Profitability:** margin trend, cost structure and the latest-month P&L.
- **Account-level P&L:** all 30 P&L accounts from the trial balance for the current month, the prior month and the prior year, reconciled to the management summary.
- **Actual vs budget:** month and year-to-date variances, labelled favourable or unfavourable, with the principal drivers explained rather than every account listed.
- **Cash:** liquidity position and two measures of runway, with the working-capital items that explain the difference between them.
- **Customers:** MRR movement, retention and customer base.
- **Data checks:** the controls described below, with their results.

## Control approach

1. **Source-level conventions.** Each file was profiled before use: header position, sign convention and how totals are formed. The three sources recorded the same revenue adjustment under three different conventions (negative; positive and subtracted; debit-positive). Each treatment is documented on the dashboard and tested independently.
2. **Reconciliation before analysis.** Trial-balance totals were reconciled to the management summary to the cent for all three periods, from revenue through net income, before any account-level analysis was presented.
3. **Correct measurement basis.** P&L closing balances in the trial balance are cumulative. Monthly results are therefore derived from period activity (debits less credits), not closing balances.
4. **Controls on every data load.** Twenty-four arithmetic and completeness checks rerun whenever new data is loaded. Loading the following month's file identified a customer count that did not roll forward.
5. **Balanced presentation of liquidity.** Runway is shown on both a cash-movement basis and a reported-loss basis, because accrued compensation not yet paid materially separates the two.
6. **Evidence for commentary.** Narrative statements are generated from the data and checked against the source files. Statements that could not be supported were corrected.

## Using the dashboard

The page is a single self-contained HTML file and works offline. It opens on August 2026. The **Load data (CSV)** button accepts a later monthly summary with the same column headings; all figures, comparisons and checks are then recalculated, and any failed checks are reported on screen.

## Acknowledgements

Exercise design and sample data: the AI Finance Club (Nicolas Boucher and the club's coaches). Build: Claude (Anthropic), directed and reviewed by Madhavi Ananth.
