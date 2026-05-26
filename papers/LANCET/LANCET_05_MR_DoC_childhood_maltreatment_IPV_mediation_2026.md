# LANCET_05 — Personality and Mental Health as Mediators Linking Childhood Maltreatment to IPV Victimization: MR-DoC Twin Study

**Citation:** Pezzoli P, Barkhuizen W, Oginni O, Pingault J-B, McCrory E, Viding E. Personality and mental health as mediators linking childhood maltreatment to intimate partner violence victimization: a Mendelian randomization–direction of causation twin study. *The Lancet Regional Health – Europe.* 2026;66:101653. doi:10.1016/S2666-7762(26)00065-7. Published online March 2026 (Volume 66, July 2026 issue). [Open Access]

---

## Brief Summary

This study examined whether personality and mental health traits mediate the causal pathway from childhood maltreatment to intimate partner violence (IPV) victimization in young adults, using data from the UK Twins Early Development Study (N = 11,342, age 22). Using a novel Mendelian Randomization–Direction of Causation (MR-DoC) twin model that adjusts for shared genetic and environmental confounding, the authors found that 65% of the maltreatment–IPV association is mediated through personality and mental health intermediaries — specifically low well-being, conduct problems, and aggression. These findings demonstrate that the maltreatment–IPV link is not wholly attributable to shared genetic liability, and that causal mediation operates through modifiable psychological pathways. The study informs targeted prevention strategies for IPV in young people exposed to childhood maltreatment.

---

## Methodology Step-by-Step

### Step 1: Causal Question as PICO / Target Trial Specification

| Element | Specification |
|---|---|
| **Exposure** | Childhood maltreatment (abuse/neglect by parent or caregiver) |
| **Mediators** | 18 personality and mental health intermediary phenotypes (incl. well-being, aggression, conduct problems, depression, anxiety, impulsivity) |
| **Outcome** | Intimate partner violence (IPV) victimization at age 22 |
| **Population** | UK young adults, population-based twin cohort |
| **Causal question** | Does maltreatment causally increase IPV risk through personality/mental health, beyond shared genetic and environmental confounding? |
| **Design** | MR-DoC twin model; also structural equation modeling and twin modeling |

### Step 2: Data Sources

| Feature | Detail |
|---|---|
| **Cohort** | UK Twins Early Development Study (TEDS) |
| **Country** | United Kingdom |
| **N** | N = 11,342 (full sample, age 22); genotyped subsample n = 8,406 |
| **Recruitment** | Population-based twin registry, born 1994–1996 |
| **GWAS data** | External GWAS summary statistics (Linkage Disequilibrium Score Regression for genetic correlations) |
| **Linkages** | Twin data + genome-wide genotyping + self-reported questionnaire measures |

### Step 3: Eligibility Criteria

- Same-sex and opposite-sex twin pairs in TEDS
- Aged 22 at assessment
- Genotyped subsample required valid genotype data passing QC
- Exclusions: missing data on key exposures/outcomes (handled by full information maximum likelihood)

### Step 4: Time Zero and Treatment Classification

- **Exposure time zero:** Retrospective self-report of childhood maltreatment (cumulative exposure up to age 16)
- **Outcome assessment:** IPV victimization at age 22 (concurrent with personality/mental health assessment)
- **Mediator assessment:** 18 personality/mental health traits measured at age 22 (cross-sectional with outcome, but temporally downstream of childhood exposure by design)

### Step 5: Confounder Adjustment

| Method | Details |
|---|---|
| **Twin modeling** | Separates genetic (A), shared environmental (C), and non-shared environmental (E) variance components |
| **Structural equation modeling (SEM)** | Phenotypic mediation model with 18 intermediaries condensed into 2 latent factors |
| **MR-DoC** | Mendelian Randomization–Direction of Causation model in genotyped twins; uses SNP instruments from GWAS to separate genetic confounding from causal effects |
| **LD Score Regression** | Estimates genetic correlations (rg) between maltreatment, IPV, and intermediary phenotypes |
| **Lived-experience input** | Community advisors informed design, variable selection, and interpretation |

### Step 6: Statistical Analysis

- **Effect measure:** Standardised regression coefficients (β); indirect effect (ab), direct effect (c')
- **SEM mediation:** Total indirect effect via 2 latent factors; % mediated
- **MR-DoC mediation:** Causal indirect and direct effects adjusting for genetic + environmental confounding
- **Individual mediator analyses:** Separate and simultaneous MR-DoC models for each of 18 phenotypes
- **Adjustment:** Multiple testing correction (FDR / padj reported)

### Step 7: Sensitivity Analyses

- SEM with individual mediators examined separately and simultaneously
- MR-DoC models repeated with individual mediators (separately and jointly)
- Heritability estimates from twin modeling (h²twin) compared with SNP heritability (h²SNP) from LDSC
- Genetic correlations cross-validated across maltreatment and IPV definitions
- Lived-experience validation of findings and interpretation

---

## Key Results Table

| Model | Estimate | Value | Significance |
|---|---|---|---|
| Phenotypic association: maltreatment → IPV | β | 0.23 | p < 0.001 |
| Heritability of maltreatment | h²twin | 17–31% | — |
| Heritability of IPV victimization | h²twin | 17–31% | — |
| SNP heritability (LDSC) | h²SNP | 1–4% | — |
| Genetic correlation: maltreatment–IPV | rg | 0.52–0.82 | — |
| SEM: total indirect effect (∑ab) | β | 0.11 (48% mediated) | padj < 0.001 |
| SEM: direct effect (c') | β | 0.12 | padj < 0.001 |
| MR-DoC: total indirect effect (∑ab) | β | 0.09 (65% mediated) | padj < 0.001 |
| MR-DoC: direct effect (c') | β | 0.05 | padj = 0.161 (NS) |
| Key individual mediators (robust across models) | ab | 0.01–0.05 | padj < 0.05 |
| — Low well-being | — | significant | — |
| — Conduct problems | — | significant | — |
| — Aggression | — | significant | — |

**Interpretation:** After accounting for shared genetic and environmental confounding (MR-DoC), 65% of the maltreatment–IPV association is causally mediated through personality/mental health traits; no significant direct effect remains.

---

## Strengths

- Novel MR-DoC twin design disentangles genetic confounding from causal mediation — methodologically rigorous
- Large, population-based twin cohort (N = 11,342) with genetic data
- 18 intermediary phenotypes examined — comprehensive mediator scope
- Complementary methods (SEM + twin modeling + MR-DoC + LDSC) allow triangulation
- Open access; lived-experience community involvement in design
- Identifies modifiable mediators (well-being, conduct problems, aggression) with prevention implications

## Limitations

- Cross-sectional measurement of mediators and outcome at age 22 — temporal ordering assumed, not directly tested
- Retrospective self-report of maltreatment — recall and reporting biases
- Low SNP heritability (1–4%) limits power of MR instruments; MR-DoC relies on polygenic score validity
- UK twin sample — may not generalise to ethnically diverse or lower-income populations
- IPV victimization only (not perpetration); bidirectional dynamics not captured
- Full text causal inference limited by observational nature despite genetic approaches
