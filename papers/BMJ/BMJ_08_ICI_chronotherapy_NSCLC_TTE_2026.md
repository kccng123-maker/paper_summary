# Morning versus Afternoon Administration of Immune Checkpoint Inhibitors in Metastatic Non-Small-Cell Lung Cancer

**Citation:** Gonzalez RT, Datta R, Rehmani S, Strohbehn GW, et al. Morning versus afternoon administration of immune checkpoint inhibitors in metastatic non-small-cell lung cancer. *Journal for ImmunoTherapy of Cancer (JITC).* 2026;14(5):e013830. doi:10.1136/jitc-2025-013830. Published 14 May 2026. [Open Access]

---

## Brief Summary

This study emulated a pragmatic randomised trial of morning (AM) versus afternoon (PM) immune checkpoint inhibitor (ICI) dosing in stage IV non-small-cell lung cancer (NSCLC) patients using Veterans Health Administration (VHA) electronic health records from 2010–2024. Among 4,688 eligible patients, those receiving the first three ICI infusions in the AM had a median overall survival of 10.3 months versus 8.1 months for PM dosing (HR for PM vs AM: 1.15, 95% CI 1.04–1.26; p=0.004). A negative control chemotherapy cohort of 7,951 patients showed no time-of-day effect (HR 1.05, 95% CI 0.98–1.12; p=0.15), supporting a specific ICI chronotherapeutic causal mechanism. The findings suggest that scheduling ICI infusions before noon is a low-cost, immediately actionable intervention warranting prospective randomised confirmation.

---

## Methodology

### Step 1: Causal Question as PICO Target Trial Specification

| Component | Specification |
|-----------|---------------|
| **Population** | Stage IV NSCLC patients receiving first-line or second-line ICI therapy at VHA facilities, 2015–2024 |
| **Intervention** | Morning ICI infusions: all first three infusions received before 12:00 PM |
| **Comparator** | Afternoon ICI infusions: all first three infusions received at or after 12:00 PM |
| **Outcome** | Primary: Overall survival (OS); Secondary: Progression-free survival (not reported in abstract) |
| **Time zero** | Date ICI therapy was ordered in the electronic health record (proxy for randomisation) |
| **Follow-up** | Administrative follow-up through end of VHA data; median 4.7 years |
| **Causal contrast** | Per-protocol effect estimated via marginal structural models with IPCW |
| **Negative control** | Contemporaneous chemotherapy cohort (same eligibility criteria, chemotherapy order as time zero) |

### Step 2: Data Sources

| Feature | Detail |
|---------|--------|
| **Database** | VHA Corporate Data Warehouse (CDW) |
| **Type** | Electronic medical records — nationwide Veterans Health Administration |
| **Country** | United States |
| **Period** | 2010–2024 (ICI cohort: 2015–2024) |
| **ICI cohort N (eligible)** | 4,688 |
| **ICI cohort N (AM)** | 1,171 (first three infusions before noon) |
| **ICI cohort N (PM)** | 794 (first three infusions at/after noon) |
| **Chemotherapy negative control N** | 7,951 |
| **ICI median follow-up** | 4.7 years |
| **Chemo median follow-up** | 8.9 years |

### Step 3: Eligibility Criteria

**Inclusion (ICI cohort):**
- Stage IV NSCLC
- First-line or second-line ICI therapy ordered at VHA
- 2015–2024 (ICI era)

**Exclusion (ICI cohort):**
- Prior ICI therapy
- Received <1 infusion within 30 days of order (protocol deviation)

**Protocol deviations defined as:**
- ≥1 of first three infusions outside assigned timing window (AM/PM), OR
- Failure to receive ≥1 infusion within 30 days of ICI order

*Note: Patients receiving only 1–2 total infusions were NOT considered deviators if those infusions matched assigned timing.*

### Step 4: Time Zero and Treatment Classification

- **Time zero:** Date of ICI therapy order in EHR (proxy for the moment a patient would have been "randomised" in the hypothetical RCT)
- **Treatment classification:**
  - *AM arm:* First three ICI infusions all delivered before 12:00 PM
  - *PM arm:* First three ICI infusions all delivered at or after 12:00 PM
- **Rationale for first three infusions:** Prior studies suggest the early immunopriming period (first ~6–9 weeks) is critical for establishing antitumor immune responses
- **Protocol deviation handling:** Per-protocol analysis — deviators censored at time of deviation

