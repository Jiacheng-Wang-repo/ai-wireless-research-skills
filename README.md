# AI + Wireless Research Skills

Three focused skills for AI + wireless and computational research workflows.

## Choose a skill

| Skill | Responsibility |
|---|---|
| [research-spec-loop](skills/research-spec-loop/SKILL.md) | Research authority, decision lifecycle, evidence states, scoped changes and closeout. |
| [academic-writing](skills/academic-writing/SKILL.md) | Scientific narrative, paragraph coherence, evidence calibration and functional control of defensive writing. |
| [reviewer-response-writing](skills/reviewer-response-writing/SKILL.md) | Complete reviewer-comment coverage, response stance, truthful completion and faithful manuscript quotations; builds on academic-writing. |

## Examples

```text
Use $academic-writing to revise this Results paragraph against the supplied
results. Remove unnecessary defensive wording; preserve the strongest supported
conclusion, numerical values, necessary assumptions and evidence boundaries.
```

```text
Use $research-spec-loop in audit mode to identify authority and evidence-state
drift in the current research design. Report findings without changing files.
```

```text
Use $reviewer-response-writing to answer these comments in their original order.
Address every sub-question using completed evidence and current manuscript text;
keep necessary explanations and label unfinished work accurately.
```

## Installation

The canonical sources are under `skills/`. For user-scope Codex discovery,
symlink the three complete directories into `~/.agents/skills/` under their
existing names. Keep academic-writing and reviewer-response-writing as siblings
so the response skill's dependency resolves.

## Writing references

The functional distinction between self-protection and necessary scientific
content draws on [defensive-writing-governance](https://github.com/Sun-Lebs-For-DeepOM/defensive-writing-governance/tree/6a920c15a95a7bff083fccd5bfa63de169c2d9e0)
and [Nature-Paper-Skills anti-defensive-writing](https://github.com/Boom5426/Nature-Paper-Skills/tree/6f8eaa07b4ea19fecdc73618cad9a65beb49d542/skills/core/anti-defensive-writing).
Rules are integrated in original wording into academic-writing, with no separate
skill, venue-specific default or copied implementation.
