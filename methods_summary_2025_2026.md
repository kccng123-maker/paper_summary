# Methodology Reference: Target Trial Emulation in BMJ / Lancet / JAMA / NEJM, 2025–2026

**Window:** 2025-01-01 → 2026-05-10
**Focus:** methodology, not topic. What design and analytic choices the high-impact journals are publishing and demanding from TTE manuscripts.
**Compiled:** 2026-05-10

---

## 1. The target-trial protocol — the seven required components

Every TTE in this window writes down two protocols side by side: a hypothetical *target trial* and its *emulation* in observational data. The TARGET Statement (Cashin/Hernán et al., BMJ 2025;390:e087179 / JAMA 2025; PMC13084563) standardizes the seven components:

1. **Eligibility criteria.** The population to which results apply.
2. **Treatment strategies.** Specified in enough detail to be implementable (point interventions vs. sustained strategies; dose; duration; switching rules).
3. **Assignment procedure.** In the *target* trial: random; in the *emulation*: classification based on observed data, conditional on baseline confounders (the conditional-exchangeability assumption replaces randomization).
4. **Follow-up start and end.** Follow-up *must* start at assignment.
5. **Outcomes.** Including how and when measured.
6. **Causal contrast(s).** ITT-analog vs. per-protocol; effect measures (HR, RD, RR).
7. **Identifying assumptions and analysis plan.** Including handling of missing data, censoring, competing events.

Every protocol component must be (a) specified for the target trial and (b) explicitly mapped to an operationalization in the data — TARGET items 6a–6h paired with 7a–7h.ii.

---

## 2. The TARGET Statement — 21-item reporting checklist (verbatim from PMC13084563)

### Abstract
- **1a.** Identify that the study attempts to emulate a target trial using observational data. State the study objectives and briefly summarize the specified target trial.
- **1b.** Report the data sources used for emulation.
- **1c.** Summarize key assumptions, statistical methods, findings and conclusions.

### Introduction
- **2 (Background).** Describe the scientific background of the study and the gap in knowledge.
- **3 (Causal question).** Summarize the causal question specified by the target trial protocol including the target population (eligibility criteria), treatment strategies compared, end of follow-up, and outcomes.
- **4 (Rationale).** Describe why the specific gap in knowledge (causal question) may be addressed by emulating a target trial (study design) with the available data.

### Methods
- **5 (Data sources).** Cite the data sources used for the analyses and for each one describe: original purpose, type, geographic locations, setting, time-period; describe linkage/pooling if any.
- **6a–6h (Target trial specification).**
  - **6a Eligibility** — describe the eligibility criteria.
  - **6b Treatment strategies** — describe in sufficient detail to allow implementation.
  - **6c Assignment** — eligible individuals would be randomly assigned; allocation may be unblinded.
  - **6d Follow-up** — starts at assignment; specify when it ends.
  - **6e Outcomes** — what, how, when measured.
  - **6f Causal contrasts** — including ITT effect, per-protocol effect, effect measures.
  - **6g Identifying assumptions** — for each estimand.
  - **6h Data analysis** — including modeling assumptions and missing-data handling.
- **7a–7h.ii (Emulation = mapping to data).**
  - **7a** how eligibility was ascertained in the data.
  - **7b** how each component of the treatment strategies was ascertained/defined.
  - **7c** how individuals were classified to each treatment strategy.
  - **7d** clarify follow-up starts at assignment; describe how end of follow-up was operationalized.
  - **7e** how outcomes were ascertained, including any differences from the target trial.
  - **7f** how causal contrasts were operationalized, including effect measures.
  - **7g.i** for each estimand, the assumptions made — explicitly including baseline confounding due to lack of randomization.
  - **7g.ii** how variables related to those assumptions were operationalized.
  - **7h.i** modifications to the target trial's analysis methods needed by the emulation.
  - **7h.ii** sensitivity analyses for choice of operationalizations, assumptions and analysis.

### Results
- **8 Participant selection** — assessed / eligible / assigned per strategy; flow diagram strongly recommended.
- **9 Baseline data** — characteristic distributions by strategy.
- **10 Follow-up** — length and reasons for end, by strategy and contrast.
- **11 Missing data** — frequency, by strategy.
- **12 Outcomes** — frequency or distribution, by strategy.
- **13 Effect estimates** — for each contrast, with precision; absolute and relative measures.
- **14 Additional analyses** — sensitivity results for operationalizations, assumptions and analysis.

### Discussion
- **15 Interpretation** — under the identifying assumptions, in light of precision.
- **16 Limitations** — explicitly the target-vs-emulation gap and assumption plausibility, including baseline confounding.

