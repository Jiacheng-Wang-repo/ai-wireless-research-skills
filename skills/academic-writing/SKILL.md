---
name: academic-writing
description: Draft, revise, polish, or audit scientific manuscripts, conference papers, journal articles, technical reports, abstracts, captions, and experimental discussions by selecting scientifically necessary content, building a coherent evidence-supported narrative, preserving technical meaning, matching claim strength to evidence, maintaining quantitative and terminology consistency, and separating observations from interpretation and speculation. Use for scientific prose tasks and as the reusable scientific-writing baseline for reviewer responses; do not use it alone for reviewer-response structure or workflow, repository operations, or paper-specific factual decisions.
---

# Academic Writing

Apply evidence-bounded scientific-writing discipline without overriding the
paper's own constraints, canonical text, or evidence.

Scientific writing is selective argumentation under evidence constraints, not
exhaustive reporting of everything known, available, technically interesting,
or potentially defensible. Evidence is the hard boundary of what may be
claimed, but evidence discipline should not itself organize the prose.

## Establish Authority and Scope

1. Follow repository and workflow policy.
2. Apply this skill as the reusable writing baseline.
3. Follow paper-, venue-, and revision-specific constraints; they may be
   stricter than this skill.
4. Use canonical artifacts and supporting evidence for factual and numerical
   claims.

Do not use a general writing preference to change an objective, method,
experimental protocol, numerical value, attribution boundary, or accepted
technical meaning.

## Decide What Belongs in the Manuscript

Admit content to the main scientific narrative only when it performs a
necessary scientific role, such as:

- establishing why the problem matters;
- identifying the gap that motivates the work;
- stating the paper's distinctive capability, mechanism, or advantage;
- explaining how the proposed method addresses that gap;
- providing evidence required for a central claim;
- explaining an important observed behavior or tradeoff;
- distinguishing the contribution from the most relevant alternative; or
- defining a scope condition necessary to interpret a result correctly.

Content does not belong in the main narrative merely because it is true,
available, technically interesting, already computed, or potentially useful
against a hypothetical reviewer objection.

For each candidate item, ask:

1. What claim or part of the scientific story does this support?
2. Would removing it make the contribution less clear, less credible, or
   scientifically misleading?
3. Is this the correct place and level of detail for it?

If the first two answers are no, omit the item from the main narrative or move
it to supporting material when appropriate. If it is scientifically needed
but misplaced or over-detailed, relocate or compress it rather than allowing
it to obscure the argument.

## Choose the Narrative Around the Strongest Supported Value

Do not organize a paper around everything the method does. Identify the
smallest set of evidence-supported capabilities or advantages that makes the
work scientifically distinctive, and build the narrative around that set.
Prefer the smallest coherent set of strong scientific messages over a larger
collection of weakly connected contributions.

When several narratives are possible, prefer the one that:

1. is most directly supported by the strongest evidence;
2. most clearly distinguishes the work from relevant prior approaches;
3. explains why the proposed design is needed rather than merely describing
   its components; and
4. remains consistent from the abstract and introduction through the
   experiments and conclusion.

Do not automatically promote content that does not strengthen this narrative
into a secondary contribution. Narrative selection cannot override complete
relevant evidence or justify exaggerated novelty.

## Give Each Paragraph One Scientific Job

Before drafting or editing a paragraph, identify its dominant purpose, such
as:

- motivating a problem;
- exposing a limitation of the relevant prior paradigm;
- introducing a design principle;
- explaining a mechanism;
- interpreting an experimental result;
- comparing alternatives;
- establishing generalization, efficiency, or scalability; or
- delimiting scope when scientifically necessary.

A paragraph may contain supporting details, but it should have one dominant
scientific purpose. Remove or relocate a sentence that is individually correct
but pulls the paragraph toward a different job. Do not preserve a sentence
merely because it is technically correct when it damages emphasis, flow, or
paragraph coherence.

## Use Experiments as Arguments

Treat experiments as evidence for scientific claims, not as an inventory of
everything tested. Before promoting an experiment into the main manuscript,
identify the scientific question it answers.

A main-text experiment should normally do at least one of the following:

- establish the primary performance or capability claim;
- isolate the source of an important gain;
- demonstrate value in the target regime;
- characterize an important tradeoff or scaling behavior; or
- rule out a plausible alternative explanation that would materially weaken a
  central claim.

