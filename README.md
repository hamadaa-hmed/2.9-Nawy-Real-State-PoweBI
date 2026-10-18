# Nawy Real Estate Analytics Dashboard

An interactive Power BI project built to analyze real-estate transactions, deals, properties, leads, follow-ups, and activity access by role. The report uses a branded landing page and dedicated analysis pages to turn operational data into business-focused insights.

## Dashboard Pages

- **Overview** — high-level KPIs, monthly deal trends, and transactions by property type.
- **Deals Breakdown** — closed deals, total deal value, average deal value, commission rate, and deal value by payment plan and deal status.
- **Properties Analysis** — property inventory, average bedrooms, available properties, property type mix, developer comparison, and regional availability.
- **Leads Analysis** — lead volume, follow-ups, conversion rate, lead sources, contact attempts by temperature, and lead budget by status.
- **Security Dashboard** — detailed agent/team activity view designed to support role-based data access.
- **Landing Page** — navigation hub for the report.

## Tools & Techniques

- **Power BI** for report design, data visualization, and interactive filtering.
- **DAX** for KPI measures and calculations.
- **Data modeling** to connect the report's business entities.
- **Power BI Row-Level Security (RLS)**, including security-related tables such as `RLS_Users` and `RLS_Guide`, to support controlled data visibility.
- **Interactive report navigation**, slicers, KPI cards, charts, and custom-styled page headers.
- **HTML Content visual** for a scrolling KPI ticker / marquee-style summary.

## Key Business Insights

> Values below are those visible in the recorded report walkthrough. Some KPIs change with report filters, including the selected year, so figures should be interpreted in the context of the active filter state.

### Portfolio & Transactions
- The overview displays **450 properties** and approximately **1K clients**.
- The report shows **1,735 transactions** and total deal value of approximately **$20.59B** in the displayed overview state.
- Monthly deal value is not uniform: the visible trend drops notably around **September–October**, then shows a partial recovery toward year-end. This is a useful period to investigate for seasonality, supply changes, campaign timing, or data completeness.
- Apartments are the largest property type in the transaction breakdown (**811**), ahead of villas (**233**) and townhouses (**212**). This suggests apartments dominate transaction volume in the displayed dataset.

### Deals Performance
- The Deals Breakdown page shows **432 closed deals**, **21B total deal value**, an **average deal value of 23M**, and a **0.9% commission rate**.
- Total deal value by payment plan is relatively close across the three displayed categories: **Installments (7.1B)**, **Cash (6.8B)**, and **Mortgage (6.7B)**. Installments lead in the displayed view, but the gap is modest.
- Average deal value by status is close across the shown categories: **Contracted (22.4M)**, **Closed (22.9M)**, **Reservation (23.3M)**, and **Cancelled (23.5M)**. The cancelled average is slightly higher in this view, which may warrant checking cancellation reasons and the value of cancelled deals rather than assuming higher value means better performance.

### Property Inventory
- The Properties Analysis page shows **450 properties**, an average of **2.9 bedrooms**, and **329 available properties** in the displayed filter state.
- Apartments account for **224 properties**, much more than villas (**59**) and townhouses (**50**), making apartments the largest inventory category in the report.
- The displayed regional availability is highest in **Alexandria (94)** and **New Cairo (94)**, followed by **Cairo (71)** and **West Cairo (70)**.
- Average bedrooms by developer ranges from about **2.7 to 3.3** across the developers shown. This may help compare the types of units each developer contributes to the portfolio.

### Lead Generation & Conversion
- In one displayed filter state, the report shows **4K leads**, **12K follow-ups**, and a **14.6% lead conversion rate**. Another screenshot shows different KPI values under a different year/filter state; therefore these are filter-dependent rather than fixed totals.
- Lead source counts are close in the displayed view: **Paid (906)**, **Referral (889)**, **Organic (857)**, and **Direct (848)**. No single source overwhelmingly dominates, so source quality and conversion rate should be compared alongside lead volume before reallocating marketing spend.
- Average contact attempts by lead temperature are close: **Cold (7.7)**, **Hot (7.6)**, and **Warm (7.5)**. Contact effort appears similar across groups in this view; comparing conversion by temperature could reveal whether effort is being directed effectively.
- The lead-status budget visual shows the largest displayed budget for **Qualified (12B)**, with **Converted (10B)** and several other statuses contributing substantial amounts. This supports monitoring both budget value and progression through the funnel.

## Recommended Business Actions

1. **Investigate the September–October deal-value decline** by checking lead volume, conversion, property availability, and marketing activity for the same months.
2. **Measure conversion by lead source**, not only the number of leads, to determine which channels generate qualified opportunities and closed deals.
3. **Review cancelled deals by value, source, and reason.** The visible average cancelled deal value is not lower than other statuses, so cancellation volume and lost value deserve attention.
4. **Compare payment plans by deal count and value.** The total values are close in the current view; count, average value, and conversion by plan can clarify which option performs best.
5. **Align inventory and demand by region and property type.** Apartments dominate the portfolio, while regional availability varies; compare availability with lead and transaction demand before making allocation decisions.
6. **Track the lead funnel consistently** from leads to follow-ups, qualified leads, conversions, and closed deals, with rates broken down by source and lead temperature.
7. **Validate RLS with test users** across agent, team-lead, and manager roles to confirm each role sees only the intended records.

## Notes & Limitations

- KPI values are transcribed from the dashboard screenshots in the project walkthrough and may change when slicers or filters are changed.
- The business actions above are analytical recommendations based on the visible charts, not proof of causation.
- Do not publish real customer or employee data, credentials, or sensitive source files in a public repository. If the PBIX or source data contains private information, keep it private or publish anonymized screenshots/sample data instead.


