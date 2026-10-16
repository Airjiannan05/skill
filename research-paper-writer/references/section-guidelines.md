# Reader-Centered Section and Naming Guide

Use the section functions that serve this paper. Do not treat this as a universal mandatory outline; a theoretical paper, benchmark paper, or systems paper may require a different composition.

## Abstract — the shortest coherent scientific story

Aim for: specific task/problem; root challenge; core insight and what the method exploits; strongest supported finding; correct scope. Prefer one decisive number or comparison to a catalogue of results. Do not lead with run identifiers, local registration, auditing, endpoint migrations, or a broad future-work warning. If performance is still pending, write no empirical superiority claims.

**Reader test:** after one read, can a colleague say why the problem matters, what was discovered, and what evidence exists?

## Introduction — motivation, not a defensive rebuttal

Move from concrete problem to scientific tension to insight. Explain the root reason existing approaches leave a gap; cite the closest work fairly. State the distinct contribution positively and precisely, rather than `we do not claim X is new`. Use contribution statements tied to actual evidence or formal results. Avoid restating the whole experiment table and attaching a list of failed prototypes immediately after the contribution.

**Reader test:** can the method seem like a natural response to the stated challenge rather than a collection of modules?

## Related work — intellectual positioning

Group relevant studies by scientific question, mechanism, or assumption, not by publication date. Name closest similarities directly; distinguish exact technical conditions and evidence, not general claims of superiority. Keep citations trustworthy and aligned to what each source supports. Never erase the closest competitor to create an artificial gap.

## Method and theory — understandable rigor

Suggested passage rhythm:

1. Explain the observed or hypothesized phenomenon.
2. Define input, output, setting, and relevant quantities.
3. Motivate the necessary assumptions.
4. Explain the operation or mathematical relationship in words.
5. State the exact equation, algorithm, proposition, or theorem with a **semantic title**.
6. Interpret its meaning, applicability, and sufficient/necessary conditions.

Examples of descriptive mathematical labels:

- `Theorem 1 (Conditional Success Guarantee)`
- `Theorem 2 (Search Cost Lower Bound)`
- `Proposition 3 (Expected Access Cost)`
- `Lemma 1 (Monotonicity Under Refinement)`
- `Assumption 2 (Bounded Local Interference)`

The numbers support cross-references; the parenthesized names convey meaning. If LaTeX uses `\begin{theorem}[Conditional Success Guarantee]`, retain its numbering and labels. An unmotivated series of theorem environments is not a good explanation. Keep important conditions visible in the main text; move only supportive algebra when appropriate.

For algorithms, describe the data it consumes, operations it performs, and output it produces. Do not substitute architectural labels for scientific mechanisms. No invented complexity results.

## Experiments — evidence organized by question

Use functional, reader-visible names such as:

- `Main Performance Comparison`
- `Accuracy at Matched Compute`
- `Effect of Field Density`
- `Localisation Versus Recognition`
- `Mechanism Isolation`
- `Sensitivity to Image Resolution`
- `Generalization Across Unseen Layouts`
- `Error Analysis`

**Do not name main-paper experiments** `E1`, `E2`, `Pilot`, `Confirmatory Study`, `Phase II`, `Registered Evaluation`, or any chronology-based heading. Preserve internal IDs in logs only.

Each subsection should be readable as:

- **Question:** what alternative explanations or behavior does this test distinguish?
- **Design:** what is held equal; what changes; what dataset, model, and metric are used?
- **Result:** the key paired comparison, distribution, effect size, and uncertainty.
- **Interpretation:** what follows, and what attribution is not established?

A result on the same data used to design the method cannot be described as independent testing. Do not label an ablation as a full-method baseline or treat changing multiple protocol factors as isolated causality.

### Experimental setup

Keep dataset definition, model and method identity, split, important hyperparameters, budgets, sample counts, metric, and statistic visible enough for readers to judge the comparison. Put detailed run hashes, time stamps, administrative decisions, provider migrations, and minor configs in reproducibility material; mention actual endpoint differences only if they affect the claimed comparison.

### Tables and figures

A table should let readers reconstruct the relevant comparison. State whether values are percent or fraction, precision, sample count, baseline, and uncertainty. Figures should show a scientific relationship, not implementation clutter. Captions must not imply an unmeasured comparison or an accuracy threshold that has not been defined.

## Analysis, limitations, and conclusion

**Analysis:** interpret mechanism, model predicted/observed distinctions, competing explanations, and important errors. Avoid announcing new factual claims unsupported by experiments.

**Limitations:** identify *material* boundaries (data scope, model family, proven conditions, benchmark fairness, latency vs tokens); do not repeat every failed trial or speculative risk. If a failure directly contradicts a central claim, it must be handled honestly at the relevant location.

**Conclusion:** answer the original question and state the scientific knowledge now established. No new numbers, new methods, or defensive apologies.

## Transitions and paragraph responsibilities

Use a reverse outline: name each paragraph's single retained scientific message. Every adjacent pair must have a real causal, evidential, contrastive, refinement, or consequence relation. Repair missing logic rather than inserting `Moreover`, `Furthermore`, or an em dash.

Make new concepts intelligible before introducing abbreviations or nested references. One stable term is better than a thesaurus of approximate synonyms.
