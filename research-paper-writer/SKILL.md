---
name: research-paper-writer
description: Draft, rewrite, polish, structure, humanize, or compress computer-science research manuscripts and manuscript sections, including abstracts, introductions, related work, theory, methods, experiments, captions, limitations, conclusions, and LaTeX. Use for reader-centered scientific storytelling, semantic naming of experiments and theorems, CS-appropriate terminology, removal of defensive or research-log prose, and evidence-preserving revisions. Do not use as the primary workflow for independent peer review, experiment execution, or mathematical/data integrity audits.
---

# Research Paper Writer

## Mission and decision order

Write **for human readers to understand a scientific discovery**. Make every paragraph, equation, theorem, experiment, and figure serve the paper's coherent scientific thesis. Never mistake abundant detail, administrative provenance, technical complexity, or elegant prose for evidence.

Prioritize in this order:

1. Scientific truth.
2. Evidence integrity and disclosure of material facts.
3. Human understanding.
4. Logical coherence.
5. Conciseness.
6. Presentation.

Treat user-approved research direction, actual methods, measurements, data splits, mathematical assumptions, citations, and changes of scope as protected. Ordinary writing authorization does not authorize research redesign, invented experiments, or unsupported claims. User-supplied source materials take precedence over generic examples; identify missing evidence instead of guessing.

## Select the editing mode before acting

| User request | Perform | Do not silently do |
| --- | --- | --- |
| New paper / full draft | Draft a coherent, content-complete manuscript from known research and known evidence | Invent missing results, or prematurely force a page quota |
| A named section, abstract, or caption | Draft that section in context and preserve its relationships | Rewrite other sections without necessity |
| Polish / humanize / defensive-writing cleanup | Repair scientific meaning and local prose; preserve scope, numbers, equations, citations | Delete material caveats or overstate findings |
| Terminology and experiment-title cleanup | Apply `references/terminology-policy.md` and semantic naming | Rename a reused test set as an independent test |
| Structure / logic repair | Restore the single scientific thesis, paragraph roles, and evidence links | Add disconnected contributions |
| Compress / adapt to length | Compress *after* scientific alignment; protect essential mechanisms and evidence | Cut key explanations solely to meet a quota |
| User requests review only | Report scoped writing issues and precise repairs without changing files | Launch an unrequested complete manuscript rewrite |

Standalone novelty assessment, formal proof auditing, statistics reconstruction, experimental execution, and final venue-compliance certification require their own specialist workflows; do not claim to have completed them during writing alone.

## Essential rules

### Explain one coherent scientific argument

Use **Problem -> Challenge -> Insight -> Method -> Evidence -> Implication** as a reasoning guide, not mandatory literal headings. The method follows a supported insight; observations, proofs, and experimental comparisons converge on the same thesis. Related contributions are welcome when logically connected. Choose an appropriate structure for method, empirical, benchmark, systems, or theory papers instead of imposing a universal section template.

### Name objects for what they mean

- Use descriptive experiment and section names: `Resolution Sensitivity Analysis`, `Mechanism Isolation`, or a precise question-specific title. **Do not put `E1`, `E2`, `Experiment A`, `Trial 1`, or development-phase identifiers in reader-facing section headings.** Internal IDs may remain in scripts, logs, and private records.
- Give theorems, lemmas, propositions, assumptions, algorithms, tables, and figures descriptive scientific names. Automatic theorem numbers for citation are fine; **never rely on `Theorem 1` or `Lemma 2` alone** as the scientific name. Example: `Theorem 2 (Conditional Success Guarantee)`.
- Keep one canonical name per concept. Do not inflate the terminology with fashionable synonyms or unexplained abbreviations.

### Use native CS research language, not imported study-management framing

For ordinary computational research, **do not use** `Pilot Study`, `Exploratory Study`, `Confirmatory Experiment`, `Post-hoc Analysis`, `Independent Confirmation`, `Registered Evaluation`, `Frozen Protocol`, `Phase I/II Trial`, `Treatment Arm`, or `Discovery Cohort` as manuscript experiment/stage titles. Do not narrate timestamp registries, Git hashes, registration or attestation status, provider migration chronology, repeated verification, or internal run history as scientific contribution.

Use a direct functional title such as `Threshold Sensitivity`, `Error Analysis`, `Generalization to New Pages`, `Model Comparison`, or `Controlled Ablation` **only when factually accurate**. Preserve actual information about data reuse, changed configurations, tuning on evaluation data, or unequal baselines when these affect the claim. Standard technical phrases such as `frozen weights`, `validation set`, `held-out test set`, `control variate`, and `API endpoint` remain valid. For genuinely registered studies or human-subject/causal studies, use required methodology terminology accurately. See `references/terminology-policy.md`.

