# GLP-1 RA Discontinuation and Risk of Major Adverse Cardiovascular Events

**Citation:** Xie Y, Choi T, Al-Aly Z. Glucagon-like peptide 1 receptor agonist discontinuation and risks of major adverse cardiovascular events in adults with type 2 diabetes: target trial emulation. *BMJ Medicine.* 2026;5(1):e002150. doi:10.1136/bmjmed-2025-002150. PMC13007077.

**Journal:** BMJ Medicine
**Access:** Open access via PMC (full text available)
**Search date:** 2026-05-11

---

## Brief Summary

Using the US Veterans Affairs (VA) healthcare database (n=333,687; GLP-1RA initiators n=132,551; sulfonylurea initiators n=201,136), this TTE characterised 16 prespecified GLP-1RA treatment strategies varying by duration, discontinuation, and interruption patterns over 3 years. Cardiovascular benefit (MACE reduction) accumulated with continuous use — continuous 3-year GLP-1RA use had the strongest reduction (IRR 0.82, 95% CI 0.78–0.85 vs sulfonylureas). Even brief discontinuation (0.5 years) increased MACE risk by 4% vs continued use, with progressive erosion of benefit with longer breaks. This is the first study to quantify the dose-time relationship between GLP-1RA continuity and cardiovascular protection.

---

## Methodology (Step-by-Step)

### Step 1 — Causal Question (Target Trial Specification)

| Component | Target Trial Specification | Emulation |
|---|---|---|
| **Population** | VA users with T2DM, no prior GLP-1RA or sulfonylurea in past year, no contraindications | Same — VA Corporate Data Warehouse 2017–2023 |
| **Strategies** | GLP-1RA vs sulfonylurea initiation; then 16 GLP-1RA sub-strategies by 6-month status (continue/discontinue/interrupt) | Pharmacy records every 6 months |
| **Assignment** | Random at enrolment; re-randomised every 6 months in GLP-1RA arm | New-user design; 6-month reassignment based on prescription fill status |
| **Follow-up** | 3 years | Same |
| **Outcomes** | 3-year cumulative incidence of MACE (MI + stroke + all-cause death) | ICD codes from VA inpatient/outpatient + Medicare |
| **Causal contrast** | ITT (primary); per-protocol (secondary) | Both estimands reported |

---

### Step 2 — Data Sources

- **US Department of Veterans Affairs Corporate Data Warehouse**
  - Period: 01 Jan 2017 – 31 Dec 2023
  - Domains: outpatient/inpatient encounters, outpatient pharmacy, laboratory results, vital signs, patient demographics, VA vital status
  - Linked to **Medicare data** (via VA Information Resource Center) to capture care outside VA
  - Area deprivation index (composite SES measure) from external source

- VA operates the largest nationally integrated US healthcare system: >9 million veterans, 1,380 facilities

---

### Step 3 — Eligibility Criteria

- VA users with type 2 diabetes
- Initiated GLP-1RA or sulfonylurea (first prescription — new-user design)
- No GLP-1RA or sulfonylurea use in the prior year
- No contraindications to either drug class
- ≥2 VA visits in year before enrolment
- Used VA outpatient pharmacy in year before enrolment

**Cohort size:**
- GLP-1RA initiators: n=132,551
- Sulfonylurea initiators: n=201,136
- Total: n=333,687

---

### Step 4 — Treatment Strategies (16 Pre-specified GLP-1RA Strategies)

Treatment status reassigned every **6 months** for up to 3 years (6 reassignment windows), generating 16 strategies:
- **Continuous use strategies**: GLP-1RA for 0.5, 1.0, 1.5, 2.0, 2.5, or 3.0 years then stop (or full 3 years)
- **Discontinuation strategies**: stop at 0.5, 1.0, or 2.0 years vs continued use
- **Interruption strategies**: stop for 0.5, 1.0, or 2.0 years then resume vs continued use
- All strategies compared against:
  1. Sulfonylurea reference group (primary)
  2. Continuous GLP-1RA use (secondary — to isolate discontinuation effect)

---

### Step 5 — Confounder Adjustment

**Inverse probability weighting (IPW):**
- At enrolment: propensity score for GLP-1RA vs sulfonylurea initiation
- Every 6 months: propensity score for treatment status (continue/discontinue/interrupt) conditional on current status
- Covariates at each timepoint: demographics, comorbidities, medications, lab values, BMI, healthcare utilisation, area deprivation index
- **Marginal structural models** (MSM) with stabilised IPW weights to handle time-varying confounding by indication

---

### Step 6 — Statistical Analysis

- **Primary estimand**: cumulative incidence risk ratio (IRR) at 1, 2, and 3 years for each strategy vs sulfonylureas
- **Secondary estimand**: IRR comparing discontinuation/interruption strategies vs continuous GLP-1RA
- **Discrete-time survival models** (complementary log-log) for cumulative incidence
- Bootstrap confidence intervals (500 iterations)
- Results presented as IRR + 95% CI at each annual timepoint

---

### Step 7 — Sensitivity Analyses

- Supplemental table S1: full target trial specification
- Multiple sensitivity analyses testing robustness of 6-month reassignment window
- Subgroup analyses by GLP-1RA agent class, baseline cardiovascular risk
- Per-protocol analysis in addition to ITT

---

## Key Results

**vs Sulfonylurea reference:**

| GLP-1RA Strategy | 3-year IRR (95% CI) |
|---|---|
| Continuous 3 years | **0.82 (0.78–0.85)** |
| Continuous 2.5 years, then stop | 0.85 (0.81–0.90) |
| Continuous 2.0 years, then stop | 0.93 (0.88–0.98) |
| Continuous 1.5 years, then stop | ~1.0 (NS) |
| Continuous 0.5 years, then stop | ~1.0 (NS) |

**vs Continuous GLP-1RA use:**

| Discontinuation duration | IRR (95% CI) |
|---|---|
| 0.5-year discontinuation | **1.04 (1.01–1.08)** |
| 1-year discontinuation | **1.14 (1.09–1.18)** |
| 2-year discontinuation | **1.22 (1.16–1.27)** |
| 0.5-year interruption | Increased (significant) |
| 1-year interruption | **1.12 (1.06–1.19)** |
| 2-year interruption | **1.16 (1.11–1.22)** |

**Key conclusions:**
- ≥2 years of continuous GLP-1RA use required for significant MACE reduction
- Even 0.5-year gaps erode benefit; longer gaps progressively increase risk
- Interrupted use (stop then restart) also reduces cumulative protection

---

## Strengths

- Largest dataset for this question (n=333,687; VA national)
- 16 pre-specified strategies with time-varying treatment classification — rigorous causal question
- Marginal structural models with IPW handle time-varying confounding
- Medicare linkage captures care outside VA (reduces outcome misclassification)
- New-user, active comparator design (GLP-1RA vs sulfonylurea)
- Open access; full methods in supplement table S1

## Limitations

- VA population predominantly male, older veterans — limited generalisability to women and younger adults
- Discontinuation reasons unobserved (side effects, cost, provider decision)
- 6-month reassignment windows may miss finer-grained temporal patterns
- Medicare linkage incomplete for some veterans
- Drug-specific analyses by GLP-1RA agent (liraglutide, semaglutide, etc.) not primary analysis
