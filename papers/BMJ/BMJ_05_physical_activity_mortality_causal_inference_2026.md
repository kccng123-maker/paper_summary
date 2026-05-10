# BMJ_05 — Light vs Moderate-to-Vigorous Physical Activity and Mortality: Causal Inference Analysis

**Citation:** Luo M, Clare PJ, Tarp J, Dalene KE, Sanchez-Lastra MA, Nguyen B, Owen K, Nau T, Chen L, Ekelund U, Ding D. Dose-response interplay between light and moderate-to-vigorous physical activity on all-cause mortality risk: a causal inference analysis. *British Journal of Sports Medicine (BJSM/BMJ).* 2026. doi:10.1136/bjsports-2025-110782. Published online March 23, 2026.

---

## Brief Summary

This study used a counterfactual causal inference framework to estimate the joint dose-response effects of light-intensity physical activity (LPA) and moderate-to-vigorous-intensity physical activity (MVPA) on all-cause mortality in UK Biobank participants (n=71,715). Using accelerometer-measured activity and flexible parametric survival models under the counterfactual framework, the study demonstrated a non-linear protective effect of LPA on 10-year mortality that diminishes as MVPA levels increase. At the lower WHO-recommended MVPA threshold (22 min/day), increasing LPA from 60 to 360 min/day was estimated to reduce the 10-year probability of death from 9.5% to 4.2%. These findings suggest that LPA meaningfully complements MVPA to reduce mortality risk, particularly for those unable to achieve higher-intensity exercise targets.

---

## Methodology Step-by-Step

### Step 1: Causal Question as PICO

| Component | Specification |
|---|---|
| **Population** | UK Biobank participants with valid accelerometer data; general UK adult population |
| **Intervention** | Varying doses of light-intensity physical activity (LPA, min/day) under fixed MVPA scenarios |
| **Comparator** | Counterfactual distributions of LPA at alternative dose levels |
| **Outcomes** | All-cause mortality within 10 years of follow-up |
| **Time horizon** | Median 8.0 years follow-up; 10-year mortality probability estimated |
| **Causal contrast** | Marginal counterfactual effect of shifting the population distribution of LPA |

---

### Step 2: Data Sources

| Feature | Detail |
|---|---|
| **Database** | UK Biobank |
| **Country** | United Kingdom |
| **Period** | Accelerometer assessment 2013–2015; mortality follow-up through ~2022 |
| **Sample size** | 71,715 eligible participants |
| **Activity measurement** | Wrist-worn accelerometer (objective measurement); LPA and MVPA classified by intensity thresholds |
| **Mortality data** | National Death Registry linkage |

---

### Step 3: Eligibility Criteria

- Valid accelerometer wear data (sufficient wear duration)
- Complete baseline covariate information
- No prevalent terminal illness at recruitment
- Available mortality follow-up data

---

### Step 4: Time Zero and Exposure Classification

- **Time zero**: Date of accelerometer assessment (baseline)
- **LPA**: Light-intensity physical activity (min/day) — below MVPA threshold, above sedentary behaviour
- **MVPA**: Moderate-to-vigorous physical activity (min/day) — at or above moderate intensity threshold per accelerometer calibration
- **Scenarios**: Three fixed MVPA levels examined:
  1. Low MVPA (below WHO lower threshold: <22 min/day)
  2. WHO lower threshold: 22 min/day MVPA
  3. WHO higher threshold: 44 min/day MVPA
- LPA dose varied continuously from 60 to 360+ min/day within each MVPA scenario

---

### Step 5: Confounder Adjustment

| Feature | Detail |
|---|---|
| **Framework** | Counterfactual/potential outcomes framework |
| **Method** | Flexible parametric survival models with covariate adjustment |
| **Covariates** | Age, sex, BMI, smoking status, alcohol use, diet quality, prevalent chronic conditions, socioeconomic status, sedentary time |
| **Dose-response modelling** | Restricted cubic splines to capture non-linearity |

---

### Step 6: Statistical Analysis

| Feature | Detail |
|---|---|
| **Primary model** | Flexible parametric survival model (counterfactual framework) |
| **Effect measure** | Marginal predicted probability of death at 10 years |
| **Dose-response** | Non-linear (spline-based) counterfactual dose-response curves for LPA at fixed MVPA levels |
| **Causal identification** | Conditional exchangeability assumed given measured covariates; positivity and consistency assumed |
| **Optimal dose** | Identified as dose where marginal mortality reduction attenuates (plateau point) |

---

### Step 7: Sensitivity Analyses

- Analyses stratified by age, sex, BMI category
- Exclusion of first 1–2 years of follow-up (to address reverse causation from pre-existing illness)
- Alternative MVPA intensity thresholds
- Adjusted for sedentary time as additional covariate

---

## Key Results

| Scenario | LPA (min/day) | 10-yr Prob. of Death |
|---|---|---|
| WHO lower MVPA (22 min/day) | 60 | 9.5% |
| WHO lower MVPA (22 min/day) | 360 | 4.2% |
| WHO higher MVPA (44 min/day) | 60 | 6.6% |
| WHO higher MVPA (44 min/day) | 345 (optimal) | 3.7% |

- Non-linear dose-response: mortality benefit of LPA diminishes at higher MVPA levels
- Optimal LPA dose across MVPA scenarios: **195–225 min/day**
- 2,195 deaths occurred during median 8.0 years follow-up
- LPA benefit most pronounced at low MVPA levels — suggesting substitutability and complementarity

---

## Strengths

- Large sample (n=71,715) with objective accelerometer measurement — avoids self-report bias in physical activity assessment
- Counterfactual causal inference framework with flexible dose-response modelling — goes beyond conventional hazard ratio estimation
- Clinically actionable finding: quantifies LPA benefit at specific MVPA thresholds relevant to current WHO guidelines
- Non-linear modelling captures biological dose-response reality
- Mortality ascertained via national death registry (complete follow-up)

## Limitations

- Observational design: unmeasured confounding (e.g., pre-illness activity reduction) may remain despite adjustment
- Accelerometer measurement is a single time point — activity levels may change over follow-up
- UK Biobank is a volunteer cohort with healthy worker effect — predominantly White, higher socioeconomic status; limited generalisability
- Causal assumptions (conditional exchangeability, positivity, consistency) cannot be fully verified
- Physical activity classification thresholds vary across calibration standards — sensitivity to threshold choice
- 10-year mortality probability extrapolated beyond median follow-up duration
