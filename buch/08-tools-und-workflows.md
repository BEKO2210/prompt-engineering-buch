# Kapitel 8: Tools und Workflows

## Die richtige KI für die richtige Aufgabe

Nicht alle KIs sind gleich. Jede hat Stärken und Schwächen. Hier ist meine Einschätzung nach hunderten Stunden Nutzung.

## Text-KIs im Vergleich

### ChatGPT (OpenAI)
**Stärken:**
- Vielseitig
- Code-Interpreter für Daten
- GPTs für spezialisierte Aufgaben
- DALL-E für Bilder

**Schwächen:**
- Kann zu "glatt" klingen
- Manchmal zu eifrig zu gefallen
- Wissenscutoff

**Beste für:**
- Allgemeine Aufgaben
- Brainstorming
- Code mit Erklärung
- Datenanalyse (mit Code-Interpreter)

### Claude (Anthropic)
**Stärken:**
- Lange Kontextfenster (200k Tokens)
- Natürlicher Schreibstil
- Ehrlich bei Unwissenheit
- Ausgezeichnet für lange Dokumente

**Schwächen:**
- Keine Internet-Suche
- Keine Bildgenerierung
- Weniger "Werkzeuge" als ChatGPT

**Beste für:**
- Lange Texte analysieren
- Schreiben mit natürlichem Fluss
- Komplexe Dokumente
- Wenn Ehrlichkeit wichtiger ist als Eifer

### Gemini (Google)
**Stärken:**
- Internet-Suche integriert
- Multimodal (Text, Bild, Video)
- Große Kontextfenster

**Schwächen:**
- Inkonsistente Qualität
- Manchmal halluziniert bei Fakten
- Weniger fein steuerbar

**Beste für:**
- Recherche mit aktuellen Daten
- Multimodale Aufgaben
- Wenn du Google-Ökosystem nutzt

### Perplexity
**Stärken:**
- Quellenangaben
- Fokus auf Fakten
- Gute Zusammenfassungen

**Schwächen:**
- Weniger kreativ
- Weniger für Schreibaufgaben

**Beste für:**
- Recherche
- Faktenprüfung
- Schnelle Zusammenfassungen

## Spezialisierte Tools

### Für Bilder
- **Midjourney:** Künstlerische Bilder, beste Qualität
- **DALL-E 3:** Integriert in ChatGPT, gut für präzise Anweisungen
- **Stable Diffusion:** Open Source, volle Kontrolle
- **Adobe Firefly:** Kommerziell sicher, gut für Marketing

### Für Video
- **Runway:** KI-Video-Generierung und -Editing
- **Pika:** Text-to-Video
- **HeyGen:** KI-Avatar-Videos
- **Descript:** Text-basiertes Video-Editing

### Für Audio
- **ElevenLabs:** Beste KI-Stimmen
- **Murf:** Voiceovers für Videos
- **Whisper (OpenAI):** Transkription

### Für Code
- **GitHub Copilot:** Autocomplete für Code
- **Cursor:** KI-Editor mit Kontext
- **Replit Ghostwriter:** Für Anfänger

### Für Daten
- **ChatGPT Code-Interpreter:** Analyse und Visualisierung
- **Claude:** Für große Datensätze
- **Airtable AI:** Datenbank + KI

## Workflows bauen

Ein Workflow ist eine Abfolge von Prompts, die ein komplettes Ergebnis liefern.

### Beispiel: Blogartikel-Workflow

**Schritt 1: Recherche**
```
Recherchiere aktuelle Statistiken und 
Studien zu [Thema]. Liste 5 relevante 
Fakten mit Quellen.
```

**Schritt 2: Outline**
```
Erstelle eine Gliederung für einen 
Blogartikel über [Thema].

Zielgruppe: [Zielgruppe]
Ziel: [Ziel]

Struktur:
- Einleitung mit Hook
- 3-4 Hauptabschnitte
- Praktische Tipps
- Fazit

Für jeden Abschnitt: 3 Bullet Points mit 
Inhalt.
```

