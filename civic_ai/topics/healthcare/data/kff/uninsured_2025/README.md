# KFF – State-Level Uninsured Impact Estimates (2025 Budget Reconciliation Law)

**Source:** Kaiser Family Foundation (KFF), “How Will the 2025 Reconciliation Law Affect the Uninsured Rate in Each State,” 2025.  
**Original Data URL:** https://www.kff.org/uninsured/how-will-the-2025-reconciliation-law-affect-the-uninsured-rate-in-each-state/  
**Derived From:** Congressional Budget Office (CBO) national coverage estimates allocated by KFF to states.  

## Files
- `kff_uninsured_impact_2025.csv` – Cleaned, standardized state-level table for all 50 states + DC.  
- `kff_uninsured_impact_2025.json` – JSON keyed by two-letter `state_code` for easy frontend/app use (to be added next).

## Columns (CSV)
- `state_code` – Two-letter postal code (e.g., `TX`).
- `geography` – State name.
- `medicaid_expansion_status` – `Adopted` or `Not Adopted`.
- `uninsured_increase` – Estimated number of people who become uninsured under the 2025 law.
- `uninsured_increase_ci` – Uncertainty range (as provided by KFF).
- `pp_increase` – Percentage-point increase in uninsured rate (law-only scenario).
- `uninsured_increase_ptc` – Estimated number who become uninsured if the law is implemented *and* enhanced ACA premium tax credits expire.
- `uninsured_increase_ptc_ci` – Uncertainty range for the combined scenario.
- `pp_increase_ptc` – Percentage-point increase in uninsured rate in the combined scenario.
- `medicaid_uninsured_increase` – Subset losing Medicaid coverage.
- `marketplace_uninsured_increase` – Subset losing ACA Marketplace coverage.
- `marketplace_uninsured_increase_ptc` – Marketplace losses if enhanced PTC expire.
- `medicare_other_uninsured_increase` – Subset affected under Medicare or other categories.

## Notes
- Numbers are **modeled estimates** based on CBO’s national projections, apportioned by KFF to states.
- “United States” national totals are excluded from the state table but available in the original KFF file.
- Use `uninsured_increase` for baseline impact messaging; use `pp_increase` for relative impact visuals.
- For “worst-case” subsidy expiration messaging, use the `*_ptc` columns.

## Suggested Repo Path
