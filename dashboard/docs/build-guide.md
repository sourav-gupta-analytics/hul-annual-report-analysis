# Power BI Desktop — build and validation guide

Status: original manual build specification. A separate refined editable PBIP report has now opened successfully in Power BI Desktop, with three pages and 28 measures. Screenshots confirmed FY26 slicer behavior and selected key outputs. Source archive upload, native PBIX export and full interaction testing remain pending. The final report uses a signed horizontal contribution chart rather than a native waterfall, and compact dropdown slicers.

## Import
1. Install Power BI Desktop from Microsoft Store. Download the four CSV files under data/ (Financial, Segments, Historical, Year).
2. Open Power BI Desktop > Get data > Text/CSV. Load Financial, Segments and Year individually. Historical is optional and must remain disconnected.
3. Transform data: FY = whole number, all amounts = whole number, Segment = text. Confirm no missing/duplicate FY in Financial or Year, and one row per FY/Segment in Segments. Rename queries exactly Financial, Segments, Year. Close & Apply.
4. Model view: Year[FY] (1) -> Financial[FY] (*) and Year[FY] (1) -> Segments[FY] (*), single-direction filtering. Do not join Financial directly to Segments. Set relationships active.
5. For manual reproduction, add measures individually using Modeling > New measure; copy from measures.dax. For the final measure `Profit movement`, create a disconnected Profit Bridge table with Driver and numeric Change columns (EBIT 256, Other income -231, Exceptional credit -258, Tax reduction 600). Use percentages for margins/growth, whole numbers with commas for amounts. Set single-select Year slicer for headline cards and default FY26. Historical is not used in current-basis YoY.

## Page 1 — Executive overview
16:9 canvas, navy #102A43 background, white/teal #168B92 accents; light chart panels. Title: HUL | Financial Performance Intelligence. Subtitle: Standalone continuing operations | INR crore | FY25 restated vs FY26.
Cards: Turnover, Turnover YoY, EBITDA, EBITDA Margin, Continuing PAT. Year slicer. Add clustered columns for revenue and operating costs, and a matrix for EBITDA, EBIT, PAT, margins. For two-year trend visuals either disable slicer interaction or use a separate unsliced comparison page.

## Page 2 — Segment intelligence
Year slicer, horizontal bar: Segment vs Segment Turnover. Clustered column: Segment on X, Year[FY] legend, Segment Turnover as value (disable slicer interaction for two years). Matrix: Segment, turnover, segment YoY, share and contribution. Use conditional formatting; negative growth red. Never use segment filters for company totals.

## Page 3 — Profitability and cost bridge
Use a matrix of operating revenue, operating costs, EBITDA, depreciation, EBIT, other net income, pre-exceptional PBT, exceptional credit, PBT, tax and continuing PAT. Create waterfall manually from the FY25 to FY26 PAT movement: starting PAT 10653, EBIT change +256, other income -231, exceptional credit -258, tax expense reduction +600, ending PAT 11020. Mark first/last as totals. Explain that discontinued PAT and gain are excluded from continuing figures.

## Validate before publication
FY26 turnover 61315; EBITDA 14464; revenue 61975; continuing PAT 11020; turnover growth 3.9854%; EBITDA margin 23.3384%; segment turnover total 61315. FY25: turnover 58965, EBITDA 14144, revenue 59676, PAT 10653. Segment contribution total 100% for FY26, subject to rounding. FY25 YoY must be blank (no comparable prior year loaded). An editable PBIP/PBIR project already exists locally; native PBIX export is optional for distribution. Export screenshots for the repository and verify the displayed results. Review privacy and publish only after checking results against the workbook.

Official FY26 report: https://www.hul.co.in/files/annual-report-2025-26-single-page.pdf (printed p.90). Native Desktop report rendering has been observed in screenshots; a PBIX binary and Power BI Service deployment are not yet published.
