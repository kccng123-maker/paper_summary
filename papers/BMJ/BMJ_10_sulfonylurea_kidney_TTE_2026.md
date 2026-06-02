# Comparative Effectiveness of Sulfonylureas on Kidney Outcomes in Adults with Type 2 Diabetes: A Target Trial Emulation

**Citation:** Sklepinski S, Ratzki-Leewing AA, Herrin J, et al. Comparative effectiveness of sulfonylureas on kidney outcomes in adults with type 2 diabetes and moderate cardiovascular risk: a target trial emulation. *BMJ Open Diabetes Research & Care.* 2026;14(3):e005775. doi:10.1136/bmjdrc-2025-005775. Published online 21 May 2026. [Open Access]

---

## Brief Summary

This large US target trial emulation compared head-to-head the three most commonly prescribed second-generation sulfonylureas — glimepiride, glipizide, and glyburide — on kidney outcomes in approximately 295,000 adults with type 2 diabetes (T2D) at moderate cardiovascular risk and without baseline chronic kidney disease (CKD). Using US commercial and Medicare claims data (2014–2021) with super learner propensity score weighting, the study found that glyburide was associated with a modestly lower risk of kidney complications (HR 0.84 vs glimepiride; HR 0.81 vs glipizide for the primary kidney composite) despite carrying a substantially higher risk of severe hypoglycemia. Glipizide was associated with modestly higher kidney risk versus glimepiride across all endpoints. These hypothesis-generating findings suggest important within-class pharmacological differences that have been largely overlooked, given the absence of dedicated postmarketing kidney outcomes trials for these agents. The authors conclude that glimepiride may be the safest overall sulfonylurea given its intermediate kidney profile and lowest hypoglycemia risk.

---

## Methodology Step-by-Step

### Step 1: Causal Question as PICO Target Trial Specification

| Component | Specification |
|---|---|
| **Population** | Adults ≥21 years with T2D at moderate cardiovascular risk (annualized claims-based MACE risk 1–5%), without baseline CKD stage 3+, no prior sulfonylurea use (12-month washout) |
| **Intervention** | Initiation of glimepiride |
| **Comparator** | Initiation of glipizide OR glyburide (three pairwise comparisons) |
| **Outcome** | Primary: incident CKD stage 3 or worse (including kidney failure + kidney replacement therapy); Secondary: CKD stage 3–4, kidney failure, all-cause mortality, composite; hypoglycemia requiring ED/hospital |
| **Time horizon** | Up to 9 years (index 2014–2021, follow-up to Dec 31, 2022) |
| **Estimand** | Intention-to-treat effect of sulfonylurea class initiation |

### Step 2: Data Sources

| Element | Detail |
|---|---|
| **Database** | Optum Labs Data Warehouse (OLDW) — commercial + Medicare Advantage plans, linked to 100% traditional Medicare Parts A/B/D claims |
| **Country** | United States |
| **Period** | January 2014 – December 2022 |
| **N (weighted cohort)** | 295,092 (glimepiride n=134,926; glipizide n=145,984; glyburide n=14,182) |
| **Linkages** | OLDW + Social Security Administration Death Master File; EHR-linked; Medicare beneficiary records |

### Step 3: Eligibility Criteria

- Age ≥21 years with T2D
- First fill for glimepiride, glipizide, or glyburide (new-user design; 12-month washout without sulfonylurea)
- Second fill of same drug within 30 days (to confirm adherence)
- No type 1 diabetes, metastatic cancer, pregnancy, meglitinide/insulin use at baseline
- No CKD stage 3+ at baseline (ICD-9/10 codes + procedural codes for KRT)
- Moderate cardiovascular risk: annualized MACE risk 1–5% (claims-based estimator)
- No concurrent OLDW + Medicare coverage on index date

### Step 4: Time Zero and Treatment Classification

- **Time zero**: Date of first sulfonylurea prescription fill (index date)
- **Treatment**: Assigned to glimepiride, glipizide, or glyburide based on first fill
- **New-user design**: 12-month baseline period before index date; 30-day grace period for second fill confirmation

### Step 5: Confounder Adjustment

