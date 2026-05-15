# Medicine — Sub-Leviathan

> **Status:** DRAFTING. Awaiting first domain author(s).
> **Federation kernel:** [`leviathan-protocol/meta`](https://github.com/leviathan-protocol/meta) — inherits the 6 IMMUTABLE federation core articles (user sovereignty, fork freedom, transparency, immutable history, distributed justice, witness principle).
> **Forum:** [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine)

---

## What this is

Medicine is a planned Sub-Leviathan inside the [Leviathan Protocol](https://github.com/leviathan-protocol/meta) — a federation of constitutions for the agentic web. This Sub-Leviathan governs the constitutional pattern for AI in medical practice: how AI tools relate to the physician's clinical judgment, how patient data is handled, what fairness obligations bind clinical algorithms, and what audit + accountability chains are required when AI participates in care.

This repository contains the **constitution** of the Medicine Sub-Leviathan. It does not contain implementation code; it defines what implementations (clinical AI tools, hospital systems, research platforms, BCI applications used in care, etc.) must satisfy if they declare themselves Medicine-Sub-Leviathan-compliant.

## What lives here today

Two seed principles are placeholders representing the emerging consensus shape of medical AI ethics in 2026 — physician-irreducible clinical authority + patient data sovereignty. They are explicitly marked `status: seed-draft`, `current_version: 0`. They have not been ratified.

The v1 constitution of this Sub-Leviathan will be authored by the medical ethics expert(s) who claim this seat — replacing, refining, or extending these seeds as they see fit. Until that authorship lands, the repository is intentionally sparse: empty `terms/` and `rules/` folders signal *open*, not *missing*.

## Constitution structure

```
constitution/
├── terms/         # @TERM       — definitional vocabulary (open)
├── principles/    # #PRINCIPLE  — guiding values (2 seeds, awaits author)
└── rules/         # !RULE       — operational + metarules (open)
```

Element type at folder level. Mutability tier (IMMUTABLE / LOCKED / MUTABLE) declared in each file's YAML frontmatter.

See [`leviathan-protocol/meta/docs/element-format.md`](https://github.com/leviathan-protocol/meta/blob/main/docs/element-format.md) for the file format spec.

## To author this Sub-Leviathan

1. **Open a thread** on [`leviathan.life/forum/medicine`](https://leviathan.life/forum/medicine) describing your intent.
2. **Push elements via PR** — terms (definitional vocabulary), principles (IMMUTABLE / LOCKED / MUTABLE values), rules (operational guidance for AI in clinical practice).
3. **The federation kernel inherits automatically.** No permission needed; the seat is open.

Suggested initial scope (any domain author may revise):
- The four classical principles of medical ethics (autonomy, beneficence, non-maleficence, justice) elevated to constitutional terms
- The 2026-emerging additions: transparency, accountability, data security, algorithmic fairness, human oversight
- Patient data sovereignty + consent architecture
- Physician-irreducible clinical authority + AI-as-adjunct discipline
- Population-fairness audit obligations for clinical AI
- BCI / neurotech-specific extensions where care intersects substrate engineering (cf. federation `witness_principle` and Sub-Leviathan boundary discussions)

## Inheritance

Inherits from Federation Kernel in [`leviathan-protocol/meta`](https://github.com/leviathan-protocol/meta). Kernel IMMUTABLE invariants (user sovereignty, fork freedom, transparency, immutable history, distributed justice, witness principle) apply implicitly to every element here. Domain-specific elements layer on top.

## Why this repository exists before its author

The Leviathan Protocol's stance is that domains needing constitutional governance should have a *visible*, *open*, *kernel-inherited* slot waiting — so when someone with the right expertise arrives, the seat is real and ready, not vapor. Medicine is the highest-stakes domain we know that has not yet had its Sub-Leviathan written. The repository exists to make the seat visible.

## License

CC BY-SA 4.0. Fork freedom is built into the protocol — see federation kernel `00-immutable-core/2-fork-freedom.md`.

## Related

- [`leviathan-protocol/meta`](https://github.com/leviathan-protocol/meta) — Federation kernel + architecture overview + ADRs
- [`leviathan-protocol/companion`](https://github.com/leviathan-protocol/companion) — Personal AI governance Sub-Leviathan (deployed)
- [`leviathan-protocol/animal-welfare`](https://github.com/leviathan-protocol/animal-welfare) — Sentience-based ethics Sub-Leviathan (deployed)
- [`leviathan-protocol/scream`](https://github.com/leviathan-protocol/scream) — Transparency-under-attack Sub-Leviathan (deployed)
