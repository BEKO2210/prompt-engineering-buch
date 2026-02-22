# Kapitel 5: Fortgeschrittene Techniken

## Chain-of-Thought: Denk mit der KI

Die meisten Menschen erwarten von der KI, dass sie sofort die richtige Antwort gibt. Das funktioniert bei einfachen Aufgaben. Bei komplexen nicht.

Chain-of-Thought (CoT) bedeutet: Du lässt die KI Schritt für Schritt denken.

**Ohne CoT:**
```
Löse diese Matheaufgabe: Ein Zug fährt mit 
80 km/h. Ein anderer mit 100 km/h. Wann 
treffen sie sich?
```

**Mit CoT:**
```
Löse diese Matheaufgabe Schritt für Schritt:
1. Identifiziere die gegebenen Informationen
2. Formuliere die Gleichung
3. Löse die Gleichung
4. Überprüfe das Ergebnis

Aufgabe: Ein Zug fährt mit 80 km/h. Ein 
anderer mit 100 km/h. Wann treffen sie sich?
```

Der Unterschied? Die KI zeigt ihren Denkprozess. Das Ergebnis ist präziser und nachvollziehbarer.

### Wann CoT nutzen
- Komplexe Probleme
- Mathematische Aufgaben
- Logische Schlussfolgerungen
- Analysen mit mehreren Faktoren

### Wann CoT nicht nutzen
- Einfache Faktenabfragen
- Kreative Texte (kann den Fluss stören)
- Wenn Geschwindigkeit wichtiger ist als Präzision

## Few-Shot Prompting: Beispiele geben

Die KI lernt aus Beispielen. Gibst du gute Beispiele, bekommst du gute Ergebnisse.

**Zero-Shot (kein Beispiel):**
```
Klassifiziere diese Reviews als positiv oder negativ:
"Das Produkt ist okay, nicht besonders."
```

**Few-Shot (mit Beispielen):**
```
Klassifiziere Reviews als positiv oder negativ:

Beispiel 1:
Review: "Absolut fantastisch! Beste Kauf 
entscheidung ever."
Klassifikation: positiv

Beispiel 2:
Review: "Total enttäuscht. Ging nach 2 Tagen 
kaputt."
Klassifikation: negativ

Beispiel 3:
Review: "Das Produkt ist okay, nicht besonders."
Klassifikation:
```

Der Unterschied? Die KI versteht, was du meinst. "Okay, nicht besonders" ist neutral bis leicht negativ – das erkennt sie durch die Beispiele.

### Few-Shot Best Practices
- 2-5 Beispiele sind optimal
- Beispiele sollten deckungsgleich mit der gewünschten Ausgabe sein
- Edge-Cases zeigen, wenn nötig
- Konsistentes Format in allen Beispielen

## System-Prompts: Die unsichtbare Anweisung

System-Prompts sind Anweisungen, die der KI vor dem eigentlichen Prompt gegeben werden. Sie definieren das Verhalten für die gesamte Konversation.

**Beispiel System-Prompt:**
```
Du bist ein hilfreicher Assistent, der:
- Immer präzise und kurz antwortet
- Keine Floskeln verwendet
- Bei Unsicherheit "Ich weiß es nicht" sagt
- Fachbegriffe erklärt, wenn sie das erste Mal vorkommen
```

### Wo System-Prompts funktionieren
- ChatGPT Custom Instructions
- Claude Projekte
- API-Integrationen
- Team-Workflows

### System-Prompt-Template
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

## Self-Consistency: Mehrfach prüfen

Bei wichtigen Entscheidungen lässt du die KI mehrmals antworten und wählst das beste Ergebnis.

**Prompt:**
```
Generiere 3 verschiedene Überschriften für 
diesen Artikel. Jede soll einen anderen 
Ansatz haben:
1. Neugier wecken
2. Nutzen versprechen
3. Schmerzpunkt adressieren

Artikel: [Dein Artikel]
```

Dann wählst du die beste oder kombinierst Elemente.

## Tree of Thoughts: Verzweigende Pfade

