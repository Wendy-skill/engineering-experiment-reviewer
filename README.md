# Engineering Experiment Reviewer

A focused AI Skill for reviewing **engineering experimental manuscripts** before submission or revision.

Unlike generic peer-review prompts that spend heavily on language and formatting, this Skill prioritises the parts most likely to affect scientific credibility:

- experimental design and control variables
- instrumentation, calibration, sampling and measurement validity
- repeatability and uncertainty
- data processing and quantitative consistency
- statistical support when relevant
- physical plausibility and mechanism claims
- validation and literature comparison
- scale similarity for scaled experiments
- reproducibility and internal consistency
- claim–evidence alignment

## Core review logic

```text
research question
→ experiment
→ measurement
→ analysis
→ result
→ interpretation
→ conclusion
```

The reviewer looks for breaks in this evidence chain and prioritises issues that could materially weaken the paper.

## Token-conscious design

The Skill uses **conditional checks** rather than forcing every module to run on every manuscript.

Examples:

- scale similarity is checked only for scaled experiments;
- statistics are examined only when statistical inference is relevant;
- validation checks are triggered only when the manuscript makes validation claims or relies on external comparison.

This keeps the Skill compact while preserving the domain-specific checks that matter.

## Output

The default review produces:

1. an overall experimental assessment;
2. a compact experimental evidence map;
3. approximately **5–15 prioritised substantive issues**;
4. a claim–evidence audit;
5. a final risk check identifying the highest-risk issue, the most valuable additional analysis, and any claims that should be weakened.

Each substantive issue includes its location, severity, evidence, scientific consequence, required action, and confidence level.

## Suitable for

Especially useful for experimental papers in fields such as:

- fluid mechanics
- wind-tunnel research
- thermal engineering
- energy engineering
- mechanical engineering
- environmental engineering
- materials engineering
- other laboratory and scaled engineering experiments

## Use

Add `SKILL.md` to a compatible agent/Skill environment, then provide the manuscript and ask the agent to review it using **Engineering Experiment Reviewer**.

Example:

```text
Use the Engineering Experiment Reviewer Skill to review this manuscript.
Prioritise experimental and scientific weaknesses over language editing.
Base every criticism on manuscript evidence and do not invent missing information.
```

## Reliability rules

The Skill explicitly requires the reviewer to:

- distinguish confirmed problems from potential concerns and unreported information;
- avoid inventing experiments, values, uncertainty, specifications or references;
- avoid treating many samples from one run as independent experimental replication;
- avoid treating correlation as demonstrated mechanism;
- avoid demanding additional experiments unless they are genuinely necessary.

Created by **Wendy.z**.
