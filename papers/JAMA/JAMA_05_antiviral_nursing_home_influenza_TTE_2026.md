# JAMA_05 — Prompt Antiviral Chemoprophylaxis in Nursing Home Influenza Outbreaks: Sequential TTE

**Citation:** Silva JBB, Hsieh HCT, Howe CJ, et al. Prompt and Intensive Antiviral Chemoprophylaxis in Nursing Home Influenza Outbreaks. *JAMA Internal Medicine.* 2026;186(5):597–607 [published online March 30, 2026]. doi:10.1001/jamainternmed.2026.0401

---

## Brief Summary

This study used a sequential cluster-randomised target trial emulation to evaluate whether initiating oseltamivir chemoprophylaxis in ≥70% of eligible nursing home (NH) residents within 2 days of influenza outbreak detection reduces mortality and hospitalisation compared with less intensive approaches. Across 404 influenza outbreaks in 318 US NHs (35,086 resident-trial observations; Sept 2018–May 2022), intensive prophylaxis was associated with significantly lower 14-day hospitalisation (RD −0.96%, 95% CI −1.78% to −0.19%; RR 0.79, 0.64–0.96) but not with reduced mortality (RD −0.06%, 95% CI −0.73% to 0.93%). The study provides the first quantified coverage threshold (≥70% within 2 days) and offers actionable guidance supporting current CDC/IDSA recommendations, though confirmatory RCT evidence remains absent.

---

## Methodology Step-by-Step

### Step 1: Causal Question as PICO Target Trial Specification

| Component | Specification |
|---|---|
| **Population** | Nursing home residents aged ≥18 years, present on day of influenza outbreak detection, no antiviral use in prior 7 days, no influenza in prior 14 days, complete baseline data |
| **Intervention (NH-level)** | Intensive antiviral chemoprophylaxis: oseltamivir administered to ≥70% of eligible residents within 2 days of outbreak detection |
| **Comparator (NH-level)** | Nonintensive: 0% to <70% of eligible residents receiving oseltamivir |
| **Outcomes** | All-cause death and all-cause hospitalisation at 14 days and 30 days post-outbreak |
| **Time horizon** | 14-day and 30-day follow-up per outbreak |
| **Causal contrast** | Intention-to-treat effect of outbreak-level prophylaxis strategy assignment |
| **Unit of randomisation** | Nursing home (cluster-level) |

---

### Step 2: Data Sources

| Feature | Detail |
|---|---|
| **Database** | Proprietary EHR data from 12 US nursing home corporations |
| **Country** | United States |
| **Period** | September 1, 2018 – May 31, 2022 (4 influenza seasons, including COVID-19 pandemic period) |
| **Outbreaks** | 404 influenza outbreaks across 318 NHs |
| **Sample** | 35,086 resident-trial observations (29,683 unique residents) |
| **Data elements** | Resident demographics, ICD diagnosis codes, medication orders, electronic medication administration records (eMAR), MDS clinical assessments |
| **Outbreak definition** | Second incident influenza case within 72 hours of the first in a NH; 2-week gap required between distinct outbreaks |

---

### Step 3: Eligibility Criteria

**NH-level:**
- NH experienced a detected influenza outbreak
- ≥30 residents present at baseline (to enable reliable chemoprophylaxis utilisation estimates)
- Complete covariate information for ≥50% of residents at baseline
- Active eMAR at baseline
- No influenza outbreak in preceding 14 days

**Resident-level:**
- Present in NH on outbreak detection day (baseline)
- Age ≥18 years
- Complete MDS covariate information
- No antiviral use in prior 7 days
- No influenza identified in prior 14 days

---

### Step 4: Time Zero and Treatment Classification

