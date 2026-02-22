# Kapitel 4: Der ROKA-Rahmen

## Meine Methode für Prompts, die funktionieren

Ich habe den ROKA-Rahmen entwickelt, nachdem ich hunderte Prompts geschrieben habe, die nicht das geliefert haben, was ich wollte. ROKA steht für:

- **R**olle
- **O**rganisation (Kontext)
- **K**onkrete Aufgabe
- **A**usgabeformat

Es ist eine Erweiterung der vier Säulen, aber systematischer und praktikabler.

## Warum ROKA?

Die meisten Prompt-Frameworks sind zu akademisch. Sie funktionieren in der Theorie, aber nicht, wenn du unter Druck ein Ergebnis brauchst.

ROKA ist für den echten Einsatz gemacht. Es ist schnell, wiederholbar und skalierbar.

## Schritt 1: Rolle definieren

Die Rolle bestimmt den Blickwinkel. Ein Arzt erklärt anders als ein Patient. Ein Anfänger fragt anders als ein Experte.

### Die Rolle-Formel
```
Als [spezifische Rolle] mit [Erfahrung/Kontext] 
für [Zielgruppe/Audienz]...
```

**Beispiele:**

```
Als Marketingmanager mit 10 Jahren Erfahrung 
im B2B-Bereich für ein Team von Einsteigern...
```

```
Als erfahrener Programmierer, der komplexe 
Konzepte einfach erklären kann, für einen 
Junior-Developer...
```

```
Als knallharter Business-Coach ohne Zeit für 
Ausreden für einen Gründer, der sein Business 
nicht vom Fleck kriegt...
```

### Rollen-Tipps
- Spezifisch sein: "Marketingexperte" ist zu vage
- Erfahrung hinzufügen: "mit 5 Jahren Erfahrung"
- Zielgruppe nennen: "für Anfänger", "für Fachleute"

## Schritt 2: Organisation (Kontext)

Der Kontext gibt der KI den Rahmen. Ohne Kontext arbeitet sie im luftleeren Raum.

### Der Kontext-Check
Beantworte diese Fragen:
1. Wer ist der Empfänger?
2. Was ist das Ziel?
3. Was ist der Hintergrund?
4. Gibt es Einschränkungen?
5. Was wurde bereits getan?

**Beispiel:**
```
Kontext:
- Wir sind ein SaaS-Startup mit 20 Mitarbeitern
- Unser Produkt hilft bei der Zeiterfassung
- Wir wollen in den Enterprise-Market
- Unsere aktuelle Website spricht kleine Teams an
- Wir brauchen neue Copy für die Enterprise-Seite
```

### Kontext-Fallen
- **Zu viel**: 500 Wörter Hintergrundstory
- **Zu wenig**: "Wir sind ein Unternehmen"
- **Irrelevant**: Details, die nicht zur Aufgabe passen

## Schritt 3: Konkrete Aufgabe

Die Aufgabe ist das Herzstück. Sie muss präzise sein.

### Die Aufgaben-Formel
```
[Verb] + [Objekt] + [Parameter] + [Ziel]
```

**Beispiele:**

```
Erstelle (Verb) eine Content-Strategie (Objekt) 
für 3 Monate (Parameter), die zu 20% mehr 
Leads führt (Ziel).
```

```
Analysiere (Verb) diese E-Mail (Objekt) auf 
Verkaufspotenzial (Parameter) und identifiziere 
3 Verbesserungspunkte (Ziel).
```

```
Schreibe (Verb) 5 Überschriften (Objekt) für 
eine Landing Page (Parameter), die Neugier 
wecken und zum Klicken animieren (Ziel).
```

### Gute Verben für Aufgaben
- Erstelle
- Analysiere
- Optimiere
- Strukturiere
- Übersetze
- Fasse zusammen
- Vergleiche
- Empfehle

## Schritt 4: Ausgabeformat

Das Format bestimmt, wie du das Ergebnis bekommst. Definiere es immer.

### Format-Elemente
1. **Struktur**: Liste, Tabelle, Fließtext, JSON
2. **Länge**: Wörter, Sätze, Zeichen
3. **Ton**: Formell, locker, professionell, freundlich
4. **Stil**: Kurz, ausführlich, bullet-points, nummeriert

**Beispiel:**
```
Ausgabeformat:
- Tabelle mit 3 Spalten: Problem, Lösung, Zeitaufwand
- Maximal 10 Zeilen
- Ton: pragmatisch, ohne Füllwörter
- Fachbegriffe in Klammern erklären
```

## ROKA in Aktion: Ein kompletter Prompt

```
ROLLE:
Als erfahrener SEO-Experte mit Fokus auf 
E-Commerce für einen Online-Shop-Betreiber, 
der gerade erst anfängt.

ORGANISATION (Kontext):
- Wir verkaufen nachhaltige Haushaltsprodukte
- Der Shop läuft seit 6 Monaten
- Aktueller Traffic: 500 Besucher/Monat
- Ziel: 5000 Besucher/Monat in 12 Monaten
- Budget für SEO-Tools: 100€/Monat
- Kein Team, alles selbst gemacht

KONKRETE AUFGABE:
Erstelle einen 90-Tage-SEO-Plan mit konkreten 
Aktionen, die ohne teure Tools umsetzbar sind. 
Jede Aktion soll einen geschätzten Impact haben 
(low/medium/high).

AUSGABEFORMAT:
- Wochenweise Aufschlüsselung (Woche 1-12)
- Pro Woche: 3 konkrete Aktionen
- Jede Aktion: Was? Wie? Zeitaufwand? Impact?
- Zusammenfassung am Ende: Top 3 Prioritäten
- Ton: motivierend, aber realistisch
```

## ROKA-Template für deine Prompts

```
ROLLE:
Als [Rolle] mit [Erfahrung] für [Zielgruppe]...

ORGANISATION:
- [Kontextpunkt 1]
- [Kontextpunkt 2]
- [Kontextpunkt 3]

KONKRETE AUFGABE:
[Verb] [Objekt] [Parameter] [Ziel]

AUSGABEFORMAT:
- [Struktur]
- [Länge]
- [Ton]
- [Stil]
```

## Übung: ROKA anwenden

Nimm eine Aufgabe, die du heute hast. Schreib sie als ROKA-Prompt. Vergleiche das Ergebnis mit deinem üblichen Prompt-Stil.

Die Verbesserung wird dich überraschen.
