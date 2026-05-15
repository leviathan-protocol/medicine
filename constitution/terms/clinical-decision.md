---
slug: clinical_decision
element_type: TERM
mutability: MUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

A `@clinical-decision` is any judgment that affects diagnosis, treatment, intervention, referral, deferral, or risk allocation for a specific patient. It is distinguished from:

- **Information lookup** (the AI returns guideline content, drug interaction data, literature)
- **Triage suggestion** (the AI orders a queue, surfaces a flag, scores urgency — without acting)
- **Administrative process** (scheduling, billing, documentation generation)

Information lookup, triage suggestions, and administrative processes may be AI-mediated. **Clinical decisions remain the licensed physician's.** This is the boundary that `01-human-in-the-loop-authority` enforces.

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. Placeholder. The boundary between "AI-mediated suggestion" and "AI-made decision" is the highest-stakes definitional question in this Sub-Leviathan; the first domain author must sharpen it.

## Why this term is load-bearing

Without a clear definition of what constitutes a clinical decision, the principle "AI augments, does not replace" is unenforceable in practice. Hospitals will deploy AI tools whose outputs are nominally "suggestions" but operationally function as decisions (because the physician routinely defers to them under time pressure, liability framing, or workflow design).

The term must be operational enough to draw lines that vendors, hospitals, and regulators can apply.

## Edge cases the domain author should address

- **Continuous monitoring** (ICU, telemetry, sepsis prediction): the AI flags but the response is human; clearly a suggestion, not a decision.
- **Closed-loop systems** (insulin pumps, anesthesia regulation): the AI both decides and acts; this is a decision, made by the AI, with implications for accountability.
- **Diagnostic radiology AI**: the AI marks suspicious findings; physician reviews and decides. Suggestion. But what about cases where physician routinely accepts AI verdict without re-reading? At what point does the de facto practice cross into AI decision-making?
- **Triage AI in emergency departments**: the AI orders the queue; this affects who gets seen first, which is a clinical decision about resource allocation.

## Reasoning trail

- Medical-legal precedent: "clinical decision" is defined in malpractice doctrine as the judgment that physicians are accountable for. This term aligns with that definition while making AI involvement explicit.
- Aligns with `01-human-in-the-loop-authority` and reinforces `02-patient-data-sovereignty` (a clinical decision involves patient data; both must be governed).

## Related elements

- `01-human-in-the-loop-authority` (PRINCIPLE)
- `physician-irreducible` (TERM) — the residue AI cannot occupy
- `physician-accountability-chain` (RULE)

## Awaiting domain author

Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
