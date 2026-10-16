# Before / After Patterns (Illustrations, Not Research Results)

The examples below deliberately use placeholders. Never treat them as experimentally observed facts.

## 1. Scientific introduction vs research-log narrative

**Avoid:** `After several registered trials, our frozen experimental setup confirmed that the proposed approach is robust.`

**Prefer:** `We evaluate [method] under [dataset and budget]. It achieves [measured result] relative to [comparable baseline], indicating [supported interpretation].`

Only fill brackets using genuine observed evidence. If evidence is missing, do not draft a success claim.

## 2. Semantic experiment naming

**Avoid heading:** `E7: Confirmatory Experiment`

**Prefer if true:** `Generalization to Unseen Layouts`

**Prefer when same data were used for tuning:** `Performance on Development Queries`

A descriptive heading may be less favorable, but it must be accurate.

## 3. Named theorems

**Avoid as the only label:** `Theorem 3`

**Prefer:** `Theorem 3 (Conditional Retrieval Success Bound)`

Before the theorem, explain what uncertainty the theorem resolves; after it, explain which assumptions make its result useful. Retain correct numbering/labels for cross-references.

## 4. Defensive novelty and prior work

**Avoid:** `We do not claim that coarse-to-fine inspection is new.`

**Prefer:** `Existing work uses coarse representations to select high-resolution evidence. We quantify [new measurable relationship] and test [distinct implication].`

Only assert novelty for a verified difference, with citations to the closest work.

## 5. Meaningful qualification, not generic apology

**Avoid:** `It should be noted that our result does not guarantee universal applicability, and the method may still have some limitations.`

**Prefer:** `The guarantee holds when [precise assumption]; our evaluation covers [actual population].`

A real condition belongs next to the claim, not in five repeated conclusions.

## 6. Separate observation from mechanism attribution

**Avoid:** `The higher accuracy proves that the localisation step alone causes the gain.`

**Prefer when multiple steps differ:** `The full localisation-then-reading protocol improves accuracy relative to [baseline]. Because [other factors] also differ, the comparison does not isolate the localisation step's contribution.`

## 7. Research administration versus relevant configuration

**Avoid:** `We switched inference providers during Phase II and later verified the original registration.`

**Prefer when comparability is material:** `Method A and Method B were evaluated on different inference endpoints. Their costs are therefore compared descriptively rather than as a same-endpoint controlled test.`

If no scientific claim depends on the history, omit it from the main paper and keep provenance in supporting records.

## 8. Reader-oriented equations

**Avoid:** `Let x be... [five equations, no explanation] ... hence the proof is complete.`

**Prefer:** `The relevant quantity is [definition]. It controls [behavior] because [reason]. Under [assumption], [equation] gives [bound]. The bound means [interpretation].`

Do not fabricate a new proof to make the narrative flow smoothly. If the mathematics does not work, flag it for technical review.
