---
slug: algorithm_disclosure_to_patient
element_type: RULE
mutability: MUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

When AI participates materially in a patient's care, the patient must be told — before the care episode if practicable, otherwise at the earliest reasonable point — that:

1. **An AI tool is involved**, named at the level of vendor + role (diagnostic, triage, monitoring, suggestion).
2. **What the tool's role is.** Is it suggesting a diagnosis to the physician? Scoring risk for triage? Continuously monitoring for deterioration? The patient gets the operational picture, not just the brand name.
3. **What its known limitations are.** Especially: known performance gaps for the patient's subgroup (age, sex, ethnicity, comorbidity profile) where reportable.
4. **That the physician is the decision-maker.** The AI suggests; the physician decides; the patient may discuss either with the physician.

Disclosure is in language the patient can understand. Technical specification language is not disclosure. Comprehension is a clinical responsibility.

Material participation is defined by the domain author; the seed proposes: any AI involvement that influences a `@clinical-decision` (diagnosis, treatment, intervention, referral, deferral, risk allocation).

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. Placeholder. The threshold for "material participation", the medium of disclosure (verbal, written, both), and the exception conditions (emergency, incapacity) are for the domain author.

## Why this rule

The patient cannot exercise informed consent over AI's role in their care if they don't know AI has a role. Disclosure is the prerequisite for autonomy.

It is also the prerequisite for trust calibration: a patient who knows the AI's limitations for their subgroup can ask the physician questions that align the care plan with their values.

## Reasoning trail

- Aligns with classical informed-consent doctrine (Beauchamp/Childress autonomy principle).
- Aligns with `informed-consent` TERM — operationalizes the disclosure-of-AI-involvement requirement.
- Aligns with `02-patient-data-sovereignty` PRINCIPLE — the patient knowing what AI processes their care is the substrate of being able to decide about their data.
- Aligns with federation kernel `transparency` IMMUTABLE applied at the patient-facing layer.

## Open questions for the domain author

- What is "material participation"? Where is the threshold below which disclosure is excessive (a spell-checker on the dictation), and above which it is required (a sepsis prediction model)?
- Verbal, written, both? Recorded acknowledgement, or default-on with opt-out?
- Emergency exception: when the disclosure cannot precede the care, what is the post-hoc disclosure obligation?

## Related elements

- `informed-consent` (TERM) — the AI-era consent standard this rule serves
- `01-human-in-the-loop-authority` (PRINCIPLE) — the principle this rule communicates to the patient
- `physician-accountability-chain` (RULE) — record-side counterpart
- `algorithmic-fairness` (TERM) — the subgroup-limitations field draws from this

## Awaiting domain author

Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
