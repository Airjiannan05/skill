# Research Paper Writing Constitution

This document is the enduring, venue-independent scientific writing standard for computer-science research. It governs research writing, not the design of a new experimental methodology. Apply its **scientific intent** before stylistic heuristics.

## Non-negotiable decision order

**Scientific Truth > Evidence Integrity > Human Understanding > Logical Coherence > Conciseness > Presentation**.

- When brevity and explanation conflict, keep the explanation necessary for the reader.
- When style and mathematical correctness conflict, preserve mathematics.
- When a tidy main-text story and material negative evidence conflict, preserve the truth; move nonessential detail but state the boundary or qualify the claim.
- When external conventions and user-approved research scope conflict, do not silently change the research question. Identify the actual issue and request authorization for a substantive shift.

## 1. Write for Humans

A research paper exists to help a human understand a scientific discovery, not to display the researcher's effort, code, administrative history, or ability to write equations.

Before each passage ask:

- What does the reader already understand?
- What must they know to understand the next idea?
- Why does this concept, assumption, equation, or experiment appear *here*?
- What scientific connection does it establish?
- What should the reader remember afterward?

Provide intuition before formalization, context before procedures, evidence before generalization. Make references and pronouns unambiguous. Prefer an interpretable explanation to deliberately sophisticated-sounding language. Scientific rigor and readability must coexist.

## 2. One Paper, One Coherent Scientific Thesis

Anchor the paper on a single coherent **scientific thesis**, not necessarily on a single theorem, experiment, or component. Multiple related contributions are acceptable when they jointly answer the same question.

Use the reasoning chain **Problem -> Challenge -> Insight -> Method -> Evidence -> Implication**. Do not necessarily print this chain as headings. The method must follow from an identified challenge and insight; theory and experiments must genuinely support the claimed explanation. Do not introduce extra mechanisms merely to look novel.

## 3. Scientific Discovery Before Presentation

**Published is not identical to scientifically universal.** A close prior paper is reason to understand its assumptions and tested regime, not a reason to retreat automatically to a new dataset.

**Hole-finding over slot-finding.** Seek missing state variables, contradictions, untested assumptions, invalid proxy metrics, hidden resource constraints, breakdowns, and explanatory gaps. An unused pairing of model and benchmark is not by itself a scientific contribution.

**Investigate before generalizing.** Check code, data, evaluation, statistical procedures, and configurations before proposing a new conceptual explanation for anomalous outcomes.

When appropriate, use a limiting thought experiment to vary task demand while holding a resource fixed. Any claimed higher-dimensional or unifying mechanism must produce a discriminating, falsifiable implication; rhetoric does not suffice.

## 4. Linear Scientific Storytelling

Write in the order a reader needs to understand the claim, not the chronological order of experiments or code changes.

- **Abstract:** specific problem, missing explanation, core insight/method, decisive evidence, supported implication; avoid turning it into a numeric inventory.
- **Introduction:** make importance, technical difficulty, gap, and proposed scientific insight legible before the method details; present a concise contribution summary.
- **Related Work:** compare relevant research families and assumptions; discuss the closest competitors accurately, not as dismissive summaries or chronology.
- **Method / Theory:** motivate formal objects, define terms, explain mechanism, state assumptions and results, interpret their meaning.
- **Experiments:** test scientific questions in claim-driven order, not trial history.
- **Analysis:** explain comparisons and mechanisms without attributing causality that controls do not isolate.
- **Limitations:** state material scope restrictions once at the natural location; do not collect a defensive inventory of every failed attempt.
- **Conclusion:** answer the original question and what is now known; add no new unsupported results.

Adapt structure and emphasis to the actual contribution (algorithm, empirical regularity, benchmark, systems, theory, human-centered computing). Do not force all papers to have the same method section or equal-length chapters.

## 5. Meaningful Naming

Use scientific, descriptive names for experiments, headings, assumptions, lemmas, propositions, theorems, algorithms, figures, and tables.

- Reader-facing experimental titles must not be `E1`, `E2`, `Study 1`, `Experiment A`, or research-stage labels. Use what is tested or measured: `Threshold Sensitivity Analysis`, `Mechanism Isolation`, `Generalization Across Layouts`, etc.
- Keep internal run identifiers inside logs, filenames, code, and provenance material, not scientific headings.
- Do not rely on `Theorem 1`, `Lemma 2`, or `Proposition 3` alone. Pair automatic numbering with a truthful title: `Theorem 2 (Conditional Search Bound)`.
- Avoid inventing new acronyms solely for novelty. Stable, accurate names matter more than clever names.

## 6. Mathematics Must Tell a Story

Follow **Intuition -> Definition -> Assumption -> Derivation -> Result -> Interpretation**. Every significant formula should answer a scientific question. Define symbols before using them, preserve units and dimensions, and avoid unmotivated chains of equations.

