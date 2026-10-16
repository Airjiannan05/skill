# Reader-Centered Manuscript Quality Audit

Use as a final local gate after significant writing changes. This is a **writing and consistency checklist**, not a substitute for external formal proof verification or data reconstruction. Do not invent reviewer scores or new measurements.

## Reader-first audit

- **Clarity:** can a researcher unfamiliar with the project's development history explain the central question after reading the opening?
- **Motivation:** is each definition, equation, component, and comparison motivated before it appears?
- **Coherence:** does each section support the same scientific thesis?
- **Argument:** are connections genuine (cause, evidence, contrast, consequence), not transitions standing in for missing reasoning?
- **Rememberability:** after reading, can a colleague state what was discovered and why it matters in two sentences?

## Reverse outline

For each paragraph, state internally its one main scientific message. Mark `keep`, `merge`, `move`, `rewrite`, or `delete` based on role. Remove duplicated arguments; preserve necessary constraints. When adjacent paragraphs lack a logical dependency, repair that relation with existing evidence rather than inventing a rationale.

## Evidence integrity

| Audit dimension | Test |
| --- | --- |
| Claim -> evidence | Is every important claim backed by the correct experiment, theorem, or citation? |
| Measurement origin | Are denominator, run version, model, dataset, prompt, budget, and unit consistent? |
| Statistical meaning | Are confidence intervals, pairing, test set reuse, and multiple tests described accurately? |
| Independent evidence | Are additional datasets truly held out from method/threshold selection? |
| Theory boundaries | Are assumptions, quantifiers, and non-degeneracy conditions retained? |
| Main vs supplementary | Does the main paper remain truthful if extended diagnostics move out? |
| Cross-section alignment | Do abstract, method, figures, tables, analysis, and conclusion refer to the same results? |
| References | Do cited sources exist, and do they support the specific statement? |

Missing evidence should yield a narrower claim or a concrete unresolved question, not an invented result or a blanket disclaimer.

## Semantic naming gate

- Experiments have scientific titles instead of `E1`, `E2`, `Experiment A`, or clinical/preregistration-style stages.
- Theorems, lemmas, propositions, assumptions, algorithms, figures, and tables have descriptive scientific names in addition to any numbering.
- Titles describe what the evidence actually supports; do not rename a development-informed experiment into a purported independent test.

## CS terminology gate

Consult `terminology-policy.md` when editing experiments and methods:

- Scan **headings first** for `pilot`, `preliminary trial`, `exploratory`, `confirmatory`, `post-hoc`, `independent confirmation`, `registered`, `frozen protocol`, `cohort`, `treatment arm`, and `Phase I/II`.
- Check whether any such label is an imported study-management framing. Replace it with the actual scientific question or functional analysis title.
- Exempt legitimate computational terms, such as `frozen weights`, `validation set`, or `control variate`.
- If a distinction reflects real test-set reuse, changed protocol, or multiple-comparison bias, **retain the fact in plain language**.

## Prose gate

Check for: apology-led novelty positioning, self-certified fairness/rigor, imagined reviewer objections, automatic limitations at every paragraph's end, unnecessary em-dash/semicolon chains, repeated `Moreover`/`Furthermore`, excessive acronyms, synonym cycling, same-length sentence templates, formula dumping, and results tables rewritten as prose.

Revise semantics, not a word count. Keep necessary mathematical negation, uncertainty, and genuine contrasting relations.

## Final consistency gate

Before delivery:

1. Verify protected numerical values and labels did not change without explicit authorization.
2. Check theorem statements and their cited proofs share assumptions and symbol definitions where the project includes proofs.
3. Ensure reworded claims do not imply stronger causality or universal generalization.
4. Inspect any caption or table affected by deleted comparisons.
5. Preserve material negative evidence and fairness conditions.
6. For LaTeX source, check compilation and references if tools permit; otherwise state they were not checked.
7. Report only material unresolved decisions, not a generic self-certification checklist.

## Model revision requests

- `Remove all defensive writing` -> remove empty defenses while retaining true evidence constraints.
- `Remove failed experiments from the main paper` -> move nonessential analyses, but retain or narrow central claims affected by counterevidence.
- `Delete all registration language` -> remove administrative narrative; keep accurate information about data splits, post-selection, comparability, and reproducibility where needed.
- `Make the writing stronger` -> lead with specific supported statements, not with invented results or confidence inflation.