### Step 5: Confounder Adjustment

| Method | Detail |
|--------|--------|
| **Primary** | Marginal structural models (MSM) with inverse probability of censoring weights (IPCW) |
| **Baseline confounders** | Age, sex, race/ethnicity, smoking history, ECOG performance status, stage, histology (adenocarcinoma vs squamous), treatment line (1st vs 2nd), calendar year, VHA facility |
| **Time-varying confounders** | Hospitalisation during treatment, dose delays, comorbidity changes affecting subsequent infusion timing |
| **Longitudinal confounding** | Addressed by time-varying IPCW updating at each infusion |
| **Immortal time bias** | Eliminated by defining time zero as ICI order date, not first infusion date |

### Step 6: Statistical Analysis

| Element | Detail |
|---------|--------|
| **Primary model** | Weighted Cox proportional hazards regression (MSM-IPCW) |
| **Effect measure** | Hazard ratio for PM vs AM with 95% CI |
| **Censoring** | Administrative censoring; IPCW accounts for informative censoring |
| **Negative control** | Same MSM-IPCW applied to chemotherapy cohort to detect non-specific time-of-day confounding |
| **Kaplan-Meier** | Marginal survival curves plotted for AM vs PM arms |

### Step 7: Sensitivity Analyses

1. **Alternate timing thresholds** — varied AM/PM cutoff (e.g., 10 AM, 2 PM)
2. **Extended exposure window** — varied number of defining infusions (e.g., first two or first five)
3. **Subgroup analyses** — by ICI agent class, treatment line, histology
4. **Chemotherapy negative control** — key internal validity check: no significant time-of-day effect in chemotherapy (HR 1.05, 95% CI 0.98–1.12; p=0.15)
5. **Calendar year stratification** — to account for secular changes in ICI use and scheduling patterns

---

## Key Results Table

| Cohort | Outcome | AM Median Survival | PM Median Survival | HR PM vs AM (95% CI) | p-value |
|--------|---------|-------------------|--------------------|----------------------|---------|
| **ICI (primary)** | **Overall survival** | **10.3 months** | **8.1 months** | **1.15 (1.04–1.26)** | **0.004** |
| Chemotherapy (negative control) | Overall survival | — | — | 1.05 (0.98–1.12) | 0.15 |
| Sensitivity analyses | Overall survival | — | — | Consistent | Robust |

*HR >1 = worse survival with PM dosing (PM as the "exposed" group).*

---

## Strengths

1. **Largest TTE of ICI chronotherapy to date** — 4,688 patients from a national VHA database
2. **Marginal structural model with IPCW** — directly addresses time-varying confounding, protocol deviation, and informative censoring; prior studies used simple regression
3. **Explicitly eliminates immortal time bias** — time zero set at ICI order date, not first infusion
4. **Chemotherapy negative control cohort** — methodological gold standard for ruling out non-specific time-of-day confounding (e.g., healthier patients scheduled in AM in general)
5. **Long median follow-up** (4.7 years) — sufficient to assess OS
6. **National VHA dataset** — large, geographically diverse; standardised EHR data
7. **Per-protocol analysis** — estimates effect of actual adherence to AM dosing, not just assignment
8. **Open access** with full methods transparency

## Limitations

1. **VHA population** — predominantly male veterans; may not generalise to women or civilian populations
2. **Residual confounding** — patients scheduled in AM vs PM may differ in unmeasured ways: rural vs urban residence, transportation access, caregiver support, functional status not captured in EHR
3. **ICI timing reflects scheduling convenience**, not planned chronotherapy — complex selection forces may operate
4. **ICI agent heterogeneity** — different PD-1/PD-L1/CTLA-4 agents pooled; differential circadian effects not assessed
5. **No PD-L1 expression data** — major predictor of ICI response; not routinely available in VHA CDW at population level
6. **Effect size modest** — HR 1.15 (PM worse): clinically meaningful but small; scheduling changes in real infusion centres may have practical barriers
7. **Observational design** — despite MSM methodology, unmeasured confounders remain possible; prospective RCT confirmation required before policy change
8. **ICI cohort restricted to 2015+** — limited calendar time for newer agents (e.g., pembrolizumab approvals shifted over study period)

---

*File created: 2026-05-18 | Search window: 7-day filter | Journal: JITC (BMJ family)*
