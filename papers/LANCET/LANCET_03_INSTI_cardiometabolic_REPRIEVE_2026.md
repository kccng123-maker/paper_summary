# LANCET_03 — INSTI Switch and Cardiometabolic Risk: TTE in REPRIEVE

**Citation:** Kileel EM, Malvestutto CD, Zanni MV, Davies-Smith E, Fichtenbaum CJ, Lake JE, et al. Risk of obesity, diabetes, hypertension, and major adverse cardiovascular events after a switch to an integrase inhibitor: a target trial emulation in REPRIEVE. *The Lancet HIV.* 2026;13(5):e306–e315. doi:10.1016/S2352-3018(25)00354-6

---

## Brief Summary

This study used the target trial emulation (TTE) framework to estimate whether switching antiretroviral therapy (ART) to an integrase strand-transfer inhibitor (INSTI)-based regimen increases cardiometabolic risk in people with HIV at low-to-moderate cardiovascular risk. Drawing on longitudinal data from the global REPRIEVE trial (12 countries, 5,114 participants), the authors emulated a series of 37 sequential trials comparing INSTI switchers versus non-switchers over up to 5 years of follow-up. Switchers had significantly higher hazard of incident obesity (HR 1.41, 95% CI 1.22–1.59), diabetes (HR 1.50, 1.24–1.81), and hypertension (HR 1.45, 1.26–1.67), but no statistically significant effect on MACE (HR 1.17, 0.87–1.57) was observed. These findings highlight that INSTI-associated weight gain translates into measurable cardiometabolic harm, underscoring the need for long-term monitoring in INSTI-treated people with HIV globally.

---

## Methodology Step-by-Step

### Step 1: Causal Question as PICO Target Trial Specification

| Component | Specification |
|---|---|
| **Population** | People with HIV aged 40–75 years, on stable non-INSTI ART ≥6 months, CD4 >100 cells/μL, low-to-moderate ASCVD risk, no prior INSTI exposure, no prior outcome of interest |
| **Intervention** | Switch to an INSTI-containing ART regimen within the 60-day baseline window |
| **Comparator** | Remain on non-INSTI ART regimen (PI- or NNRTI-based) |
| **Outcomes** | Incident obesity, diabetes, hypertension, MACE (cardiovascular death, MI, unstable angina, stroke, TIA, peripheral arterial ischaemia, revascularisation, undetermined-cause death) |
| **Time horizon** | Up to 5 years per emulated trial |
| **Causal contrast** | Intention-to-treat (ITT) effect of treatment assignment |

---

### Step 2: Data Sources

| Feature | Detail |
|---|---|
| **Database** | REPRIEVE (Randomized Trial to Prevent Vascular Events in HIV; NCT02344290) |
| **Countries** | 12 countries: USA, Botswana, Brazil, Canada, Haiti, India, Peru, South Africa, Spain, Thailand, Uganda, Zimbabwe |
| **Period** | Enrolment March 2015 – July 2019; follow-up through August 2023 |
| **Sample size** | 5,114 participants eligible for ≥1 emulated trial; 99,357 person-trials |
| **Linkages** | Longitudinal clinical measurements within REPRIEVE (lab values, BP, medications, clinical events) |

---

### Step 3: Eligibility Criteria

- Age 40–75 years
- On stable ART regimen ≥6 months at REPRIEVE enrolment
- CD4 count >100 cells/μL
- Low-to-moderate ASCVD risk
- No prior INSTI exposure
- No history of the specific outcome (obesity/diabetes/hypertension/MACE) at each trial baseline
- Participants from low/middle-income regions required INSTI availability (enrolled from 2018 onward)

---

### Step 4: Time Zero and Treatment Classification

- **Time zero**: End of the 60-day baseline window for each sequential trial (Day 0 of REPRIEVE + 60-day intervals)
- **Treatment classification**: If a participant switched to an INSTI-based regimen during days 0–59, classified as "switcher"; otherwise "non-switcher"
- **Sequential trials**: 37 trials emulated at 60-day intervals (Day 0 through Day 2160 of REPRIEVE)
- **ITT approach**: Participants retain their original assignment regardless of subsequent regimen changes

---

### Step 5: Confounder Adjustment

| Feature | Detail |
|---|---|
| **Method** | Inverse probability of treatment weighting (IPTW) using stabilised weights |
| **Weight model** | Logistic regression predicting probability of switching |
| **Covariates** | Sex at birth; age; race; enrolment region and year; alcohol, cigarette, substance use; diet quality; physical activity; total ART duration; nadir CD4 count; eGFR; statin randomisation group; ASCVD risk score; BMI at trial start; sequential trial number |
| **Balance assessment** | Standardised differences and means/SDs of stabilised IPTWs per trial |

---

### Step 6: Statistical Analysis

| Feature | Detail |
|---|---|
| **Primary model** | IPTW cause-specific Cox proportional hazard regression, pooled across all sequential trials |
| **Competing events** | Death treated as competing event |
| **Effect measure** | Hazard ratio (HR) — average over 5 years follow-up |
| **Confidence intervals** | Non-parametric bootstrapping (500 replicates); percentile-based 95% CIs |
| **Subgroups** | Overall, male (sex at birth), female (sex at birth) |
| **Software** | SAS 9.4, Linux |

---

### Step 7: Sensitivity Analyses

1. Additional adjustment for tenofovir alafenamide (TAF) use at trial baseline (TAF associated with weight gain)
2. Additional adjustment for tenofovir disoproxil fumarate (TDF) use (potential weight-suppressive effect)
3. Eligibility restricted to TDF users at baseline
4. Eligibility restricted to efavirenz users at baseline
5. Alternative weight-based obesity definitions

---

## Key Results

| Outcome | HR (95% CI) | Interpretation |
|---|---|---|
| **Incident obesity** | 1.41 (1.22–1.59) | 41% higher hazard in INSTI switchers |
| **Incident diabetes** | 1.50 (1.24–1.81) | 50% higher hazard |
| **Incident hypertension** | 1.45 (1.26–1.67) | 45% higher hazard |
| **MACE** | 1.17 (0.87–1.57) | No statistically significant effect |

- 80.9% of switchers initiated dolutegravir-based regimen
- Effect on obesity and diabetes was heightened in females
- Median follow-up: 5 years (up to 5 per emulated trial)

---

## Strengths

- Large global cohort (12 countries including low/middle-income settings) — rare for HIV TTE studies
- Sequential trial emulation with IPTW avoids immortal time bias and time-lag bias
- 5-year follow-up substantially exceeds prior studies (12–24 months)
- Clinical adjudication of MACE outcomes
- Pre-specified sensitivity analyses for TDF/TAF confounding
- Follows TTE framework rigorously; ITT contrast mirrors pragmatic trial

## Limitations

- Cannot fully exclude prior INSTI exposure (no full ART history in REPRIEVE)
- INSTI availability varied by region and time, limiting comparability of non-switchers in low-income regions (addressed by restricting eligibility from 2018)
- REPRIEVE enrolled low-to-moderate ASCVD risk population — may not generalise to higher-risk individuals
- Observational emulation: unmeasured confounders (e.g., provider preference for INSTI) may remain
- MACE analysis underpowered at 5 years (longer follow-up needed to detect cardiovascular harm)
- Weight data self-reported at some sites; BMI-based obesity thresholds vary by Asian ancestry
