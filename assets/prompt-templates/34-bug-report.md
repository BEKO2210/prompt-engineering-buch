# Prompt-Template 34: Bug-Report

## Zweck
Reproduzierbare Fehlerbeschreibungen für schnelle Fixes.

## Prompt
```
ROLLE: Als QA-Engineer...

KONTEXT:
Feature/Bereich: [Wo tritt der Bug auf?]
Ernstgrad: [Critical/Major/Minor]
Umgebung: [Browser/Gerät/Version]

AUFGABE: Schreibe einen detaillierten Bug-Report.

FORMAT:
- Titel: Kurz und prägnant (Was + Wo)
- Beschreibung: 1-2 Sätze zum Problem
- Schritte zur Reproduktion: Nummerierte Liste
- Erwartetes Ergebnis: Was sollte passieren?
- Tatsächliches Ergebnis: Was passiert stattdessen?
- Screenshots/Logs: Referenzen zu Anhängen
- Impact: Wie viele Nutzer betroffen?
- Workaround: Gibt es einen temporären Fix?
```

## Variationen
- Für Crash: Stacktrace und Logs priorisieren
- Für UI: Screenshots und Design-Vergleich
- Für Performance: Metriken und Benchmarks
