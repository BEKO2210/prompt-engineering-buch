# Prompt-Template 36: Test-Case

## Zweck
Vollständige Testfälle für Qualitätssicherung.

## Prompt
```
ROLLE: Als QA-Engineer...

KONTEXT:
Feature: [Was wird getestet?]
Voraussetzungen: [Setup/Daten/State]
Test-Typ: [Unit/Integration/E2E]

AUFGABE: Schreibe einen Test-Case.

FORMAT:
- ID: Eindeutige Kennung (z.B. TC-001)
- Titel: Was wird getestet?
- Beschreibung: Kontext und Ziel
- Voraussetzungen: Was muss vorher erledigt sein?
- Test-Schritte: Nummerierte Aktionen
- Erwartetes Ergebnis: Was sollte passieren?
- Akzeptanzkriterien: Pass/Fail Kriterien
- Priorität: High/Medium/Low
```

## Variationen
- Für Regression: Abdeckung bestehender Features
- Für Edge Cases: Grenzwerte und Fehlerfälle
- Für Usability: User Flow und Interaktionen
