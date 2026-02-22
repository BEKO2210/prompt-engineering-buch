# Kapitel 6: Häufige Fehler

## Die 10 größten Fehler, die Anfänger machen

Ich habe Tausende Prompts analysiert. Diese Fehler sehe ich immer wieder. Vermeide sie, und du bist bereits besser als 90% der Nutzer.

## Fehler 1: Zu vage sein

**Falsch:**
```
Schreib was über Marketing.
```

**Warum es schlecht ist:** Die KI hat keinen Rahmen. Sie produziert generischen Text, der niemandem nutzt.

**Richtig:**
```
Schreibe einen LinkedIn-Post (150 Wörter) über 
Content-Marketing für B2B-SaaS. Zielgruppe: 
Marketingmanager. Ton: professionell, aber 
locker. Fokus: praktische Tipps, nicht Theorie.
```

## Fehler 2: Mehrere Aufgaben in einem Prompt

**Falsch:**
```
Schreib einen Blogartikel über SEO, übersetze 
ihn ins Englische, erstelle dazu Social Media 
Posts und schreib eine E-Mail an meine Liste.
```

**Warum es schlecht ist:** Die KI verliert den Fokus. Die Qualität sinkt bei jeder zusätzlichen Aufgabe.

**Richtig:**
Teile es auf:
1. Prompt: Blogartikel schreiben
2. Prompt: Blogartikel übersetzen
3. Prompt: Social Posts erstellen
4. Prompt: E-Mail schreiben

## Fehler 3: Keinen Kontext geben

**Falsch:**
```
Bewerte diese Idee: Eine App für Zeiterfassung.
```

**Warum es schlecht ist:** Die KI weiß nichts über deine Zielgruppe, deinen Markt, deine Ressourcen.

**Richtig:**
```
Bewerte diese Idee im Kontext:
- Zielgruppe: Freelancer in der Kreativbranche
- Markt: DACH-Region
- USP: KI-gestützte Projektprognosen
- Team: 2 Entwickler, 1 Designer
- Budget: 50k€ für 6 Monate

Idee: Eine App für Zeiterfassung...
```

## Fehler 4: Den Ton nicht definieren

**Falsch:**
```
Schreib eine E-Mail an den Kunden.
```

**Warum es schlecht ist:** Die KI wählt einen neutralen Ton. Der passt selten.

**Richtig:**
```
Schreibe eine E-Mail an einen Kunden, der sein 
Abo gekündigt hat. Ton: freundlich, aber nicht 
übermäßig verständnisvoll. Ziel: Herausfinden, 
warum er gekündigt hat, ohne aufdringlich zu 
sein.
```

## Fehler 5: Zu komplizierte Prompts

**Falsch:**
```
Als erfahrener Marketingexperte mit 15 Jahren 
Erfahrung im B2B-Bereich, spezialisiert auf 
SaaS-Unternehmen im DACH-Raum, der bereits 
über 100 erfolgreiche Kampagnen geleitet hat 
und für seine kreativen aber dennoch 
datengetriebenen Ansätze bekannt ist...
```

**Warum es schlecht ist:** Die KI verliert sich in den Details. Die wichtigen Informationen gehen unter.

**Richtig:**
```
Als B2B-Marketingexperte für SaaS...
```

Kurz. Prägnant. Relevant.

## Fehler 6: Keine Beispiele geben

**Falsch:**
```
Schreibe im Stil von Seth Godin.
```

**Warum es schlecht ist:** Die KI hat eine allgemeine Vorstellung von Seth Godin. Aber nicht deine spezifische Interpretation.

**Richtig:**
```
Schreibe im folgenden Stil:

Beispiel 1: [Textausschnitt]
Beispiel 2: [Textausschnitt]

Dein Text sollte:
- Kurze Sätze haben
- Direkt an den Leser sprechen
- Eine unerwartete Perspektive bieten
- Ohne Floskeln auskommen
```

## Fehler 7: Das Format vergessen

**Falsch:**
```
Liste 10 Tipps für bessere Produktivität.
```

**Warum es schlecht ist:** Die KI entscheidet selbst über Format und Länge. Das Ergebnis ist unvorhersehbar.

**Richtig:**
```
Liste 10 Tipps für bessere Produktivität.

Format:
- Nummerierte Liste (1-10)
- Jeder Titel maximal 5 Wörter
- Jede Erklärung maximal 2 Sätze
- Am Ende: Zusammenfassung in einem Satz
```

## Fehler 8: An die falsche KI stellen

**Falsch:**
```
Analyse diesen Datensatz mit 10.000 Zeilen 
und erstelle Visualisierungen.
```

An ChatGPT ohne Code-Interpreter.

**Warum es schlecht ist:** Die KI kann das nicht. Sie wird halluzinieren oder scheitern.

**Richtig:**
Nutze das richtige Tool:
- ChatGPT + Code-Interpreter für Daten
- Claude für lange Dokumente
- Midjourney für Bilder
- Spezialisierte Tools für spezielle Aufgaben

## Fehler 9: Nicht iterieren

**Falsch:**
```
Prompt → Schlechtes Ergebnis → Aufgeben
```

**Warum es schlecht ist:** Der erste Prompt ist selten perfekt. Prompt Engineering ist ein Dialog.

**Richtig:**
```
Prompt → Ergebnis → "Kürzer" → Ergebnis → 
"Füge Beispiel hinzu" → Ergebnis → "Ändere 
Ton zu professioneller" → Finales Ergebnis
```

## Fehler 10: Alles der KI überlassen

**Falsch:**
```
Erstelle meine komplette Content-Strategie 
für das nächste Jahr.
```

**Warum es schlecht ist:** Die KI kennt dein Business nicht. Sie wird generische Ratschläge geben.

**Richtig:**
```
Hier ist meine aktuelle Content-Strategie: 
[Details]

Hier sind meine Ziele: [Ziele]

Hier sind meine Ressourcen: [Ressourcen]

Analysiere Schwachstellen und schlage 3 
konkrete Verbesserungen vor.
```

## Die Fehler-Checkliste

Vor jedem Prompt, prüfe:

- [ ] Ist die Aufgabe spezifisch?
- [ ] Ist der Kontext klar?
- [ ] Ist die Rolle definiert?
- [ ] Ist der Ton festgelegt?
- [ ] Ist das Format angegeben?
- [ ] Ist es eine Aufgabe pro Prompt?
- [ ] Sind Beispiele gegeben (wenn nötig)?
- [ ] Ist die KI das richtige Tool?
- [ ] Bin ich bereit zu iterieren?
- [ ] Habe ich genug Kontext geliefert?

## Wenn etwas schiefgeht

**Die KI versteht nicht:**
→ Vereinfache den Prompt. Eine Sache nach der anderen.

**Das Ergebnis ist zu generisch:**
→ Füge mehr Kontext und spezifischere Anweisungen hinzu.

**Die KI halluziniert:**
→ Frage nach Quellen. Gib Fakten vor, die die KI nutzen soll.

**Der Ton ist falsch:**
→ Gib konkrete Beispiele für den gewünschten Ton.

**Das Format passt nicht:**
→ Zeige ein Beispiel der gewünschten Ausgabe.

## Lernen aus Fehlern

Jeder schlechte Prompt ist eine Lernchance. Analysiere, was schiefgelaufen ist. Passe deinen Prompt an. Wiederhole.

Nach 20 iterierten Prompts wirst du ein Gespür dafür entwickeln, was funktioniert.

Im nächsten Kapitel zeige ich dir 20+ konkrete Anwendungsfälle. Damit siehst du, wie gute Prompts in der Praxis aussehen.
