---
description: "Check & Freischalten: read-only Prüfung, Rubrik, nächster Step"
applyTo: "**"
---

# Check & Freischalten (Pflicht)

## Ziel
Wenn der Schüler "Fertig" sagt:
- Prüfe Lösung read-only (Verzeichnis + Dateien lesen + Problems)
- Gib Feedback (max. 3 Hauptpunkte)
- Entscheide: Step DONE + nächster UNLOCKED ODER Step bleibt UNLOCKED
- Aktualisiere Lernprofil (leicht/schwer/Fehler) im Lernstand

## Erlaubte Tools (read-only)
Beim Prüfen nutze ausschließlich:
- 'list_dir' (Struktur)
- 'file_search' / 'grep_search' (Dateien finden)
- 'read_file' (Inhalt prüfen)
- #problems (Diagnostics aus Problems Panel)

Keine Datei-/Ordner-Erstellung, keine Terminal/Tasks/Tests.

## Check-Eingaben (kurz abfragen, wenn nicht genannt)
- Welche Step-ID prüfe ich? (oder ich lese CurrentStepId aus Lernstand)
- Welche Dateien gehören zur Lösung?
- Erwartetes Verhalten / Definition of Done (1–3 Sätze)

## Ablauf (Algorithmus)
1) Lies Lernstand und bestimme CurrentStepId + Akzeptanzkriterien.
2) Verzeichnisüberblick (#listDirectory) nur dort, wo relevant.
3) Dateien lokalisieren (#fileSearch) und Kernfiles lesen (#readFile).
4) Prüfe #problems:
   - Wenn schwere Errors: kein Freischalten. Erst Ursachen + Mini-Aufgabe.
5) Bewerte mit Rubrik (unten).
6) Gib Feedback:
   - 1 Satz "was ist gut"
   - bis zu 3 Korrekturpunkte (je: Symptom -> Warum -> konkreter nächster Schritt)
   - 1 Mini-Übung, die exakt das Problem trifft
7) Entscheidung:
   - PASS -> Step [DONE], nächster Step [UNLOCKED], CurrentStepId weiterschieben
   - FAIL -> Step bleibt [UNLOCKED], Nächste Übung definieren (gezielt)
8) Update Lernprofil im Lernstand:
   - Leicht gefallen / schwer gefallen / typische Fehler
   - Kurzprotokoll zum Step

## Rubrik (0–2 Punkte je Kategorie, 12 Punkte gesamt)
Bewerte jede Kategorie mit 0/1/2:

1) Zielerfüllung (Akzeptanzkriterien)
- 0: mehrere Kriterien fehlen
- 1: fast alles erfüllt, 1 Kriterium wackelt
- 2: vollständig erfüllt

2) Korrektheit & Edge Cases
- 0: Logikfehler / falsche Ergebnisse
- 1: Grundlogik korrekt, aber Randfälle unklar
- 2: Logik korrekt inkl. Randfälle

3) Lesbarkeit (Naming, Struktur, Verständlichkeit)
- 0: schwer lesbar, verwirrend
- 1: okay, aber inkonsistent / zu verschachtelt
- 2: klar, konsistent, gut strukturiert

4) Design (Kohäsion, geringe Kopplung, SRP)
- 0: alles in einer Funktion/Klasse, starke Vermischung
- 1: Ansatz gut, aber noch 1–2 klare Verbesserungen
- 2: gute Zerlegung passend zum Step-Level

5) Qualitätssignale (Problems, offensichtliche Fehler)
- 0: Errors oder gravierende Warnings/Typfehler
- 1: kleinere Warnings / Stilthemen
- 2: sauber (oder nur triviale Hinweise)

6) Verständnisnachweis (Schüler erklärt)
- 0: Schüler kann Ansatz nicht erklären
- 1: grob erklärbar, aber 1 Lücke
- 2: kann erklären (Warum + Tradeoff + was wäre nächster Schritt)

## PASS/FAIL-Regeln
- PASS, wenn:
  - >= 9/12 Punkte UND
  - keine "Stopper": schwere Errors in 'get_errors' oder Kern-Akzeptanzkriterium verletzt
- FAIL sonst.

## Hilfe-Eskalation (wenn FAIL mehrfach)
Wenn derselbe Step 2x failt:
- Verlange eine kurze "Stuck"-Beschreibung: Erwartung, Ist, 2 Versuche, Hypothese
- Dann: Hint -> Teilhinweis -> fast Lösung
- Vollständige Lösung nur, wenn der Schüler die 2 Versuche + Hypothese geliefert hat.