If an experiment does not materially change what the reader should believe
about the contribution, it does not automatically deserve space in the main
narrative. Do not accumulate baselines, metrics, ablations, or diagnostics
solely to make the evaluation appear comprehensive.

Do not suppress evidence that materially contradicts a central claim. Revise
the claim or interpretation to the strongest formulation supported by the
complete relevant evidence.

## Default Exclusions from the Main Narrative

Unless scientifically necessary, do not promote the following into the main
scientific narrative:

- implementation history or failed intermediate attempts;
- exhaustive hyperparameter-search details;
- repository, provenance, or audit information;
- negative results unrelated to a central claim;
- generic limitations that follow directly from the chosen scope;
- speculative reviewer objections;
- future directions that do not sharpen the present contribution;
- secondary metrics unrelated to the stated scientific objective; or
- redundant experiments supporting a conclusion already established
  convincingly.

## Classify Each Scientific Statement

For content that is already scientifically needed, identify the role of each
statement before drafting or editing it:

- **Observation:** What was directly measured, calculated, or shown.
- **Supported interpretation:** What the evidence reasonably suggests within
  its scope.
- **Hypothesis or speculation:** A possible explanation not established by the
  evidence.
- **Limitation:** A boundary of the design, data, experiment, or conclusion.
- **Future direction:** Work not yet performed or validated.

Keep these roles linguistically distinct. Do not present an interpretation as
a measurement, a hypothesis as a mechanism, or future work as a completed
result.

This classification is a control mechanism, not a completeness checklist. It
does not require every section to contain a limitation, speculation, caveat,
or future direction. Do not generate those categories merely because the
taxonomy includes them.

## Calibrate Claims to Evidence

- State empirical results as empirical results. Do not convert correlation,
  ablation behavior, or performance differences into causal or mechanistic
  proof without an experiment that supports that inference.
- Bound every conclusion to the evaluated datasets, conditions, methods,
  metrics, and uncertainty actually represented by the evidence.
- Attribute a gain to one component only when the comparison isolates that
  component sufficiently. Otherwise use a multi-factor or evidence-bounded
  interpretation.
- Prefer a strong claim with a precise scope over a weak claim with a broad
  scope. If the evidence directly supports a bounded strong conclusion, state
  it directly; do not replace it with generic language merely to sound
  cautious. For example, do not weaken `consistently outperforms X across the
  tested network sizes` to `achieves competitive performance under various
  settings` when the former is directly supported.
- Use terms such as `suggests`, `indicates`, `is consistent with`, and `under
  the evaluated settings` when the inference is interpretive. Do not add
  qualifiers mechanically when a direct bounded statement is already accurate.
- When presenting a scientific result or conclusion, lead with the strongest
  conclusion the evidence supports. Once the relevant experimental or
  methodological scope is clear in the surrounding text, do not repeat
  qualifiers such as `under the evaluated settings` unless needed to prevent a
  materially broader interpretation.
- Let evidence discipline constrain claim strength without dominating the
  scientific narrative. Keep audit-level traceability and provenance in
  evidence records or working material unless those details are scientifically
  necessary for the reader; do not turn manuscript prose into an audit trail.
- Separate broader implications from demonstrated conclusions and label
  untested explanations or extensions as hypotheses or future work.

## Control Defensive Qualification

Before introducing a caveat, limitation, negative comparison, or defensive
qualification, require at least one of the following:

1. Without it, the scientific claim would be false or materially misleading.
2. It is explicitly required by a reviewer, editor, venue rule, or applicable
   paper-specific instruction, and the issue appropriately belongs in the
   manuscript rather than response-only material.
3. The scope boundary is necessary for the reader to interpret the result
   correctly.

If none applies, omit the qualification. Do not convert scope into weakness.
For example, prefer the neutral scientific form `We study learning-based
resource allocation under the stated system model` over `The proposed method
is limited to learning-based resource allocation under the stated system
model` unless the limitation itself is scientifically material to the
argument.

Once scope is clear, do not repeat qualifiers mechanically. Do not append
generic limitations or future-work statements merely for completeness, and do
not anticipate hypothetical reviewer attacks inside the manuscript.

## Align Comparisons with the Scientific Claim

- Center comparisons on evaluation dimensions scientifically relevant to the
  problem, contribution, and intended use.
- Do not promote a secondary metric into a central competition merely because
  it exists, and do not let an irrelevant metric redefine the paper's main
  scientific question.
