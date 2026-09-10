# Projektregeln für Codex

## Grundprinzip

- Arbeite ausschließlich im aktuellen Repository und Arbeitsordner.
- Erstelle keine Dateien außerhalb des Projekts.
- Websites bleiben lokal im Projektordner.
- Niemals Sites Hosting verwenden.
- Niemals automatisch deployen oder veröffentlichen.
- Keine Dateien nach Sites übertragen.
- Die ausdrücklichen Anweisungen des Benutzers haben Vorrang.
- Bestehende Architektur, Scripts, Dependencies und Package Manager beibehalten.

## Webentwicklung

- Baue normale Websites, keine Landingpages, sofern der Benutzer nichts anderes sagt.
- Untersuche zuerst die bestehende Projektstruktur.
- Verwende lokale Assets aus `public/` oder `src/`.
- Keine externen CDN-Abhängigkeiten ohne ausdrückliche Freigabe.
- Responsive für Mobile, Tablet und Desktop entwickeln.
- Accessibility, SEO und Ladezeit berücksichtigen.
- Vor Abschluss die Website lokal im Browser prüfen.

## Animationen

- Jede Animation wird mit lokal eingebundenem GSAP umgesetzt.
- Kein GSAP über CDN.
- Keine Framer-Motion-, Anime.js- oder ähnlichen Libraries verwenden.
- Für Scroll-Animationen GSAP mit ScrollTrigger verwenden.
- Animationscode unter `src/animations/` organisieren.
- Animationen müssen performant und touch-tauglich sein.
- `prefers-reduced-motion` berücksichtigen.
- In React Animationen korrekt aufräumen, zum Beispiel mit `gsap.context()`.
- Sobald eine Aufgabe Animationen, Motion, Scroll-Effekte, Parallax,
  Transitions oder Page Transitions enthält, automatisch `ui_gsap` verwenden.
- Der Lead-Agent darf Animationscode nicht mit einer anderen Library umsetzen.

## Lokales SEO

- Jede normale Website muss auf lokales SEO geprüft werden.
- Landingpages sind von dieser Pflicht ausgenommen, sofern nichts anderes
  angeordnet wird.
- Prüfe regionale Keywords und Ortsbezeichnungen.
- Prüfe Title, Meta Description und H1.
- Prüfe Name, Adresse und Telefonnummer.
- Prüfe Kontakt- und Standortinformationen.
- Prüfe Öffnungszeiten.
- Prüfe LocalBusiness-Schema.
- Prüfe Google-Maps-Verlinkung.
- Prüfe interne Verlinkung.
- Prüfe Sitemap, Robots und Canonicals.
- Prüfe Indexierbarkeit, mobile Darstellung und Ladezeit.
- Wenn lokales SEO nicht sinnvoll ist, begründe dies im Abschlussbericht.

## Automatisches Routing

- Der Benutzer muss keinen Agenten ausdrücklich nennen.
- Entscheide anhand des Auftrags automatisch, welcher Agent zuständig ist.
- Frage nicht nach, welcher Agent verwendet werden soll.

### Animation

Wenn Animationen benötigt oder erwähnt werden:

1. `ui_gsap` einsetzen.
2. GSAP lokal einbinden.
3. Animationscode zentral organisieren.
4. Das Ergebnis anschließend in die Website integrieren.
5. Lokal im Browser prüfen.

### Prüfung

Wenn der Benutzer „prüfe“, „überprüfe“, „auditieren“ oder „review“ sagt:

- Bei einer normalen Website automatisch `local_seo` und `reviewer` verwenden.
- Bei einer Landingpage automatisch `reviewer` verwenden.
- Lokales SEO bei Landingpages nur bei ausdrücklicher Anweisung prüfen.
- Beide Prüfungen zuerst read-only durchführen.
- Ergebnisse nach Priorität zusammenfassen.

### Social Media

Wenn der Auftrag Social-Media-Content, Redaktionsplanung, Captions,
Hooks oder Visual-Briefings betrifft:

- automatisch `social_content` verwenden.
- Nur in `content/` und `public/social/` arbeiten.
- Keinen Anwendungscode verändern.
- Nichts veröffentlichen.

## Agents

- `lead` koordiniert Planung, Umsetzung und Integration.
- `ui_gsap` bearbeitet Animationen und Motion.
- `local_seo` prüft lokales SEO read-only.
- `reviewer` prüft Code, UI, Accessibility und Qualität read-only.
- `social_content` erstellt Social-Media-Material.
- Schreibende Agents dürfen nicht gleichzeitig dieselben Dateien bearbeiten.
- Read-only-Prüfungen dürfen parallel laufen.

## Abschluss

Vor dem Abschluss einer normalen Website automatisch:

1. lokale SEO-Prüfung
2. Code- und UI-Review
3. lokale Browserprüfung
4. Build
5. Lint
6. vorhandene Tests

Keine Veröffentlichung und kein Deployment durchführen.
