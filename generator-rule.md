---
title: Generator Rule
tags: [unfold/core]
schema: expansion
jsonld:
  "@context": https://schema.org
  "@type": Collection
  name: Generator Rule
---

# Generator Rule

## Summary

- Capture the anamorphic functions (`u`) that expand seeds into ordered
  structures.
- Define how generator rules operate over the fold schema with explicit
  input/output behavior.

## Evidence

- Instances of generator rules will map minimal seeds to sequences
  `[e₀, e₁, e₂, …]`.
- Connects to the `fold` note through `seed(F)` composition.

## Graph links

- Hub: [[readme.md]], [[sitemap.md]], [[obsidian-handbook.md]]
- Backlinks: [[fold.md]], [[termination.md]], [[examples.md]]
- Tags: `#unfold/core`, `#unfold/schema`

## Next steps

- Document concrete generator functions (e.g., even number pipeline).
- Capture annotations for rule persistence/termination interplay.

## Schema map

- `u: seed → [e₀, e₁, e₂, …]` anamorphism
- `u(seed(F))` equal to `unfold(F, u)`
