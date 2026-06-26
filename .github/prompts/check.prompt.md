---
name: check
description: "Prüfen & Freischalten: Code/Struktur lesen, Feedback geben, Step DONE setzen"
agent: "Code Learning Coach"
tools: ["search/listDirectory", "search/fileSearch", "read/readFile", "search/textSearch", "read/problems", "edit/editFiles"]
argument-hint: "Schreibe: Welche Step-ID? Welche Dateien soll ich prüfen?"
---

A) Lies `99-learning-state.instructions.md` und bestimme CurrentStepId.
B) Bitte den Schüler um:
   - Welche Dateien gehören zur Lösung?
   - Was ist das erwartete Verhalten?
C) Prüfe read-only:
   - 'list_dir' (relevante Ordner)
   - 'file_search' (Glob nach relevanten Files)
   - 'read_file' (Kernfiles)
   - 'get_errors' (Diagnose-Sicht)
D) Ergebnis:
   - Wenn Akzeptanzkriterien erfüllt: Step auf [DONE], nächsten Step auf [UNLOCKED], CurrentStepId weiterziehen.
   - Wenn nicht erfüllt: konkrete Hinweise (max. 3), neue Mini-Übung, Step bleibt [UNLOCKED].
E) Update in Lernstand:
   - Leicht/Schwer, typische Fehler, Notizen, Checkpoint-Protokoll.
