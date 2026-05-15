---
slug: algorithmic_fairness
element_type: TERM
mutability: MUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

`@algorithmic-fairness` in the Medicine Sub-Leviathan is the property of an AI tool that performs comparably across the patient populations it is deployed for. It is **not** satisfied by aggregate accuracy. A model that is 95% accurate overall but 60% accurate for women over 65, or for rural patients, or for any underrepresented group, **fails algorithmic fairness regardless of its aggregate score**.

Operationally, fairness requires:

1. **Stratified performance reporting.** Performance is reported separately for each clinically meaningful subgroup the tool is intended to serve.
2. **Subgroup floor.** A minimum acceptable per-subgroup performance is defined before deployment, not after.
3. **Continuous monitoring.** Fairness is re-measured in production, not just at validation. Drift in subgroup performance triggers review.
4. **Disclosure to clinician and patient.** When a tool's performance is materially worse for the patient's subgroup, the physician knows and the patient is told.

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. Placeholder. The fairness literature is large and evolving; the domain author should pick the operational definition that fits the regulatory and clinical reality of the deployment context.

## Why this is load-bearing

Aggregate-accuracy framing systematically hides harm to minority populations. A tool can pass FDA validation, look excellent in trials, and still produce statistical harm at scale because the trial population was not representative. This term names the failure mode and makes it auditable.

## Reasoning trail

- Connects directly to `medical-harm` term's "statistical harm" category.
- Aligns with 2025–2026 medical AI ethics literature naming algorithmic fairness + bias monitoring as core requirements.
- Aligns with federation kernel `distributed-justice` IMMUTABLE applied at the population level.
- Anticipates the regulatory direction signaled by FDA, EMA, and equivalent bodies' moves toward stratified performance disclosure.

## Open questions for the domain author

- Which subgroups must be reported on by default (age, sex, race, geography, comorbidity status)? Is there a universal minimum, or domain-specific?
- What's the acceptable subgroup floor — relative to aggregate (e.g., no subgroup more than X% below) or absolute (no subgroup below Y)?
- How is fairness enforced when training data is itself biased and cannot be fixed at the dataset level?

## Related elements

- `medical-harm` (TERM) — statistical harm category
- `bias-monitoring-requirement` (RULE) — operational implementation
- `02-patient-data-sovereignty` (PRINCIPLE) — consented training data is part of the fairness substrate

## Awaiting domain author

Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