**Schritt 3: Schreiben**
```
Schreibe den Blogartikel basierend auf 
dieser Gliederung:
[Gliederung einfügen]

Nutze diese Fakten:
[Recherche einfügen]

Tonalität: [Ton]
Länge: 1000 Wörter
```

**Schritt 4: Review**
```
Review diesen Blogartikel:
[Artikel einfügen]

Bewerte:
- Einleitung (fängt sie an?)
- Struktur (logisch?)
- Inhalt (wertvoll?)
- Schreibstil (lesbar?)
- Call-to-Action (klar?)

Gib 3 konkrete Verbesserungsvorschläge.
```

**Schritt 5: Finalisieren**
```
Optimiere diesen Blogartikel basierend auf 
dem Feedback:
[Artikel einfügen]

Feedback:
[Feedback einfügen]

Erstelle außerdem:
- 5 Vorschläge für Überschriften
- Meta-Beschreibung (160 Zeichen)
- 3 Social Media Posts zur Promotion
```

### Workflow-Template

```
WORKFLOW: [Name]

ZIEL: [Was soll am Ende rauskommen?]

SCHRITTE:
1. [Aufgabe] → ERGEBNIS: [Was kommt raus?]
2. [Aufgabe] → ERGEBNIS: [Was kommt raus?]
3. [Aufgabe] → ERGEBNIS: [Was kommt raus?]

TOOLS:
- Schritt 1: [Welche KI?]
- Schritt 2: [Welche KI?]
- Schritt 3: [Welche KI?]

ZEIT: [Geschätzte Dauer]
```

## Automatisierung

### Zapier/Make + KI
Verbinde KI mit anderen Tools:
- Neue E-Mail → KI fasst zusammen → Slack-Benachrichtigung
- Formular-Eintrag → KI qualifiziert Lead → CRM-Update
- RSS-Feed → KI schreibt Social Post → Automatischer Post

### API-Nutzung
Für wiederholte Aufgaben lohnt sich die API:
- Gleiche Prompts mit variablen Inputs
- Batch-Verarbeitung
- Integration in eigene Tools

### Custom GPTs / Claude Projects
Erstelle spezialisierte Assistenten:
- "SEO-Content-Writer"
- "Code-Reviewer"
- "E-Mail-Optimierer"

Mit festen System-Prompts für konsistente Ergebnisse.

## Best Practices für Workflows

### 1. Modular bauen
Jeder Schritt sollte eigenständig funktionieren. Wenn Schritt 3 scheitert, musst du nicht bei 1 neu anfangen.

### 2. Review-Punkte einbauen
Nach jedem wichtigen Schritt: Pause. Review. Dann weiter.

### 3. Fallbacks haben
Wenn die KI nicht liefert, was du willst: Was ist Plan B?

### 4. Dokumentieren
Schreib auf, was funktioniert. Nach 3 Monaten weißt du nicht mehr, warum du das so gemacht hast.

### 5. Iterieren
Kein Workflow ist perfekt vom ersten Mal. Optimiere basierend auf Ergebnissen.

## Mein persönlicher Workflow-Stack

**Täglich:**
- Claude für lange Texte und Analysen
- ChatGPT für schnelle Fragen und Code
- Perplexity für Recherche

**Wöchentlich:**
- Midjourney für Bilder
- ElevenLabs für Voiceovers
- Whisper für Transkriptionen

**Projekte:**
- Custom GPTs für wiederkehrende Aufgaben
- Zapier für Automatisierung
- Cursor für Coding

## Zusammenfassung

| Aufgabe | Bestes Tool | Alternative |
|---------|-------------|-------------|
| Lange Texte | Claude | ChatGPT |
| Recherche | Perplexity | Gemini |
| Code + Erklärung | ChatGPT | Claude |
| Bilder | Midjourney | DALL-E 3 |
| Video | Runway | HeyGen |
| Transkription | Whisper | Otter |
| Automatisierung | Zapier | Make |

Wähle das richtige Tool. Baue Workflows. Skaliere deine Produktivität.

Im nächsten Kapitel zeige ich dir den Lernpfad: Wie du in 30 Tagen vom Anfänger zum Prompt Engineering-Profi wirst.
