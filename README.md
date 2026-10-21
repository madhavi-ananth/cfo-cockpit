# FP&A Board Dashboard: Generative AI with Governance by Design

**Live dashboard:** https://madhavi-ananth.github.io/cfo-cockpit/
**Prepared by:** Madhavi Ananth

Generative AI can compress the cycle from period close to board reporting from weeks to hours. As it does, the constraint on a finance function moves from the capacity to produce analysis to the ability to assure it. This project examines what an FP&A function needs in place to rely on AI-produced management reporting, and demonstrates one way to build that assurance into the reporting itself.

## Overview

The project is a board-level FP&A dashboard for a fictional subscription software company, developed with Claude (Anthropic) under my direction and review. It draws on three sources: 24 months of management accounts, the general ledger trial balance for the current month, prior month and prior year, and the FY2026 operating budget. It forms part of a portfolio of work on the responsible use of generative AI in finance, developed within the AI Finance Club's monthly program.

All data is illustrative. No real company, client or employer data is used.

## Design principles

1. **Conclusion first.** Each section opens with a one-sentence management conclusion. Variance commentary addresses the few drivers that are material rather than listing every account.
2. **A consistent comparison framework.** Every headline metric is shown against the prior month, the same month of the prior year and the budget, and the definition of favorable and unfavorable is stated on screen.
3. **Governance by design.** Controls are part of the product, not a separate review step. Their results are visible alongside the figures they support.
4. **Human judgment at the decision points.** AI drafts the analysis and commentary; finance specifies, challenges, reconciles and signs off.
5. **Refreshable each period.** A new month's management accounts can be loaded directly. Figures, comparisons, commentary and controls are recalculated from the data, with no hard-coded narrative.

## Analytical scope

- **Performance management:** revenue by stream, gross and operating margin, operating leverage, Rule of 40 and revenue per employee.
- **Budget-to-actual analysis:** month and year to date, a bridge from budgeted to actual operating income by P&L line, and the principal drivers with commentary on cause.
- **Account-level P&L:** all P&L accounts from the trial balance, month on month and year on year, reconciled to the management accounts.
- **Liquidity and working capital:** cash position, months of liquidity on two bases, and the working-capital items that explain the difference (deferred revenue, accrued compensation, receivables and days sales outstanding).
- **Revenue quality and unit economics:** annual recurring revenue, the recurring-revenue bridge (new business, expansion, contraction and attrition), net revenue retention, churn and average revenue per account.

## Governance and controls

1. **Source-specific conventions.** Each data source was profiled before use: layout, sign convention and how totals are derived. The three sources recorded the same revenue adjustment under three different conventions. Each treatment is documented and tested independently, so that no assumption carries over from one source to another.
2. **Reconciliation before analysis.** The trial balance was reconciled to the management accounts to the cent, from revenue through net income, for all three periods before any account-level analysis was presented.
3. **Correct measurement basis.** P&L balances in the trial balance are cumulative. Monthly results are derived from period activity rather than closing balances.
4. **Controls at every refresh.** Twenty-four completeness, arithmetic and cross-source checks run each time data is loaded, and their results are reported on the dashboard.
5. **Balanced presentation.** Where a single measure would mislead, both bases are shown. Liquidity is presented on a cash basis and on a reported-earnings basis, because accrued compensation not yet paid separates the two materially.
6. **Evidence for commentary.** AI-generated narrative is derived from the data and verified against source. Statements that could not be supported were corrected before publication.

## Illustrative findings (August 2026)

- **Growth and margin.** Monthly revenue of $1.62M, up 26% year over year; annual recurring revenue of $17.9M; gross margin of 74%, an improvement of 3.9 percentage points.
- **Performance against plan.** Year-to-date operating income is $744K below budget: a loss of $3.19M against a budgeted $2.44M. The shortfall sits in G&A ($556K over budget, including an unbudgeted $240K item in May) and R&D ($337K over). S&M is $205K under budget, although part of that reflects lower non-cash amortization rather than an operating saving.
- **Liquidity.** Net cash of $2.12M, equivalent to approximately 22 months of liquidity on a cash basis but approximately 5 months on a reported-earnings basis. The difference is largely $4.5M of accrued compensation not yet paid.
- **Matter for management review.** Amortization of capitalized software declined while the capitalized balance increased from $1.43M to $1.62M, which warrants explanation before external reporting.
- **Data quality.** On loading the following month's management accounts, the controls identified a customer count that did not reconcile to additions and attrition.

## Implications for finance leaders

**The bottleneck moves from production to assurance.** When analysis can be produced in hours, the value of an FP&A team lies in specifying the right analysis, challenging the output and deciding what is material. Capacity released from report production should be redeployed to review, scenario analysis and business partnering.

**Controls must sit where the data enters, and travel with the report.** Reconciliation and completeness checks belong at the point of ingestion, with their results visible to the reader. In banking, these are the same principles that underpin risk data aggregation and reporting under BCBS 239; in corporate reporting, they mirror the expectations of internal control over financial reporting.

**Domain expertise becomes more valuable, not less.** The errors that matter in AI-produced reporting are rarely computational. They come from misread conventions, an incorrect measurement basis or a figure presented without its context. Recognizing them depends on accounting and business judgment that the tool does not supply.

## Using the dashboard

The dashboard is a single self-contained web page and works offline. It opens on August 2026. A subsequent month's management accounts, with the same column headings, can be loaded with the **Load data (CSV)** button; all figures, comparisons, commentary and controls are recalculated and any exceptions are reported on screen.

## Acknowledgements

Program design and sample data: the AI Finance Club (Nicolas Boucher and the club's coaches). Development: Claude (Anthropic), directed and reviewed by Madhavi Ananth.
