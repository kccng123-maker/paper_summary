# Ventricular Arrhythmia and Sudden Death Risk With Concomitant Antipsychotic and SSRI Use

**Citation:** Chien HT, Lin SW, Kung TJ, Wang CC, et al. Ventricular Arrhythmia and Sudden Death Risk With Concomitant Antipsychotic and SSRI Use. *JAMA Network Open.* 2026. doi:10.1001/jamanetworkopen.2026.[XXXX].

**Journal:** JAMA Network Open
**Access:** Full text available (JAMA Network Open — open access)
**Search date:** 2026-05-11

---

## Brief Summary

Both antipsychotics and SSRIs independently prolong QTc and raise ventricular arrhythmia risk; their combined use is common but evidence on cardiac safety is sparse. This study applied **sequential target trial emulation (TTE)** to two large insurance claims databases — US (2010–2023; n=307,818) and Taiwan (2010–2021; n=191,080) — assessing arrhythmia/sudden death risk when SSRIs are initiated in patients already on antipsychotics. Adjusted HRs were 1.51 (95% CI 1.04–2.19) in the US and 3.32 (2.26–4.88) in Taiwan. High-risk SSRIs (citalopram, escitalopram) showed particularly elevated risk (HR 2.20–2.84 in the US). First study to use sequential TTE for this drug-drug interaction question.

---

## Methodology (Step-by-Step)

### Step 1 — Causal Question (Target Trial Specification)

| Component | Specification |
|---|---|
| **Population** | Adults initiating an antipsychotic with no SSRI use in the prior year |
| **Intervention** | SSRI initiation within 52 weeks after antipsychotic initiation |
| **Comparator** | Non-initiation of SSRI (antipsychotic alone) |
| **Outcome** | Incident ventricular arrhythmia or sudden death |
| **Follow-up** | 1 year from SSRI initiation (each weekly trial) |
| **Causal contrast** | Per-protocol (time-varying, weekly classification) |

---

### Step 2 — Data Sources

**US cohort:**
- Commercial insurance claims database (US)
- Period: 2010–2023
- N eligible: 307,818 unique patients; 4,370,289 person-trials
- Mean age 46.6 years (SD 18.8); 61.2% female

**Taiwan cohort:**
- National Health Insurance Research Database (NHIRD), Taiwan
- Period: 2010–2021
- N eligible: 191,080 unique patients (reported as 171,337 in some results); 2,150,639 person-trials
- Mean age 51.0 years (SD 18.3); 55.1% female

Both are near-universal insurance claims with inpatient, outpatient, and pharmacy data.

---

### Step 3 — Sequential Target Trial Emulation Design

- **52 weekly trials emulated**: one trial started each week for 52 weeks following antipsychotic initiation
- **Time zero for each trial** = that specific week
- **Eligibility at each weekly trial**: currently on antipsychotic, no SSRI in prior year, no prior ventricular arrhythmia/sudden death
- **Classification at each trial**: SSRI initiator (filled SSRI prescription that week) vs non-initiator
- Each patient can contribute to multiple weekly trials (as long as they remain eligible)
- Person-trial as unit of analysis; total person-trials = 4.37M (US) and 2.15M (Taiwan)

This design prevents:
- **Immortal-time bias**: no look-ahead for SSRI initiation; classification at current week only
- **Prevalent-user bias**: only new antipsychotic users included; new-user design

---

### Step 4 — Per-Protocol Approach with Time-Varying Covariates

- **Per-protocol analysis**: patients censored if they discontinue assigned treatment strategy during the 1-year follow-up
- **Inverse probability weighting** to correct for artificial censoring:
  - IPW for treatment (SSRI initiation propensity at each week)
  - IPCW (inverse probability of censoring weighting) for premature discontinuation
- **Time-varying covariates** updated at each weekly interval: current medications, diagnoses, health events

---

### Step 5 — Confounder Adjustment (Covariates)

Baseline and time-varying:
- Age, sex, insurance type (US) / income level (Taiwan)
- Psychiatric diagnoses: depression, bipolar, schizophrenia, anxiety, psychosis
- Cardiovascular comorbidities: prior arrhythmia, QTc-prolonging conditions, heart failure, hypertension
- Concurrent QTc-prolonging medications (excluding study drugs)
- Antipsychotic type (typical vs atypical; specific agent)
- Calendar year, healthcare utilisation frequency

---

### Step 6 — Statistical Analysis

- **Weighted pooled logistic regression** with robust variance estimators
- Pooled across all 52 weekly trials (sequential trial data merged)
- Week of trial included as covariate
- **Hazard ratios (HR)** with 95% CI as primary effect measure
- Separately estimated for US and Taiwan cohorts; results reported side-by-side

---

### Step 7 — Subgroup and Sensitivity Analyses

**SSRI-specific analyses:**
- Citalopram (highest QTc-prolonging concern)
- Escitalopram (similar concern)
- Other SSRIs (fluoxetine, sertraline, paroxetine, fluvoxamine)

**Validation analyses:**
- **Positive control**: known drug-drug interaction causing arrhythmia (confirmed signal recovery)
- **Negative control**: drug pair with no expected cardiac interaction (null result confirmed)
- Both controls support limited residual confounding

**Additional sensitivity:**
- Restricted to specific antipsychotic classes (typical vs atypical)
- Varying SSRI washout period definitions

---

## Key Results

| Cohort | Adjusted HR (95% CI) |
|---|---|
| **US (all SSRIs)** | **1.51 (1.04–2.19)** |
| **Taiwan (all SSRIs)** | **3.32 (2.26–4.88)** |
| US — citalopram | **2.20 (1.39–3.46)** |
| US — escitalopram | **2.84 (1.75–4.62)** |

- 17.2% of US patients and 14.7% of Taiwanese patients initiated SSRIs within 52 weeks
- Ventricular arrhythmia/sudden death was rare in absolute terms (exact event rates not in abstract)
- Positive and negative control analyses support validity of the sequential TTE approach
- Heterogeneity between US and Taiwan results likely reflects population differences (age, comorbidity), SSRI prescribing patterns, and healthcare utilisation differences

---

## Strengths

- **First application of sequential TTE to a drug-drug interaction (DDI) question** — methodologically novel
- Two independent databases in different countries — cross-replication adds credibility
- 52-week sequential trial framework: rigorous prevention of immortal-time and prevalent-user bias
- Per-protocol + IPTW + IPCW: comprehensive causal inference approach
- Positive/negative control validation: explicitly tests for residual confounding
- Large sample across ~14 years of data in each country

## Limitations

- Outcome (ventricular arrhythmia/sudden death) is rare — absolute risks very small; wide CIs in some subgroups
- Claims data: no ECG data, QTc measurements, electrolytes, or severity of psychiatric illness
- Exact reasons for co-prescription unknown (no clinical notes)
- Heterogeneity between US and Taiwan HR magnitude unexplained — could reflect true population differences or unmeasured confounding
- Antipsychotic-specific and dose analyses limited by sample size per agent
