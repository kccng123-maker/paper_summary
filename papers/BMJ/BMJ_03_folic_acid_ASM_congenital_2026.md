# Timing of High-Dose Folic Acid and Risk of Major Congenital Anomalies in Women on Antiseizure Medications

**Citation:** Sun Y, Alvestad S, Cohen JM, Igland J, Gilhus NE, Vegrim HM, Tomson T, Christensen J, Leinonen MK, Gissler M, Zoega H, Razaz N, Dreier JW, Bjørk M-H. Timing of high-dose folic acid supplementation in the periconceptional period among women taking antiseizure medications and risk of major congenital anomalies: a target trial emulation. *Journal of Neurology, Neurosurgery & Psychiatry (JNNP).* 2026. doi:10.1136/jnnp-2025-337395.

**Journal:** JNNP (BMJ Publishing Group)
**Access:** Open access (CC BY-NC 4.0); full text accessible
**Search date:** 2026-05-11

---

## Brief Summary

Women taking antiseizure medications (ASMs) face elevated risk of major congenital anomalies (MCAs) in offspring, and high-dose folic acid (4–5 mg/day) is recommended periconceptionally — but evidence for this recommendation has been limited and inconsistent. This sequential TTE used nationwide Nordic register data from Denmark, Iceland, Norway, and Sweden (1997–2020; n=18,255–13,619 pregnancies by period) to evaluate folic acid initiation timing. Initiation **1–12 weeks before pregnancy** was associated with a 45% relative risk reduction in MCA (RR 0.55, 95% CI 0.25–0.91; ARD −2.2 percentage points). Initiation after pregnancy onset conferred no benefit (RR 1.27, 0.94–1.64). This is the most rigorous evidence to date supporting preconception-only timing of high-dose folic acid in ASM users.

---

## Methodology (Step-by-Step)

### Step 1 — Causal Question (Target Trial Specification)

| Component | Specification |
|---|---|
| **Population** | Pregnant women using ASMs (Denmark, Iceland, Norway, Sweden; 1997–2020) |
| **Intervention** | Initiation of high-dose folic acid (4 or 5 mg/day) within 1 week of inclusion |
| **Comparator** | Non-initiation of high-dose folic acid |
| **Outcomes** | Major congenital anomalies (MCAs) diagnosed before 1 year of age in offspring |
| **Three exposure windows** | (1) 13–52 weeks before pregnancy onset; (2) 1–12 weeks before pregnancy onset; (3) 1–12 weeks after pregnancy onset |
| **Causal contrast** | Risk difference (RD) and risk ratio (RR) — absolute and relative scales |

---

### Step 2 — Data Sources

**Four nationwide Nordic registers:**
- **Denmark**: Medical Birth Register, National Patient Register, National Prescription Register
- **Iceland**: equivalent national health registers
- **Norway**: Medical Birth Registry, Norwegian Patient Registry, Norwegian Prescription Database
- **Sweden**: Medical Birth Register, National Patient Register, Prescribed Drug Register

All linked via personal identification numbers at individual level.

**Data period:** 1997–2020
**Unit of analysis:** Pregnancy (not woman) — a woman can contribute multiple pregnancies

---

### Step 3 — Eligibility Criteria

- Women with at least one dispensed ASM prescription in the periconceptional period (by country-specific register definitions)
- Live births or stillbirths recorded in national birth registers
- ASM use confirmed by prescription dispensing records (not just prescribing)
- High-dose folic acid defined as ≥4 mg/day (4 mg or 5 mg tablet dispensing)

**Sample sizes (by exposure window):**
- 13–52 weeks before pregnancy: **18,255 eligible pregnancies** (1,047 initiators, 5.7%)
- 1–12 weeks before pregnancy: **13,619 eligible pregnancies** (521 initiators, 3.8%)
- 1–12 weeks after pregnancy onset: **12,365 eligible pregnancies** (1,778 initiators, 14.4%)

---

### Step 4 — Sequential Target Trial Emulation

- **Nested weekly trials**: eligible women included and re-classified weekly as initiators or non-initiators based on whether they filled a high-dose folic acid prescription within 1 week of inclusion
- Each woman can contribute to multiple weekly trials across the periconceptional period
- Three separate emulation series: one per exposure window
- **Time zero** = week of inclusion; follow-up = from time zero to outcome ascertainment (MCA diagnosis by age 1 year) or censoring

---

### Step 5 — Confounder Adjustment

- **Inverse probability of treatment weighting (IPTW)**
- Covariates included: maternal age, parity, calendar year, country, type of ASM (valproate, lamotrigine, levetiracetam, carbamazepine, other), number of ASMs (monotherapy vs polytherapy), indication (epilepsy vs psychiatric), socioeconomic indicators
- Propensity score estimated by logistic regression
- Stabilised weights; balance checked via SMD

---

### Step 6 — Outcome Ascertainment

- **Major congenital anomalies (MCAs)**: defined by EUROCAT classification
- Ascertained from national patient registers using ICD codes
- Time window: diagnosis before 1 year of age
- Country-specific ICD-9 and ICD-10 coding cross-walked

---

### Step 7 — Statistical Analysis

- **Risk difference (RD)** and **risk ratio (RR)** — primary effect measures on absolute and relative scales
- Pooled across four countries using meta-analytic approaches with country-stratified IPW models
- **95% CI** via bootstrap (country-level) or delta method
- Pre-registered protocol: https://osf.io/vph2n/

---

### Step 8 — Sensitivity Analyses

- Restricted to specific ASMs (valproate subgroup; highest teratogenic risk)
- Country-stratified analyses to assess cross-national consistency
- Alternative MCA definitions (including/excluding chromosomal anomalies)
- Sustained use analysis (vs initiation only) as additional exploratory analysis

---

## Key Results

| Exposure Window | Initiators (%) | RR (95% CI) | ARD (95% CI) |
|---|---|---|---|
| 13–52 weeks before pregnancy | 5.7% | 0.99 (0.65–1.36) | NS |
| **1–12 weeks before pregnancy** | **3.8%** | **0.55 (0.25–0.91)** | **−2.2 pp (−3.5 to −0.5)** |
| 1–12 weeks after pregnancy onset | 14.4% | 1.27 (0.94–1.64) | NS |

- **45% relative risk reduction** with preconception initiation (1–12 weeks before)
- No benefit with post-conception initiation
- No significant benefit with very early initiation (>12 weeks before) — may reflect insufficient sustained use
- MCA prevalence ~4.8% in non-initiators (1–12 weeks before group), reduced to ~2.6% in initiators

---

## Strengths

- **Four-country Nordic population registers** with near-complete ascertainment of prescriptions, births, and diagnoses
- Sequential TTE design: avoids immortal-time bias; rigorous ITT-analog causal contrast
- Pre-registered protocol (OSF); open access
- Largest and most methodologically rigorous study to date on this clinical question
- Timing comparison across 3 periconceptional windows is clinically actionable
- National data = near-complete follow-up (no loss to follow-up)

## Limitations

- Small number of initiators in the pre-pregnancy window (3.8% = 521 pregnancies) → wide CIs
- High-dose folic acid defined by dispensing (may not equal actual consumption)
- Cannot distinguish specific ASM teratogenic mechanisms (confounding by ASM type partially addressed by covariate adjustment)
- MCA classification relies on ICD coding quality across 4 different health systems
- Generalisability outside Nordic countries limited (different baseline folic acid fortification practices)
- No data on dose compliance after initiation