| Element | Detail |
|---|---|
| **Method** | Inverse probability of treatment weighting (IPTW) using propensity scores estimated via SuperLearner ensemble method |
| **SuperLearner algorithms** | Diverse binomial prediction algorithms (cross-validated ensemble) |
| **Stabilized weights** | Stabilized IPTW (propensity × marginal drug frequency); no trimming |
| **Balance check** | Standardized mean differences (SMD) <0.10 across all pairwise comparisons after weighting |
| **Covariates** | Demographics (age, sex, race/ethnicity, US census region); clinical comorbidities; concomitant medications (metformin, TZDs, GLP-1RA, SGLT2i, DPP4i, etc.); baseline-period variables |

### Step 6: Statistical Analysis

| Element | Detail |
|---|---|
| **Primary model** | Propensity score-weighted proportional hazards models (one per outcome) |
| **Effect measure** | Hazard ratios (HR) with 95% CIs (simulation-based) |
| **Cumulative incidence** | IPTW Kaplan-Meier method; pseudo-values with isotonic regression for monotonicity |
| **Predicted probabilities** | Cumulative incidence at 1, 2, and 3 years post-initiation |
| **Framework** | Intention-to-treat (ITT) — follow to death, disenrollment, or Dec 31, 2022 |
| **Proportional hazards** | Tested using Grambsch-Therneau test |

### Step 7: Sensitivity Analyses

1. **As-treated (censoring on discontinuation)**: Patients censored on gap >30 days after dispensed pill count
2. **As-treated (censoring on switch/add-on)**: Additionally censored on addition of another glucose-lowering drug
3. **Falsification endpoints**: Hospitalizations for pneumonia and appendicitis (prespecified; no drug differences expected or found)

---

## Key Results Table

| Comparison | Primary Kidney Composite HR (95% CI) | CKD Stage 3–4 HR (95% CI) | Kidney Failure HR (95% CI) | All-Cause Mortality HR (95% CI) | Severe Hypoglycemia HR (95% CI) |
|---|---|---|---|---|---|
| Glipizide vs Glimepiride | 1.04 (1.00–1.07) | 1.04 (1.01–1.07) | 1.09 (1.02–1.16) | 1.06 (1.03–1.09) | — |
| Glyburide vs Glimepiride | **0.84 (0.76–0.92)** | **0.80 (0.72–0.89)** | NS | NS | 1.22 (1.05–1.42) |
| Glyburide vs Glipizide | **0.81 (0.73–0.89)** | **0.77 (0.70–0.86)** | NS | 0.90 (0.85–0.96) | 1.47 (1.27–1.71) |

*1-year incidence: glimepiride 2.1%, glipizide 2.2%, glyburide 1.8% (primary composite); 3-year: 5.0%, 5.2%, 4.2%.*

---

## Strengths and Limitations

### Strengths
- First head-to-head comparison of all three US second-generation sulfonylureas on kidney outcomes
- Large, geographically and demographically diverse US population (commercial + Medicare Advantage + traditional Medicare)
- Rigorous TTE framework with new-user design, 12-month washout, ITT analysis
- SuperLearner ensemble propensity scoring with balance verification (SMD <0.10)
- Prespecified falsification endpoints to evaluate unmeasured confounding
- Long follow-up (up to 9 years); preregistered (NCT05214573)

### Limitations
- Observational design — residual unmeasured confounding and bias by indication possible (e.g., clinician preferences not captured)
- Claims-based outcome ascertainment may misclassify CKD stage
- Predominantly non-Hispanic White cohort (76–78%) — generalizability limited
- Small glyburide arm (n=14,182) limits precision for some subgroup analyses
- Sensitivity analyses showed larger effect sizes for glyburide vs comparators, suggesting some residual confounding
- Restricted to moderate cardiovascular risk — cannot generalize to high-risk T2D populations
- Mechanism for glyburide's apparent kidney benefit is unclear and may reflect residual confounding

---

*File created: 2026-06-02. Time window: 7-day Google Scholar filter (published 21 May 2026, 12 days before index date; included under 14-day fallback for BMJ family journals).*
