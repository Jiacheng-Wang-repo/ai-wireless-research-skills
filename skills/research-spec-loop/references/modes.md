# Mode Procedures

Use only the procedure for the selected mode. The repository's instructions
and the user's allowed scope override these defaults.

## Audit

Audit mode is read-only. Do not fix findings unless the user separately
authorizes implementation.

1. **Record the gate.** Capture worktree status and recent history before
   inspection. If the user specified an expected branch, commit, or clean
   state, enforce that gate before continuing.
2. **Read the authority entrypoints.** Read the effective agent rules and the
   repository's existing docs index, live status owner, current research spec,
   decision register, and representative protocol/result/historical surfaces.
   Keep the scan targeted to the requested facts.
3. **Map mutable facts.** For each relevant fact, record its current owner,
   consumers, lifecycle, and evidence state. Distinguish a duplicated mutable
   value from a stable pointer or a deliberately frozen historical snapshot.
4. **Check drift.** Look for:
   - multiple active owners for phase, blockers, next step, design, or decision
     state;
   - active `Current`, `Next`, or task-order language outside the live owner;
   - current-looking historical or superseded documents;
   - implementation status mixed into the design spec;
   - configs or protocols presented as run evidence;
   - code, tests, smoke, or dry-run evidence presented as formal or scientific
     validation;
   - active references to retired authorities;
   - decision state copied outside the decision register.
5. **Classify by impact.** Prioritize issues that can change an agent's next
   action, accepted design, experiment authorization, evidence interpretation,
   or paper claim. Do not turn wording or style preferences into blockers.
6. **Apply the stopping criterion.** Governance is sufficient when relevant
   mutable facts have one discoverable owner, consumers point rather than
   fork, evidence levels are bounded, and historical material cannot direct
   current work. Do not continue cleanup merely to make every historical phrase
   uniform.
7. **Verify read-only completion.** Re-run worktree status and confirm it is
   unchanged from the gate.

Audit output should identify resolved, partial, and unresolved risks; name the
owner for each high-value fact; and recommend at most the smallest next patch.

## Implement

Implement mode requires an authorized, owner-scoped change.

1. **Record the gate and preserve WIP.** Capture status, recent history, and the
   allowed edit/run scope. Stop on unexpected changes that overlap the task;
   never discard existing work to obtain a clean tree.
2. **Resolve the changed fact before editing.** State the fact, its single
   owner, its present lifecycle/evidence state, and the dependent consumers
   that may need synchronization.
3. **Check decision and design authority.** A proposal is not the current
   design. Treat lifecycle and evidence as separate axes: a `Current` decision
   means accepted design, not implementation or validation. If the requested
   change alters accepted research design, confirm the required decision state
   and update the authoritative spec within scope. If the task changes only
   implementation, do not manufacture a design change or a new decision.
4. **Reconcile requirement changes before continuing.** Use a light
   `retain / revise / remove / historical / replace` check across affected
   design, implementation, tests, configs, protocols, results, and current
   docs.
   - Revise the same Working owner when an unfinished proposal changes; do not
     manufacture replacement history for mid-task discoveries.
   - When a stable accepted design is replaced, use the repository's
     cross-linked replacement or supersession convention and do not silently
     rewrite the earlier accepted history.
   - For partial supersession, state what the replacement now owns and what the
     earlier decision continues to own.
   - Stop for decision-authority input when the new direction is not already
     authorized and would materially change the research formulation or an
     accepted trade-off.
5. **Change the owning surface.** Implement the smallest coherent change in
   the active owner. Do not edit archived copies or use them as current
   instructions.
6. **Synchronize only true dependents.** Use these triggers:
   - update the live status owner only if phase, completed work, blocker,
     formal-evidence status, or next step materially changed;
   - update the research spec only if accepted design changed;
   - update the decision register only if decision content or lifecycle changed;
   - update tests when implementation behavior or interfaces require it;
   - update configs when intended execution inputs changed;
   - update protocols when the experiment contract changed;
   - create or update results only for an execution that actually occurred and
     is in scope;
   - update routing/index material only when an authority role or lifecycle
     changed.
