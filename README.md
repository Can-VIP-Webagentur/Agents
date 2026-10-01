# Can VIP Agent Kit

Eine Sammlung von Codex-Regeln und Skills für Webprojekte. Die Anleitung ist bewusst einfach gehalten: Sie zeigt, welche Rolle und welcher Skill bei welcher Aufgabe hilft.

## Schnellstart

1. Öffne den Ordner `codex-agent-kit`.
2. Kopiere seinen Inhalt in den Hauptordner deines Projekts.
3. Wenn dort bereits eine `AGENTS.md` liegt, führe die Regeln zusammen und ersetze die Datei nicht blind.
4. Starte Codex neu oder öffne eine neue Sitzung im Projekt.
5. Beschreibe deine Aufgabe. Codex kann passende Skills automatisch auswählen. Du kannst einen Skill auch ausdrücklich nennen, zum Beispiel `$threejs-web`.

## Was ist ein Agent? Was ist ein Skill?

- Ein **Agent** ist eine spezialisierte Rolle für einen Teil der Arbeit, zum Beispiel eine Prüfung oder Animation.
- Ein **Skill** ist Fachwissen mit konkreten Hinweisen für eine bestimmte Aufgabe, zum Beispiel GSAP in React.
- `AGENTS.md` enthält die Regeln, nach denen Codex die Arbeit organisiert.

## Agentenrollen

Die folgenden Rollen sind in [`codex-agent-kit/AGENTS.md`](codex-agent-kit/AGENTS.md) beschrieben:

| Rolle | Einsatz |
| --- | --- |
| `lead` | Plant die Arbeit und fügt Teilergebnisse zusammen. |
| `ui_gsap` | Setzt Animationen mit GSAP um. |
| `local_seo` | Prüft lokale Suchmaschinenoptimierung, zum Beispiel Ortsangaben, Öffnungszeiten und LocalBusiness-Daten. |
| `reviewer` | Prüft Code, Darstellung und Barrierefreiheit. |
| `social_content` | Erstellt Social-Media-Texte und Inhalte. |

Die Rollen werden über die Projektregeln angesprochen. Eigene Agent-Konfigurationsdateien liegen derzeit nicht im Paket.

## Skills

Alle 14 Skills liegen unter `codex-agent-kit/.agents/skills/`.

| Skill | Wann er hilft |
| --- | --- |
| `agent-orchestration` | Teilt größere Aufgaben bei Bedarf in unabhängige Arbeit für mehrere Codex-Agenten auf und fügt die Ergebnisse zusammen. |
| `frontend-skill` | Plant und gestaltet visuell starke Webseiten, Apps und Prototypen. Für eine sichere Auswahl `$frontend-skill` nennen. |
| `german-frontend-naming` | Vergibt verständliche deutsche Namen für eigene HTML-, CSS- und JavaScript-Elemente. |
| `threejs-web` | Plant und baut interaktive 3D-Erlebnisse mit Three.js. |
| `gsap-core` | Erstellt grundlegende Animationen mit GSAP. |
| `gsap-frameworks` | Nutzt GSAP in Vue, Svelte und ähnlichen Frameworks. |
| `gsap-performance` | Macht GSAP-Animationen flüssiger und effizienter. |
| `gsap-plugins` | Nutzt Erweiterungen wie Flip, Draggable und SplitText. |
| `gsap-react` | Bindet GSAP in React und Next.js ein. |
| `gsap-scrolltrigger` | Steuert Animationen passend zum Scrollen. |
| `gsap-timeline` | Ordnet mehrere Animationen zeitlich. |
| `gsap-utils` | Nutzt Hilfsfunktionen von GSAP. |
| `exportvip` | Entwickelt aus Webseiten hochwertige VIP-Landingpage-Entwürfe. |
| `landingpages-wording-vip` | Schreibt Texte für Premium-Angebote, Anzeigen und Landingpages. |

## Aufbau

```text
codex-agent-kit/
├── AGENTS.md                 Projektregeln und Rollen
├── README.md                 Anleitung für das Kit
├── .agents/skills/           Die 14 Skills
├── THIRD_PARTY_LICENSES/     Lizenztexte für GSAP und Three.js Skills
└── src/animations/gsap.ts    Zentraler GSAP-Import
```

## Herkunft und Lizenzen

- Die acht GSAP-Skills stammen aus [greensock/gsap-skills](https://github.com/greensock/gsap-skills). Sie stehen unter MIT-Lizenz; der Lizenztext liegt in `codex-agent-kit/THIRD_PARTY_LICENSES/GSAP-SKILLS-MIT.txt`.
- `threejs-web` stammt aus [cesartevisual/threejs-skills](https://github.com/cesartevisual/threejs-skills). Es steht unter MIT-Lizenz; der Lizenztext liegt in `codex-agent-kit/THIRD_PARTY_LICENSES/THREEJS-SKILLS-MIT.txt`.
- `frontend-skill` stammt aus [winklerbremen/codex-skills](https://github.com/winklerbremen/codex-skills/tree/main/skills/frontend-skill). Im Quell-Repository ist keine Lizenzdatei angegeben. Der Skill ist hier mit Herkunftshinweis enthalten; prüfe die Nutzungsrechte, bevor du ihn weiterverteilst.
- `german-frontend-naming`, `exportvip` und `landingpages-wording-vip` wurden aus deinem lokalen Codex-Profil übernommen.

## Sicherheit

Skills enthalten Anweisungen für Codex. Lies fremde Skills, bevor du sie in wichtigen Projekten einsetzt, und gib ihnen nur die Rechte, die sie für die Aufgabe benötigen.
