# Training Workspace – Einstieg für Schüler (VS Code + GitHub Copilot)

Willkommen! In diesem Repository nutzt Du **GitHub Copilot Chat** als **Trainer**, der Dich Schritt für Schritt durch ein Lernziel führt.  
Wichtig: **Du lernst aktiv.** Du erstellst Dateien/Ordner selbst, Du schreibst den Code selbst – der Trainer hilft Dir beim Denken, Prüfen und Verbessern.

---

## Was dieses Repo macht (und was nicht)

✅ Der Trainer darf:

- Deinen Code **lesen** (Dateien/Ordnerstruktur ansehen, Dateien öffnen)
- Dir **kurz & präzise** erklären, Beispiele zeigen und Übungen geben
- Deinen Fortschritt in einer **Lernstands-Datei** speichern (damit Du später weiterlernen kannst)

❌ Der Trainer darf NICHT:

- Dateien/Ordner für Dich **anlegen**
- Terminal/Tasks/Debugging **ausführen**
- Dein Projekt automatisch **scaffolden** (z. B. “neues Projekt erzeugen”)

---

## Voraussetzungen

1. **Visual Studio Code** installiert
2. Extensions installiert:
   - **GitHub Copilot**
   - **GitHub Copilot Chat**
3. Du bist in VS Code mit GitHub angemeldet und Copilot ist für Deinen Account aktiv.

---

## Schritt-für-Schritt Start (Erstes Mal)

### 1) Repo öffnen
- Klone oder lade das Repo herunter und öffne den Ordner in VS Code.
- Wenn VS Code “Recommended Extensions” anzeigt: **Installieren**.

### 2) Workspace Trust erlauben
- Wenn VS Code fragt: **Trust this workspace** → **Trust**  
  (Ohne Trust sind einige Funktionen eingeschränkt.)

### 3) Copilot Chat öffnen
- Links in der Activity Bar: **Copilot Chat** öffnen  
  oder Command Palette: `Copilot Chat: Focus on Chat View`

### 4) Den Trainer-Agent auswählen
- Oben im Chat findest Du ein Dropdown für **Agent/Mode**.
- Wähle den Agent: **Code Learning Coach** (oder ähnlich benannt).

> Falls Du den Agent nicht siehst: Siehe **Troubleshooting** unten.

### 5) Training starten: `/start`
Tippe im Chat z. B.:

`/start Ich will TypeScript-Grundlagen lernen (Funktionen + Typen). Ich bin Anfänger. 3h/Woche.`

Der Trainer wird:
- Dich kurz begrüßen
- Dir ein paar Fragen stellen (Ziel, Niveau, Zeitbudget …)
- einen **Plan (STEP-01, STEP-02, …)** erstellen
- den Plan in die Lernstands-Datei schreiben

### 6) Änderungen bestätigen (wichtig)
VS Code zeigt ggf. eine Änderung an einer Datei an (Proposal/Edit).

✅ **Erlaubt/Ok:** Änderungen an  
- `.github/instructions/99-learning-state.instructions.md`

❌ **Nicht akzeptieren:** Änderungen an Code-Dateien oder neue Dateien/Ordner.

---

## So läuft ein Trainings-Step ab (immer gleich)

### A) Der Trainer erklärt kurz
- Maximal einige Zeilen: Was ist das Ziel dieses Steps?

### B) Du bekommst eine Übung
- Klar und messbar: “Baue X”, “Implementiere Y”, “Erfülle Kriterien Z”

### C) Du arbeitest selbst
- Du erstellst ggf. die nötigen Dateien/Ordner **selbst**
- Du schreibst den Code **selbst**

### D) Du meldest Dich mit “Fertig” + `/check`
Beispiel:

`Fertig. /check STEP-01 Dateien: src/palindrome.ts`

### E) Der Trainer prüft (read-only)
Der Trainer darf:
- Ordnerstruktur ansehen
- Dateien lesen
- Problems/Diagnostics ansehen

Er gibt Dir:
- Feedback (max. 3 Hauptpunkte)
- 1 Mini-Übung zur Korrektur **oder** schaltet den nächsten Step frei

### F) Fortschritt wird gespeichert
Wenn bestanden:
- Step wird als **DONE** markiert
- Nächster Step wird **UNLOCKED**
- Lernprofil wird aktualisiert (leicht/schwer/typische Fehler)

---

## Weitermachen nach Chat-Clear oder später

Wenn Du den Chat-Verlauf löschst oder später zurückkommst:

1) Öffne Copilot Chat
2) Wähle den Agent **Code Learning Coach**
3) Tippe:

`/continue`

Der Trainer liest den Lernstand und macht **genau dort** weiter, wo Du aufgehört hast.

---

## Wenn Du feststeckst: `/stuck`

Nutze:

`/stuck Erwartung: ... Ist: ... Fehlermeldung/Beobachtung: ... Versuche: (1)... (2)... Hypothese: ...`

Der Trainer hilft dann stufenweise:
1) Hint
2) Teilhinweis
3) Fast-Lösung
4) Voll-Lösung (nur wenn wirklich nötig)

---

## Was Du beim Prüfen mitgeben solltest

Damit der Trainer gut prüfen kann, schreibe immer:
- **Step-ID** (oder sag: “aktueller Step”)
- **Dateien**, die geprüft werden sollen
- **Erwartetes Ergebnis** (1–2 Sätze)

Beispiel:

`/check aktueller Step. Dateien: src/app.ts, src/lib.ts. Erwartung: Eingabe "aba" -> true, "abc" -> false.`

---

## Troubleshooting

### Agent “Code Learning Coach” ist nicht sichtbar
- VS Code: `Developer: Reload Window`
- Stelle sicher, dass Copilot Chat installiert/aktiv ist
- Prüfe, ob der Ordner `.github/agents/` im Repo existiert und eine `*.agent.md` Datei enthält

### `/start` wird nicht erkannt
- Prüfe, ob `.github/prompts/start.prompt.md` vorhanden ist
- Reload Window

### Der Trainer will etwas ändern, das nicht erlaubt ist
- **Nicht akzeptieren**
- Antworte im Chat:  
  “Bitte nur Lernstand-Datei aktualisieren, keine Code-Dateien ändern.”

---

## Golden Rules (damit Du wirklich lernst)

- Du schreibst den Code. Der Trainer ist Dein Coach.
- Frage nach “Warum?”, nicht nur nach “Wie?”
- Wenn Du Hilfe brauchst: erst `/stuck`, dann gemeinsam Schritt für Schritt.

Viel Erfolg – und starte mit `/start` 🚀
