# GLP-1 Receptor Agonists and Risk of Acute Pancreatitis — TTE

**Citation:** Xie Y, Choi T, Al-Aly Z. GLP-1 receptor agonists and risk of all cause and cause specific acute pancreatitis: target trial emulation. *BMJ Medicine.* 2026;5(1):e002183. doi:10.1136/bmjmed-2025-002183. PMC13110570.

**Journal:** BMJ Medicine
**Access:** Open access via PMC (full text available)
**Search date:** 2026-05-11

---

## Brief Summary

Using the same VA national cohort (n=333,687; GLP-1RA n=132,551; sulfonylurea n=201,136) as the companion MACE paper, this TTE evaluated risk of all-cause and cause-specific acute pancreatitis at 12 months. The headline result is **null for all-cause pancreatitis** (rate difference −3.64, 95% CI −30.76 to 23.48 per 100,000 persons), but this masks opposing cause-specific effects: GLP-1RA increased risk of suspected **drug-induced pancreatitis** (RD +23.45 per 100,000) while decreasing **hypertriglyceridaemia-associated** (−16.96) and **alcohol-induced** (−10.32) pancreatitis. Drug-induced events cluster early (42% in first 3 months), while protective effects accrue later. Clinicians should counsel on early risk while recognising the long-term neutral overall effect.

---

## Methodology (Step-by-Step)

### Step 1 — Causal Question (Target Trial Specification)

| Component | Target Trial Specification | Emulation |
|---|---|---|
| **Population** | VA users with T2DM, no prior GLP-1RA or sulfonylurea in past year, no contraindications | VA Corporate Data Warehouse 2017–2023 |
| **Intervention** | Initiate GLP-1RA | First GLP-1RA prescription (new-user) |
| **Comparator** | Initiate sulfonylurea (active comparator) | First sulfonylurea prescription |
| **Outcomes** | All-cause acute pancreatitis; cause-specific pancreatitis (5 subtypes) | ICD codes + clinical note NLP classification |
| **Follow-up** | 12 months | Same |
| **Causal contrasts** | ITT (primary); per-protocol (secondary — continued vs initiated) | Both reported |

---

### Step 2 — Data Sources

- **Same VA Corporate Data Warehouse** as companion MACE paper (01 Jan 2017 – 31 Dec 2023)
- Outpatient + inpatient encounters, pharmacy, lab results (lipase, amylase, triglycerides), vital signs, clinical notes
- **Key advantage for this study**: VA longitudinal EHR allows **cause-specific classification of pancreatitis** via:
  - ICD codes for acute pancreatitis
  - Laboratory data: triglycerides (hypertriglyceridaemia-associated), alcohol markers
  - Clinical notes / discharge summaries: NLP-assisted drug-induced pancreatitis identification
  - Linked Medicare for out-of-system events

---

### Step 3 — Outcome Classification (5 Pancreatitis Subtypes)

| Subtype | Classification Method |
|---|---|
| **Drug-induced (suspected)** | Temporal association with GLP-1RA initiation, no other identified cause, clinical note review |
| **Hypertriglyceridaemia-associated** | Triglycerides >500 mg/dL in proximity to pancreatitis episode |
| **Alcohol-induced** | Alcohol use disorder diagnosis + pancreatitis; alcohol documentation in clinical notes |
| **Biliary** | Gallstone/biliary tract diagnosis concurrent with pancreatitis |
| **Idiopathic / other** | Residual (none of the above criteria met) |

---

### Step 4 — Confounder Adjustment

- **Inverse probability weighting (IPW)** at baseline
- Covariates: demographics, T2DM severity (HbA1c, duration), comorbidities, alcohol use disorder, obesity, triglyceride levels, baseline medications (statins, fibrates, antidiabetics), healthcare utilisation
- **Discrete-time survival models** with IPW for cumulative incidence at monthly intervals over 12 months
- Stabilised weights; balance assessed via SMD

---

### Step 5 — Statistical Analysis

**ITT analysis (primary):**
- **Rate differences per 100,000 persons** at 1 year — absolute risk scale preferred for rare events
- 95% CI from bootstrap or Delta method

**Per-protocol analysis (secondary):**
- Restricted to participants who maintained assigned treatment status (continued GLP-1RA vs continued sulfonylurea)
- Allows temporal pattern analysis of when each subtype risk manifests

**Temporal analysis:**
- Monthly cumulative incidence curves for each pancreatitis subtype
- Compared timing of excess drug-induced events vs timing of protective effects for alcohol/hypertriglyceridaemia subtypes

---

### Step 6 — Sensitivity Analyses

- Supplemental table S1: full target trial protocol
- Restricted to specific GLP-1RA agents (liraglutide vs semaglutide vs other)
- Varying lookback windows for prior pancreatitis exclusion
- Sensitivity using alternative triglyceride thresholds for hypertriglyceridaemia classification

---

## Key Results

**ITT (1-year, per 100,000 persons):**

| Pancreatitis Subtype | Rate Difference (95% CI) | Direction |
|---|---|---|
| All-cause | −3.64 (−30.76 to 23.48) | **Null** |
| Drug-induced | **+23.45 (14.27 to 33.85)** | Increased |
| Hypertriglyceridaemia-associated | **−16.96 (−27.41 to −7.34)** | Decreased |
| Alcohol-induced | **−10.32 (−18.12 to −3.17)** | Decreased |
| Biliary | Similar rates | Null |
| Idiopathic / other | Similar rates | Null |

**Temporal patterns (per-protocol):**
- Drug-induced: **42% of attributable events in first 3 months** (early signal)
- Alcohol-induced reduction: concentrated months 4–6
- Hypertriglyceridaemia reduction: concentrated months 10–12
- Net all-cause pancreatitis: small increase in first 2 months, neutral thereafter

---

## Strengths

- Same large VA cohort as MACE paper — excellent statistical power for rare outcomes
- **Cause-specific pancreatitis classification** is a major methodological innovation (most prior studies reported all-cause only)
- VA EHR depth enables NLP-assisted drug-induced classification + lab-based subtyping
- ITT + per-protocol + temporal analysis comprehensively characterises risk trajectory
- Active comparator (sulfonylurea) design reduces confounding by indication
- Directly addresses UK MHRA investigation signal (June 2025)

## Limitations

- VA population predominantly male veterans — limited generalisability to women
- Cause-specific classification relies on EHR data and NLP — misclassification possible
- Drug-induced pancreatitis is a diagnosis of exclusion; sensitivity of algorithm uncertain
- 12-month follow-up may miss longer-term drug-induced events (rare late-onset)
- Pancreatitis is rare; even in VA cohort, absolute event counts per subtype are small
- GLP-1RA agent-specific analyses not primary (semaglutide vs liraglutide may differ)
