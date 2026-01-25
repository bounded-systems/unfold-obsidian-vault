---
title: Termination
tags: [unfold/core]
schema: guard
jsonld:
  "@context": https://schema.org
  "@type": Collection
  name: Termination
---

# Termination

## Summary

- Enumerate the predicates `p(e)` that halt expansions, especially for
  coinductive or infinite structures.
- Capture the guardrails that ensure the unfolding process remains tractable
  when mapping to published content.

## Evidence

- Every unfold must respect termination criteria (`p(e_n)` stops expansion when
  true).
- Builds on the `generator-rule` note to describe the point at which sequences
  stop.

## Graph links

- Hub: [[readme.md]], [[sitemap.md]], [[obsidian-handbook.md]]
- Backlinks: [[fold.md]], [[generator-rule.md]], [[examples.md]]
- Tags: `#unfold/core`, `#unfold/schema`

## Next steps

- Record termination predicates used by existing sitemap pages (e.g.,
  even-numbers example).
- Relate predicates to business/publishing rules from `publish-limitations.md`.

## Schema map

- `p(e)` predicate definition
- Termination boundary vs. infinite anamorphism tracking
