# Hindustan Unilever | Annual Report Analysis

**Financial analytics · Excel · Power BI Desktop · FY25 restated vs FY26**

How much of Hindustan Unilever's turnover growth translated into operating profitability? This case study compares standalone continuing operations after the Ice Cream demerger. The editable three-page Power BI Desktop report includes 28 measures and source-linked financial and segment data.

[Download editable Power BI project](https://github.com/sourav-gupta-analytics/hul-annual-report-analysis/raw/refs/heads/main/dashboard/HUL_PowerBI_Project.zip) · [Dashboard gallery](dashboard/README.md) · [Desktop validation](dashboard/desktop-validation.md) · [Portfolio](https://souravgupta.vercel.app/#projects)

![Actual Power BI Desktop report showing HUL FY26 turnover, EBITDA and continuing PAT](dashboard/01-executive-overview.png)

## Key findings

- **Growth outpaced profit expansion.** Turnover increased **3.99%** to INR 61,315 crore. EBITDA rose **2.26%** to INR 14,464 crore, and EBITDA margin moved from **23.70% to 23.34%**.
- **Operating costs grew ahead of revenue.** Costs rose **4.35%** and operating revenue rose **3.85%**. The gap points to a follow-up on unit costs, product mix and distribution.
- **Home Care made the largest contribution to growth.** It contributed **30.51%** of the INR 2,350 crore turnover increase. Beauty & Wellbeing led segment turnover growth at **4.98%**.
- **Tax effects helped lift continuing PAT.** Continuing PAT increased **3.45%** and pre-exceptional PBT increased **0.18%**. The PAT bridge separates tax, exceptional and operating effects.

The [executive case study](docs/executive-case-study.md) includes the full metric table, profit bridge, recommendations and limitations.

## Deliverables

| File | Purpose |
| --- | --- |
| [Financial.csv](data/Financial.csv) | Source-linked comparable P&L |
| [Segments.csv](data/Segments.csv) | Source-linked segment data |
| [Historical.csv](data/Historical.csv) | FY24–25 originally reported historical context only |
| [Year.csv](data/Year.csv) | Power BI year dimension |
| [Source register](docs/source-register.csv) | Provenance and reporting basis |
| [DAX measures](dashboard/measures.dax) | Power BI model calculations |
| [Theme](dashboard/theme.json) | Power BI styling |
| [Build guide](dashboard/docs/build-guide.md) | Reproduce three report pages and validate |
| [Editable Power BI project](dashboard/HUL_PowerBI_Project.zip) | Download, extract and open the PBIP in Power BI Desktop |
| [Dashboard gallery](dashboard/README.md) | Three actual Desktop screenshots and validation |
| [Static preview](dashboard/financial-summary.svg) | Verified-data summary; not a Power BI screenshot |
| [Executive case study](docs/executive-case-study.md) | Findings and business recommendations |

## Methodology and quality

Use FY25 restated and FY26 standalone continuing operations from the FY26 report (printed p.90). Ice Cream was demerged effective 1 December 2025; the FY25 originally reported figures are retained separately, not mixed with restated numbers. All amounts are INR crore; costs are positive expense magnitudes. Margins use operating revenue; segment shares use turnover. Eighteen arithmetic reconciliation checks (nine per year) yield zero variance. This is not an independent audit.

## Official sources

- [FY26 annual report](https://www.hul.co.in/files/annual-report-2025-26-single-page.pdf) — Financial Review, printed p.90.
- [FY25 annual report](https://www.hul.co.in/files/hul-integrated-annual-report-2024-25.pdf) — Results, historical context.

## Reproduce

Download the CSVs and follow the build guide for manual reproduction. The separate editable project uses embedded data, 28 measures, a year dimension and a disconnected profit bridge. Selected values, slicer behavior and visuals were checked in Power BI Desktop on 25 November 2026. The published ZIP contains the editable PBIP/PBIR project and embedded data. The workbook is a local supporting artifact. Native PBIX export and Power BI Service hosting are outside the published deliverables. FY25 growth is intentionally blank because no comparable FY24 is loaded. The segment scorecard may require scrolling. Download the published project ZIP, extract it and open the PBIP in Power BI Desktop. Aggregate annual data cannot establish causal cost drivers or reliable forecasts.

Independent AI-assisted educational portfolio project; not affiliated with HUL. Author: Sourav Gupta (MBA Business Analytics). [LinkedIn](https://www.linkedin.com/in/souravguptaanalyst/).
