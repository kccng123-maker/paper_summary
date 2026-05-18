# Emulated Trial of Artificial Intelligence Use and Subsequent Depressive Outcomes in a Survey of US Adults

**Citation:** Perlis RH, Gunning FM, Uslu A, et al. Emulated trial of artificial intelligence use and subsequent depressive outcomes in a survey of US adults. *BMJ Mental Health.* 2026;29(1):e302609. doi:10.1136/bmjment-2025-302609. Published online 13 May 2026. [Open Access]

---

## Brief Summary

This study applied target trial emulation (TTE) to a nationally representative longitudinal US survey to estimate the causal effect of frequent generative AI use on depressive symptoms. Among 19,099 adults surveyed at baseline, 2,862 (15%) reported high-frequency AI use (multiple times/week or more). In the primary weighted analysis among 3,109 participants with follow-up data, high-frequency AI use was not significantly associated with change in PHQ-9 depression score (mean difference −0.18, 95% CI −0.94 to 0.59; p=0.65). Multiple sensitivity analyses and causal forest heterogeneity testing confirmed null findings. The study directly challenges widely circulated concerns that AI use causes depression at the population level, while acknowledging inability to exclude harms in vulnerable subgroups.

---

## Methodology

### Step 1: Causal Question as PICO Target Trial Specification

| Component | Specification |
|-----------|---------------|
| **Population** | US adults ≥18 years, nationally representative sample via internet survey panel |
| **Intervention** | High-frequency generative AI use (≥multiple times per week at baseline) |
| **Comparator** | Low-frequency AI use (≤once per week at baseline) |
| **Outcome** | Primary: PHQ-9 depressive symptom score at follow-up; Secondary: alternate depression definitions |
| **Time zero** | Wave 32 survey completion (Jun–Jul 2024) |
| **Follow-up** | Wave 33 (Aug–Oct 2024) or Wave 34 (Nov 2024–Jan 2025); first return visit used |
| **Causal contrast** | Per-protocol intention-to-treat equivalent with inverse probability weighting |

### Step 2: Data Sources

| Feature | Detail |
|---------|--------|
| **Survey** | Civic Health and Institutions Project (CHIP-50) |
| **Type** | Non-probability internet survey with reweighting for representativeness |
| **Country** | United States (50 states + DC) |
| **Waves used** | Wave 32 (baseline), Wave 33 & 34 (follow-up) |
| **Baseline period** | 18 June – 21 July 2024 |
| **Follow-up period** | 30 August 2024 – 8 January 2025 |
| **N at baseline** | 19,099 |
| **N at follow-up** | 3,109 (16.3% return rate) |
| **Panel aggregator** | PureSpectrum (commercial survey panel) |

### Step 3: Eligibility Criteria

**Inclusion:**
- Age ≥18 years
- US resident (any of 50 states or DC)
- Completed baseline survey (Wave 32)
- Responded to AI use frequency question

**Exclusion:**
- Failed attention checks (automated/inattentive responses)
- Missing baseline AI use data
- Did not return for follow-up (handled via attrition weighting)

### Step 4: Time Zero and Treatment Classification

- **Time zero:** Date of Wave 32 survey completion
- **Exposure classification:**
  - *High-frequency (treated):* AI use "multiple times per week," "every day," or "multiple times per day"
  - *Low-frequency (comparator):* AI use "never," "once or twice," "about once a month," or "about once a week"
- **Exposure ascertainment:** Self-report; single item "How often do you use artificial intelligence (AI)?" with 7-point ordinal response scale
- **Alternative phrasing:** Parallel question using "generative AI / large language models" — results nearly identical, primary question used

### Step 5: Confounder Adjustment

| Method | Detail |
|--------|--------|
| **Primary** | Inverse probability weighting (IPW) with survey-design weights |
| **Attrition weights** | Modelled probability of returning for follow-up based on baseline characteristics |
| **Covariates (treatment model)** | Age, sex, race/ethnicity, education, employment, political affiliation, baseline PHQ-9 score, prior mental health diagnoses, social media use, technology use |
| **Covariates (attrition model)** | Same set as treatment model |
| **Combined weight** | Product of treatment and attrition weights |
| **Heterogeneity** | Generalised causal forests (GCF) to detect subgroup effect modification |

### Step 6: Statistical Analysis

| Element | Detail |
|---------|--------|
| **Primary model** | Weighted linear regression of PHQ-9 change score on AI use group |
| **Effect measure** | Mean difference in PHQ-9 change with 95% CI |
| **Causal heterogeneity** | Generalised causal forests (GCF); calibration p-value for CATE heterogeneity |
| **Survey weighting** | Applied to correct for non-probability sampling design |
| **Software** | R (implied by GCF methodology; not explicitly stated) |

### Step 7: Sensitivity Analyses

1. **Alternate outcome definitions** — different PHQ-9 thresholds and binary depression indicators
2. **Alternate exposure thresholds** — daily vs non-daily AI use
3. **Subgroup analysis via GCF** — tested whether any identifiable subgroup showed significant treatment effect heterogeneity (p=0.81; no evidence found)
4. **Multiple follow-up waves** — Wave 33 and Wave 34 separately (only first return used in primary)

---

## Key Results Table

| Outcome | High AI Use | Low AI Use | Effect (95% CI) | p-value |
|---------|------------|------------|-----------------|---------|
| **PHQ-9 change (primary)** | — | — | **MD −0.18 (−0.94 to 0.59)** | 0.65 |
| Alternate outcome definitions | — | — | Non-significant | — |
| GCF CATE heterogeneity | — | — | p=0.81 (no heterogeneity) | — |

*Negative MD indicates lower PHQ-9 (fewer symptoms) with high AI use; result is null and clinically trivial.*

---

## Strengths

1. **TTE framework** applied to longitudinal survey data — explicitly addresses the causal inference gap in prior cross-sectional AI/mental health studies
2. **Nationally representative** sample with state-level quotas by age, sex, and race/ethnicity; inverse probability weighting applied
3. **Both treatment and attrition confounding** modelled simultaneously via product weights
4. **Generalised causal forests** provide a principled test for subgroup heterogeneity rather than post-hoc subgroup testing
5. **Multi-wave longitudinal design** — clear temporal ordering (exposure precedes outcome measurement)
6. **Open access** — full methods transparent and reproducible
7. Directly addresses a high-profile public concern about AI and mental health with appropriate methodology

## Limitations

1. **Non-probability internet survey** — opt-in panel may not capture those without internet access, very elderly, or most vulnerable populations despite quota reweighting
2. **Low follow-up rate (16.3%)** — substantial attrition; attrition weights may not fully recover a representative retained sample
3. **Self-reported AI use** — no objective measure of frequency, duration, or type of AI interaction (ChatGPT vs others)
4. **Short follow-up** (1–7 months) — insufficient to detect long-term effects on mental health trajectories
5. **PHQ-9 is not diagnostic** of depression — symptom scale captures severity but cannot establish clinical depression
6. **No measure of AI use content** — beneficial vs harmful interactions not distinguished; someone using AI for creative writing differs from someone in harmful parasocial relationships
7. **Excludes non-users entirely** — causal contrast is high-frequency vs low-frequency, not AI use vs no use
8. **Residual confounding** possible — people who use AI frequently may differ in unmeasured ways (digital literacy, socioeconomic stability, employment)

---

*File created: 2026-05-18 | Search window: 7-day filter | Journal: BMJ Mental Health (BMJ family)*