7. **Map acceptance to evidence.** Each material acceptance criterion must be
   falsifiable. Record `acceptance criterion -> failure surface -> direct
   evidence/check -> actual result -> highest evidence state`. “Has tests” or
   “has documentation” is a task description, not direct evidence. For a
   negative guarantee or deletion, inspect absence from active owners and
   dependencies; do not require accurate historical/archive references to
   disappear or force a repository-wide zero match. For a governance-only
   criterion, record its direct result and mark the research evidence ladder
   unchanged or not applicable instead of forcing a research-state promotion.
8. **Validate at the correct level.** Run only authorized, proportionate
   checks and record exact commands and outcomes. A test, smoke, preflight, or
   dry-run file only defines a check; only an actual recorded execution can
   establish scoped implementation-test evidence. A config or protocol does
   not establish execution. Artifacts/results default to scoped execution
   evidence. Formal experiment evidence additionally requires explicit
   authorization, the applicable protocol, required provenance/metadata, and
   satisfaction of its artifact contract.
9. **Inspect the final diff.** Confirm allowed files only, no accidental result
   numbers or scientific interpretations changed, and no mutable state was
   duplicated into consumers.
10. **Close the implementation loop.** Report the highest evidence state
   reached and any higher states that remain unproven. Do not mark the task's
   scientific objective validated solely because the implementation task is
   complete.

## Closeout

Closeout mode verifies convergence; it is not a command to update every
document.

1. **Reconstruct the task claim.** Compare the user's requested outcome, the
   actual diff, and recorded commands/artifacts. Separate what was designed,
   implemented, tested, executed, and interpreted.
2. **Check the owner chain.** For each changed mutable fact, verify one current
   owner and accurate dependent pointers. Ensure repo-wide status remains in
   its single live owner and decision lifecycle remains in the decision
   register. Confirm unfinished proposal changes stayed with their Working
   owner, stable replacements are cross-linked, and partial supersession gives
   every retained scope exactly one current owner.
3. **Reconcile acceptance and evidence.** For each material criterion, verify
   the recorded `acceptance criterion -> failure surface -> direct
   evidence/check -> actual result -> highest evidence state` mapping. A
   criterion must be falsifiable, and the actual result must come from a check
   that was really executed; the presence of tests or docs is not enough. For
   governance-only work, report the research evidence ladder as unchanged or
   not applicable.
4. **Check evidence boundaries.** Assign the highest established state:
   proposal, accepted design, implemented, implementation-tested, formal-
   experiment-validated, or supported paper claim. List missing transitions
   explicitly; do not infer them.
5. **Check protocol versus result.** A protocol/config without artifacts is
   pending execution. Artifacts/results default to scoped execution evidence;
   they become formal experiment evidence only when authorization, the
   applicable formal protocol, required provenance/metadata, and its artifact
   contract are all satisfied.
6. **Check historical boundaries.** Current docs must not depend on retired
   authorities. Historical snapshots may retain exact references to retired
   files, old paths, and past statuses when their lifecycle is clear. Negative
   guarantees apply to active owners and dependencies, not accurate historical
   provenance. Do not rewrite history to make a repository-wide text search
   return zero.
7. **Check documentation impact.** Update only surfaces whose owned facts
   changed and that are within scope. If a needed owner is out of scope, report
   the suggested update instead of editing it.
8. **Run final gates.** Use repository-prescribed validation, diff checks, and
   worktree status. Report skipped checks with the reason. Do not run formal
   research workloads merely for closeout.
9. **State the terminal condition.** Use one of:
   - converged at `<evidence state>`;
   - implementation complete, higher evidence pending;
   - blocked by an authority conflict or missing authorization;
   - scoped work complete with an explicitly out-of-scope dependent update.

Closeout is successful when its wording matches the actual evidence state,
not when every possible research stage has been completed.
