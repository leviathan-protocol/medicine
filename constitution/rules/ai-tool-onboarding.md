---
slug: ai_tool_onboarding
element_type: RULE
mutability: MUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

Before an AI tool is deployed in clinical practice, it must complete a structured onboarding that produces a **deployment dossier**. The dossier is reviewable by the institution, the operating physicians, and (in summary form) the patient. It contains, at minimum:

1. **Intended use statement.** Population, indication, role in the clinical pathway, what decision it informs, what it explicitly does not decide.
2. **Training-data lineage.** Source(s), date range, population characteristics, known representational gaps. Where consent was the basis for inclusion, the consent regime is summarized.
3. **Validation results, stratified.** Per-subgroup performance with confidence intervals. Aggregate performance is reported alongside, never alone.
4. **Known failure modes.** Documented cases where the tool was wrong in a clinically meaningful way; what triggered the failure; what the mitigation is.
5. **Monitoring plan.** Per `bias-monitoring-requirement`: subgroups monitored, drift thresholds, escalation path.
6. **Accountability map.** Vendor's clinical-affairs counterparty, institutional owner, escalation contact for a clinically suspected error.
7. **Sunset plan.** Conditions under which the tool will be withdrawn (regulatory, performance, vendor discontinuation), and the patient/care continuity plan when that happens.

The dossier is a **living document**, updated when training data, model version, or known failure modes change. Each version is retained.

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. Placeholder. Format, audit access, and the precise threshold of "deployed in clinical practice" (vs. evaluation, vs. research) are for the domain author.

## Why this rule

Most AI failures in medicine are not technical surprises; they are **deployment surprises** — the tool was used in a population it wasn't trained for, the EHR field it depends on changed schema, the vendor stopped updating it, the clinical workflow drifted. The dossier is the artifact that lets institutions detect and prevent these failures before they become harm.

It is also the document a regulator, payor, or court can request after an incident — the answer to "what did you know, when, and what did you do about it?"

## Reasoning trail

- Aligns with `01-human-in-the-loop-authority` PRINCIPLE — the dossier is the record that lets physicians know what they're working with.
- Aligns with `02-patient-data-sovereignty` PRINCIPLE — the training-data lineage section is the patient-facing accountability for how their data class was used.
- Aligns with `physician-accountability-chain` RULE — the dossier feeds the per-encounter chain.
- Aligns with `bias-monitoring-requirement` RULE — the monitoring plan is part of the dossier.
- Aligns with `algorithm-disclosure-to-patient` RULE — patient-facing summary draws from the dossier.
- Aligns with federation kernel `transparency` IMMUTABLE and `immutable-history` IMMUTABLE.

## Open questions for the domain author

- Audit cadence: annually? On every major version? On every minor?
- Patient-facing summary: standardized one-pager? Plain-language pamphlet? Verbal at point of care?
- How does the rule scale to thousands of small tools (a hospital may deploy hundreds of AI components)? Tiered by risk class?

## Related elements

- `01-human-in-the-loop-authority` (PRINCIPLE)
- `02-patient-data-sovereignty` (PRINCIPLE)
- `physician-accountability-chain` (RULE) — per-encounter counterpart
- `bias-monitoring-requirement` (RULE) — monitoring plan section
- `algorithm-disclosure-to-patient` (RULE) — patient-facing summary draws from dossier
- `algorithmic-fairness` (TERM) — stratified validation requirement

## Awaiting domain author

Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
