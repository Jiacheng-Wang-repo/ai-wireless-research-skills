---
name: research-spec-loop
description: "Keep authority, lifecycle, and evidence aligned in research code repositories. Use for a targeted governance audit, an owner-scoped research change, or a closeout that must reconcile accepted design, implementation, tests, configs, protocols, results, decisions, live status, and historical provenance. Adapt to the repository's existing authority surfaces instead of imposing a directory layout."
---

# Research Spec Loop

Use this skill as a small governance loop around research work. It does not
replace the repository's rules, research documents, tests, or experiment
protocols. Read and obey the effective rule chain first.

## Select one primary mode

- **audit**: perform a read-only check for authority, lifecycle, and evidence
  drift.
- **implement**: make one authorized change whose mutable facts have clear
  owners, then update only affected dependent surfaces.
- **closeout**: reconcile the completed task across design, implementation,
  evidence, documentation, and historical boundaries.

Honor an explicitly requested mode. Otherwise infer `audit` for review-only
requests, `implement` for requested changes, and `closeout` for handoff or
completion checks. If a change request also asks for final reconciliation,
perform `implement` and finish with its closeout checks; do not invent another
mode or workflow layer.

Read [references/modes.md](references/modes.md) after selecting the mode.

## Discover roles before paths

Do not require `specs/`, `decisions/`, or any other fixed structure. Discover
the repository's existing surfaces from its effective rules, documentation
index, entry documents, code tree, tests, configs, protocols, artifacts, and
Git history. Record which existing surface owns each relevant fact.

Use this semantic routing unless the repository defines a more specific
owner:

| Surface | Owns | Does not prove or own |
|---|---|---|
| `AGENTS.md` or equivalent | Slow-moving working, safety, validation, and routing rules | Current formulation details, campaign status, or task queue |
| Live status document | Repo-wide current phase, blockers, and next step | Technical truth that conflicts with code or evidence |
| Current research spec | Current accepted research design | Implementation status, run evidence, or task queue |
| Active source tree, commonly `src/` | Implementation truth | Acceptance of the design or scientific validity |
| Tests, commonly `tests/` | Implementation-check definitions; their recorded executions may provide scoped implementation-test evidence | Evidence that an unexecuted check passed, or formal experiment evidence |
| Configs, commonly `configs/` | Intended or frozen execution configuration | Proof that execution occurred |
| Experiment protocol | Experiment contract, gates, commands, and required evidence | Proof that the protocol was executed |
| Artifacts and result records | Scoped execution evidence; formal evidence only when the applicable experiment contract is satisfied | Unrecorded runs, automatic formal status, or broader paper claims |
| Decision register | Decision lifecycle and state | Duplicate lifecycle state in consumer documents |
| Git history | Historical provenance | Current status or current accepted design by itself |
| Historical or superseded documents | Time-bounded provenance and context | Current authority |

Path names are examples, not layout requirements. If the repository identifies
an active source tree other than `src/`, use that owner and report the mapping.

## Enforce single ownership

Each mutable fact has one owner. Other surfaces may consume it through a short
pointer, identifier, or scoped summary, but must not independently maintain the
same mutable value.

In particular:

1. Repo-wide phase, blockers, and next step have exactly one live owner.
2. The current research spec owns the accepted system model, representation,
   architecture, objective, loss, inference, and baseline definitions. It does
   not own implementation status or task order.
3. A decision register alone owns each decision's lifecycle or state. Other
   documents reference the decision ID and own only their narrative, question,
   dependency, gate, or experiment content.
4. Update an owner first, then only consumers whose own content or pointer is
   affected. Do not mechanically copy status across files.

When two active surfaces claim the same mutable fact, do not silently choose
the more convenient one. Resolve authority from repository rules and evidence;
if authority remains ambiguous, report the conflict and stop before making a
substantive change.

## Separate lifecycle from evidence

Decision or design lifecycle and research evidence are independent axes. Map
the host repository's words by meaning rather than by spelling:

- **Working**: a proposal is unaccepted, incomplete, or still changing.
- **Current**: a research design or decision is currently accepted by its
  authority owner.
- **Declined**: an evaluated proposal was not adopted.

`Current` does not mean implemented, tested, formally validated, or suitable
for a paper claim. Replacement or supersession is a relationship between
decision owners, not a higher evidence state. Cross-link replacements; for a
partial supersession, state the scope the new owner replaces and the scope the
earlier current owner retains. Preserve the earlier accepted history instead
of rewriting it as though it never existed.

## Keep research evidence states separate

Treat these as distinct states and never promote between them automatically:

| State | Minimum meaning |
|---|---|
| Design proposal | A candidate idea not yet accepted as the current design |
| Current accepted research design | The design recorded by the authoritative spec and any required accepted decision |
| Implementation | Active source code implements a scoped behavior |
| Implementation test / smoke / dry-run | A scoped code-path, interface, or launch check was actually executed and its result recorded |
| Formal experiment | An authorized applicable protocol was executed with the required provenance, metadata, and artifact contract satisfied |
| Scientific claim | A bounded interpretation supported by applicable formal evidence and the project's claim-review process |

The working evidence sequence is:

```text
proposal --acceptance--> current design
current design --code change--> implemented
implemented --recorded test--> implementation-tested
implementation-tested --protocol execution + artifacts--> formal-experiment-validated
formal evidence --bounded interpretation/review--> paper claim
```

Every arrow requires its own evidence. Code presence does not establish the
accepted design. A test, smoke, preflight, or dry-run definition is only a
check definition; only an actual recorded execution can establish its scoped
implementation-test evidence. Such success does not establish formal
experiment evidence. A frozen config records intent, not an actual run. A
protocol defines the contract, while artifacts and result records default to
scoped execution evidence. Call them formal experiment evidence only when the
applicable protocol, authorization, required provenance and metadata, and
artifact contract are all satisfied. Formal results support only claims within
their recorded scope.

## Preserve lifecycle boundaries

- Mark historical or superseded material so it cannot look current, while
  preserving original facts, paths, status snapshots, result numbers, and
  provenance.
- A historical mention of a retired file or path is not a dangling active
  dependency merely because the target no longer exists. Ask whether a current
  agent is instructed to read, update, or rely on it now.
- Retiring an authority removes active rules, routing entries, maintenance
  requirements, and live dependencies. It does not rewrite historical
  evidence. Git history remains the provenance surface.
- Do not infer current authority from words such as `current`, `next`, or
  `original` inside an explicitly historical snapshot; judge document
  lifecycle and surrounding scope.

## Respect task authority

This skill does not expand permission. Preserve existing worktree changes,
stay inside allowed files and systems, and do not run training, evaluation,
baselines, comparisons, dataset generation, or formal experiments unless the
user explicitly authorized them and the repository's protocol gates are met.

Prefer the smallest change that restores a clear owner and accurate pointers.
Do not create a new index, status document, decision framework, or directory
when an existing authority surface can be reused.

## Completion receipt

Report:

- selected mode and scope;
- relevant mutable facts and their owners;
- highest evidence state actually established;
- changed or inspected dependent surfaces;
- validation performed and what was intentionally not run;
- unresolved conflicts, historical references intentionally preserved, and
  any next action that remains with its live owner.

Never summarize a lower evidence state with language from a higher one.
