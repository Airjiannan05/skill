# CS Terminology and Research-Stage Naming Policy

Use this when drafting experiments, naming result sections, humanizing prose, or cleaning a paper's research-log language. This is an enforceable **function-based writing policy**, not a language-only blacklist.

## Hard rule: ordinary computational experiment headings

Do not title an ordinary CS algorithmic or ML experiment/stage with any of the following patterns:

| Prohibited framing as a stage / heading | Describe the actual function instead |
| --- | --- |
| `Pilot Study`, `Pilot Experiment`, `Preliminary Trial` | `Threshold Sensitivity`, `Configuration Selection`, `Dataset Construction` as applicable |
| `Exploratory Study`, `Exploratory Evaluation` | `Error Analysis`, `Resolution Dependence`, `Parameter Sensitivity` if accurate |
| `Confirmatory Experiment`, `Independent Confirmation` | `Generalization to Unseen Data`, `Evaluation on an Additional Dataset` **only if accurate** |
| `Post-hoc Analysis`, `Retrospective Study` | `Error Analysis`, `Failure Mode Analysis`, `Additional Comparison` |
| `Registered Evaluation`, `Preregistered Trial` | `Evaluation Protocol`, a concrete dataset/metric title |
| `Frozen Evaluation Protocol`, `Locked Experimental Criteria` | `Evaluation Settings`, `Fixed Threshold`, `Unchanged Parameters` if technically meaningful |
| `Discovery Cohort`, `Validation Cohort`, `Treatment Arm`, `Control Arm` | `Development Set`, `Validation Set`, `Method`, `Baseline` when those are the actual roles |
| `Phase I / Phase II Trial`, `Trial 1 / Trial 2` | A section title stating the scientific question or comparison |
| `E1`, `E2`, `Study A`, `Experiment B` | The actual question tested, not an internal run ID |

Do not substitute a more flattering scientific title for a weak or non-independent design. `Generalization to Unseen Data` is impermissible if the dataset was seen during tuning. `Calibration` is not a euphemism for test-set optimization; name the actual operation.

## Keep research administration out of the main scientific story

Ordinary main-text prose should not chronicle:

- locally timestamped registrations or their absence of external attestation;
- Git commit hashes, run lineage IDs, archival snapshots, administrative validation;
- provider migrations and sequential replication history as a narrative arc;
- `frozen protocol` or `registered original run` as evidence of contribution;
- a sequence of debugging efforts, failed configuration sweeps, or subsequent repair labels.

Put necessary full logs, identifiers, hashes, and reproducibility notes in supplemental materials or the project repository. If a provider change, method version, data reuse, benchmark contamination, or configuration mismatch **affects an advertised comparison**, state the relevant difference directly at that comparison or do not make a strict controlled claim.

## Preserve facts relevant to statistical interpretation

The naming restriction must never conceal:

- a threshold selected by inspecting evaluation outcomes;
- reuse of the same examples to design and evaluate a method;
- comparisons performed with different models, endpoints, prompts, or budgets;
- multiple comparison / selection effects;
- tuning on test data, contamination, inconsistent splits;
- the actual origin of a reported number;
- experiments materially limiting the paper's central claim.

Use direct prose describing what happened: `The method was revised after examining errors on these queries; results on the same queries are not an independent evaluation.`

## Technical exceptions are context-dependent

- `Frozen weights`, `frozen backbone`, `frozen layers`: valid model parameters not updated by training.
- `Validation set`, `cross-validation`, `held-out test set`: valid only when these data roles are real.
- `Control variate`, `control policy`, `controlled comparison`: standard CS/statistical constructs.
- `API endpoint`, `network endpoint`: valid system/inference terms.
- `Replication` and `reproduction`: valid if a genuine re-execution or separate replication is scientifically at issue.
- `Intervention`, `cohort`, `randomized trial`, `registered report`: may be indispensable in HCI, software engineering field experiments, computational medicine, or causal research. Use accurate discipline-specific methodology when the study genuinely requires it.

**Never ban a word solely because it resembles a term used by another discipline. Ban irrelevant research-stage framing, not legitimate CS technical semantics.**

## Before / after examples (illustrative only)

**Administrative self-certification**

Bad: `To ensure rigor, we registered and froze the evaluation protocol before our confirmatory phase.`

Better, if true: `We select the threshold on the validation set and report accuracy on a separate test set.`

Better, if data were reused: `We selected the threshold using these evaluation examples; reported performance on them is therefore not an independent test.`

**Stage labels**

Bad: `E3: Pilot Study` / `E8: Confirmatory Experiment`

Better, if true: `Label Resolution Sensitivity` / `Generalization Across Independent Pages`

**Provider chronology**

Bad: `After migration, we replicated the registered original result.`

Better, if material: `The two methods were run on different inference endpoints; the comparison is descriptive rather than a controlled same-endpoint test.`

**Evidence from error-driven changes**

Bad: `Our post-hoc intervention independently confirmed a robust improvement.`

Better: `The variant was designed after inspection of the test-set errors. The improvement measured on that same set is exploratory rather than an independent validation.`

For every replacement, inspect the actual protocol. If the factual condition is unknown, flag it instead of replacing it with an invented split or stricter evaluation claim.
