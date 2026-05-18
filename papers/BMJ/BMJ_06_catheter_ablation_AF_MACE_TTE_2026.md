# Catheter Ablation and Risk of Major Adverse Cardiovascular Events in High-Risk Patients with Newly Diagnosed Atrial Fibrillation: A Target Trial Emulation

**Citation:** Ho CC, Lin KH, Lai CC, Tsai WW, Lu KH. Catheter ablation and risk of major adverse cardiovascular events in high-risk patients with newly diagnosed atrial fibrillation: a target trial emulation. *Heart.* 2026 May 7. doi:10.1136/heartjnl-2025-327113. [Epub ahead of print]

---

## Brief Summary

This study used a target trial emulation design to evaluate whether catheter ablation reduces major adverse cardiovascular events (MACE) in high-risk patients with newly diagnosed atrial fibrillation (AF). Using the TriNetX global federated electronic health record database, 263,329 patients with incident AF were identified, of whom 2,018 underwent catheter ablation. After 1:1 propensity score matching and a 1-year landmark analysis, catheter ablation was associated with a 58% lower risk of MACE (HR 0.42, 95% CI 0.29–0.60) and a 37% lower risk of heart failure (HR 0.63, 95% CI 0.49–0.80). The findings support early rhythm control via ablation as a potentially beneficial strategy for high-risk newly diagnosed AF patients, though the authors caution about the highly selected population undergoing ablation.

---

## Methodology

### Step 1: Causal Question as PICO Target Trial Specification

| Component | Specification |
|-----------|---------------|
| **Population** | Adults with newly diagnosed AF between Jan 2015–Apr 2022; no prior stroke, prior cardiovascular events, or valvular heart disease |
| **Intervention** | Catheter ablation (assigned at baseline) |
| **Comparator** | No catheter ablation (medical management) |
| **Outcome** | Primary: MACE (composite); Secondary: heart failure, stroke, all-cause mortality |
| **Time zero** | Date of AF diagnosis |
| **Follow-up** | 1-year landmark (Day 366 onward), primary analysis; 2-year sensitivity analysis |
| **Causal contrast** | Per-protocol effect of ablation vs no ablation |

### Step 2: Data Sources

| Feature | Detail |
|---------|--------|
| **Database** | TriNetX Global Collaborative Network |
| **Type** | Federated de-identified electronic health records |
| **Country** | Multi-national (predominantly USA) |
| **Period** | January 2015 – April 2022 |
| **N (eligible)** | 263,329 patients with incident AF |
| **N (ablation)** | 2,018 (0.8%) |
| **N (matched)** | 2,018 per arm (4,036 total) |
| **Linkages** | EHR data only; no external registry linkage reported |

### Step 3: Eligibility Criteria

**Inclusion:**
- Adults with newly diagnosed AF within study period
- First AF diagnosis during study window

**Exclusion:**
- Prior stroke
- Prior cardiovascular events (MI, HF, etc.)
- Valvular heart disease
- Patients without adequate follow-up data

### Step 4: Time Zero and Treatment Classification

- **Time zero:** Date of AF diagnosis
- **Landmark design:** Follow-up began at Day 366 to allow time for ablation to be performed and to avoid immortal time bias
- **Treatment classification:** Catheter ablation performed within the first year post-diagnosis vs no ablation
- **Exposure window:** First 365 days post-AF diagnosis

### Step 5: Confounder Adjustment

| Method | Detail |
|--------|--------|
| **Primary** | Propensity score matching (1:1, nearest-neighbour) |
| **Covariates** | Age, sex, comorbidities (hypertension, diabetes, CKD, heart failure, COPD), medications (anticoagulants, antiarrhythmics, beta-blockers), AF-related characteristics |
| **Balance check** | Standardised mean differences after matching (not reported in abstract) |

### Step 6: Statistical Analysis

| Element | Detail |
|---------|--------|
| **Primary model** | Cox proportional hazards regression in matched cohort |
| **Effect measure** | Hazard ratio (HR) with 95% confidence interval |
| **Censoring** | Administrative censoring at end of follow-up |
| **Software** | Not specified |

### Step 7: Sensitivity Analyses

1. **2-year follow-up sensitivity analysis** — extended landmark to assess durability of effect
2. **Subgroup analyses** — age, sex, AF risk score subgroups (specific subgroups not detailed in abstract)

---

## Key Results Table

| Outcome | Ablation (%) | No Ablation (%) | HR (95% CI) | p-value |
|---------|-------------|-----------------|-------------|---------|
| **MACE (primary)** | 2.1% | 5.0% | **0.42 (0.29–0.60)** | <0.001 |
| **Heart failure** | — | — | **0.63 (0.49–0.80)** | <0.001 |
| Sensitivity (2-year) | — | — | Consistent | — |

*Full text paywalled; subgroup HR estimates not available from abstract.*

---

## Strengths

1. **TTE framework** with landmark design explicitly avoids immortal time bias — a common flaw in prior ablation studies
2. **Large sample** from the TriNetX federated network spanning multiple institutions and countries
3. **Propensity score matching** balances measured confounders at baseline
4. **Pre-specified sensitivity and subgroup analyses** test robustness across follow-up duration and patient subgroups
5. Focuses specifically on **high-risk newly diagnosed AF** patients — a population with limited existing RCT evidence for ablation

## Limitations

1. **Full text paywalled** — detailed confounder list, balance tables, and subgroup HRs not accessible; summary from abstract only
2. **Only 0.8% underwent ablation** — highly selected population with likely unmeasured residual confounding (healthier, higher-functioning patients)
3. **No active-comparator** — comparison is ablation vs any non-ablation management, which is heterogeneous
4. **TriNetX federated network** — data completeness and coding accuracy vary by contributing institution; ICD coding may misclassify AF type (paroxysmal vs persistent)
5. **No information on AF burden** (paroxysmal vs persistent vs long-standing) or ablation technique — key effect modifiers
6. **Landmark design** introduces selection bias if patients who survive to Day 366 differ systematically by treatment arm
7. **Self-reported use of GPT-4** during manuscript preparation — authors note review of AI output

---

*File created: 2026-05-18 | Search window: 7-day filter | Journal: Heart (BMJ family)*
