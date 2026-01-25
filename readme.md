---
title: Unfold Obsidian Vault
jsonld:
  "@context": https://schema.org
  "@type": CreativeWork
  name: Unfold Obsidian Vault
---

# Unfold Obsidian Vault

This repository is the starting point for turning the **Unfold** concept into a
navigable Obsidian vault rooted in this directory. The unfolding process is the
inverse of a cognitive **fold**, and the vault will document how the structured
engine behind your Basis project expands compressed views into richly detailed
representations.

## Definition (explicit)

An **unfold** is a systematic expansion of a concise, folded schema or set into
a more detailed representation according to a defined generator function or
rule. In this project, unfolding takes a compressed cognitive **fold** (a
navigable view over a Borel-like set) and expands it into a sequence or
structure that reveals the elements composing it under a specific generative
rule.

## Reasoning steps

1. **Input — Folded structure**\
   Start with a fold (`F`), a schema-bounded markdown view representing an
   abstract set (`S`). This compressed information has an associated generator
   function (`g`). The known fact is that `F` encodes `S` under a compression
   mapping `c: S → F`.

2. **Generator rule (`G`)**\
   Define an **unfold rule** `u` that maps a seed (often a minimal
   representation inside `F`) into a potentially infinite sequence or expanded
   set of elements. Formally, `u: seed → [e₀, e₁, e₂, …]`. This embodies the
   anamorphism over the schema.

3. **Operation**\
   Apply `u` iteratively to produce detail: `unfold(F, u) = u(seed(F))`. Each
   output element is guided by `u`, representing the rule-driven expansion of
   the compressed view.

4. **Closure and termination criteria**\
   Respect termination constraints or coinductive definitions for infinite
   structures. Define a predicate `p(e)` that halts expansion when `p(eₙ)` is
   true.

5. **Output — Expanded structure**\
   The result is a sequence or enriched structure that mirrors the original
   Borel-like set in detail while preserving schema constraints. This can be
   presented as detailed markdown, navigable nodes, or annotated sets.

## Invariant summary

Unfold = **Generator rule + Seed extraction + Iterative expansion + Termination
criterion**\
This reconstructs the latent structure from the compressed fold without losing
traceability.

## Mini example (schema frame)

- Fold (`F`): “Even numbers up to `N` compressed with step 2”
- Seed: `0`
- Unfold rule: `u(x) = x + 2`
- Termination: `p(x) = (x > N)`
- Result: `[0, 2, 4, ..., N]`

## Output summary

Unfold in the Basis engine is the **rule-guided expansion** of a compressed
cognitive fold into a detailed structure, operationalized by an anamorphic
generator that preserves schema boundaries and termination semantics. Learn more
at [https://unfold.robertdelanghe.com](https://unfold.robertdelanghe.com).

## Graph links

- Hub: [[sitemap.md]], [[obsidian-handbook.md]], [[graph-schema.md]]
- Related: [[fold.md]], [[generator-rule.md]], [[termination.md]],
  [[examples.md]]
- Tags: `#unfold/vault`, `#unfold/core`

## Next steps: Obsidian vault conversion

1. Treat this repository root as the Obsidian vault so each conceptual
   note—definition, rule set, examples, and invariants—lives in a markdown file
   within the vault.
2. Create vault notes for `fold.md`, `generator-rule.md`, `termination.md`, and
   `examples.md`, linking them through Obsidian backlinks to reflect the unfold
   workflow.
3. Build templates for anamorphic expansions and schema frames so contributors
   can capture new folds/unfolds consistently.
4. Start parsing the provided sitemap XML into markdown so the vault includes
   each canonical page and can evolve into detailed notes for each URL.
5. Each canonical page now has a seed vault note (`vault/*.md`) with frontmatter
   pointing back to the sitemap; expand them with summaries, backlinks, and
   further unfolds as you explore the published content.
6. Model the vault graph and schema via `vault/graph-schema.md`, and use
   `vault/templates/standard-note.md` as the template for every new concept
   note.
7. Build/validation context lives under `build/obsidian-validation.md`, and the
   minimal `.obsidian/` folder demonstrates a root-level configuration the
   validator expects.
8. See `vault/obsidian-handbook.md` for how we’re modeling Obsidian’s config,
   storage, and editing conventions in this vault.

Next steps: 1) Populate each sitemap-based note with published-page detail using
the standard template, 2) Refresh `vault/sitemap.md` through
`scripts/parse_sitemap.py` whenever the sitemap changes so the graph stays in
sync, 3) Define `.obsidian/` settings (workspace, dataview, templates) from
`vault/obsidian-handbook.md` once tooling settles.
