# BMJ_09 — Concordance between Target Trial Emulation and RCTs: Systematic Review and Meta-analysis

**Citation:** Wang C, Tang D, von Dadelszen P, Ju C, Liu L, Wang Y, Magee LA. Concordance between target trial emulation and randomised controlled trials: systematic review and meta-analysis. *BMJ.* 2026;393:e086810. doi:10.1136/bmj-2025-086810. Published 19 May 2026.

---

## Brief Summary

This systematic review and meta-analysis assessed how closely target trial emulations (TTEs) reproduce effect estimates from their benchmarking randomised controlled trials (RCTs), analysing 107 TTE–RCT pairs identified from five databases (2010–2025). Overall concordance was moderate (Pearson r = 0.59; 79% standardised difference agreement; ratio of ratios 0.96, 95% CI 0.92–1.01). When restricted to 63 pairs with closer emulation of trial design, concordance improved substantially (r = 0.83; 87% agreement). TTEs systematically underestimated effects for VTE and MACE outcomes, and overestimated effects for respiratory outcomes; emulations using claims data showed a tendency to underestimate treatment effects. The findings provide the most comprehensive empirical evidence to date on TTE validity, identify key determinants of emulation success, and offer actionable guidance for improving TTE design quality.

---

## Methodology Step-by-Step

### Step 1: Causal Question as PICO / Target Trial Specification

| Element | Specification |
|---|---|
| **Study type** | Systematic review and meta-analysis (not a primary TTE) |
| **Question** | Do TTEs of drug/device/surgical interventions reproduce RCT effect estimates, and what design features predict concordance? |
| **Population** | TTE–RCT pairs across any therapeutic area and population |
| **Intervention** | Drug, surgical procedure, or medical device (as in the emulated trials) |
| **Comparator** | Active comparator or placebo/standard care (as specified in benchmarking RCT) |
| **Outcome** | Concordance of effect estimates: Pearson r, standardised difference agreement, ratio of ratios |
| **Time horizon** | TTE publications 2010–2025 |

### Step 2: Data Sources

- **Databases searched:** MEDLINE, EMBASE, Scopus, PsycINFO, Web of Science
- **Search period:** 1 January 2010 – 1 October 2025
- **Inclusion:** Observational studies explicitly aiming to emulate a specified benchmarking RCT of a health intervention
- **Exclusion:** Emulations of hypothetical trials; emulations not specifying the target RCT; behavioural, lifestyle, policy, financial, or educational interventions
- **Registration:** PROSPERO CRD42024619811

### Step 3: Eligibility Criteria

- Published in English
- Explicitly stated aim to emulate a specified benchmarking RCT
- Health intervention: drugs, surgical procedures, or medical devices
- No restriction on therapeutic area, geography, or data source

### Step 4: Time Zero and Treatment Classification

- Each included TTE defined its own time zero (treatment initiation or randomisation date analogue)
- 21 predefined emulation design features were extracted and assessed for concordance with the benchmarking RCT protocol

### Step 5: Confounder Adjustment

- **Extracted features:** Baseline population balance, covariate adjustment methods, active comparator use, linkage to multisource databases
- **Key finding:** Imbalanced baseline population characteristics were associated with poorer concordance
- **Regression analyses:** Univariate regression of 21 design features against concordance metrics

### Step 6: Statistical Analysis

- **Primary concordance metrics:**
  - Pearson correlation coefficient of log-transformed effect estimates
  - Standardised difference agreement (within ±0.25 SD of RCT estimate)
  - Ratio of ratios (TTE effect estimate / RCT effect estimate), meta-analysed with random effects
- **Subgroup analyses:** By outcome type (VTE, MACE, respiratory, other), data source (claims vs. electronic health records vs. linked databases), intervention type

### Step 7: Sensitivity Analyses

- Restricted analysis to 63 pairs with closer design emulation (pre-specified subgroup)
- Domain-specific subgroups (VTE, MACE, respiratory outcomes)
- Data source subgroups (claims-based vs. other)
- Univariate regression of 21 individual design features against concordance

---

## Key Results Table

| Analysis | Metric | Estimate (95% CI) | I² |
|---|---|---|---|
| All 107 TTE–RCT pairs | Pearson r | 0.59 (0.45–0.70) | — |
| All 107 pairs | Standardised difference agreement | 79% (85/107) | — |
| All 107 pairs | Ratio of ratios | 0.96 (0.92–1.01) | 36% |
| 63 closer-design pairs | Pearson r | 0.83 (0.73–0.89) | — |
| 63 closer-design pairs | Standardised difference agreement | 87% (55/63) | — |
| VTE outcomes | Ratio of ratios | 0.76 (0.58–1.00) | 40% |
| MACE outcomes | Ratio of ratios | 0.91 (0.86–0.96) | 32% |
| Respiratory outcomes | Ratio of ratios | 1.20 (1.03–1.40) | 40% |
| Claims-based data | Ratio of ratios | 0.90 (0.82–0.99) | 38% |

**Predictors of poorer concordance (univariate regression):**
- Imbalanced baseline population characteristics
- Treatment started in hospital (not captured in claims)
- Lower outcome emulation quality

---

## Strengths

- Most comprehensive quantitative synthesis of TTE–RCT concordance to date (107 pairs vs. 32 in prior work)
- Broad scope: multiple therapeutic areas, diverse data sources, geographical settings
- Pre-specified 21 design features systematically assessed
- PROSPERO-registered; PRISMA-reported
- Provides actionable guidance: linked multisource databases and closer design emulation improve concordance

## Limitations

- Full text unavailable for some emulation studies; concordance features partially based on reported information
- Univariate (not multivariable) regression limits causal interpretation of design-feature associations
- Restricted to published, English-language papers — publication bias may overestimate concordance
- Heterogeneous definitions of "concordance" across primary studies
- Excludes non-drug interventions (behavioural, lifestyle, policy), limiting generalisability
- Cannot distinguish residual confounding from design deficiencies as drivers of discordance