### Other information
- **17** Ethics. **18** Registration. **19** Data/code sharing. **20** Funding and funder role. **21** COIs.

**Innovations vs. STROBE/RECORD.** TARGET is the first reporting guideline that (a) requires self-identification as a TTE; (b) makes the *hypothetical* target-trial protocol a reportable object; (c) demands an explicit *mapping table* from protocol component → data operationalization; (d) elevates identifying assumptions (especially unmeasured confounding) to a top-level reporting requirement.

**Identifying assumptions the paper requires you to state.**
- **Conditional exchangeability** at baseline (no unmeasured confounding given measured covariates) — substitutes for randomization.
- **Positivity** — non-zero probability of each strategy at every confounder pattern.
- **Consistency / well-defined interventions** — the observed treatment value equals the counterfactual under that strategy.
- **Independent / informative censoring** assumptions for loss to follow-up, non-adherence, competing events.

---

## 3. Time-zero alignment — Fu et al., BMJ 2026

**Citation.** Fu EL, Harhay MO, Schneeweiss S, Desai RJ, Hernán MA. *Starting right: aligning eligibility and treatment assignment at time zero when emulating a target trial.* BMJ 2026;392:e084909 (PMID 41526041).

**Why this paper exists.** A 2025 systematic review (J Clin Epidemiol, Fu et al.) found **49% of 199 published TTEs misaligned** the times of eligibility / treatment assignment / start of follow-up, and **60% of those did not apply any analytic method to correct it.** Misalignment reintroduces the very biases TTE exists to prevent.

### 3.1 The single rule
Time zero ≡ the calendar moment when, *for that individual*: (i) eligibility is met, (ii) the treatment strategy is assigned, and (iii) follow-up begins. These three must coincide. If any piece uses post-baseline information, you have misalignment.

### 3.2 Misalignment patterns and the biases they create

| Misalignment pattern | Bias produced |
|---|---|
| Eligibility ascertained using data after t=0 (e.g., "had ≥6 months of follow-up") | Selection / immortal-time bias |
| Treatment strategy assigned using post-baseline data (e.g., "ever-user" or "received drug within 1 year") | Immortal-time bias; depletion of susceptibles |
| "Prevalent users" included instead of new users | Healthy-user / depletion-of-susceptibles bias |
| Follow-up starts before assignment is determinable | Immortal time before t=0 |
| Adjustment for variables measured after t=0 | Mediator/collider conditioning bias |

### 3.3 The three target-trial scenarios in the paper
The paper walks through *three increasingly complex target trials* and shows how to align all three timing elements in each. (Detail at the protocol level requires the full text; the structural takeaway is below.)

- **Scenario A — point intervention (single-time decision).** Both arms initiate or do not initiate at t=0. Alignment is straightforward: define eligibility and assignment at the same encounter; new-user, active-comparator design.
- **Scenario B — sustained strategy with deterministic continuation.** Strategy = "initiate and remain on treatment for X months." Patients who deviate must be handled, not excluded post-hoc. Solutions: per-protocol estimand with **inverse probability of censoring weights (IPCW)** for non-adherence.
- **Scenario C — strategy with a treatment-initiation window ("grace period").** Strategy = "initiate within K days of eligibility." A patient's treatment status during the grace period is ambiguous at t=0. Solutions: **clone-censor-weight (CCW)** — clone every eligible person into both strategies at t=0, censor a clone when its observed data become inconsistent with the assigned strategy, then up-weight surviving clones with IPCW.

### 3.4 Decision diagram (the paper's contribution)
Fu et al. provide a decision diagram that maps the structure of the treatment strategies to the appropriate analytic approach:

- **Strategies fully determined at t=0?** → standard new-user/active-comparator analysis (Scenario A).
- **Strategies require sustained behavior over time?** → per-protocol with IPCW for deviation (Scenario B).
- **Strategies have an initiation window / grace period?** → **clone-censor-weight** (Scenario C).
- **Strategies depend on time-varying conditions (e.g., treat-when-CD4-drops)?** → **g-methods** (parametric g-formula or sequential trial emulation) for the per-protocol effect.

### 3.5 What this means for the choice of causal contrast
- **ITT-analog effect** is identified under simpler assumptions but is sensitive to non-adherence; reasonable when adherence in the target trial would itself be imperfect.
- **Per-protocol effect** requires modeling deviations and applying IPCW or g-methods; needed when the policy question is about being-on-treatment.

---

## 4. Analytic methods seen across 2025–2026 TTEs in the four journals

