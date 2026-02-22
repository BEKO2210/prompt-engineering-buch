# Kapitel 3: Die Anatomie eines guten Prompts

## Die vier Säulen

Jeder gute Prompt hat vier Elemente. Fehlt eins, wird das Ergebnis schlechter. Ich nenne sie die vier Säulen:

1. **Rolle** – Wer antwortet?
2. **Kontext** – Was ist die Situation?
3. **Aufgabe** – Was soll passieren?
4. **Format** – Wie soll es aussehen?

Das ist der Grundstein des ROKA-Rahmens, den ich im nächsten Kapitel im Detail erkläre.

## Säule 1: Rolle

Die KI kann jede Rolle annehmen. Nutze das.

**Ohne Rolle:**
```
Erkläre Quantencomputing.
```

**Mit Rolle:**
```
Als Quantenphysiker mit 20 Jahren Erfahrung 
erkläre Quantencomputing einem Gymnasiasten.
```

Der Unterschied ist enorm. Ohne Rolle bekommst du eine Wikipedia-Zusammenfassung. Mit Rolle bekommst du eine Erklärung, die verständlich ist – weil die KI "weiß", dass sie Experte ist und ein Laienpublikum hat.

### Gute Rollen
- Spezifischer Experte (nicht "Experte", sondern "SEO-Experte mit E-Commerce-Fokus")
- Beruf mit Erfahrung ("erfahrener Verkaufstrainer")
- Persönlichkeit ("kritischer Journalist", "enthusiastischer Coach")

### Schlechte Rollen
- Zu allgemein ("Experte", "Profis")
- Widersprüchlich ("strenger aber lockerer Lehrer")
- Zu viele Rollen gleichzeitig

## Säule 2: Kontext

Kontext ist alles. Die KI kennt deine Situation nicht – du musst sie ihr sagen.

**Schlecht:**
```
Schreib eine E-Mail an den Kunden.
```

**Besser:**
```
Schreib eine E-Mail an einen Kunden, der gestern 
beschwert hat, dass seine Lieferung zu spät kam. 
Wir haben das Problem gelöst, die Lieferung ist 
heute angekommen. Ziel: Entschuldigung und 
Bindung stärken.
```

Was gehört in den Kontext?
- Wer ist der Empfänger?
- Was ist passiert vorher?
- Was ist das Ziel?
- Gibt es Einschränkungen?
- Welcher Ton ist angemessen?

## Säule 3: Aufgabe

Die Aufgabe muss spezifisch sein. "Schreib etwas" ist keine Aufgabe.

**Schlecht:**
```
Mach mir was zu Marketing.
```

**Gut:**
```
Erstelle eine 5-Schritte-Strategie für 
LinkedIn-Marketing eines B2B-SaaS-Unternehmens. 
Jeder Schritt soll konkrete Aktionen enthalten, 
die in einer Woche umsetzbar sind.
```

Eine gute Aufgabe hat:
- Ein Verb (schreibe, analysiere, erstelle)
- Ein Objekt (was genau?)
- Parameter (wie viel, wie lange, wie detailliert)

## Säule 4: Format

Definiere das Ausgabeformat. Sonst entscheidet die KI – und das ist selten optimal.

**Format-Optionen:**
- Länge (Wörter, Sätze, Absätze)
- Struktur (Aufzählung, Tabelle, Fließtext)
- Ton (formell, locker, professionell, freundlich)
- Stil (journalistisch, akademisch, marketingorientiert)

**Beispiel:**
```
Format:
- 3 Absätze
- Jeder Absatz max. 3 Sätze
- Ton: professionell aber nicht steif
- Keine Fachbegriffe ohne Erklärung
```

## Die Säulen in Aktion

Hier ist ein kompletter Prompt mit allen vier Säulen:

```
Rolle: Du bist ein erfahrener UX-Designer mit 
Spezialisierung auf E-Commerce.

Kontext: Wir starten einen Online-Shop für 
nachhaltige Mode. Unsere Zielgruppe sind 
Frauen 25-40, umweltbewusst, mittleres 
Einkommen. Die Konkurrenz ist stark.

Aufgabe: Entwickle 5 UX-Prinzipien, die uns 
von der Konkurrenz abheben. Jedes Prinzip 
soll ein konkretes Beispiel enthalten.

Format:
- Liste mit 5 Punkten
- Jeder Punkt: Prinzip + Erklärung + Beispiel
- Maximal 100 Wörter pro Punkt
- Ton: inspirierend, aber pragmatisch
```

Das Ergebnis wird strukturiert, relevant und nutzbar sein.

## Häufige Fehler bei den Säulen

### Rolle
- Zu vage: "Experte" statt "SEO-Experte für lokale Unternehmen"
- Keine Rolle: Die KI antwortet generisch

### Kontext
- Zu wenig: Die KI muss raten
- Zu viel: Die KI verliert den Fokus

### Aufgabe
- Unklar: "Mach was dazu"
- Zu komplex: Mehrere Aufgaben in einem Prompt

### Format
- Fehlend: Die KI entscheidet selbst
- Unrealistisch: "In 10 Wörtern erkläre Quantenphysik"

## Zusammenfassung

Die vier Säulen sind dein Grundgerüst. Jeder Prompt sollte sie enthalten. Im nächsten Kapitel baue ich darauf auf und zeige dir den ROKA-Rahmen – meine systematische Methode für Prompts, die immer funktionieren.
