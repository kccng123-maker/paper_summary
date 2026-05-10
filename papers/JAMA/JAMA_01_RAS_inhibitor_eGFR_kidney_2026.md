# Discontinuation of RAS Inhibitors After Acute eGFR Decline

**Citation:** Ku E, Tangri N, Brar R, McCulloch CE, et al. Discontinuation of RAS Inhibition After an Acute Decline in Estimated Glomerular Filtration Rate. *JAMA Network Open.* 2026. doi:10.1001/jamanetworkopen.2026.[XXXX].

**Journal:** JAMA Network Open
**Access:** Full text available (JAMA Network Open — open access)
**Search date:** 2026-05-11

---

## Brief Summary

RAS inhibitors (RASIs: ACE inhibitors and ARBs) slow CKD progression but are frequently discontinued when an acute eGFR decline occurs after initiation. Using a TTE approach in 4,233 patients in Manitoba, Canada who had ≥15% eGFR decline after starting a RASI, discontinuers (33.3%) had significantly higher risk of ESKD (HR 1.74, 95% CI 1.28–2.38) and death (HR 1.23, 1.07–1.41) compared with continuers. No significant difference in MACE (HR 1.13, 0.99–1.28) or acute kidney injury (HR 1.11, 0.90–1.37). Results support continuing RASI despite acute eGFR dips and call for strategies to improve RASI persistence.

---

## Methodology (Step-by-Step)

### Step 1 — Causal Question (Target Trial Specification)

| Component | Specification |
|---|---|
| **Population** | Adults ≥18 years receiving a new RASI prescription who subsequently had ≥15% eGFR decline within 90 days of prescription |
| **Intervention** | Discontinuation of RASI (no refill within 90 days of eGFR decline) |
| **Comparator** | Continuation of RASI (refill within 90 days) |
| **Primary outcomes** | ESKD or death |
| **Secondary outcomes** | MACE (MI, heart failure, stroke, CV mortality); acute kidney injury (AKI) |
| **Follow-up** | 180 days after the eGFR decline event |
| **Causal contrast** | Intention-to-treat |

---

### Step 2 — Data Sources

- **Manitoba Centre for Health Policy (MCHP)** electronic health records
- Linked to: provincial vital statistics (mortality), provincial pharmacy records, provincial laboratory data (serum creatinine/eGFR)
- Coverage: entire province of Manitoba, Canada — near-universal population coverage
- Study period: 01 Jan 2008 – 31 Dec 2021
- Data analysis period: 14 Jan 2024 – 22 Jan 2026

---

### Step 3 — Eligibility Criteria

- Adults ≥18 years
- New RASI prescription between 01 Jan 2008 – 31 Dec 2021 (new-user design: no RASI use in prior 365 days)
- ≥15% decline in eGFR within 90 days of the first RASI prescription (based on serum creatinine lab results)
- At least one eGFR measurement before and after RASI initiation within 90 days

**Final sample:** n=4,233 patients
- Discontinuers: 1,411 (33.3%)
- Continuers: 2,822 (66.7%)
- Mean age: 64.6 years (SD 16.2); 51.1% male

---

### Step 4 — Time Zero and Treatment Classification

- **Time zero** = date of eGFR decline documentation (≥15% below baseline within 90 days of RASI initiation)
- **Discontinuation**: no RASI prescription refill within 90 days after the eGFR decline event
- **Continuation**: RASI prescription refilled within 90 days
- **Follow-up**: from time zero to outcome event, death, disenrollment, or 180 days

---

### Step 5 — Confounder Adjustment

- **Propensity score matching (1:2 matching — discontinuers:continuers)**
- Propensity score estimated by logistic regression
- Covariates: age, sex, comorbidities (diabetes, hypertension, CKD stage, heart failure, prior MACE), baseline eGFR, magnitude of eGFR decline, medications (diuretics, NSAIDs, contrast agents), healthcare utilisation
- Balance assessed post-matching by SMD (target <0.1)

---

### Step 6 — Statistical Analysis

- **Cox proportional hazards models** — hazard ratios (HR) with 95% CI
- ITT approach: treatment group fixed at time zero regardless of subsequent RASI status changes
- Outcomes at 180 days follow-up
- Analyses performed using matched cohort

---

### Step 7 — Sensitivity Analyses

- Varying eGFR decline threshold (e.g., ≥20%, ≥30%)
- Extended follow-up beyond 180 days
- Subgroup analyses by CKD stage, diabetes status, degree of eGFR decline

---

## Key Results

| Outcome | HR (95% CI) | Significance |
|---|---|---|
| **ESKD or death (composite)** | — | — |
| Death | **1.23 (1.07–1.41)** | Significant |
| ESKD | **1.74 (1.28–2.38)** | Significant |
| MACE | 1.13 (0.99–1.28) | NS (borderline) |
| AKI | 1.11 (0.90–1.37) | NS |

- Discontinuers had substantially higher risk of hard kidney and mortality outcomes
- No significant difference in MACE or AKI — suggests RASI discontinuation does not protect against further acute kidney events
- 33% discontinuation rate highlights the clinical problem's scale

---

## Strengths

- Population-based EHR from Manitoba with near-universal coverage — minimal selection bias
- New-user, propensity-score matched TTE design
- Linked provincial lab data allows precise eGFR-based eligibility and exposure definition
- Multiple hard outcomes (ESKD, death, MACE, AKI) comprehensively assessed
- 14-year study period (2008–2021): large sample despite eligibility restrictions

## Limitations

- Short follow-up (180 days): may underestimate long-term ESKD impact of discontinuation
- Discontinuation defined by prescription records — actual consumption unknown
- Reasons for discontinuation not captured (provider vs patient decision; symptom-driven vs precautionary)
- Manitoba population may not be fully generalisable to other health systems
- Propensity score matching may not control for unmeasured confounders (e.g., severity of acute illness driving eGFR decline)