### 4.1 Clone-censor-weight (CCW)
**Use when** the treatment strategy includes a grace period or an initiation window in which treatment status at t=0 is undefined.
**How.** (1) Clone each eligible patient at t=0, assign one clone to each strategy. (2) Artificially censor a clone the moment its observed data become incompatible with the assigned strategy. (3) Apply IPCW so that the remaining clones represent the original eligible population. CCW eliminates immortal time *by construction* because the clone-arms are identical at t=0.
**Where it shows up in 2025–2026.** Increasingly the default for "treat within X days" strategies; flagged by Fu et al. (BMJ 2026) as the recommended method for Scenario C; also appears in CMI 2025 COVID-19 TTE methods piece.

### 4.2 Inverse probability weighting — three flavors used in 2025–2026
- **IPTW (treatment weights, ATE).** Standard PS weighting for ATE.
- **SMR weighting (ATT).** Average treatment effect on the treated; used by Cai/Al-Aly group in the BMJ 2026 GLP-1 / SUD paper to retain the GLP-1-initiator population as the target.
- **Overlap weighting.** Down-weights extreme PS values; preserves an "overlap population" with strong covariate balance even with severe non-overlap. Used in Straub et al. BMJ 2026 (prenatal antiseizure) and Cho et al. BMJ 2026 (prenatal benzodiazepine).
- **IPCW.** For loss to follow-up, non-adherence, and CCW censoring.

### 4.3 Active-comparator / new-user design (NUACD)
The default frame in this window. Required ingredients:
- Restrict to *initiators* of the treatment of interest, not prevalent users.
- Compare to *initiators of an active comparator* drug used for the same indication, not unexposed.
- t=0 = first dispensing of either drug.
**Effect.** Eliminates prevalent-user bias and the bulk of confounding-by-indication; mandatory in Lin et al. BMJ 2025 (OAC for VTE), Hong et al. BMJ 2025 (SGLT-2i), Cai NEJM 2025 (Covid VE; flu-only as comparator), Cai BMJ 2026 (GLP-1 vs SGLT-2i), Straub BMJ 2026 (lamotrigine as active comparator).

### 4.4 Grace period and per-protocol estimand specification
Concrete numbers used in this window:
- **30 days** to define discontinuation refill gap (Lin et al., OAC).
- **3 months** initiation window after diagnosis (Zhang et al., ADHD; Cai et al., GLP-1).
- Per-protocol effects are estimated by IPCW for deviation; ITT-analog effects by classifying at t=0 and ignoring subsequent deviation.

### 4.5 Negative AND positive control outcomes (paired controls)
Single-sided controls are no longer accepted as sufficient. Hong et al. BMJ 2025 is the textbook pair:
- **Positive control:** genital infections, expected to be elevated by SGLT-2i (HR 2.78) — confirms detectability.
- **Negative control:** herpes zoster, expected to be null (HR ≈ 1.03) — confirms absence of broad residual confounding.
Krüger et al. JAMA 2025 prespecifies negative-control outcomes alongside the primary endpoint.

### 4.6 Trial-benchmarking design (emulate the RCT before going beyond it)
Krüger/Schneeweiss et al. JAMA 2025: build five cohorts. **Two emulate existing RCTs (STEP-HFpEF DM, SUMMIT) within trial-eligible patients.** If the emulation reproduces the RCT effect, the **three expansion cohorts** that go beyond trial inclusion criteria carry credibility transferred from that calibration. This is becoming a standard credibility argument when an RCT exists.

### 4.7 Triangulation with within-family / sibling controls
Cho et al. BMJ 2026 (prenatal benzodiazepine): primary analysis with PS overlap weighting, sensitivity with **sibling-controlled analysis** to address shared familial confounding. When TTE assumptions (no unmeasured baseline confounding) are doubtful, sibling/within-family designs are the preferred orthogonal robustness check.

### 4.8 Sequential trial emulation
For time-varying treatment decisions: re-emulate the target trial at each new eligibility time (each calendar month or each new clinical event), pool across the sequential trials, and use g-methods or IPTW with robust SEs. Mentioned as the recommended approach when treatment depends on time-varying triggers (Fu BMJ 2026 decision diagram).

### 4.9 Confounding-bias reduction beyond regression
- **PS overlap weighting** (Straub BMJ 2026, Cho BMJ 2026, multiple JAMA 2025 papers).
- **PS 1:1 matching** (Lin BMJ 2025) — preferred when overlap is good and a clean matched table is needed for transparency.
- **High-dimensional propensity scores (hdPS)** — implicit in the Schneeweiss-group papers (Krüger JAMA 2025).
- **E-values** for sensitivity to unmeasured confounding — referenced but not headlined in 2025–2026 in these four journals.

---

## 5. The required methodological self-checklist for a TTE manuscript in BMJ/Lancet/JAMA/NEJM (2026)

