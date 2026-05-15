---
slug: health_data_vs_ordinary_data
element_type: TERM
mutability: MUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

`@health-data` is the class of patient information that carries the patient's body, history, vulnerability, and intimate facts. It is **not** "data" in the generic governance sense; it inherits the more demanding standard of **patient-physician confidentiality**, applied uniformly across every system that touches it — clinical, AI training, secondary research, hospital analytics, downstream products.

This term distinguishes health data from ordinary data along four operational axes:

1. **Sensitivity asymmetry.** A leak of ordinary data is reversible (passwords change, cards are reissued). A leak of health data — HIV status, mental-health history, genetic risk, abortion history — is permanent and follows the patient through employment, insurance, family relationships.
2. **Re-identification floor.** "Anonymized" health data, especially genomic + longitudinal, is increasingly re-identifiable in modern AI contexts. Anonymization alone is not adequate governance.
3. **Consent inheritance.** Consent for one use does not inherit to another. Consent for clinical care is **not** consent for training. Consent for one study is **not** consent for downstream model fine-tuning.
4. **Substrate continuity.** As the substrate of experience becomes addressable (BCI, neurotech), neural data joins the health-data class. The term must be future-proof against that expansion.

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. Placeholder. The legal definitions of "health data" / "PHI" / "sensitive personal data" vary across jurisdictions (HIPAA, GDPR, KVKK, etc.); this term is the federation-internal definition that sits **above** any single jurisdiction.

## Why a federation-level term, not just a legal one

Jurisdictional definitions are the floor, not the ceiling. The federation needs a definition that:

- Holds across jurisdictions (a tool deployed in 50 countries cannot use 50 different floors)
- Anticipates substrate expansion (neural data, behavioral biometrics, ambient health monitoring)
- Is actionable — vendors, hospitals, and regulators can apply it to a specific data flow

## Reasoning trail

- Aligns with classical Hippocratic confidentiality, generalized to the AI substrate.
- Aligns with `02-patient-data-sovereignty` PRINCIPLE — this term defines what the principle applies to.
- Aligns with 2025–2026 emerging consensus that "data security" in medical AI requires more than HIPAA-style minimums.
- Aligns with UNESCO Recommendation on the Ethics of Neurotechnology (Nov 2025) on neural-data status.

## Open questions for the domain author

- Where is the boundary between health data and behavior data (steps, sleep, pulse from a wearable)? Is wearable data health data once it enters a clinical pathway?
- How does the term apply to **inferred** health data — a model's prediction of disease risk derived from non-clinical inputs?
- What is the consent posture for health data **about** a person held by **another** person (genetic relatives, household members in a wearable network)?

## Related elements

- `02-patient-data-sovereignty` (PRINCIPLE) — the principle this term is the operational substrate of
- `re-identification-risk-floor` (RULE) — minimum protection against re-identification attacks
- `informed-consent-architecture` (RULE) — operational consent standard for this data class
- `data-flow-audit-mandate` (RULE) — what auditing is required

## Awaiting domain author

Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
