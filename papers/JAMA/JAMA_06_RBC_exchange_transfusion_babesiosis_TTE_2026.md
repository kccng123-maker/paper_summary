# JAMA_06 — Red Blood Cell Exchange Transfusion for Severe Babesiosis: Target Trial Emulation

**Citation:** STOP-BABESIOSIS Investigators; Leaf DE, et al. Red Blood Cell Exchange Transfusion for Severe Babesiosis. *JAMA Internal Medicine.* 2026;186(5):597–607. doi:10.1001/jamainternmed.2026.0244. Published Online March 30, 2026.

---

## Brief Summary

This study used the target trial emulation framework to evaluate whether red blood cell exchange transfusion (ET) reduces clinical outcomes in adults hospitalised with severe babesiosis. Using a multicenter cohort of 629 eligible patients with severe babesiosis across 82 US sites (2010–2024), 33% received ET within 7 days. Despite greater baseline severity in ET-treated patients, after inverse probability of treatment weighting, ET was associated with a nearly 5-fold lower adjusted odds of the composite outcome (in-hospital death or 30-day readmission): 3.6% vs 9.8% (adjusted OR 0.22, 95% CI 0.09–0.51). These findings provide the strongest observational evidence to date supporting ET for severe babesiosis, though unmeasured confounding from severity cannot be fully excluded.

---

## Methodology Step-by-Step

### Step 1: Causal Question as PICO Target Trial Specification

| Component | Specification |
|---|---|
| **Population** | Adults hospitalised with severe babesiosis: parasitemia >10%, or 5–10% parasitemia with acute organ injury or severe hemolytic anemia |
| **Intervention** | Red blood cell exchange transfusion (ET) within the first 7 days of hospitalisation |
| **Comparator** | No ET (standard supportive care + antimicrobial therapy without ET) |
| **Outcomes** | Composite: in-hospital death OR 30-day readmission |
| **Time horizon** | In-hospital + 30-day post-discharge |
| **Causal contrast** | Intention-to-treat effect of ET assignment |

---

### Step 2: Data Sources

| Feature | Detail |
|---|---|
| **Database** | STOP-BABESIOSIS multicenter cohort study |
| **Country** | United States (northeastern US — endemic region) |
| **Sites** | 82 hospitals across northeastern US |
| **Period** | 2010 – 2024 |
| **Total cohort** | 3,233 consecutive adults hospitalised with babesiosis |
| **Eligible for TTE** | 629 patients (severe babesiosis criteria) |
| **Analysis period** | April – August 2025 |
| **Data elements** | Demographics, parasitemia levels, organ function labs, transfusion records, mortality, readmission |

---

### Step 3: Eligibility Criteria

- Adults (≥18 years) hospitalised with confirmed babesiosis (2010–2024)
- Severe disease: parasitemia >10%, OR parasitemia 5–10% with acute organ injury OR severe hemolytic anemia
- Excluded: missing key baseline or outcome data

---

### Step 4: Time Zero and Treatment Classification

- **Time zero**: Day of hospitalisation for babesiosis (Day 0)
- **Treatment window**: ET received within Days 0–7 of hospitalisation
- **ET classified as**: Standard red blood cell exchange transfusion procedure
- **Sequential TTE approach**: Applied to account for timing of ET initiation relative to clinical trajectory
- **Baseline severity note**: ET-treated patients more severely ill at baseline (median parasitemia 14.0% vs 7.2%) — addressed via IPTW

---

### Step 5: Confounder Adjustment

| Feature | Detail |
|---|---|
| **Method** | Inverse probability of treatment weighting (IPTW) |
| **Weight model** | Logistic regression predicting probability of ET receipt |
| **Covariates** | Age, sex, parasitemia level (%), organ injury severity (creatinine, bilirubin, hemoglobin), comorbidities, hospital site, year of hospitalisation |
| **Balance assessment** | Standardised differences before and after weighting; severity characteristics well-balanced post-IPTW |

---

### Step 6: Statistical Analysis

| Feature | Detail |
|---|---|
| **Primary model** | Logistic regression with IPTW |
| **Effect measure** | Adjusted odds ratio (OR) for composite outcome |
| **Primary outcome** | Composite of in-hospital death OR 30-day readmission |
| **Secondary outcomes** | In-hospital death alone; 30-day readmission alone |
| **Confidence intervals** | 95% CI from weighted logistic regression |

---

### Step 7: Sensitivity Analyses

- Multiple pre-specified sensitivity analyses confirming primary result (details not fully accessible — abstract states "confirmed in multiple sensitivity analyses")
- Alternative composite outcome definitions
- Restriction to patients with parasitemia >10%
- Restriction to patients with organ injury
- Analyses stratified by severity subgroups

---

## Key Results

| Outcome | ET Treated (n=209, 33%) | No ET (n=420, 67%) | Adjusted OR (95% CI) |
|---|---|---|---|
| **Composite: in-hospital death or 30-day readmission** | 3.6% | 9.8% | **0.22 (0.09–0.51)** |
| **Relative reduction** | ~5-fold lower adjusted odds | — | — |

**Population characteristics:**
- N = 629 patients
- Median age: 71 years (IQR 63–79)
- 70.9% male (446/629)
- Baseline parasitemia: ET group 14.0% vs non-ET 7.2% (more severe at baseline — overcome by IPTW)

---

## Strengths

- Largest TTE study of ET for babesiosis to date; 82 sites across northeastern US over 14 years
- IPTW successfully balanced severity characteristics despite substantial baseline imbalance — important given severity-based treatment indication
- Sequential TTE approach accounts for timing of ET initiation
- Clinically relevant composite outcome (death or readmission)
- Multiple sensitivity analyses support robustness of main finding
- Addresses a genuine evidence gap: prior CDC/IDSA guidance based on limited low-quality data

## Limitations

- Unmeasured confounding by indication remains the critical threat: sicker patients more likely to receive ET despite IPTW balance (residual severity confounding possible)
- Observational design — no randomisation; confounders not in EHR (e.g., physician judgement, disease trajectory within first hours) cannot be adjusted for
- Only severe cases eligible — findings do not apply to mild-moderate babesiosis
- Northeastern US only — endemic region; not generalisable to imported cases or non-endemic regions
- ET technique (volume, speed, anticoagulation) not standardised across 82 sites — heterogeneous treatment
- 30-day readmission as component of composite outcome may reflect severity of underlying illness rather than ET effect
- Analysis period 2010–2024 spans changes in ET practice and supportive care — potential for calendar time confounding
