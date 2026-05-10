# Low-Dose Aspirin for CVD Prevention in Giant Cell Arteritis — TTE

**Citation:** Beydon M, Hajage D, Guédon AF, Carrat F, et al. Low-dose aspirin for cardiovascular disease primary prevention in patients with giant cell arteritis. *JAMA Network Open.* 2026. doi:10.1001/jamanetworkopen.2026.[XXXX].

**Journal:** JAMA Network Open
**Access:** Full text available (JAMA Network Open — open access)
**Search date:** 2026-05-11

---

## Brief Summary

Patients with giant cell arteritis (GCA) face markedly elevated cardiovascular risk, but the benefit of low-dose aspirin in this population is unknown as RCTs are lacking. This population-based TTE used the **French National Health Data System (SNDS)** with a **clone-censor-weight (CCW)** approach — one of the few applied TTE studies to explicitly use cloning to handle grace periods. Among 14,528 incident GCA patients (2010–2022), low-dose aspirin was associated with reduced 1-year MACE (RR 0.86, 95% CI 0.75–0.96; RD −0.54%), but increased major hemorrhage (RR 1.29, 1.05–1.53; RD +0.51%). At 3 years, MACE benefit persisted (RD −1.08%) with no difference in hemorrhage. The benefit was more pronounced in women and diabetic patients.

---

## Methodology (Step-by-Step)

### Step 1 — Causal Question (Target Trial Specification)

| Component | Specification |
|---|---|
| **Population** | Adults ≥50 years with incident GCA (2010–2022), no prior CVD, no antiplatelet/anticoagulant use at diagnosis |
| **Intervention** | Initiation of low-dose aspirin (≤100 mg/day) within 14 days of GCA diagnosis |
| **Comparator** | No aspirin initiation (control group) |
| **Primary outcome** | MACE: composite of ischemic stroke + MI + all-cause mortality |
| **Secondary outcomes** | Major hemorrhage |
| **Follow-up** | 1 year (primary); 3 years (secondary) |
| **Causal contrast** | Intention-to-treat (via cloning) |

---

### Step 2 — Data Sources

- **French National Health Data System (SNDS / PMSI)**
  - Population-based: covers >99% of French population (~67 million)
  - Includes: hospital stays (PMSI), outpatient consultations, drug dispensing (pharmacy claims), long-term disease registry, vital status
  - GCA identified by: ICD-10 code M31.5 (giant cell arteritis) + corticosteroid dispensing (as diagnostic confirmation proxy)
  - Period: 2010–2022
  - Analysis: Nov 2024 – Jun 2025

---

### Step 3 — Eligibility Criteria

- Age ≥50 years at GCA diagnosis
- Incident GCA (no prior GCA code in 5-year lookback)
- No prior CVD event (MI, stroke, peripheral arterial disease, coronary revascularisation) in 5-year lookback
- No antiplatelet or anticoagulant use in 6 months before GCA diagnosis
- No contraindications to aspirin (e.g., active GI bleeding)

**Final sample:** N=14,528
- Aspirin initiators: 5,220 (35.9%)
- Non-initiators: 9,308 (64.1%)
- Median age: 74 years (IQR 67–80); 72% female

---

### Step 4 — Clone-Censor-Weight (CCW) Design

This study explicitly used **cloning** to handle the **14-day grace period** for aspirin initiation:

**Step 4a — Cloning:**
- Each patient **cloned** (duplicated) at GCA diagnosis
- Clone A assigned to aspirin initiation strategy
- Clone B assigned to no-aspirin strategy
- Both clones are initially compatible with both strategies at time zero

**Step 4b — Censoring:**
- Clone A censored if patient has not initiated aspirin by day 14 (deviates from assigned strategy)
- Clone B censored if patient initiates aspirin within 14 days (deviates from assigned strategy)
- Censoring is **artificial** (induced by the design)

**Step 4c — Weighting (IPCW):**
- **Inverse probability of censoring weighting (IPCW)** applied to correct for selection bias induced by artificial censoring
- Propensity score for remaining uncensored at each time point estimated by logistic regression
- Covariates: age, sex, GCA manifestations (cranial vs large vessel), corticosteroid dose at diagnosis, comorbidities (hypertension, diabetes, dyslipidaemia, CKD), calendar year, treating physician specialty, SES proxy (CMU-C complementary health insurance)

This design avoids immortal-time bias that would arise from classifying patients as aspirin users/non-users based on what they actually took post-baseline.

---

### Step 5 — Statistical Analysis

- **Cause-specific hazard models** (Cox) for time-to-event outcomes
- **Relative risk (RR)** and **risk difference (RD)** on cumulative incidence scale
- Estimated at 1 year and 3 years
- 95% CI via bootstrap

---

### Step 6 — Subgroup Analyses

Pre-specified subgroups:
- **Sex** (women vs men) — cardiovascular risk differs
- **Diabetes at GCA diagnosis** — aspirin benefit may be greater
- **GCA manifestation type** (cranial vs large vessel involvement)
- **Age group** (<70, 70–79, ≥80)
- **Calendar period** (2010–2015 vs 2016–2022) — changing GCA management practices

---

### Step 7 — Sensitivity Analyses

- Varying grace period (7 days vs 14 days vs 30 days)
- Restricting to biopsy-confirmed GCA (subset)
- Competing-risk analysis (treating non-CVD death as competing event for MACE)
- Varying definition of "low-dose aspirin" (≤75 mg vs 76–100 mg)

---

## Key Results

**At 1 year:**

| Outcome | RR (95% CI) | RD (95% CI) |
|---|---|---|
| **MACE** | **0.86 (0.75–0.96)** | **−0.54% (−0.99% to −0.12%)** |
| All-cause mortality | Reduced | RD −0.43% (−0.77% to −0.10%) |
| **Major hemorrhage** | **1.29 (1.05–1.53)** | **+0.51% (0.13% to 0.91%)** |

**At 3 years:**

| Outcome | RD (95% CI) |
|---|---|
| MACE | **−1.08% (−1.77% to −0.41%)** |
| Major hemorrhage | No significant difference |

**Subgroups with more pronounced MACE benefit at 1 year:**
- Women: RD −0.78% (−1.29% to −0.25%)
- Diabetes: RD −2.23% (−3.48% to −1.02%)

---

## Strengths

- **Clone-censor-weight design**: one of few applied TTE studies to use cloning — methodologically exemplary, avoids immortal-time bias from grace-period aspirin initiation
- Population-based French SNDS: >99% coverage, eliminates selection bias
- Both absolute (RD) and relative (RR) effect measures at 1 and 3 years
- Pre-specified sex/diabetes subgroups — clinically actionable heterogeneity
- Addresses a genuine clinical evidence gap (no RCTs in GCA)

## Limitations

- GCA diagnosis based on ICD codes + corticosteroid use — some misclassification possible (no biopsy confirmation for all)
- Aspirin dose and adherence captured only through pharmacy dispensing
- Confounding by indication possible (clinicians may preferentially prescribe aspirin to patients perceived as higher CV risk)
- IPCW may not fully correct for unmeasured confounders (e.g., GCA severity, inflammatory markers, CRP)
- Major hemorrhage endpoint: GI vs intracranial hemorrhage not distinguished in primary analysis
- 1-year follow-up short for a chronic autoimmune disease requiring prolonged treatment
