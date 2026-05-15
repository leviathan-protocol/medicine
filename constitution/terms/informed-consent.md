---
slug: informed_consent
element_type: TERM
mutability: MUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

`@informed-consent` in the AI-mediated medical context is consent that meets the classical informed-consent standard (capacity, disclosure, comprehension, voluntariness) **and additionally** the AI-era requirements:

1. **Disclosure of AI involvement.** The patient is told which AI tool participates in their care, what role it plays (diagnostic, triage, suggestion, monitoring), and what its known uncertainty / failure modes are.
2. **Scope, duration, revocation.** Consent for AI use in care is separately scoped from consent for AI training. Each scope is time-bound and revocable, with downstream cleanup obligations on every system that received the data.
3. **Comprehension does not require expertise.** The disclosure must be in language the patient can understand, not in technical specification language. Comprehension is a clinical responsibility, not a documentation formality.
4. **No bundled consent.** Consent for clinical care cannot be conditioned on consent for AI training or secondary research. Each is a separate decision.

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. Placeholder representing the AI-era extension of classical informed consent. Awaits domain author refinement.

## Why this is more demanding than classical informed consent

Pre-AI informed consent assumed the physician was the locus of clinical judgment and the patient was the locus of value. AI introduces a third actor whose role, uncertainty, and training history are usually opaque to both. Without explicit disclosure + separately-scoped + revocable consent, the patient consents to a black box wearing the physician's coat.

## Reasoning trail

- Beauchamp/Childress autonomy principle is the philosophical floor.
- 2025–2026 medical AI ethics literature names "transparency" and "data security" as required additions; this term operationalizes both within the consent framework.
- Aligns with federation kernel `transparency` IMMUTABLE and Companion L2 `transparent-mediation` LOCKED.
- Anticipates BCI / neurotech intersection: consent in the substrate-engineering era requires more, not less, granularity.

## Related elements

- `02-patient-data-sovereignty` (PRINCIPLE) — the constitutional ground
- `informed-consent-architecture` (RULE) — operational standard
- `algorithm-disclosure-to-patient` (RULE) — what the patient is told about AI's role

## Awaiting domain author

Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
