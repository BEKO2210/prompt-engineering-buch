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

## Messbarkeit: KPIs für Prompt Success

Wie weißt du, ob deine Prompts gut sind? Intuition reicht nicht – du brauchst Metriken.

### Die Prompt-Performance-Matrix

| Metrik | Was misst sie? | Wie messen? |
|--------|----------------|-------------|
| **Response Quality** | Erfüllt der Output die Anforderungen? | 1-5 Rating nach definierten Kriterien |
| **Consistency** | Ist die Qualität reproduzierbar? | Gleichen Prompt 5x ausführen, Varianz messen |
| **Efficiency** | Wie viele Iterationen braucht es? | Durchschnittliche Versuche bis zum akzeptablen Ergebnis |
| **Time-to-Result** | Wie schnell kommt das Ergebnis? | Zeit von Prompt bis fertigem Output |
| **Token Efficiency** | Wie viele Tokens werden verbraucht? | Input + Output Tokens tracken |
| **User Satisfaction** | Wie zufrieden ist der Nutzer? | Post-hoc Bewertung 1-5 |

### Das Prompt-Scorecard-Template

```
PROMPT SCORECARD
================
Prompt-Name: [Name]
Datum: [Datum]
Tester: [Name]

QUALITÄT (1-5)
□ Output entspricht der Anfrage     [ ]
□ Format wurde korrekt angewendet   [ ]
□ Keine Halluzinationen/Fehler      [ ]
□ Angemessene Länge/Tiefe           [ ]
□ Nützlich für den Use Case         [ ]
Gesamt: ___/25 Punkte

KONSISTENZ (1-5)
□ Gleiches Ergebnis bei Wiederholung
□ Keine unerwarteten Variationen
Gesamt: ___/10 Punkte

EFFIZIENZ
□ Erster Versuch erfolgreich: +5 Punkte
□ Zweiter Versuch: +3 Punkte
□ Dritter+ Versuch: +1 Punkt
Gesamt: ___/5 Punkte

GESAMTSCORE: ___/40 Punkte
Bewertung:
35-40: Hervorragend (Production-Ready)
25-34: Gut (Mit kleinen Anpassungen)
15-24: Akzeptabel (Überarbeitung nötig)
0-14: Unzureichend (Grundlegend überdenken)
```

### A/B-Testing für Prompts

**Setup:**
```
Variante A (Kontrolle):
"Schreibe eine Produktbeschreibung für [Produkt]."

Variante B (Test):
"ROLLE: Als erfahrener E-Commerce-Copywriter...
KONTEXT: Wir verkaufen [Produkt] an [Zielgruppe]...
AUFGABE: Schreibe eine überzeugende Produktbeschreibung...
FORMAT: 150 Wörter, emotional, benefit-fokussiert"
```

**Messung:**
- 10 Outputs pro Variante generieren
- Blind von 3 Reviewern bewerten lassen
- Durchschnittliche Scores vergleichen
- Signifikanten Unterschied ermitteln (p < 0.05)

### Prompt-Optimierungs-Framework

```
SCHRITT 1: Baseline messen
→ Prompt 10x ausführen
→ Durchschnittlichen Score ermitteln

SCHRITT 2: Eine Variable ändern
→ Z.B. mehr Kontext hinzufügen
→ Oder: Output-Format spezifizieren
→ Oder: Few-Shot Beispiele einfügen

SCHRITT 3: Neue Version testen
→ Wieder 10x ausführen
→ Neuen Durchschnitt berechnen

SCHRITT 4: Vergleichen
→ Ist die neue Version besser?
→ Ist der Unterschied signifikant?
→ Wenn ja: Neue Baseline
→ Wenn nein: Zurück zu Schritt 2

SCHRITT 5: Dokumentieren
→ Was hat funktioniert?
→ Warum hat es funktioniert?
→ Für zukünftige Prompts merken
```

### Beispiel: Messbare Verbesserung

**Ausgangslage:**
```
Prompt: "Schreibe eine E-Mail an einen Kunden."
Baseline-Score: 14/40 (Unzureichend)
Probleme: Zu generisch, kein Kontext, unklares Ziel
```

**Iteration 1: Kontext hinzufügen**
```
Prompt: "Schreibe eine E-Mail an einen Kunden, der 
unser Produkt gekauft hat. Danke ihm und frage nach Feedback."
Score: 22/40 (Akzeptabel)
Verbesserung: +57%
```

**Iteration 2: ROKA-Rahmen anwenden**
```
Prompt: "ROLLE: Als Customer Success Manager...
KONTEXT: Kunde hat vor 2 Wochen gekauft...
AUFGABE: Danke per E-Mail und bitte um Review...
FORMAT: Kurz, persönlich, mit Call-to-Action"
Score: 34/40 (Gut)
Verbesserung: +143% zur Baseline
```

**Iteration 3: Few-Shot hinzufügen**
```
Prompt: [ROKA-Struktur] + 2 Beispiele guter E-Mails
Score: 38/40 (Hervorragend)
Verbesserung: +171% zur Baseline
```

### Tools für Prompt-Tracking

