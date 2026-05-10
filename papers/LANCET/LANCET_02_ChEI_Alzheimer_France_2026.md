# Long-term Effect of Discontinuing Anticholinesterase Treatment in Alzheimer's Disease

**Citation:** Lecerf S, Guinebretiere O, Bentegeac R, Gauthier V, Aymes E, Mekkaouif C, et al. Long-term effect of discontinuing anticholinesterase treatment on cognitive decline and mortality in Alzheimer's disease in France: a quasi-experiment and target trial emulation study. *Lancet Regional Health – Europe.* 2026;62:101607. doi:10.1016/S2666-7762(26)00019-0

**Journal:** The Lancet Regional Health – Europe
**Access:** Open access (full text and methods accessible)
**Search date:** 2026-05-11

---

## Brief Summary

In 2018, France withdrew reimbursement for cholinesterase inhibitors (ChEIs) in Alzheimer's disease, creating a natural quasi-experiment. This study emulated a "stop trial" using two French databases (BNA: n=7,319; Meotis: n=829), comparing patients who discontinued ChEIs after delisting vs those who continued. Discontinuation was associated with significantly accelerated cognitive decline: a 0.97-point greater MMSE decline at 1 year (95% CI 0.68–1.27), rising to 1.81 points at 4 years (0.91–2.71). No significant difference in mortality was observed over 5 years (RR 1.10, 0.95–1.29). The study argues for reconsidering France's 2018 delisting decision.

---

## Methodology (Step-by-Step)

### Step 1 — Causal Question (Target Trial Specification)

| Component | Target Trial Specification | Emulation |
|---|---|---|
| **Eligibility** | Age >18, AD diagnosis, MMSE >10, ChEI use in past 6 months, registered Aug 2017–Aug 2018 | Same — BNA and Meotis databases |
| **Strategies** | Discontinue ChEI vs continue ChEI at baseline | Classified by baseline medication records |
| **Assignment** | Random allocation | IPTW to emulate randomisation; quasi-experimental context of national delisting reduces confounding by indication |
| **Follow-up** | From assignment to death, loss to follow-up, or end (31 Jul 2024) | Same |
| **Outcomes** | MMSE trajectory (primary); all-cause mortality (secondary) | MMSE from clinical visits; mortality from Meotis/INSEE |
| **Causal contrast** | Intention-to-treat | Observational ITT analog |
| **Analysis** | ITT | Sequential trial emulation + IPTW |

---

### Step 2 — Data Sources

**BNA (Banque Nationale Alzheimer):**
- Established 2010; all patients attending memory centres in mainland France
- Systematically collected: demographics, education, living situation, diagnosis, MMSE scores, anti-dementia and psychotropic medications
- Used for: cognitive trajectory (primary outcome)
- ~84,943 patients with stable ChEI at baseline screened

**Meotis database:**
- Founded 1993; 32 memory centres in Nord/Pas-de-Calais region
- >140,000 patients by 2025; death date reliably retrieved via French INSEE platform
- Used for: mortality (secondary outcome)

---

### Step 3 — Eligibility and Baseline Definition

- Adults >18 years, AD diagnosis, MMSE ≥10, registered in BNA or Meotis 01 Aug 2017 – 01 Aug 2018
- ChEI use in the 6 months prior to baseline
- Baseline = first month meeting all eligibility criteria
- **Exclusion**: first follow-up visit >1 year after baseline (reduces uncertainty in inferred discontinuation date)
- Conservative discontinuation assumption: discontinuation date = visit immediately before first record of non-use (interval censoring)

---

### Step 4 — Treatment Assignment

- **Discontinuers**: not taking ChEI at baseline visit (policy-driven discontinuation)
- **Continuers**: still on ChEI at baseline
- **ITT principle**: patients remain in assigned group regardless of subsequent restart/stop behaviour
- Exchangeability assumed conditional on observed covariates (reinforced by quasi-experimental policy context)

---

### Step 5 — Sequential Trial Emulation

