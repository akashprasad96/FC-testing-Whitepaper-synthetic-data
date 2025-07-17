# FC-Testing Performance Analysis (Sanitized Demo)

> – North-American (NA) fulfillment centers lagged their EU peers in test-case throughput.  
> This repo shows how we uncovered root causes, quantified the gap, and rolled out fixes that are on track to close **>50 %** of the performance delta.

---

## 1. Business Problem

Amazon’s NA fulfillment-center (FC) testing throughput—measured in **Units-Per-Hour (UPH)**—trailed EU sites by nearly **60 %**.  
The gap throttled inventory availability and created labor-cost inefficiencies.  
Ops leadership requested a deep-dive analysis to:

1. **Pinpoint drivers** of the performance deficit.  
2. **Model scenarios** to close the gap.  
3. **Recommend actions** that could be operationalized within the fiscal year.

---

## 2. Analytical Approach

| Step | Description | Tools |
|------|-------------|-------|
| **Data Ingest** | Pulled 12 months of test-case logs (NA & EU) – 9 M+ rows. | **Amazon Redshift**, S3 |
| **Wrangling & EDA** | Cleaned, joined, and profiled the data; created derived KPIs. | **SQL**, **Python (pandas)** |
| **Visualization** | Built interactive dashboards for slice-and-dice analysis. | **QuickSight**, **Tableau** |
| **Stat Modeling** | Capacity models & what-if scenarios to project savings. | **Excel**, **Python (statsmodels)** |

---

## 3. Techniques Used

- **Root-Cause Analysis** – Pareto charts, cohort segmentation, and variance decomposition to isolate “ghosted” labor hours and site-type outliers.  
- **Capacity Modeling** – Simulated labor-code fixes and backlog restoration to forecast UPH uplift under multiple scenarios.  
- **Benchmarking** – Normalized NA vs EU workloads by site type (ARS, NONSORT, TSSL) to ensure apples-to-apples comparisons.  

---

## 4. Sanitized Key Findings

| Finding | Impact (Sanitized) |
|---------|--------------------|
| **Ghosted labor** in ADMIN bucket | Accounted for **~45 %** of NA’s UPH delta. |
| **Backlog starvation** at NONSORT/TSSL | Drove a **>90 %** drop in productivity during peak weeks. |
| **ARS sites** proved attainable targets | Achieved a **>130 %** RAW-UPH jump after buffer reinstatement. |

---

## 5. Recommended Actions & Status

1. **Create dedicated labor codes** for FC testing tasks.  
2. **Re-enable buffer storage** in NONSORT/TSSL to smooth work inflow.  
3. **Standardize pick & stow** SOPs using EU best practices.  

**Status:** White paper approved by senior ops leadership → Region-wide rollout of labor-hour audits and best-practice workshops in progress (Q3 2025).

---

## 6. Repo Contents

| Folder / File | Purpose |
|---------------|---------|
| `/visuals/` | Sanitized PNGs of trend charts, capacity models, and Pareto analyses. |
| `example_queries.sql` | Redshift SQL snippets (metric calculations, anomaly checks). |
| `backlog_model.xlsx` | Simplified Excel model for capacity scenarios (synthetic data). |
| `README.md` | You’re reading it. |
| `LICENSE` | MIT license for sanitized assets. |

---

## 7. Getting Started

1. Clone the repo  
   ```bash
   git clone https://github.com/yourhandle/fc-testing-analysis.git
