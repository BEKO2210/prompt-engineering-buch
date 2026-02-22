# Checkliste: Fortgeschrittene Techniken

## Chain-of-Thought (CoT)

**Wann nutzen:**
- [ ] Komplexe Probleme
- [ ] Mathematische Aufgaben
- [ ] Logische Schlussfolgerungen
- [ ] Analysen mit mehreren Faktoren

**Checkliste:**
- [ ] Explizit "Schritt für Schritt" angefordert
- [ ] Struktur vorgegeben (1., 2., 3.)
- [ ] Zwischenüberprüfung erwünscht

**Template:**
```
Löse diese Aufgabe Schritt für Schritt:
1. [Schritt 1]
2. [Schritt 2]
3. [Schritt 3]
4. [Schritt 4]

Aufgabe: [Hier die eigentliche Aufgabe]
```

---

## Few-Shot Prompting

**Wann nutzen:**
- [ ] Klassifikationsaufgaben
- [ ] Format-Konsistenz wichtig
- [ ] Stil-Vorgabe nötig

**Checkliste:**
- [ ] 2-5 Beispiele gegeben
- [ ] Beispiele deckungsgleich mit gewünschter Ausgabe
- [ ] Format in allen Beispielen konsistent
- [ ] Edge-Cases abgedeckt (falls nötig)

**Template:**
```
[Hier sind Beispiele für das gewünschte Format:]

Beispiel 1:
Input: [Input]
Output: [Output]

Beispiel 2:
Input: [Input]
Output: [Output]

Beispiel 3:
Input: [Input]
Output: [Output]

Jetzt deine Aufgabe:
Input: [Eigentlicher Input]
Output:
```

---

## System-Prompts

**Wann nutzen:**
- [ ] Wiederkehrende Aufgaben
- [ ] Konsistentes Verhalten über Sessions
- [ ] Team-Workflows

**Checkliste:**
- [ ] Rolle klar definiert
- [ ] Stilmerkmale aufgelistet
- [ ] Regeln explizit formuliert
- [ ] Verhalten in spezifischen Situationen definiert

**Template:**
```
Du bist [Rolle].

Dein Stil:
- [Stilmerkmal 1]
- [Stilmerkmal 2]
- [Stilmerkmal 3]

Deine Regeln:
1. [Regel 1]
2. [Regel 2]
3. [Regel 3]

Bei [Situation] reagierst du mit [Verhalten].
```

---

## Self-Consistency

**Wann nutzen:**
- [ ] Wichtige Entscheidungen
- [ ] Kreative Aufgaben mit Varianten
- [ ] Wenn Qualität wichtiger als Geschwindigkeit

**Checkliste:**
- [ ] Mehrere Varianten angefordert (3-5)
- [ ] Verschiedene Ansätze explizit gewünscht
- [ ] Vergleichsmöglichkeit gegeben

**Template:**
```
Generiere [Anzahl] verschiedene [Ergebnisse] für 
[Aufgabe].

Jede Variante soll einen anderen Ansatz haben:
1. [Ansatz 1]
2. [Ansatz 2]
3. [Ansatz 3]

[Aufgabe]
```

---

## Tree of Thoughts

**Wann nutzen:**
- [ ] Strategieentwicklung
- [ ] Komplexe Probleme mit mehreren Lösungswegen
- [ ] Wenn Exploration wichtiger als eine Antwort

**Checkliste:**
- [ ] Mehrere Pfade explizit erwünscht
- [ ] Bewertungskriterien angegeben
- [ ] Vergleich und Empfehlung angefordert

**Template:**
```
Wir haben ein Problem: [Beschreibung]

Entwickle [Anzahl] verschiedene Lösungsansätze.
Für jeden Ansatz:
1. Beschreibe die Idee
2. Liste Vor- und Nachteile
3. Schätze den Aufwand (low/medium/high)
4. Bewerte die Erfolgswahrscheinlichkeit

Dann empfehle den besten Ansatz mit Begründung.
```

---

## Negative Prompting

**Wann nutzen:**
- [ ] Klare Grenzen definieren
- [ ] Häufige Fehler vermeiden
- [ ] Wenn "Was nicht" einfacher ist als "Was"

**Checkliste:**
- [ ] Explizite "Vermeide"-Liste
- [ ] Konkrete Beispiele für unerwünschte Elemente
- [ ] Alternative Vorschläge erwünscht

**Template:**
```
Erstelle [Ergebnis]. Vermeide:
- [Unerwünscht 1]
- [Unerwünscht 2]
- [Unerwünscht 3]

Stattdessen:
- [Gewünscht 1]
- [Gewünscht 2]
```

---

## Kombination von Techniken

**Best Practice:**
- [ ] Nicht mehr als 2-3 Techniken pro Prompt
- [ ] Techniken sollten sich ergänzen, nicht widersprechen
- [ ] Reihenfolge beachten (System → Few-Shot → CoT)

**Beispiel-Kombination:**
```
[System-Prompt: Rolle und Stil]

[Few-Shot: Beispiele für Format]

[Chain-of-Thought: Schritt-für-Schritt-Anweisung]

[Aufgabe]
```

---

## Technik-Auswahl-Guide

| Situation | Empfohlene Technik |
|-----------|-------------------|
| Komplexes Problem | Chain-of-Thought |
| Klassifikation | Few-Shot |
| Wiederkehrende Aufgaben | System-Prompt |
| Wichtige Entscheidung | Self-Consistency |
| Strategieentwicklung | Tree of Thoughts |
| Klare Grenzen | Negative Prompting |

---

*Wähle die Technik nach der Aufgabe, nicht nach dem Gefühl.*
