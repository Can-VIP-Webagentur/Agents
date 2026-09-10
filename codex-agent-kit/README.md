# Codex Agency Agent Kit

Dieses Paket ist für lokale Webentwicklung im Repository gedacht.

## Installation

1. Kopiere den Inhalt dieses Ordners in den Root deines Kunden-Repositories.
2. Behalte eine vorhandene `AGENTS.md` und führe die Regeln bei Bedarf zusammen.
3. Installiere GSAP, falls es noch nicht im Projekt vorhanden ist:

   ```bash
   npm install gsap
   ```

4. Starte eine neue Codex-Sitzung im Repository.
5. Prüfe die Einrichtung mit:

   ```text
   Prüfe die aktiven Projektanweisungen und nenne die erkannten Agents.
   Nimm keine Änderungen vor.
   ```

## Enthalten

- `AGENTS.md` – dauerhafte Projektregeln und automatisches Routing
- `.codex/config.toml` – Multi-Agent-Konfiguration
- `.codex/agents/` – spezialisierte Agents
- `src/animations/gsap.ts` – zentraler lokaler GSAP-Import
- `content/` – Social-Media- und SEO-Arbeitsmaterial
- `public/social/` – lokale Social-Media-Assets

## Feste Regeln

- Kein Sites Hosting
- Kein automatisches Deployment
- Websites bleiben lokal im Repository
- Animationen immer mit lokal eingebundenem GSAP
- Normale Websites immer auf lokales SEO prüfen
- Landingpages nur auf ausdrückliche Anweisung auf lokales SEO prüfen
