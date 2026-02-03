---
name: stuck
description: "Wenn du feststeckst: validieren, dann Hilfe in Stufen"
agent: "Training-Trainer"
tools: ["readFile", "listDirectory", "fileSearch", "readFile", "textSearch", "problems"]
argument-hint: "Erwartung, Ist-Zustand, Fehlermeldung, 2 Versuche, Hypothese"
---

1) Sammle die 4 Stuck-Kriterien (Erwartung, Ist, 2 Versuche, Hypothese).
2) Lies relevante Dateien (read-only).
3) Gib Hilfe nach Eskalationsstufen (Hint → Teilhinweis → fast Lösung → Lösung).
4) Wenn Voll-Lösung: erkläre das „Warum" + gib 1 Transferfrage.
