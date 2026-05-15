---
slug: human_in_the_loop_authority
element_type: PRINCIPLE
mutability: IMMUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

AI tools in medical practice support physician judgment; they do not substitute for it. Final clinical authority and responsibility rest with the licensed physician. Every patient interaction involving AI must preserve a clear chain of human oversight, recorded in the medical record, with the AI's role documented as adjunct rather than authority.

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. **Not ratified.** This element is a placeholder representing the emerging consensus shape of medical AI ethics in 2026. The v1 of this principle will be authored by the medical ethics expert(s) who claim the Medicine Sub-Leviathan author seat — replacing, refining, or extending this seed.

## What this principle would establish (if ratified)

The clinical decision is the physician's, not the model's. AI in medicine is **adjunct**, not authority. This means:

1. **No autonomous clinical action.** AI tools may surface evidence, suggest options, flag patterns, score risk — but the act of treating a patient (prescribing, intervening, referring, deferring) is a human clinical decision, recorded as such.
2. **Transparent role disclosure in the record.** When AI participates in a clinical pathway, the patient's record reflects which AI tool contributed, what it suggested, what its uncertainty was, and how the physician acted on (or against) the suggestion.
3. **No removal of physician liability.** A physician cannot transfer clinical accountability to "the algorithm." The accountability chain remains intact.

## Why immutable (proposed tier)

Without this principle, the practice of medicine — a profession defined by the physician-patient relationship and the physician's accountable judgment — collapses into a delivery surface for opaque algorithmic recommendations. The AI provider then occupies the position legally, ethically, and practically reserved for the licensed clinician. That displacement is the failure mode this Sub-Leviathan exists to prevent.

If this principle is removed, fork to escape — it is the floor.

## Reasoning trail

- Aligns with classical Beauchamp/Childress autonomy + non-maleficence framing (the patient's autonomy is preserved by an accountable human counterparty, not an opaque system).
- Aligns with federation kernel `transparency` IMMUTABLE (clinical AI use is logged + reviewable) and `distributed-justice` IMMUTABLE (clinical authority cannot concentrate in a software vendor's training pipeline).
- Aligns with 2025–2026 emerging medical AI ethics literature naming "human oversight" as required addition to traditional medical ethics.

## Related elements (would be authored)

- `physician-accountability-chain` (RULE) — operational definition of how AI involvement is logged
- `algorithm-disclosure-to-patient` (RULE) — what the patient is told about AI's role in their care
- `medical-harm` (TERM) — domain-specific harm definition that includes harm from AI authority displacement

## Awaiting domain author

This element awaits the first medical-ethics domain author. Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
