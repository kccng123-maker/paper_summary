# When Evidence Meets Artificial Intelligence: AI, Target Trial Emulation, and the Future of Evidence-Based Medicine

**Citation:** Cruz-Suarez GA, Hincapié-Ayala D, Ocampo Osorio F, Gómez-Ayala MC, Alzate-Ricaurte S, Ariza F, Esteban S, Jeon S, Celi LA. **When evidence meets artificial intelligence.** *The Lancet Regional Health – Americas.* 2026;59:101472. doi:10.1016/j.lana.2026.101472. Published online April 20, 2026. [State-of-the-art Review]

---

## Brief Summary

This state-of-the-art Review asks how artificial intelligence (AI) is reshaping the methodological and ethical foundations of evidence-based medicine (EBM), and where causal-inference frameworks — particularly **target trial emulation (TTE)** — fit within an AI-augmented evidence ecosystem. The authors argue that classical trial-based EBM struggles to accommodate the scale, heterogeneity, and structural constraints of contemporary health systems, and that AI should be positioned as an *extension* of evidence generation rather than a replacement for epidemiologic reasoning. Drawing on a structured literature review, they map three principal channels through which AI interacts with EBM: multimodal data integration, target trial emulation over large-scale observational databases, and simulation-based ("virtual cohort") modelling. The central methodological message is that **predictive performance does not guarantee causal validity or clinical benefit** — strong discrimination/calibration of an AI model says nothing about whether acting on its outputs improves outcomes, which remains a causal question best disciplined by the target trial framework. The paper matters because it explicitly frames TTE as the bridge between data-rich AI prediction and the causal questions clinicians actually need answered, while warning that in the Americas fragmented health systems and uneven digital infrastructure threaten representativeness and equitable deployment.

This is a **methodological / conceptual Review**, not an applied TTE cohort study, so the standard PICO/data-source template below is adapted to a methods paper.

---

## Methodology (adapted for a methodological Review)

### Step 1 — Causal/Conceptual question as a "target trial" framing

| PICO element | Specification (as framed by the Review) |
|---|---|
| **Population** | Patients and populations served by contemporary, data-rich but structurally constrained health systems (with a regional focus on the Americas) |
| **"Intervention"** | Integration of AI methods into the EBM evidence pipeline — specifically multimodal data integration, **target trial emulation** on observational databases, and simulation/virtual-cohort modelling |
| **Comparator** | Classical trial-based EBM (RCT-centric evidence generation) and naïve predictive-only AI deployment |
| **Outcome** | Whether AI extends valid *causal* evidence generation and improves clinical decision-making — vs. merely improving predictive metrics without causal validity or demonstrated clinical benefit |
| **Design** | Narrative state-of-the-art Review synthesising methodological, epidemiologic, and ethical literature |

The Review's recurring argument is that the **target trial framework supplies the causal scaffolding** (clear eligibility, time zero, treatment strategies, assignment, follow-up, causal contrast) that AI/observational pipelines otherwise lack — converting "prediction" questions into well-defined "causation" questions.

### Step 2 — Data sources (evidence base for the Review)

- **Type:** Structured literature search with explicit "Search strategy and selection criteria" section (narrative synthesis; not a quantitative meta-analysis).
- **Scope:** Methodological, epidemiologic, data-science, and ethics/governance literature on AI in EBM, observational causal inference, TTE, and simulation modelling.
- **Regional lens:** The Americas — emphasising fragmented financing/delivery, uneven digital infrastructure, and representativeness/equity constraints on large-scale observational databases used for emulation.

### Step 3 — Eligibility / selection criteria

Sources were selected to cover (per the paper's structure): the transition from experience-based to evidence-based medicine; the prediction-vs-causation dialogue between data science and epidemiology; AI as an extension (not replacement) of classical methods; simulation/implementation from virtual models to real-world systems; and the shared limits of open science and AI. Selection prioritised conceptual and methodological contributions over individual applied studies.

### Step 4 — "Time zero" and treatment classification (conceptual)

Not an applied cohort. The Review instead stresses that any AI-enabled emulation must still respect the **TTE design discipline**: explicit time zero, alignment of eligibility/treatment assignment/start of follow-up, and avoidance of immortal-time and prevalent-user biases — the same protections that make an emulated trial interpretable as a causal contrast.

### Step 5 — Confounder adjustment (as discussed)

The Review's methodological core: predictive AI models are typically agnostic to causal structure, so high predictive accuracy can coexist with confounded/biased causal conclusions. It argues for embedding AI within causal frameworks (target trial emulation, explicit confounding-control via design and covariate adjustment) rather than treating model output as if it answered an interventional question.

### Step 6 — "Statistical analysis" / synthesis approach

Qualitative narrative synthesis organised thematically (see section list above). No pooled effect estimates. The analytic contribution is a conceptual taxonomy of how AI interfaces with EBM and a set of guardrails (causal validity, transparent validation, governance) for responsible integration.

### Step 7 — Sensitivity / robustness considerations raised

- Distinguishing **predictive validity** from **causal validity** as a recurring robustness theme.
- **Representativeness and equity:** fragmented health systems and uneven digital infrastructure in the Americas can bias the observational substrate used for emulation.
- **Governance and transparent validation:** open science and AI share limits — openness alone does not ensure valid or equitable evidence; structural reform is required to avoid reinforcing existing inequities.

---

## Key "Results" Table (thematic findings — no quantitative effect estimates)

| Theme | Key conclusion |
|---|---|
| Prediction vs. causation | Strong predictive performance ≠ causal validity or clinical benefit; the two must be kept conceptually distinct |
| Role of target trial emulation | TTE is the bridge converting large-scale observational/AI pipelines into well-defined causal questions; supplies eligibility, time zero, treatment strategies, and causal contrast |
| AI as extension, not replacement | AI augments — does not supersede — epidemiologic reasoning and classical trial methodology |
| Simulation / virtual cohorts | Simulation-based modelling can complement emulation but requires real-world validation before implementation |
| Equity in the Americas | Fragmented systems and uneven digital infrastructure constrain representativeness and risk entrenching inequities |
| Governance | Constructive AI integration requires governance reform, transparent validation, and structural change |

*(No HR/OR/RR/RD reported — this is a conceptual/methodological Review.)*

---

## Strengths

- Explicitly positions **target trial emulation** as the causal-inference linchpin connecting AI-scale observational data to clinically meaningful causal questions — a useful framing for readers building TTE pipelines on top of AI/ML data infrastructure.
- Clear, repeatedly emphasised separation of **prediction vs. causation**, a frequent source of error in AI-for-medicine work.
- Regionally grounded equity and governance lens (the Americas), addressing representativeness of the observational substrate that emulations depend on.
- Structured search strategy and transparent thematic organisation for a narrative Review.

## Limitations

- **Narrative review**, not a systematic review or meta-analysis; no pooled estimates and selection of sources is necessarily interpretive.
- High-level/conceptual — offers a framework and guardrails rather than concrete, validated protocols or reporting checklists for AI-enabled TTE.
- Regional (Americas) focus may limit generalisability of the governance/infrastructure arguments to other settings.
- Does not empirically evaluate AI-enabled emulations against RCT benchmarks (a gap that companion concordance studies — e.g., the recent BMJ TTE-vs-RCT concordance work — begin to fill).

---

*Full text accessed via The Lancet Regional Health – Americas (open access).*
