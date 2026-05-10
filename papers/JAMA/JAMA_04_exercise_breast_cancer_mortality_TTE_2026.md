# JAMA_04 — Tailored Exercise Strategies and Mortality in Breast Cancer Survivors: TTE

**Citation:** Jayasekera J, Ergas IJ, Schneider J, Tian E, et al. Tailored Exercise Strategies and Mortality Among Breast Cancer Survivors. *JAMA Network Open.* 2026;9(4):e265177. doi:10.1001/jamanetworkopen.2026.5177. Published online April 13, 2026.

---

## Brief Summary

This study used a two-stage target trial emulation (TTE) design to estimate the effect of tailored exercise strategies on mortality among breast cancer survivors. Using the Pathways Study (Kaiser Permanente Northern California), the authors first emulated a target trial mirroring the CHALLENGE randomised trial in 959 breast cancer survivors (all-cause mortality 8-year RD: −8.0 percentage points, compatible with CHALLENGE's −7.1 pp), validating the TTE approach. They then extended findings to 2,107 survivors using pragmatic adaptive strategies: engaging in an increase of 60 minutes/week vigorous (or 120 minutes/week moderate) aerobic exercise was associated with a 3.1 percentage-point lower 10-year all-cause mortality risk and 2.4 percentage-point lower breast cancer–specific mortality. The study provides TTE-based evidence for tailored exercise recommendations in clinical oncology practice while noting the need for confirmatory RCT evidence.

---

## Methodology Step-by-Step

### Step 1: Causal Question as PICO Target Trial Specification

**Target Trial 1 (CHALLENGE mirror):**

| Component | Specification |
|---|---|
| **Population** | Women ≥21 years, KPNC members, stage II/III invasive breast cancer 2005–2013, Elixhauser <14, <150 min/week recreational aerobic exercise at baseline, no prior invasive cancer |
| **Intervention** | Aerobic exercise strategy (mirroring CHALLENGE recreational exercise arm) |
| **Comparator** | Health education control (mirroring CHALLENGE control arm) |
| **Outcomes** | All-cause mortality |
| **Time horizon** | Up to 8 years (or December 2021) |
| **Causal contrast** | ITT and per-protocol effects |

**Target Trial 2 (Pragmatic tailored strategies):**

| Component | Specification |
|---|---|
| **Population** | Broader: women with stage I–III invasive breast cancer, KPNC members |
| **Intervention** | Tailored adaptive exercise strategies: increase of ≥60 min/week vigorous or ≥120 min/week moderate aerobic exercise per week, adapted to evolving clinical characteristics |
| **Comparator** | No exercise intervention |
| **Outcomes** | All-cause mortality; breast cancer–specific mortality |
| **Time horizon** | 10 years (or December 2021) |
| **Causal contrast** | ITT and per-protocol effects |

---

### Step 2: Data Sources

| Feature | Detail |
|---|---|
| **Database** | Pathways Study (prospective cohort of breast cancer survivors) |
| **Health system** | Kaiser Permanente Northern California (KPNC) |
| **Country** | United States |
| **Period** | Enrolment January 2006 – December 2013; follow-up through December 2021 |
| **Sample size (Trial 1)** | 959 eligible women; 183 deaths |
| **Sample size (Trial 2)** | 2,107 eligible women; 321 deaths |
| **Data elements** | Self-reported exercise questionnaires (~every 2 years), EHR (diagnoses, comorbidities), cancer registry, mortality records |
| **Reference trial** | CHALLENGE RCT (889 colon cancer survivors; adapted for breast cancer context) |

---

### Step 3: Eligibility Criteria

**Target Trial 1:**
- Women ≥21 years, KPNC members
- Incident stage II or III invasive breast cancer, diagnosed 2005–2013
- No substantial comorbid condition (Elixhauser Comorbidity Index <14 in prior 12 months)
- No swelling interfering with exercise in past 6 months
- Currently engaging in <150 min/week moderate-to-vigorous recreational aerobic exercise at baseline
- No prior history of invasive cancer

**Target Trial 2:**
- Broader eligibility: stage I–III breast cancer
- Required completion of at least one exercise questionnaire post-diagnosis

---

### Step 4: Time Zero and Treatment Classification

- **Time zero**: Date of assignment to an exercise strategy at baseline (post-diagnosis questionnaire)
- **Exercise assessment**: Self-reported recreational aerobic exercise (min/week) at ~2-year intervals
- **Strategy classification (Trial 1)**: Assigned to exercise strategy mirroring CHALLENGE recreational arm or health education control based on reported activity level
- **Strategy classification (Trial 2)**: Adaptive dynamic assignment — strategies modified based on evolving exercise levels and clinical characteristics; increase of 60 min/week vigorous or 120 min/week moderate aerobic exercise above current level
- **Loss to follow-up**: Defined as questionnaire non-response

---

### Step 5: Confounder Adjustment

| Feature | Detail |
|---|---|
| **Method** | Inverse probability weighting (IPW) for ITT and per-protocol effects |
| **Covariates** | Age, BMI, cancer stage, comorbidities (Elixhauser index), treatment type (chemotherapy, radiation, endocrine therapy), baseline exercise level, sociodemographic factors (race/ethnicity, education) |
| **Dynamic treatment** | Marginal structural models (MSMs) with time-varying IPTW for per-protocol analyses (Trial 2) |
| **Reporting** | TARGET statement followed (Transparent Reporting of Observational Studies Emulating a Target Trial) |

---

### Step 6: Statistical Analysis

| Feature | Detail |
|---|---|
| **Primary measure** | Risk difference (RD) in mortality probability at 8 years (Trial 1) and 10 years (Trial 2) |
| **Model** | Pooled logistic regression / discrete-time hazard models |
| **ITT effect** | Estimated from observed assignment; IPTW to account for confounding |
| **Per-protocol effect** | Additional inverse probability of censoring weights (IPCW) to account for non-adherence |
| **Bootstrapping** | 95% CIs via bootstrap resampling |

---

### Step 7: Sensitivity Analyses

- Comparison of TTE Trial 1 estimates to CHALLENGE trial findings (cross-validation)
- Subgroup analyses by cancer stage, age, BMI
- Alternative exercise thresholds for strategy classification
- Excluding first year of follow-up (reverse causation sensitivity)
- Varying loss-to-follow-up definitions

---

## Key Results

| Outcome | Estimate | 95% CI |
|---|---|---|
| **Trial 1: 8-yr all-cause mortality RD (exercise vs health education)** | −8.0 pp | −3.4 to −13.3 pp |
| **CHALLENGE trial (reference)** | −7.1 pp | −1.8 to −12.3 pp |
| **Trial 2: 10-yr all-cause mortality RD (tailored exercise vs no intervention)** | −3.1 pp | −2.0 to −4.6 pp |
| **Trial 2: 10-yr breast cancer–specific mortality RD** | −2.4 pp | −1.2 to −3.5 pp |
| **Trial 2: 10-yr all-cause mortality range across strategies** | 18.1% to 21.2% | — |
| **Trial 2: 10-yr breast cancer–specific mortality range** | 7.6% to 10.0% | — |

- Trial 1 successfully reproduced CHALLENGE trial findings, validating the TTE approach
- Mean age: 58.3 years (Trial 1); 60.1 years (Trial 2)

---

## Strengths

- Two-stage design: first validates TTE approach against known RCT result (CHALLENGE), then extends to pragmatic setting — methodologically rigorous demonstration of TTE concordance
- TARGET reporting guideline adherence ensures transparency
- Adaptive/dynamic treatment strategy (Trial 2) reflects real-world clinical practice better than static interventions
- Extends CHALLENGE findings to breast cancer survivors (original trial was colon cancer)
- Broad population in Trial 2 improves generalisability
- Long follow-up (up to 15+ years from diagnosis)

## Limitations

- Exercise assessed by self-report questionnaire (~2-year intervals) — misclassification possible; activity levels between questionnaires not captured
- KPNC cohort (insured, predominantly urban Californian women) — may not generalise to uninsured or rural populations
- Loss to follow-up via questionnaire non-response may be informative (differential by health status)
- Observational design: unmeasured confounding (e.g., overall health trajectory, motivation) may persist despite weighting
- Exercise intensity thresholds adapted from CHALLENGE trial designed for colon cancer survivors — may not fully match breast cancer survivor exercise tolerance
- Per-protocol estimates require strong no-unmeasured-confounding of adherence assumption