Bei komplexen Problemen lässt du die KI verschiedene Lösungswege erkunden.

**Prompt:**
```
Wir haben ein Problem: [Beschreibung]

Entwickle 3 verschiedene Lösungsansätze. 
Für jeden Ansatz:
1. Beschreibe die Idee
2. Liste Vor- und Nachteile
3. Schätze den Aufwand (low/medium/high)
4. Bewerte die Erfolgswahrscheinlichkeit

Dann empfehle den besten Ansatz mit Begründung.
```

## ReAct: Reasoning + Acting

ReAct kombiniert Denken und Handeln. Die KI denkt nach, handelt, beobachtet das Ergebnis, denkt weiter.

**Struktur:**
```
Gedanke: [Die KI analysiert die Situation]
Aktion: [Die KI führt eine Aktion aus]
Beobachtung: [Das Ergebnis der Aktion]
Gedanke: [Die KI analysiert das neue Ergebnis]
...
```

**Beispiel:**
```
Löse diese Aufgabe mit ReAct:

Frage: Wie viele Tage hat der Monat, in dem 
Weihnachten ist?

Gedanke: Ich muss wissen, in welchem Monat 
Weihnachten ist.
Aktion: Suche nach "Weihnachten Datum".
Beobachtung: Weihnachten ist am 25. Dezember.
Gedanke: Jetzt muss ich wissen, wie viele Tage 
der Dezember hat.
Aktion: Wissen abrufen: Dezember hat 31 Tage.
Beobachtung: Dezember hat 31 Tage.
Gedanke: Ich habe die Antwort.
Antwort: Der Monat mit Weihnachten (Dezember) 
hat 31 Tage.
```

## Negative Prompting: Was nicht gewollt ist

Manchmal ist es einfacher zu sagen, was du nicht willst.

**Beispiel:**
```
Schreibe einen Produktbeschreibung. Vermeide:
- Superlative ("das beste", "unglaublich")
- Füllwörter ("wirklich", "einfach", "natürlich")
- Passive Formulierungen
- Technische Jargon ohne Erklärung
```

## Temperature und Top-P (für API-Nutzer)

Wenn du über API arbeitest, kannst du Kreativität steuern:

- **Temperature**: 0 = deterministisch, 1 = kreativ
- **Top-P**: Wahrscheinlichkeitsverteilung der Wortwahl

**Für präzise Aufgaben:** Temperature 0.1-0.3
**Für kreative Aufgaben:** Temperature 0.7-0.9

## Techniken kombinieren

Die besten Prompts nutzen mehrere Techniken:

```
System: Du bist ein erfahrener Copywriter, 
der knapp und präzise formuliert.

Prompt:
ROLLE: Als Conversion-Optimierer für 
E-Commerce...
KONTEXT: Wir verkaufen [Produkt] an [Zielgruppe]...
AUFGABE: Erstelle 5 Überschriften...

Techniken:
- Few-Shot: Hier sind 3 Beispiele guter Überschriften...
- Chain-of-Thought: Entwickle jede Überschrift Schritt 
  für Schritt...
- Self-Consistency: Generiere 2 Varianten pro Ansatz...

FORMAT: Tabelle mit Überschrift, Ansatz, erwarteter CTR
```

## Zusammenfassung

| Technik | Wann nutzen | Effekt |
|---------|-------------|--------|
| Chain-of-Thought | Komplexe Probleme | Bessere Logik |
| Few-Shot | Klassifikation, Format | Konsistenz |
| System-Prompts | Wiederholte Nutzung | Konsistentes Verhalten |
| Self-Consistency | Wichtige Entscheidungen | Höhere Qualität |
| Tree of Thoughts | Strategieentwicklung | Mehr Optionen |
| ReAct | Multi-Step-Probleme | Nachvollziehbarkeit |
| Negative Prompting | Klare Grenzen | Vermeidung von Fehlern |

Im nächsten Kapitel schauen wir uns an, was Anfänger falsch machen – damit du es vermeidest.
