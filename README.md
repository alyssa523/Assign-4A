# Auralis Product Feedback Dashboard

An interactive, sortable, filterable dashboard for exploring consolidated customer-feedback themes for Auralis Hearing Technologies. It presents already-consolidated data pulled from four sources — the audiologist product survey, the field sales rep feedback log, the customer service email compilation, and the public Google review compilation — so a product manager can independently explore and prioritize themes ahead of the next launch.

**The dashboard only displays, sorts, and filters data. It does not compute, combine, or rank anything on its own.** Every number shown comes directly from the underlying consolidation report.

## What it shows

For each of the 10 recurring product themes (e.g. "Bluetooth connectivity," "Fitting software workflow"):

| Column | Meaning |
|---|---|
| Theme | The product/feature area feedback was grouped into |
| Total Mentions | How many times the theme was cited across all four sources |
| Audiologist Satisfaction (avg/5) | Average satisfaction score from the audiologist survey |
| Sales High-Urgency Flags | Count of sales log entries flagging the theme as high urgency |
| Public Review Rating (avg/5) | Average star rating from Google reviews mentioning the theme |

A theme shown as **n/a** in Public Review Rating means it wasn't tagged in any Google review for that period — not that its rating was zero.

## How to use it

1. Download `dashboard/feedback_dashboard.html` (or clone the repo).
2. Open the file directly in any modern browser (Chrome, Edge, Firefox) — just double-click it, or right-click → Open With → your browser. No install, no server, no internet connection required.
3. Use the **Dataset** toggle at the top to switch between:
   - **Full set** — the complete, current data (136 total mentions)
   - **Sample (test)** — a small 60-mention sample used to verify the dashboard's behavior against a report before trusting it on the full dataset
4. **Sort** by clicking any column header (click again to reverse direction).
5. **Filter** using the controls above the table: search by theme name, set a minimum mention count, cap satisfaction or review rating, or show only themes with at least one high-urgency sales flag. Click **Reset filters** to clear everything.

## Why it's built this way

The dashboard is a single self-contained HTML file with the data embedded directly in it — no build step, no external libraries, no network calls. That keeps it easy to open from anywhere (a grader's laptop, a shared drive, GitHub) without setup, and keeps the data static and auditable: anyone can view-source the file and see exactly where every number comes from.

## Source data

The consolidated figures come from:
- `Auralis_Feedback_Consolidation_Report_FullSet.docx` (full dataset)
- `Auralis_Feedback_Consolidation_Report.docx` (sample dataset used for testing)

which themselves consolidate the audiologist survey, sales feedback log, customer service emails, and Google review compilation for Auralis Hearing Technologies.
