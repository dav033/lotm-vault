---
type: review-index
status: active
last-audited: 2026-07-28
spoilers: major
---

# Pending Review

## Summary

- 256 unique notes require review.
- 236 notes use `status: interpretation` because no processed source is both official and high reliability.
- 132 Authority notes have direct medium-reliability sources but require primary verification.
- 31 Sequence notes are interpretations pending official sourcing.
- 22 Pathway Hubs are interpretations; 21 also lack Sequences 8–0.
- 20 substantive notes use workflow or classification values as epistemic `status` and require migration.
- 28 links across 20 notes still use a Sequence 9 node as if it were a Pathway Hub.
- 11 of the same policy-migration notes are missing mandatory `source-confidence`; this overlap does not increase the unique-note total.

## Interpretation Queue

```query
path:"02-Wiki" [status:interpretation]
```

## Strict Policy Migration

### Invalid epistemic status

The following 20 substantive notes MUST receive an epistemic `status`. Move lifecycle state to `workflow-status` where needed.

- Authority maps: [[Calamity of Destruction Authority Map]], [[Demon of Knowledge Authority Map]], [[Eternal Darkness Authority Map]], [[Father of Devils Authority Map]], [[God Almighty Authority Map]], [[Goddess of Origin Authority Map]], [[Key of Light Authority Map]], [[Lord of Mysteries Authority Map]], [[The Anarchy Authority Map]].
- Powers: [[Puppetry (Fool)]], [[Spirit World Access (Door)]].
- Symbolism and access maps: [[Change (Fool Symbolism)]], [[Door Pathway Symbolism]], [[Door Sefirah Borrowing]], [[Fool Pathway Symbolism]], [[Fool Sefirah Borrowing]], [[Foolishness (Fool)]], [[Inconceivable and Bizarreness (Lord of Mysteries)]], [[Lord of Mysteries Symbolism]].
- Visual classification: [[Fool Pathway Sigil - Secrecy]].

### Sequence 9 used as Pathway

The following 20 notes contain 28 invalid Pathway references. Replace them with their canonical `* Pathway` Hubs. Actual Sequence references in progression maps are excluded.

- Frontmatter: [[Filth and Corruption (Hanged Man)]], [[Grazing]], [[Knowledge (White Tower)]], [[Puppetry (Fool)]], [[Spirit World Access (Door)]], [[Change (Fool Symbolism)]], [[Decay]], [[Door Pathway Symbolism]], [[Eternal Rest]], [[Fool Pathway Symbolism]], [[Foolishness (Fool)]], [[Key of Light Symbolism]], [[Passage of Time]], [[Sacrifice (Hanged Man)]], [[Sin-Bearing]].
- Body text: [[Chaos]], [[Charm]], [[Demon of Knowledge Symbolism]], [[Eternal Darkness Symbolism]], [[God Almighty Symbolism]].

### Missing source confidence

The following 11 notes MUST add `source-confidence` consistent with their direct source classification:

- [[Calamity of Destruction Authority Map]], [[Demon of Knowledge Authority Map]], [[Eternal Darkness Authority Map]], [[Father of Devils Authority Map]], [[God Almighty Authority Map]], [[Goddess of Origin Authority Map]], [[Key of Light Authority Map]], [[Lord of Mysteries Authority Map]], [[The Anarchy Authority Map]], [[Spirit World Access (Door)]], [[Lord of Mysteries Symbolism]].

## Incomplete Pathway Progressions

### Lord of Mysteries Group

- [[Door Pathway]]
- [[Error Pathway]]

### God Almighty Group

- [[Visionary Pathway]]
- [[Tyrant Pathway]]
- [[White Tower Pathway]]
- [[Sun Pathway]]
- [[Hanged Man Pathway]]

### Eternal Darkness Group

- [[Darkness Pathway]]
- [[Death Pathway]]
- [[Twilight Giant Pathway]]

### Calamity of Destruction Group

- [[Demoness Pathway]]
- [[Red Priest Pathway]]

### Demon of Knowledge Group

- [[Hermit Pathway]]
- [[Paragon Pathway]]

### Key of Light Group

- [[Wheel of Fortune Pathway]]

### Father of Devils Group

- [[Chained Pathway]]
- [[Abyss Pathway]]

### Goddess of Origin Group

- [[Mother Pathway]]
- [[Moon Pathway]]

### The Anarchy Group

- [[Black Emperor Pathway]]
- [[Justiciar Pathway]]

## Sequence Source Queue

All 31 existing Sequence notes now have `status`, `source`, and `spoilers`. Their sources remain unofficial and medium reliability.

```query
path:"02-Wiki/Pathways/Standard-Pathways" [type:sequence] [status:interpretation]
```

## Authority Source Queue

All 132 Authority notes link a source note and carry `spoilers: major`. Official chapter, announcement, or handbook citations remain required before promotion to `canon`.

```query
path:"02-Wiki/Symbolism and Authorities/Authorities" [type:authority] [status:interpretation]
```

## Explicit Integration Gaps

- [[Lord of Mysteries Authority Map]] — Error Pathway Authority map pending sourced integration.
- [[Lord of Mysteries Symbolism]] — Error Pathway Symbolism map pending sourced integration.
- [[Fool Pathway Sigil - Secrecy]] — visual association remains unconfirmed as conceptual Symbolism.

## High-Priority Confidence Review

- [[Fate (Fool)]] — `probable-interpretation`
- [[History (Fool)]] — `strong-inference`
- [[Calamity of Destruction Symbolism]] — `strong-inference`
- [[Father of Devils Symbolism]] — `strong-inference`
- [[God Almighty Symbolism]] — `strong-inference`
- [[Goddess of Origin Symbolism]] — `strong-inference`

## Counting Rule

Total counts unique notes matching at least one condition: `status: interpretation`, a substantive note using a non-epistemic `status`, `sequence-map-status: pending`, explicit unresolved wording, or an incomplete integration map. Overlaps count once.
