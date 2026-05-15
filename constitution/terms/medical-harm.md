---
slug: medical_harm
element_type: TERM
mutability: MUTABLE
inline: true
current_version: 0
status: seed-draft
contentURI: null
---

`@harm` in the Medicine Sub-Leviathan denotes any AI-mediated outcome that injures the patient or the integrity of the physician-patient relationship. It is broader than physical injury and explicitly includes:

- **Clinical harm** — incorrect diagnosis, missed finding, inappropriate treatment, delayed care.
- **Statistical harm** — systematic underperformance for a specific population (rural, women, elderly, ethnic minority, low-income), even when aggregate accuracy is high.
- **Dignity harm** — reduction of the patient to a data object; loss of the patient's voice in their own care.
- **Privacy harm** — exposure, secondary use, or re-identification of patient health data outside consented scope.
- **Authority displacement harm** — clinical decision effectively made by an opaque algorithm, with the physician serving as legal cover rather than accountable counterparty.

<!-- BELOW THIS LINE: editorial context. Not stored on-chain. Not yet ratified. -->

---

## Status

`seed-draft` · `current_version: 0`. Placeholder representing the field's emerging consensus on what AI-era medical harm includes. The first domain author will refine, narrow, broaden, or restructure this definition.

## Why distinct from generic `@harm`

Federation-wide harm definitions exist (cf. `leviathan-protocol/animal-welfare/terms/` and `leviathan-protocol/companion/`). Medicine's harm carries the additional weight of irreversibility — many medical errors cannot be undone, and the substrate (the patient's body) is the patient. The term must reflect this.

## Reasoning trail

- Beauchamp/Childress non-maleficence principle is the philosophical floor.
- 2024–2026 medical AI ethics literature explicitly names statistical harm + algorithmic fairness as required additions to traditional harm taxonomies.
- The "authority displacement harm" category is novel-to-medicine and reflects the AI-era specific failure mode where the legal accountability rests with the physician but the actual decision is the algorithm's.

## Related elements

- `01-human-in-the-loop-authority` (PRINCIPLE) — the structural protection against authority displacement
- `algorithmic-fairness` (TERM) — equity standard against statistical harm
- `bias-monitoring-requirement` (RULE) — operational safeguard against statistical harm

## Awaiting domain author

Open the conversation at [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine).
