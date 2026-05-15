---
slug: patient_data_sovereignty
element_type: PRINCIPLE
mutability: IMMUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

Patient health data is the patient's sovereign property. It may not be used for AI training, secondary processing, or any non-care purpose without specific informed consent — with clear scope, duration, and revocation right. Data flow must be auditable end-to-end. The standard for handling health data is the patient-physician confidentiality standard, applied across all AI-mediated systems.

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. **Not ratified.** This element is a placeholder representing the emerging consensus shape of medical AI ethics in 2026. The v1 of this principle will be authored by the medical ethics expert(s) who claim the Medicine Sub-Leviathan author seat — replacing, refining, or extending this seed.

## What this principle would establish (if ratified)

Health data is not "data." It carries the patient's body, history, vulnerability, intimate facts. Its handling cannot inherit defaults from generic data ethics; it must inherit the more demanding standard of medical confidentiality, applied uniformly across every system that touches it — including AI training pipelines, secondary research uses, hospital analytics, and downstream products.

Concretely:

1. **No silent training.** Patient data may not enter an AI training corpus without specific informed consent for that use, separately from consent for clinical care.
2. **Scoped, time-bound, revocable consent.** Consent specifies what data, for what purpose, for how long, and may be revoked at any time — with downstream cleanup obligations on every system that received the data.
3. **End-to-end auditability.** Every flow of patient data through AI systems is logged: source, recipient, purpose, retention, transformation. The patient (or their representative) can request the audit trail.
4. **No anonymization shortcut for sovereignty.** "It's anonymized" is not a substitute for consent; re-identification risk in modern AI contexts is high enough that anonymization alone is insufficient governance.

## Why immutable (proposed tier)

Patient sovereignty over their own health data is the constitutional ground of the physician-patient relationship. If the data substrate is governed by a different (looser) standard than the clinical encounter, the substrate corrupts the encounter.

If this principle is removed, fork to escape — it is the floor.

## Reasoning trail

- Aligns with classical medical confidentiality (Hippocratic, Beauchamp/Childress autonomy principle).
- Aligns with federation kernel `user-sovereignty` IMMUTABLE — applied here as patient sovereignty in clinical context.
- Aligns with Companion L2 `data-on-device` IMMUTABLE — sovereignty of personal data, applied here to clinical data.
- Aligns with 2025–2026 emerging medical AI ethics literature naming "data security" as required addition to traditional medical ethics.
- Anticipates BCI / neurotech intersection: as cognitive substrate becomes addressable (Blindsight, TRIBE v2), the data-sovereignty principle extends to neural data — directly relevant to UNESCO Recommendation on the Ethics of Neurotechnology (November 2025).

## Related elements (would be authored)

- `informed-consent-architecture` (RULE) — operational standard for AI-context consent
- `data-flow-audit-mandate` (RULE) — what auditing is required, who can request it
- `health-data-vs-ordinary-data` (TERM) — definitional distinction
- `re-identification-risk-floor` (RULE) — minimum protection against re-identification attacks on "anonymized" datasets

## Awaiting domain author

This element awaits the first medical-ethics domain author. Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