Use this as a pre-submission audit:

1. **Target trial protocol written out** with the 7 components (TARGET item 6).
2. **Mapping table** from each target-trial component to its data operationalization (TARGET item 7).
3. **Time zero defined** as the calendar instant when eligibility, assignment, and follow-up start coincide (Fu BMJ 2026).
4. **New-user, active-comparator** unless explicitly justified otherwise.
5. **Strategy class identified** (point / sustained / grace-period / dynamic) and the matching analytic method chosen accordingly (Fu decision diagram).
6. **Estimand named** — ITT-analog or per-protocol — and the corresponding identification strategy stated (IPCW for per-protocol, simpler intent classification for ITT-analog).
7. **Confounding control** — PS method declared (matching, IPTW, SMR, or overlap weighting), with covariate balance reported (TARGET item 9).
8. **Censoring assumptions** — independent vs. informative; if informative, IPCW with the censoring model specified.
9. **Paired control outcomes** — at least one negative and ideally one positive control prespecified.
10. **Trial benchmarking** if an RCT exists for the same question.
11. **Triangulation** — at least one orthogonal design (sibling, instrumental variable analog, alternative comparator) when feasible.
12. **Identifying assumptions** stated explicitly: conditional exchangeability, positivity, consistency, censoring (TARGET item 7g.i).
13. **Sensitivity analyses** for operationalizations, assumptions, and analysis (TARGET item 14).
14. **Limitations section** explicitly discusses target-vs-emulation gaps and unmeasured confounding (TARGET item 16).

---

## 6. Key references

**Methodology pieces (read in order)**
- Cashin AG, Hansford HJ, Hernán MA, et al. TARGET Statement. BMJ 2025;390:e087179. https://pubmed.ncbi.nlm.nih.gov/40903028/ — full text PMC13084563: https://pmc.ncbi.nlm.nih.gov/articles/PMC13084563/
- Cashin AG, Hansford HJ, Hernán MA, et al. TARGET Statement. JAMA 2025. https://pubmed.ncbi.nlm.nih.gov/40899949/
- Fu EL, Harhay MO, Schneeweiss S, Desai RJ, Hernán MA. Starting right: aligning eligibility and treatment assignment at time zero when emulating a target trial. BMJ 2026;392:e084909. https://pubmed.ncbi.nlm.nih.gov/41526041/
- Fu EL, et al. Review of methods to deal with the misalignment of times of eligibility, start of follow-up, and treatment assignment in studies explicitly aimed at emulating target trials. J Clin Epidemiol 2025. https://www.jclinepi.com/article/S0895-4356(25)00231-8/fulltext

**Editorial framing of causal inference (BMJ series, 2025–2026)**
- Feeney T, Zivich PN. Causal inference is hard, and advanced statistical analysis is not enough. BMJ 2025. PMID 41402049.
- Broadbent A. Explaining the facts before us: the challenge of causal inference. BMJ 2025. PMID 41402056.
- Feeney T, Islam N, Kurth T. Guiding causal inference research in general medical journals. BMJ 2026. PMID 41702645.
- Ludwig DS, Willett WC, Putt ME. Wash-in and washout effects: mitigating bias in short term dietary and other trials. BMJ 2025. PMID 40262831.

**Methodologically informative applied TTEs (cite for design templates)**
- Lin KJ et al. OAC for unprovoked VTE — TTE with PS 1:1 matching, 30-day grace. BMJ 2025. PMID 41224478.
- Zhang L et al. ADHD drugs — Swedish-register TTE, 3-month initiation window, recurrent-event analysis. BMJ 2025. PMID 40803836.
- Cai M et al. GLP-1 RA vs SGLT-2i for SUD — eight parallel new-user active-comparator TTEs, SMR-weighted Cox. BMJ 2026. PMID 41781010.
- Krüger N, Schneeweiss S et al. Sema/Tirze in HFpEF — five-cohort design with 2 RCT-benchmark cohorts and 3 expansion cohorts; prespecified negative controls. JAMA 2025. PMID 40886075.
- Hong B et al. SGLT-2i and autoimmune rheumatic diseases — paired positive (genital infections) and negative (herpes zoster) controls. BMJ 2025. PMID 41093607.
- Straub L et al. Prenatal antiseizure drugs — PS overlap weighting, lamotrigine active comparator. BMJ 2026. PMID 41813017.
- Cho Y et al. Prenatal benzodiazepine/Z-hypnotic — PS overlap weighting + sibling-controlled triangulation. BMJ 2026. PMID 42055584.
- Cai M et al. Covid-19 VE in veterans — flu-vaccine-only active comparator, IPTW, VE = 1−RR. NEJM 2025. PMID 41061231.
