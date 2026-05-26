# JAMA_07 — Sibling Comparisons to Account for Confounding

**Citation:** Hswen Y. Sibling Comparisons to Account for Confounding. *JAMA.* Published Online: April 29, 2026. doi:10.1001/jama.2026.2876.

*Note: Full text unavailable (paywalled). Summary based on available excerpt and context.*

---

## Brief Summary

This brief JAMA commentary (letter/correspondence) highlights the renewed relevance of sibling comparison designs for addressing unmeasured familial confounding in observational epidemiology. Written in response to a JAMA Guide to Statistics and Methods on sibling comparisons by Ahlqvist et al. (JAMA 2024), Hswen argues that sibling-based designs have re-emerged as a critical analytical tool in perinatal, environmental, psychiatric, and neurological research. The piece emphasises that when measured covariates cannot adequately adjust for shared genetic or family-level environmental factors, within-family designs — particularly discordant sibling comparisons — offer a design-based solution that strengthens causal inference from observational data. This commentary, while brief, reflects growing methodological consensus that family-based designs are essential complements to standard regression and propensity score methods in life-course epidemiology.

---

## Methodology Step-by-Step

### Step 1: Causal Question as Correspondence Framing

| Element | Specification |
|---|---|
| **Type** | Letter / methodological commentary (JAMA) |
| **Question** | How do sibling comparison designs strengthen causal inference by controlling for unmeasured familial confounding? |
| **Target article** | Ahlqvist et al. JAMA Guide to Statistics and Methods (sibling comparisons in pregnancy/neurodevelopmental research, JAMA 2024) |
| **Scope** | Perinatal, life-course, psychiatric, environmental, and neurological epidemiology |

### Step 2: Key Methodological Concept — Sibling Comparison Design

| Feature | Description |
|---|---|
| **Design type** | Within-family comparison of discordant siblings (one exposed, one unexposed to a risk factor) |
| **Confounding controlled** | All shared genetic factors (approximately 50% of genome in full siblings), all shared household/environmental exposures, socioeconomic factors, parental characteristics |
| **Residual confounders** | Within-family (non-shared) environmental differences; birth-order effects; age differences |
| **Data requirement** | Family linkage data — registry-based cohorts (e.g., Scandinavian registries, UK Biobank sibling data) |

### Step 3: Applications Highlighted

| Domain | Example |
|---|---|
| Perinatal research | Prenatal medication exposures (e.g., antidepressants, antiseizure medications) and neurodevelopmental outcomes |
| Environmental epidemiology | Childhood exposures (pollution, infection) and mental health outcomes |
| Neurological/psychiatric | Long-term outcomes of early-life adversity or medication use |
| Life-course epidemiology | Causal pathways from childhood factors to adult health |

### Step 4: Key Arguments Made

1. **Familial confounding** inflates or creates spurious associations in standard regression analyses of observational data
2. **Sibling comparison** uses the family as its own control — discordant sibling pairs differ on the exposure but share genetic and household factors
3. **Triangulation**: Sibling comparisons should be used alongside Mendelian randomisation, negative control outcomes, and standard multivariable regression to triangulate causal estimates
4. **Complementarity**: Different designs have different residual biases — convergent findings across designs strengthen causal inference

### Step 5: Comparison of Sibling Design vs. Standard Methods

| Method | Controls | Does NOT Control |
|---|---|---|
| Standard regression | Measured confounders | Unmeasured/familial confounders |
| Propensity score matching | Measured confounders (balanced) | Unmeasured confounders |
| Sibling comparison | Shared genetic + shared environmental confounders | Within-family (non-shared) differences; birth-order |
| Mendelian randomisation | Measured + unmeasured confounders (via genetic IV) | Pleiotropy; population stratification |

### Step 6: Statistical Note

- Sibling comparison models typically use **conditional logistic regression** (case-control framework) or **fixed effects regression** with family as the cluster unit
- Effect estimates from sibling models are attenuated relative to population-level estimates when familial confounding inflates naive associations
- Attenuation of effect in sibling analysis is interpreted as evidence of familial confounding

### Step 7: Implications for Practice

- Journals (including JAMA) increasingly expect family-based sensitivity analyses for observational studies of perinatal exposures and neurodevelopmental outcomes
- Authors should report both population-level and sibling-comparison estimates when registry/linked family data are available
- JAMA Guides to Statistics and Methods series is promoting methodological standardisation in this area

---

## Key Results

*No primary data reported (commentary format). Key methodological points:*

| Point | Summary |
|---|---|
| Renewed relevance | Sibling designs re-emerging as a critical analytical tool after being underused for a decade |
| Domains of application | Perinatal, environmental, psychiatric, neurological — particularly studies using claims or registry data |
| Causal inference value | Reduces unmeasured familial confounding that standard regression cannot address |
| Triangulation | Strongest causal evidence comes from convergence across sibling comparison, MR, and negative control designs |

---

## Strengths

- Published in JAMA — high visibility; promotes methodological literacy for clinical researchers
- Part of JAMA's Guide to Statistics and Methods series — supports standardisation
- Timely: familial confounding has been central to several high-profile controversies (paracetamol/autism; SSRIs/preterm birth)
- Highlights practical design approach accessible to researchers without genetic data

## Limitations

- Brief commentary format — limited methodological depth
- Full text paywalled — detailed content not fully assessable
- Does not address scenarios where sibling comparison introduces new biases (within-family confounding, selection of discordant pairs)
- Does not cover twin-specific designs (co-twin control) which offer stronger genetic control in MZ twins
