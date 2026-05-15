---
slug: physician_accountability_chain
element_type: RULE
mutability: MUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

When AI participates in a clinical pathway, the patient's medical record must reflect an unbroken accountability chain:

1. **Which AI tool participated.** Vendor, model identifier, version, deployment context.
2. **What it produced.** The suggestion, score, flag, or finding it returned, captured verbatim with its uncertainty / confidence indication.
3. **What the physician did with it.** Accepted, modified, or rejected — and, if rejected or modified, a brief clinical reason.
4. **Who the accountable physician is.** Named, licensed, signed.

The chain is a **record requirement**, not a workflow requirement: it does not prescribe how the physician must interact with the AI, only that the interaction is documented in a form that allows after-the-fact reconstruction.

The accountable physician is the licensed counterparty for the clinical decision. Their accountability is **not** transferred to the AI vendor by virtue of having used the tool.

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. Placeholder. The exact field-set, retention period, and audit-access rules are for the domain author to specify.

## Why this rule

`01-human-in-the-loop-authority` requires that AI is adjunct, not authority. Without an accountability-chain record, that requirement is unenforceable in practice — there is no trail by which to reconstruct who decided what and why.

This is the operational counterpart to the principle: the rule that turns "physician decides" into a thing you can audit.

## Reasoning trail

- Aligns with classical malpractice doctrine on the accountable physician.
- Aligns with `01-human-in-the-loop-authority` (PRINCIPLE) — operationalizes its requirement #2.
- Aligns with federation kernel `transparency` IMMUTABLE applied at the per-encounter level.
- Anticipates the audit needs of payors, regulators, and (rarely but importantly) malpractice litigation — the chain is what makes the claim "the physician decided" defensible.

## Open questions for the domain author

- Is the chain part of the standard record schema (HL7 / FHIR), or a parallel log? The implementation cost differs sharply.
- What is the retention period? Suggested floor: the malpractice statute of limitations in the deployment jurisdiction.
- Who can request the audit — the patient, the physician, the institution, the regulator? At what scope?

## Related elements

- `01-human-in-the-loop-authority` (PRINCIPLE) — the principle this rule operationalizes
- `clinical-decision` (TERM) — the activity being recorded
- `physician-irreducible` (TERM) — what the chain protects
- `algorithm-disclosure-to-patient` (RULE) — patient-facing counterpart

## Awaiting domain author

Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