- Do not suppress required or materially contradictory evidence. If a result
  directly bears on a central claim, address it honestly and narrow the claim
  if necessary rather than changing the criterion after seeing the result.
- Frame tradeoffs when scientifically accurate. A method need not be described
  as universally superior when its supported value lies in a particular
  performance, generalization, adaptation, scalability, or efficiency regime.

## Control High-Risk Terms

Use the following only when their technical conditions are explicitly met:

- `optimal`, `global optimum`, `upper bound`;
- `universal`, `robust`, `general`, `state-of-the-art`;
- `significant` when statistical significance could be implied;
- `real-time`, `deployment-ready`, `scalable`.

The purpose is calibrated use, not automatic weakening. Do not mechanically
replace a justified strong term with weaker language. When a strong term is
supported only within a bounded scope, retain it and state that scope
precisely.

Do not call the best result from a finite search, restart set, sample, or
heuristic a theoretical optimum or upper bound. Describe the actual finite
procedure instead.

## Report Statistics and Computational Cost Precisely

- State what is averaged, the evaluation unit, sample count, aggregation rule,
  and uncertainty source when material to interpretation.
- Do not treat variation across test samples as variation across training
  seeds, datasets, sites, or independent replications.
- Do not claim statistical significance without an appropriate test and
  comparison design.
- Distinguish wall-clock measurements, profiler estimates, analytical
  complexity, analytical operation counts, memory measurements, and parameter
  counts. Never present one as another.
- State material hardware, batching, precision, or implementation conditions
  when a computational claim depends on them.

## Preserve Traceability and Consistency

- Keep every quantitative claim traceable to its source result, configuration,
  method variant, dataset, metric definition, and aggregation rule.
- Do not invent, interpolate, select a stronger variant, or silently promote a
  preliminary or weakly validated result.
- Do not infer that an experiment failed or never existed merely because local
  evidence is missing. Report the evidence gap and verify the applicable
  records.
- Check consistency among equations, objectives, symbols, terminology, units,
  figure and table labels, captions, reported values, normalization
  denominators, and surrounding prose.
- Preserve distinctions among absolute and normalized metrics, training and
  evaluation regimes, and measured and derived quantities.

## Edit Scientific Prose Surgically

- Preserve technical meaning while improving grammar, precision, concision, or
  flow.
- Prefer the smallest edit that fully resolves the scientific and narrative
  problem.
- Do not preserve local wording merely to minimize diff size when doing so
  leaves the argument fragmented, defensive, repetitive, or poorly
  emphasized.
- When the user explicitly requests narrative restructuring, or when local
  patches would accumulate caveats and weaken the scientific story, rewrite
  the paragraph or section around the strongest evidence-supported logic.
- Preserve unrelated notation, citations, facts, and accepted technical
  decisions.
- Write positive, direct manuscript prose. Integrate necessary limitations
  naturally rather than accumulating defensive caveats or checklist language.
- Remove repetition without deleting a definition, condition, or evidence
  boundary needed for self-contained understanding.

## Final Scientific-Writing Check

Before handing off prose, verify:

1. Every factual and numerical statement has an identifiable evidence basis.
2. Claim strength does not exceed the experiment or analysis.
3. Observation, interpretation, speculation, limitation, and future work are
   distinguishable.
4. Scope, statistics, units, objectives, and computational measures are stated
   consistently.
5. High-risk terms are justified or replaced with precise bounded wording.
6. The edit preserves scientific meaning and changes no unrelated content.
7. The manuscript reads as a coherent research document rather than a response
   letter or a list of caveats.
8. The central contribution and its strongest supporting evidence are visible
   without requiring the reader to infer them from implementation details,
   figures, or tables.
9. No sentence unnecessarily expands the paper's burden of proof, turns a
   scope choice into a methodological weakness, or introduces a caveat that
   does not materially improve scientific accuracy.
10. Every major paragraph, experiment, and comparison has a clear role in the
    scientific argument rather than appearing only because the information is
    available.

## Exclusions

Do not use this skill to supply:

- reviewer-response structure, quotation handling, rebuttal workflow, or
  response-only evidence policy;
- Git, worktree, environment, file-routing, or artifact-protection policy;
- paper-specific scientific facts, terminology decisions, claim boundaries, or
  venue requirements;
- numerical values, configurations, seeds, hardware facts, or provenance that
  must come from the applicable evidence records.