- **12 monthly trials emulated**: one starting each month from 01 Aug 2017 to 01 Aug 2018
- Each individual could participate in multiple trials (more statistically efficient than single time-zero)
- Data merged into single dataset; month of inclusion treated as baseline covariate
- Variance estimated by **bootstrapping** (500 samples) to account for repeated inclusions

---

### Step 6 — Confounder Adjustment (IPTW)

Covariates for propensity score (logistic regression):
- Age, sex, MMSE at baseline
- Follow-up setting (memory centre type: MRRC vs standard)
- Living arrangement (home vs nursing home)
- Education level (primary / secondary / post-secondary)
- Psychotropic medications: antidepressants, neuroleptics, anxiolytics, hypnotics, nootropics
- For mortality model additionally: antihypertensives, diabetes medications, lipid-lowering agents

**Stabilised IPTW weights**: inverse propensity × marginal probability of treatment group
**Balance check**: absolute SMD <0.1 required across all covariates

---

### Step 7 — Statistical Models

**Cognitive trajectory (BNA):**
- **Linear mixed-effects model** with random intercepts, applied to IPTW-weighted cohort
- Fixed effects: treatment group, follow-up time (quadratic spline, knot at 8 months), treatment × time interaction
- Participants without post-baseline MMSE included in model (no multiple imputation needed for longitudinal mixed models)
- MMSE trajectories predicted; between-group differences computed at 1, 2, 3, 4 years
- 95% CI via non-parametric bootstrapping (500 samples); p-values by percentile method or bootstrap t-test

**Mortality (Meotis):**
- **Pooled logistic regression**: treatment group + follow-up time (flexible: linear + quadratic) + treatment×time + baseline trial month
- Absolute risks estimated from model predictions
- 1–5 year risk ratios computed; 95% CI via bootstrapping (500 samples)

---

### Step 8 — Sensitivity Analyses

1. **DOMINO replication**: reproduced DOMINO RCT eligibility (MMSE 5–13) as positive control
2. **Single inclusion**: each patient included only at first eligible time (tests bias from multiple inclusions)
3. **Prodromal/mild AD subgroup**: restricted to MMSE >20
4. **Meotis cognitive replication**: repeated cognitive analysis in Meotis using IPTW, then IPCW to correct for loss-to-follow-up bias
5. **MNAR sensitivity (delta adjustment)**: pattern mixture model — shifted predicted missing outcomes in continuers group by constant Δ; identified Δ at which result becomes non-significant (tipping point analysis)

---

## Key Results

| Outcome | Time point | Estimate (95% CI) |
|---|---|---|
| MMSE difference (discontinuers − continuers) | 1 year | **+0.97 points (0.68–1.27)**, p<0.001 |
| MMSE difference | 4 years | **+1.81 points (0.91–2.71)**, p<0.001 |
| All-cause mortality RR | 5 years | 1.10 (0.95–1.29), NS |

- 7,319 BNA patients (6,142 continuers, 1,177 discontinuers); 829 Meotis patients (649 continuers, 180 discontinuers)
- Discontinuers were older (81.8 vs 80.3 years), lower MMSE (17.9 vs 19.1), more nursing home residents (9.2% vs 5.8%)
- After IPTW: groups well-balanced (SMD <0.1)
- Cognitive benefit equivalent to a **6–12 month delay** in MMSE decline

---

## Strengths

- **Unique quasi-experiment**: national delisting policy creates near-natural randomisation reducing confounding by indication
- Sequential TTE across 12 months: efficient and bias-resistant design
- IPTW + IPCW + sensitivity analyses (MNAR, DOMINO replication, single-inclusion)
- Long follow-up (up to 7 years from policy change)
- Two independent databases for two separate outcomes (reduces cross-outcome bias)
- Open access full text with TARGET-compliant specification table

## Limitations

- No specific drug names/doses in BNA (only drug class)
- Interval censoring of discontinuation date → conservative bias (underestimates treatment effect)
- Selection bias possible: patients most likely to stop were already in worse health (partially corrected by IPTW but residual confounding possible)
- No data on reasons for continuation (physician preference, patient adherence)
- Meotis sample small for mortality analysis (n=829)
- MMSE is a coarse cognitive measure; no neuropsychological battery data