State assumptions adjacent to claims when necessary. A conditional theorem is not an unconditional empirical finding. Include core results and proof ideas in the main paper; move lengthy algebra or supporting lemmas to an appendix when the essential argument survives. Use a simple example when it materially helps intuition.

## 7. Experiments Must Answer Questions

Follow **Question -> Experimental Design -> Key Result -> Explanation**.

Choose only experiments that serve a claim: main comparison, controlled comparison, mechanism validation, ablation, sensitivity, generalization, or efficiency. These are possible functions, not a checklist that all papers must fill.

- Use relevant and fair baselines, not artificially weak alternatives.
- Match metrics to the scientific question and maintain correct denominators, uncertainty, and units.
- Distinguish observed correlation from causal attribution, and descriptive evidence from sufficient mathematical conditions.
- Treat repeated test-set tuning and data leakage as real issues, regardless of how plainly they are described.
- Avoid overclaiming equality based on nonsignificance or superiority from unequal conditions.

## 8. Figures and Tables Are Part of the Argument

Each main figure serves one central purpose: establish intuition, explain a mechanism, illustrate a prediction, support a result, or reveal a necessary boundary. Tables must support meaningful comparisons.

Use accurate units, axis labels, uncertainty, legends, and denominators. Avoid dense paragraphs inside visualizations. Captions should be standalone enough for correct interpretation without narrating every number. Text should explain the *scientific meaning* of the visual, not read the table aloud. Avoid redundant plots and decorative effects.

## 9. Confident but Precise

Remove apologetic novelty positioning (`we do not claim novelty`), imagined reviewer reassurance, mandatory limitation endings, meaningless hedge stacks, and generic promises of rigor. State directly what was changed, measured, and supported.

Never swap necessary scientific uncertainty for hype. Avoid unqualified `universal`, `guaranteed`, `first`, `revolutionary`, and `solves`. A useful negative result or material limitation may belong in the main argument. Do not delete real caveats merely because they use `only`, `not`, `may`, or `however`.

## 10. Computer-Science Terminology Discipline

Do not frame ordinary computational experiments as clinical trials, preregistration campaigns, administrative approvals, or staged authentication exercises. **Forbidden as ordinary CS experiment or research-stage headings**: `Pilot Study`, `Exploratory Study`, `Confirmatory Experiment`, `Post-hoc Analysis`, `Independent Confirmation`, `Registered Evaluation`, `Frozen Protocol`, `Phase I Trial`, `Treatment Arm`, and similar labels.

Use scientific functions as titles: `Validation-Set Threshold Selection`, `Error Analysis`, `Controlled Comparison`, or `Generalization Evaluation`, if those actually describe the data and procedure. Keep real CS technical meanings (`frozen backbone`, `validation set`, `control variate`, `API endpoint`) and applicable human-subject study terms. Never misrepresent development-informed data as held-out validation. See `terminology-policy.md`.

## 11. Main Paper versus Supplementary

The main paper must stand alone on its **scientific question, core insight, mechanism, assumptions, decisive evidence, and important scope**. Appendices and reproducibility artifacts can carry complete proofs, secondary ablations, expanded statistics, protocol configuration, code hashes, timestamps, administrative decisions, and run history.

Remove administrative research-process narrative from the main body. However, disclosure of a material difference in providers, datasets, evaluation data reuse, or experimental fairness remains necessary at the relevant claim. Never move away a fact that would make the remaining main text materially misleading.

## 12. Natural Academic Writing

Write like a researcher explaining science to peers, not like an agent filling a template or an author anticipating hostile reviews.

Avoid repetitive introductions, long noun stacks, em-dash or semicolon chains used to substitute for logic, mechanical `First/Second/Finally` prose, excessive named stages, awkward synonym cycling, excessive acronyms, and every paragraph ending in a warning. Use concrete subjects and verbs. Connect sentences by genuine cause, evidence, refinement, contrast, and consequence, not by filler transitions.

Do not judge quality by banned-word counts or automatic AI-detector claims. Preserve accurate standard terms even when a stylistic heuristic flags them.

## 13. Minimal, Evidence-Preserving Revision

Fix an identified defect with the smallest scientifically sufficient edit. Do not rearchitect a validated paper when the user requested line-level prose cleanup. Preserve the author's approved hypothesis, mechanism, valid theorems, datasets, observed values, methods, references, and storyline. If correctness requires a scientific change or more evidence, explicitly isolate that decision instead of quietly inventing a repair.

## Final principle

A good paper answers: **What was unknown -> Why it mattered -> What we discovered -> How we established it -> What it changes**.

**Scientific rigor makes a paper trustworthy. Clear reasoning makes it understandable. A meaningful discovery makes it worth reading.**
