# Codex Agent Kit

Dieses Paket bringt Projektregeln, Agentenrollen und Skills für die Webentwicklung mit. Eine Übersicht in einfacher Sprache findest du in der [README im Hauptordner](../README.md).

## Installation

1. Kopiere den Inhalt dieses Ordners in den Hauptordner deines Projekts.
2. Behalte eine vorhandene `AGENTS.md` und führe die Regeln bei Bedarf zusammen.
3. Installiere GSAP, falls es noch nicht im Projekt vorhanden ist:

   ```bash
   npm install gsap
   ```

4. Starte eine neue Codex-Sitzung im Repository.
5. Prüfe die Einrichtung mit:

   ```text
   Prüfe die aktiven Projektanweisungen und nenne die erkannten Agentenrollen.
   Nimm keine Änderungen vor.
   ```

## Enthalten

- `AGENTS.md` – dauerhafte Projektregeln und automatisches Routing
- `.agents/skills/` – GSAP-, Three.js- und weitere Web-Skills
- `src/animations/gsap.ts` – zentraler lokaler GSAP-Import
- `THIRD_PARTY_LICENSES/` – Lizenztexte für mitgelieferte GSAP- und Three.js-Skills

Die Rollen `lead`, `ui_gsap`, `local_seo`, `reviewer` und `social_content` sind in `AGENTS.md` beschrieben. Separate Agent-Dateien sind in diesem Paket derzeit nicht enthalten.

## Feste Regeln

- Kein Sites Hosting
- Kein automatisches Deployment
- Websites bleiben lokal im Repository
- Animationen immer mit lokal eingebundenem GSAP
- Normale Websites immer auf lokales SEO prüfen
- Landingpages nur auf ausdrückliche Anweisung auf lokales SEO prüfen