### Let mathematics and experiments answer questions

Introduce intuitions before notation, assumptions before theorems, and interpretation after results. Use **Intuition -> Definition -> Assumption -> Derivation -> Result -> Interpretation**. State real conditions, maintain symbol and dimensional consistency, and move only ancillary proof steps to an appendix.

Organize experiments by what they test, not by execution chronology: **Question -> Design -> Key Result -> Explanation**. Distinguish observed effects, mechanistic attribution, independent evidence, and conditional mathematical guarantees. Preserve fair comparisons, denominators, uncertainty, and negative evidence that constrains a central claim.

### Write directly, not defensively

Remove imagined reviewer rebuttals, apologetic novelty denials, mandatory caveat endings, self-certified rigor, filler transitions, excessive punctuation, and result-by-result inventory. Keep actual limitations, statistics, assumptions, negative findings, and material differences in experiment conditions. Do not blacklist isolated words (`not`, `only`, `may`, `however`, `frozen`) independent of meaning.

### Keep the paper independent of its research log

The **main paper** explains the scientific question, mechanism, decisive proof/results, and material qualifications. Put detailed proofs, auxiliary trials, administrative run history, timestamps, hashes, full logs, and extended diagnostics into supporting or reproducibility materials when appropriate. If a moved/omitted fact would make a main-text claim false or misleading, retain it at the relevant comparison or narrow the claim. Do not conceal an inconvenient result.

## Workflow

1. **Determine authorization**: identify draft/polish/compress/critique mode; requested section; source format; language; accepted scientific scope; whether current results are actual or planned. Avoid unnecessary questions when already clear.
2. **Read relevant source**: for a substantial revision, inspect the complete affected passage and its necessary context, not just snippets. Preserve supplied evidence, citation keys, LaTeX labels, mathematical definitions, and numerical results.
3. **Recover the science**: define one coherent thesis and identify paragraph roles, the expected takeaway, evidence source, and real dependencies. If a mechanism is missing, do not invent it.
4. **Write content before fitting length**: produce scientifically complete explanation, check internal alignment, and only then compress if a length constraint is requested. For missing results, leave dependent empirical claims unwritten rather than fabricating placeholder findings.
5. **Edit locally, semantically**: preserve valid text; repair the smallest unit needed. Favor plain scientific nouns and verbs. Do not increase confidence beyond support. Do not silently add experiments, methods, hypotheses, or citations.
6. **Validate**: check (a) reader can follow the logic, (b) terms/definitions match, (c) claims track evidence, (d) figures/captions/statistics match, and (e) no prohibited research-stage naming in ordinary CS manuscripts. For LaTeX work, compile and check references when tooling and source permit; compilation is not scientific validation.
7. **Deliver actual work first**: return edited prose/source in the requested format, then only concise material changes and unresolved evidence decisions. For review-only work, return findings with locations and direct repairs, not an unsolicited rewrite.

## Load targeted references

Use references only as relevant; do not load the whole library for a short local edit:

- `references/writing-constitution.md` — full scientific and reader-centered principles. Read for first substantial draft or cross-section rewrite.
- `references/terminology-policy.md` — hard manuscript heading/stage restrictions, exceptions, factual-preserving replacements. Read for experimental writing, naming, or humanization.
- `references/section-guidelines.md` — abstract, introduction, related work, method/theory, experiments, figures, limitations, conclusion; semantic names. Read for a section draft or restructure.
- `references/execution-protocol.md` — evidence states, content-first drafting, local change control, source/LaTeX checks. Read for whole-paper drafting, project-file edits, or compression.
- `references/quality-audit.md` — reverse outline, claim-evidence alignment, terminology and readability gates. Read for final prose QA or substantial revision.
- `references/revision-examples.md` — short bad/better pairs using placeholders, not observed results. Read when phrasing or terminology decisions are ambiguous.

## Example triggers

- "Rewrite this introduction so the insight naturally leads to the method."
- "Polish the experimental section; remove E1/E2 labels and registration-style language."
- "Make theorem statements easier to read but leave their mathematical claims unchanged."
- "Remove defensive writing without hiding the scope or data-reuse facts."
- "Compress this manuscript while preserving proofs, numbers, and the central mechanism."

A text edit is not a peer-review score, independent replication, formal proof check, or publication-readiness certification. Say what was actually checked.
