---
name: german-frontend-naming
description: "Use when creating or refactoring HTML, CSS, or JavaScript so app-specific classes and identifiers use clear, consistent German names instead of generic placeholders."
---

# German Frontend Naming

When authoring application code, use meaningful German names for app-specific CSS classes and JavaScript identifiers. Keep names tied to the actual content, component, state, or action they represent. Follow the repository's existing naming shape where practical, while keeping the names themselves German.

## Naming rules

- Prefer concrete domain terms over generic labels such as `box`, `wrapper`, `item`, `content`, or `data`. Use generic terms only when they accurately describe a reusable structural role.
- Use one consistent German spelling convention. In identifiers, prefer ASCII spellings such as `ue`, `ae`, `oe`, and `ss` rather than umlauts; use ordinary German spelling in visible UI text.
- Use component names that explain purpose, with related elements and states named consistently. BEM-style CSS names are fine when they fit the project, for example `.warenkorb`, `.warenkorb__position`, `.warenkorb__summe`, and `.warenkorb--leer`.
- Name JavaScript variables and functions by the real value or action, for example `warenkorbPositionen` or `berechneGesamtsumme`, rather than `data`, `handleClick`, or `processItem` when a more precise German name is available.
- Avoid invented abbreviations, numbered classes, redundant wrappers, and ornamental naming. Every name should help a maintainer understand the interface or behavior.
- Keep established framework, browser API, package, HTML attribute, and third-party names unchanged. Do not rename public APIs, imported symbols, generated selectors, or existing English names that must match an external contract.
- Respect the surrounding codebase's architecture and formatting. Apply the naming preference to new or requested changes; do not rename unrelated code just for consistency unless the user asks for a broader refactor.

## Anti-generic UI naming

Choose names from the real page or feature vocabulary. For example, for a booking flow use `reiseauswahl`, `abfahrtsdatum`, and `buchung-bestaetigen` instead of `section1`, `card`, and `primary-button`. Keep selectors compact and reusable; don't create a new class for every element when a semantic element or existing component already expresses the role.