- **Time zero (baseline)**: Day of influenza outbreak detection (second incident case within 72 hours)
- **Sequential design**: Each NH outbreak constitutes a separate trial; NHs can contribute multiple outbreaks (separated by ≥2-week washout)
- **Intensive prophylaxis**: ≥70% of eligible residents received oseltamivir within 2 days of outbreak detection
- **Nonintensive**: <70% coverage within 2 days (includes 0% coverage)
- **Assignment**: NH-level intervention assignment; resident outcomes aggregated
- **Randomize-censor-weight (RCW) approach**: Residents censored if NH strategy deviated from assigned strategy; inverse probability of censoring weights applied

---

### Step 5: Confounder Adjustment

| Feature | Detail |
|---|---|
| **Method** | Inverse probability of treatment weighting (IPTW) at the outbreak/NH level; randomize-censor-weight (RCW) approach for within-outbreak protocol adherence |
| **NH-level covariates** | NH corporation, influenza season, NH size, geographic region, staff-to-resident ratio |
| **Resident-level covariates** | Age, sex, race/ethnicity, vaccination status, comorbidities (via MDS), functional status, recent hospitalisation |
| **Balance** | Standardised differences assessed after weighting — severity of illness (parasitemia equivalent: median baseline characteristics) well-balanced post-weighting |

---

### Step 6: Statistical Analysis

| Feature | Detail |
|---|---|
| **Primary model** | Discrete-time hazard model with pooled logistic regression |
| **Effect measures** | Risk difference (RD) and risk ratio (RR) for death and hospitalisation at 14 days and 30 days |
| **Estimator** | Weighted risks from pooled logistic regression with IPTW and IPCW |
| **Cluster adjustment** | Robust standard errors / bootstrapping to account for NH-level clustering |
| **Software** | Not specified; standard epidemiologic analysis platform |

---

### Step 7: Sensitivity Analyses

- Restriction to outbreaks where ≥50% of residents had complete eMAR data
- Alternative definitions of outbreak onset
- Varying the coverage threshold (e.g., ≥60%, ≥80%)
- Alternative follow-up periods
- Subgroup by vaccination status, influenza season
- Exclusion of pandemic influenza seasons (COVID-19 overlap)

---

## Key Results

| Outcome | Intensive vs Nonintensive | RD (95% CI) | RR (95% CI) |
|---|---|---|---|
| **14-day death** | 35,086 observations | −0.06% (−0.73% to 0.93%) | 0.96 (0.56–1.57) |
| **14-day hospitalisation** | 35,086 observations | −0.96% (−1.78% to −0.19%) | 0.79 (0.64–0.96) |
| **30-day hospitalisation** | — | Directionally similar, less precise | — |
| **30-day death** | — | No significant difference | — |

**Population characteristics:**
- Median age: 78 years (IQR 68–86)
- 60% women; 81% White; 76% vaccinated
- 17,155 observations assigned intensive prophylaxis; 17,931 nonintensive

---

## Strengths

- Sequential cluster-randomised TTE design appropriately accounts for outbreak-level clustering and time-varying exposure
- Randomize-censor-weight (RCW) approach handles within-outbreak protocol deviations rigorously
- Large, multi-corporation NH dataset across 4 influenza seasons — excellent external validity for US NH settings
- First study to define and quantify a specific coverage threshold (≥70%) and speed (2 days) for clinical guidance
- Aligns with and provides quantitative support for existing CDC/IDSA recommendations
- Objective chemoprophylaxis ascertainment via eMAR (not self-report)

## Limitations

- Observational design: cannot fully rule out confounding by indication (sicker NHs may have adopted intensive prophylaxis differently)
- Study period includes COVID-19 pandemic (2020–2022) — infection control practices changed substantially; influenza may have been suppressed
- Missing data assumed to be missing at random — potentially non-random in practice
- Mortality benefit not demonstrated — may reflect insufficient power, short follow-up (14/30 days), or genuine absence of mortality effect
- EHR data from 12 NH corporations may not represent independent community NHs or non-US settings
- Oseltamivir dosing, duration, and adherence within the "intensive" category not granularly controlled
- Race/ethnicity data partially from administrative records — may be misclassified
