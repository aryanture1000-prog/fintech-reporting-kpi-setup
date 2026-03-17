# Fintech Reporting & KPI Setup

A complete, automated financial reporting system for Series A fintech startups — built from the ground up for founders and CFOs who need investor-ready reports but don't have time to build the infrastructure themselves.

Takes a startup from zero structured tracking to three fully automated monthly reports in one setup.

---

## Live Demo

> [View the full system walkthrough](https://aryanture1000-prog.github.io/fintech-reporting-kpi-setup)

---

## What's Delivered

### 1. KPI Framework (16 metrics across 4 categories)

| Category | Metrics |
|---|---|
| Growth | MRR, ARR, MoM Revenue Growth, New Clients, Transaction Volume |
| Unit Economics | CAC by channel, LTV, LTV:CAC Ratio, Gross Margin, Payback Period |
| Risk & Runway | Net Burn Rate, Cash Runway, Burn Multiple, Churn Rate |
| Operations | Transaction Success Rate, FX Exposure, Cost per Transaction, NRR |

### 2. Three Automated Reports

**Weekly Operations Pulse** — for the founding team every Monday
- Revenue vs prior week (USD + EUR split)
- Transaction volume and success rate
- Burn flash — week's cash out vs monthly target

**Monthly Leadership Report** — for CEO, CFO, and board
- Full P&L summary normalized to USD
- All 16 KPIs with RAG (Red/Amber/Green) status
- 3 key findings + 3 recommended actions
- Budget vs actual by department with overspend flags

**Monthly Investor Update Package** — for Series A investors
- MRR bridge (new, expansion, churned, net new)
- Unit economics snapshot — LTV:CAC, payback, gross margin
- Runway and burn statement
- FX exposure summary for USD-denominated fund investors

---

## How the Automation Works

```
Step 1 — Data Pull
         Python connects to Stripe API + QuickBooks API
         All transactions pulled automatically at month-end

Step 2 — FX Normalization
         All EUR amounts converted to USD at ECB reference rates
         Original EUR figures preserved for audit trail

Step 3 — KPI Calculation
         All 16 KPIs calculated from clean, normalized data
         Each compared to prior month and target
         RAG status assigned programmatically

Step 4 — Report Generation
         3 reports output as formatted Excel + PDF
         Ready to send — zero manual formatting

Total runtime: under 15 minutes
Replaces: 2 full working days per month
```

---

## Tech Stack

- Python 3.10+
- pandas — data pipeline and KPI calculation
- openpyxl — Excel report generation
- reportlab — PDF generation
- Stripe API — revenue and transaction data
- QuickBooks API — expense and ledger data
- exchangerate-api — live FX normalization

---

## How to Use

```bash
git clone https://github.com/aryanture1000-prog/fintech-reporting-kpi-setup.git
cd fintech-reporting-kpi-setup
pip install -r requirements.txt
```

Configure your API keys and budget targets in `config.py`, then run:

```bash
python generate_reports.py --month 2025-03
```

Three reports saved to `/output/` — ready to send.

---

## Customization

- Add or remove KPIs from the framework in `kpi_config.py`
- Adjust budget targets per department in `config.py`
- Change report recipients and delivery format
- Connect additional data sources — SQL, CSV, or any REST API
- White-label report branding with your company logo and colors

---

## Impact

| Before | After |
|---|---|
| 2 days manual work per month | 15 minutes per run |
| No structured KPI tracking | 16 metrics tracked automatically |
| Investors asking for data mid-month | Investor package ready on day 1 |
| EUR and USD figures unreconciled | All amounts normalized to USD |
| No RAG visibility on performance | Every metric flagged automatically |

---

## Services

This system is part of my freelance financial data practice. I build end-to-end financial reporting infrastructure, KPI frameworks, and automation pipelines for fintech startups globally.

**Available for freelance engagements.**
Connect on [LinkedIn](https://linkedin.com/in/aryan-kasture) or reach out via GitHub.

---

## Author

**Aryan Kasture**
Financial Data Automation & Python Specialist
Mumbai, India

> Helping fintech startups turn messy financial data into clear decisions.
