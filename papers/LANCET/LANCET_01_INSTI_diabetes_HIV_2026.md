# Incident Diabetes After Switching to INSTIs in People with HIV

**Citation:** Hwang YJ, Lesko CR, Brown TT, Alexander GC, Althoff KN, Zalla LC, et al. Incident diabetes after switching to integrase strand transfer inhibitors in people with HIV in the USA and Canada: a cohort study. *Lancet HIV.* 2026;13(5):e297–e305. doi:10.1016/S2352-3018(25)00335-2

**Journal:** The Lancet HIV
**Access:** Abstract accessible; full text paywalled (subscription required)
**Search date:** 2026-05-11

---

## Brief Summary

This target trial emulation using pooled data from 27 longitudinal HIV cohorts in the USA and Canada examined whether switching to integrase strand transfer inhibitors (INSTIs) — now the dominant antiretroviral class — increases incident diabetes in ART-experienced people with HIV. Switching from protease inhibitors (PIs) to INSTIs conferred a 38% higher diabetes risk (HR 1.38, 95% CI 1.06–1.80), concentrated in the first 2 years post-switch and not fully explained by weight gain. Switching from NNRTIs to INSTIs showed no significant increase (HR 1.10, 0.87–1.39). This is one of the largest multi-cohort TTE studies in HIV pharmacoepidemiology.

---

## Methodology (Step-by-Step)

### Step 1 — Causal Question (Target Trial Specification)

| Component | Specification |
|---|---|
| **Population** | ART-experienced adults ≥18 years with HIV, no diabetes, on NNRTI or PI for ≥180 days (2016–2022), never previously used an INSTI |
| **Intervention** | Switch to an INSTI |
| **Comparator** | Continue current NNRTI or PI (two separate comparisons) |
| **Outcome** | Incident diabetes (primary) |
| **Follow-up** | Up to 5 years from switching/continuing encounter |
| **Causal contrast** | Per-protocol (time-varying treatment classification) |

---

### Step 2 — Data Sources

- **27 longitudinal HIV cohorts** from the USA and Canada (multi-site, prospective observational)
- Individual-level data pooled across cohorts via the NA-ACCORD (North American AIDS Cohort Collaboration on Research and Design) infrastructure
- Data period: 2016–2022
- Variables: clinical encounters, antiretroviral prescriptions, diabetes diagnoses, laboratory results (glucose, HbA1c), weight measurements

---

### Step 3 — Eligibility Criteria

- Adults ≥18 years with HIV
- Currently on NNRTI or PI for ≥180 days
- No prior INSTI use
- No diabetes diagnosis at baseline
- Enrolled in participating cohort 2016–2022

---

### Step 4 — Time Zero and Treatment Classification

- **Time zero** = clinical encounter at which patient either switched to INSTI or continued NNRTI/PI
- **Sequential trial emulation**: eligible individuals could contribute at multiple encounters (nested trials at each encounter)
- **Intervention group**: switched from NNRTI → INSTI, or from PI → INSTI
- **Comparator group**: continued NNRTI, or continued PI
- Two separate emulations: (1) NNRTI-experienced switchers vs continuers; (2) PI-experienced switchers vs continuers

---

### Step 5 — Confounder Adjustment

- **Inverse probability of treatment weighting (IPTW)** with time-varying weights
- Baseline and time-varying covariates included:
  - Age, sex, race/ethnicity
  - CD4 count, HIV RNA viral load
  - BMI and weight trajectory
  - Comorbidities (hepatitis B/C, cardiovascular disease)
  - Current ART regimen specifics
  - Calendar year, cohort site
- Stabilised weights to control for extreme weighting

---

### Step 6 — Statistical Analysis

- **Weighted Cox proportional hazards regression** with robust variance estimators
- **HR with 95% CI** as primary effect measure
- Stratified by prior ART class (NNRTI vs PI)
- **Time-interaction analysis**: tested whether HR varied by time since switch (0–2 years vs >2 years; p-interaction reported)
- **Mediation analysis**: assessed whether weight gain in year 1 mediated the INSTI→diabetes association
  - Sensitivity analysis: restricted to those with <5% weight gain in year 1

---

### Step 7 — Sensitivity Analyses

1. Restricted to participants with weight data available (to assess mediation)
2. Sensitivity restricted to those with <5% weight gain in first year after switch
3. Cohort-stratified analyses (site-specific estimates)
4. Restriction by specific INSTI agent (dolutegravir, bolutegravir, elvitegravir, raltegravir)

---

## Key Results

| Comparison | Adjusted HR (95% CI) | Interpretation |
|---|---|---|
| PI → INSTI switch | **1.38 (1.06–1.80)** | Significant 38% higher diabetes risk |
| NNRTI → INSTI switch | 1.10 (0.87–1.39) | Non-significant |
| PI → INSTI, years 0–2 | **1.67 (1.21–2.30)** | Risk concentrated early |
| PI → INSTI, years >2 | 1.08 (0.75–1.57) | Risk attenuates after 2 years |
| PI → INSTI, weight gain <5% | **1.37 (1.02–1.84)** | Risk persists without weight gain |

- 13,071 unique participants; 2,702 INSTI-switch encounters from NNRTIs; 1,714 from PIs
- Weight gain did not fully explain the PI→INSTI diabetes risk

---

## Strengths

- **27 cohorts pooled**: largest multi-cohort TTE in HIV pharmacoepidemiology; excellent statistical power for a rare outcome
- Sequential TTE design: avoids immortal-time bias and prevalent-user bias
- Time-varying IPTW: accounts for time-varying confounding
- Mediation analysis disentangles weight-mediated vs weight-independent effects
- Both NNRTI-to-INSTI and PI-to-INSTI comparisons allow class-specific inference

## Limitations

- Full text paywalled; supplement not accessible for additional sensitivity analysis details
- Diabetes ascertainment relies on clinical diagnosis/lab codes — may miss subclinical cases
- Cohort data: some missing weight and lab data across sites
- Cannot exclude residual confounding by unmeasured factors (e.g., diet, physical activity)
- Most participants are male (HIV cohort demographics)
