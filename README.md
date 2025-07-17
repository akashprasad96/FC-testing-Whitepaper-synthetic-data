# FC-Testing Performance Analysis (Sanitized Demo)

## 1. Business Problem
Amazon’s NA fulfillment-center (FC) testing throughput—measured in Units-Per-Hour (UPH)—trailed EU sites.  
The gap throttled inventory availability and created labor-cost inefficiencies.  
Ops leadership requested a deep-dive analysis to:  
1. Pinpoint drivers of the performance deficit.  
2. Model scenarios to close the gap.  
3. Recommend actions that could be operationalized within the fiscal year.

## 2. Techniques Used
- **Root-Cause Analysis** – Visualizations and calculated fields to isolate “ghosted” labor hours and site-type outliers.  
- **Capacity Modeling** – Simulated labor-code fixes and backlog restoration to forecast UPH uplift under multiple scenarios.  
- **Benchmarking** – Normalized NA vs EU workloads by site type (ARS, NONSORT, TSSL) to ensure apples-to-apples comparisons.

## 3. Recommended Actions & Status
1. Create dedicated labor codes for FC testing tasks.  
2. Re-enable buffer storage in NONSORT/TSSL to smooth work inflow.  
3. Standardize pick & stow SOPs using EU best practices.  

**Status:** White paper approved by senior ops leadership → Region-wide rollout of labor-hour audits and best-practice workshops in progress (Q3 2025).
