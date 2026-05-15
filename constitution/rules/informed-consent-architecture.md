---
slug: informed_consent_architecture
element_type: RULE
mutability: MUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

The architecture of `@informed-consent` in AI-mediated care is **separately scoped, time-bound, and revocable** along at least these axes:

1. **Care vs. training.** Consent for AI use in the patient's clinical care is a separate decision from consent for the patient's data to be used in AI training. **Bundling them is prohibited.** A patient may consent to one without the other; care cannot be conditioned on training consent.
2. **Scope.** Each consent specifies which data, for which AI tool / which research program, for what purpose, with what retention.
3. **Duration.** Each consent is time-bound. Indefinite consent is not consent; it is a waiver dressed as consent.
4. **Revocation with downstream cleanup.** Consent is revocable at any time. Revocation triggers an obligation on every system that received the data: stop processing, delete (where technically possible), and document the deletion. "We can't unbake the model" is not an acceptable answer for future training; for past training, the obligation is disclosure of the limit, not pretense that it doesn't exist.
5. **Comprehension floor.** The disclosure must be in language the patient can understand. Comprehension is verified as a clinical interaction, not as a checkbox.

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. Placeholder. The exact form of separately-scoped consent (one document with multiple sections, multiple documents, conversational + recorded), the retention defaults, and the audit obligations are for the domain author.

## Why this rule

The classical informed-consent form was designed for a world where the patient's consent was for a procedure done **to** them by a known professional. AI introduces a third actor whose use of patient data continues long after the encounter ends. Without architecture — separate scopes, time bounds, revocability — consent collapses into a one-time waiver that the patient cannot meaningfully retract.

The "no bundling" rule specifically blocks a known failure mode: vendors and hospitals treating "agreement to AI training" as a precondition for accessing AI-mediated care. That conditioning makes consent coerced and is a hard floor for this rule.

## Reasoning trail

- Aligns with `02-patient-data-sovereignty` PRINCIPLE — the consent architecture is how the principle becomes operational.
- Aligns with `informed-consent` TERM — implements the separately-scoped + time-bound + revocable requirements.
- Aligns with GDPR Article 7 (specific, informed, freely given consent) and equivalent.
- Aligns with federation kernel `user-sovereignty` IMMUTABLE applied at the patient layer.

## Open questions for the domain author

- Default duration: 12 months? Care episode? Clinical relationship?
- Revocation cascade: how is "downstream cleanup" enforced when the data has flowed through 4 systems? What is the audit trail standard?
- Capacity-limited patients (incapacity, pediatrics): how does the architecture apply to surrogate decision-makers? How does the patient reclaim consent on regaining capacity / age of majority?

## Related elements

- `02-patient-data-sovereignty` (PRINCIPLE) — the principle this rule operationalizes
- `informed-consent` (TERM) — the term this rule architects
- `health-data-vs-ordinary-data` (TERM) — the data class this consent governs
- `data-flow-audit-mandate` (RULE) — what the revocation cascade is audited against

## Awaiting domain author

Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
