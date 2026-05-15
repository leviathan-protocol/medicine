---
slug: bias_monitoring_requirement
element_type: RULE
mutability: MUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

Any AI tool deployed in clinical practice must operate under a **continuous bias-monitoring regime**, not a one-time validation:

1. **Pre-deployment subgroup floors.** For each clinically meaningful subgroup the tool serves, a minimum acceptable performance level is declared in advance. Deployment is gated on meeting it.
2. **In-production stratified telemetry.** Tool performance is measured continuously, stratified by subgroup, in the actual deployment population (not the trial population).
3. **Drift triggers.** A defined drop in subgroup performance triggers human review. The trigger is automatic; the response is clinical.
4. **Disclosure on drift.** If a subgroup's performance falls below the declared floor, the operating physicians are informed and the tool's use for that subgroup is reviewed. If the issue cannot be remediated, the tool is withdrawn for that subgroup or for all use.
5. **Public-facing transparency.** A summary of subgroup performance is available to the patient (or their representative) who asks. Trade-secret claims do not extend to performance disclosure.

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. Placeholder. The exact subgroups, drift thresholds, telemetry standard, and disclosure format are for the domain author. The rule encodes the structure; the parameters are for the field.

## Why this rule

`@algorithmic-fairness` and `@medical-harm` (statistical-harm category) are unenforceable without monitoring. A model that is fair at validation can become unfair at deployment as the population shifts, the data drifts, the upstream EHR changes a field, or the disease prevalence moves. **Fairness is a property of the deployment, not the model**, and only continuous monitoring can detect when that property is violated.

The rule explicitly names the trade-secret limit. Vendors will resist disclosure of subgroup performance on commercial grounds; this rule says: that resistance does not survive contact with the patient's right to know how the tool performs for someone like them.

## Reasoning trail

- Aligns with `algorithmic-fairness` (TERM) — implements its continuous-monitoring requirement.
- Aligns with `medical-harm` (TERM) — operational defense against statistical harm.
- Aligns with `02-patient-data-sovereignty` PRINCIPLE — the patient's right to know extends to the tool's behavior on data like theirs.
- Aligns with federation kernel `transparency` IMMUTABLE and `distributed-justice` IMMUTABLE.

## Open questions for the domain author

- Which subgroups must be monitored by default? Minimum: age × sex × race; expanded by clinical context.
- What is the drift threshold? Relative (X% drop from validation) or absolute (subgroup performance below declared floor)?
- What is the standard telemetry schema so monitoring is portable across institutions and tools?
- Who pays for the monitoring infrastructure — vendor, hospital, or shared?

## Related elements

- `algorithmic-fairness` (TERM) — the property this rule monitors
- `medical-harm` (TERM) — the harm this rule prevents (statistical-harm category)
- `02-patient-data-sovereignty` (PRINCIPLE) — the basis for patient-facing disclosure
- `ai-tool-onboarding` (RULE) — pre-deployment counterpart

## Awaiting domain author

Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