**Einfach (Spreadsheet):**
```
| Prompt | Version | Datum | Score | Notes |
|--------|---------|-------|-------|-------|
| Email_01 | 1.0 | 2024-01 | 14 | Baseline |
| Email_01 | 1.1 | 2024-01 | 22 | +Kontext |
| Email_01 | 1.2 | 2024-01 | 34 | +ROKA |
| Email_01 | 1.3 | 2024-02 | 38 | +Few-Shot |
```

**Erweitert (PromptLayer/Langfuse):**
- Automatisches Logging
- Version Control
- Performance-Analytics
- Team-Kollaboration

### Zusammenfassung Messbarkeit

| Was | Warum | Wie oft |
|-----|-------|---------|
| Prompt scoren | Qualität sicherstellen | Bei jeder neuen Version |
| A/B-Tests | Beste Variante finden | Bei wichtigen Prompts |
| Iterationen tracken | Fortschritt messen | Kontinuierlich |
| Token-Usage monitoren | Kosten kontrollieren | Bei API-Nutzung |

## Weitere fortgeschrittene Techniken

### Meta-Prompting: Prompts schreiben Prompts

Manchmal ist es effizienter, die KI den Prompt schreiben zu lassen:

```
Du bist ein Prompt Engineering Experte.

Erstelle einen optimierten Prompt für folgende Aufgabe:
[Aufgabenbeschreibung]

Der Prompt soll:
- Den ROKA-Rahmen nutzen
- Chain-of-Thought für komplexe Teile enthalten
- Klare Output-Formate definieren
- 2-3 Few-Shot Beispiele enthalten

Gib mir:
1. Den fertigen Prompt
2. Eine Erklärung, warum du diese Struktur gewählt hast
3. Tipps für die Nutzung
```

### Prompt Chaining: Verkettete Prompts

Für komplexe Aufgaben: Output von Prompt 1 wird Input für Prompt 2.

**Beispiel: Whitepaper erstellen**

```
PROMPT 1: Recherche
"Recherchiere [Thema]. Liste 10 wichtige Fakten 
mit Quellen."
→ Output: Faktenliste

PROMPT 2: Outline
"Erstelle eine Gliederung für ein Whitepaper über 
[Thema] basierend auf diesen Fakten: [Faktenliste]"
→ Output: Struktur

PROMPT 3: Schreiben
"Schreibe das Whitepaper basierend auf dieser 
Gliederung: [Struktur]. Nutze diese Fakten: [Fakten]"
→ Output: Erster Entwurf

PROMPT 4: Review
"Review dieses Whitepaper: [Entwurf]. Identifiziere 
3 Schwächen und schlage Verbesserungen vor."
→ Output: Feedback

PROMPT 5: Finalisieren
"Optimiere das Whitepaper: [Entwurf]. Berücksichtige 
dieses Feedback: [Feedback]"
→ Output: Finale Version
```

### Kontextfenster-Optimierung

Für sehr lange Inputs: Strategisch vorgehen.

**Problem:** Dein Dokument hat 50.000 Wörter, aber das Kontextfenster nur 100.000 Tokens.

**Lösung: Chunking + Summarization**

```
SCHRITT 1: Dokument in Chunks aufteilen
→ Chunks von ~3000 Wörtern

SCHRITT 2: Jeden Chunk zusammenfassen
"Fasse diesen Abschnitt in 3 Sätzen zusammen: [Chunk]"

SCHRITT 3: Zusammenfassungen kombinieren
→ Neue, kürzere Version des Dokuments

SCHRITT 4: Finale Analyse
"Analysiere dieses Dokument: [Kombinierte Zusammenfassungen]. 
Fokus auf: [Deine Frage]"
```

### Conditional Prompting: Wenn-Dann-Logik

```
Analysiere diesen Text: [Text]

Wenn der Text positiv ist:
→ Danke dem Absender und bitte um einen Testimonial

Wenn der Text neutral ist:
→ Bitte um konkretes Feedback zur Verbesserung

Wenn der Text negativ ist:
→ Entschuldige dich, biete eine Lösung an, eskaliere an Manager

Format: Entscheidung + Begründung + Empfohlene Antwort
```

### Prompt-Templates mit Bedingungen

```
ROLLE: Als [Rolle: Marketingmanager/Vertriebler/Support-Agent]

KONTEXT:
- Branche: [Branche]
- Unternehmensgröße: [Größe]
- Zielgruppe: [Zielgruppe]

AUFGABE:
{% if ziel == "lead_generierung" %}
  Erstelle einen Lead-Magnet...
{% elif ziel == "conversion" %}
  Schreibe überzeugende Sales-Copy...
{% else %}
  Erstelle einen informativen Blogartikel...
{% endif %}

FORMAT:
- Länge: [Länge] Wörter
- Ton: [Ton]
{% if branche == "b2b" %}
- Fokus: ROI und Effizienz
{% else %}
- Fokus: Emotion und Lifestyle
{% endif %}
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
| Meta-Prompting | Prompt-Optimierung | Bessere Prompts |
| Prompt Chaining | Komplexe Workflows | Strukturierte Ergebnisse |
| Conditional Prompting | Flexible Templates | Vielseitigkeit |

Im nächsten Kapitel schauen wir uns an, was Anfänger falsch machen – damit du es vermeidest.
