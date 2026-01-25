---
title: Graph Schema Guide
jsonld:
  '@context': https://schema.org
  '@type': Collection
  name: Vault Graph Schema
---

# Graph + Schema Guide

## Vault graph intent

- Each note should connect back to the core unfold definitions (`fold.md`, `generator-rule.md`, `termination.md`, `examples.md`) so Obsidian can visualize the central schema.  
- Use backlinks to create star-shaped topology around the `Unfold` concept, ensuring tags like `#unfold/core` and `#unfold/schema` appear on the most referenced notes.

## Schema conventions

- Standardize metadata properties:  
  - `status:: draft` / `status:: reviewed`  
  - `schema:: fold` / `schema:: expansion`  
  - `links:: [[fold-engine]]` etc.
- Record generator rules via a structured callout: `> [!QUOTE] Generator Rule` with seed, expansion, termination bullet list.

## Template guidance

- Duplicate templates located in `vault/templates/` (see `vault/templates/standard-note.md`) so that every new note captures Summary, Evidence, Next steps, and Linkage sections.  
- For schema-heavy notes, include a `## Schema map` section that lists the rules or anchors the note references.

## Graph links

- Hub: [[readme.md]], [[sitemap.md]], [[obsidian-handbook.md]]  
- Related: [[fold.md]], [[generator-rule.md]], [[termination.md]], [[examples.md]]  
- Tags: `#unfold/schema`, `#unfold/vault`

## Visualization

- Keep the sitemap note (`vault/sitemap.md`) updated and link each entry to its note using aliases/backlinks; this ensures graph view surfaces the entire fold-engine surface.  
- Periodically open Obsidian’s graph (Core > Graph View) and validate the hubs formed around the `Unfold` tags and BFS-style paths through generator rule notes.
