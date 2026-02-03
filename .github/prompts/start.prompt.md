---
name: start
description: "Erststart: Begrüßung, Lernziel klären, Plan erstellen, Lernstand speichern"
agent: "Training-Trainer"
tools: ["readFile", "editFiles"]
argument-hint: "Was willst du lernen? (Thema, Sprache/Stack, Niveau, Zieltermin)"
---

1) Lies `.github/instructions/99-learning-state.instructions.md`.
2) Begrüße den Schüler und stelle 5–7 kurze Fragen:
   - Ziel (konkret), Vorkenntnisse, Sprache/Stack, Zeitbudget/Woche, Lernstil, Kontext (Schule/Job), Erfolgskriterium.
3) Erstelle einen Plan mit 5–12 Steps (STEP-01 …) inkl. Akzeptanzkriterien je Step.
4) Setze: CurrentStepId=STEP-01, UnlockedUpTo=STEP-01.
5) Schreibe alles in `99-learning-state.instructions.md`.
6) Gib eine kurze Erklärung + erste Übung für STEP-01 (ohne Tools zu benutzen).
