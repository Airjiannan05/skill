# Manuscript Execution Protocol: Seven Mandatory Safeguards

Use for substantial drafting, revision across sections, LaTeX source edits, or explicit length fitting. Ordinary paragraph polish only needs the relevant local steps.

## 1. Content first, length later

Three stages:

1. **Content draft**: write a complete scientific explanation with the approved claim scope and actual evidence; do not impose an arbitrary page budget prematurely.
2. **Scientific alignment**: verify consistent terms, method configuration, equations, citations, evidence, findings, and section purpose.
3. **Submission fit**: compress only if requested by the user or required for an explicitly requested submission-ready deliverable. Remove repetition, generic background, needless run history, and decorative phrasing before reducing essential mechanism or evidence explanation.

For incomplete experiments, write known setup and planned evaluation truthfully; do not claim unobserved gains. An initial manuscript may be content-complete but evidence-incomplete.

## 2. Evidence-status discipline

Determine actual status per claim, result, and method: `proposed`, `implemented`, `evaluated`, `observed`, `verified`, `missing`, or `unresolved`.

Use statuses in internal work and concise delivery notes; do not write `E1 exploratory/pilot stage` into the manuscript. Keep missing table cells visibly absent in working drafts and remove dependent results prose. Treat a proposed method's hoped-for behavior as a hypothesis, not an observation. Do not fill gaps by inference from the paper's preferred storyline.

## 3. Claim-evidence alignment gate

Before any abstract-level or cross-section assertion, locate applicable support: source citation, theorem and proof, actual experiment, validation, or explicitly stated assumption. Track internally:

`Claim -> evidence location -> evidence strength -> scope -> dependent text/tables`.

If a result changes, reconcile its dependencies across abstract, introduction, experiments, figures/captions, discussion, conclusion, and appendix. Preserve actual datasets, denominators, model versions, seeds, configs, split status, costs, and statistical test definitions. Never blend figures from different configurations or reinterpret mismatched comparisons as controlled.

For current external facts requested by the user, verify the cited original source and actual claim support; do not fabricate references, DOIs, method descriptions, or results.

## 4. Section-level cohesion check

After a substantial draft, make an internal reverse outline: one scientific message per paragraph and one natural logical relation between adjacent paragraphs. Merge duplicates, remove paragraphs without a necessary role, and repair missing explanations. Check term introductions, referents, and that the next subsection follows from the last one's result.

## 5. Task-scope protection

Distinguish `draft`, `polish`, `compress`, `reader-centered critique`, and `submission fit`. A prose edit may improve legitimate scientific wording and necessary local coherence, not change the approved experiment plan or theorem. Full technical peer review and independent evidence audit require separate explicit scope and evidence.

For revisions, prefer local patches. Don't change unrelated labels, tables, citations, project layout, or methodology. If the smallest truthful repair needs a research decision, identify the issue and request it instead of fabricating new runs.

## 6. Semantic humanization

Inspect statements for scientific payload rather than keyword count. Remove empty assurances and imagined objections, not actual limitations. Do not mechanically remove `not`, `may`, `only`, `frozen`, or useful technical hedging. Prefer concrete verbs, natural argument, varied but not forced sentence rhythm, and minimal punctuation used to substitute for thought. Avoid first/second/finally repetition unless the sequence is real.

Do not replace a true unfavorable fact with a more positive but inaccurate account. Write the actual dataset split, protocol, and evidence limits directly.

## 7. Artifact and LaTeX validation

Preserve supplied source format and repository organization:

- LaTeX: commands, theorem and equation labels, bibliography keys, figures/tables, relative includes, macros, build settings.
- Markdown: heading structure, citations, equations, tables when not specifically changed.
- Figures/captions: refer to actual rows/data, not fabricated results or legend labels.

When source/build tools are available, compile after authorized edits, inspect missing references and affected renderings, and report what was or was not compiled. Compilation is not a proof or statistical validation.

Do not create unnecessary duplicate manuscript versions; respect user-specified file output and patch only the authorized project artifacts.

## Minimal delivery contract

- For a **requested rewrite**: edited prose/source first; a short note only for material changes or unresolved evidence.
- For **writing diagnosis only**: precise problem locations and minimal fixes; no silent edits.
- For a **full project edit**: identify changed files, meaningful verification, and specific outstanding scientific decisions. Do not claim the manuscript is submission-ready from prose polishing alone.
