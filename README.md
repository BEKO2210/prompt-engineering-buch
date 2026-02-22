# Der Prompt Ingenieur
**Von Anfänger zum KI-Experten**

Von Belkis Aslani

---

## Über dieses Buch

Dieses Buch ist das Ergebnis von drei Jahren praktischer Arbeit mit über 2.000 Prompts in eigenen Projekten – von Content-Erstellung über Code-Debugging bis hin zu komplexen Business-Analysen. Keine theoretischen Abhandlungen, keine Füllseiten – nur das, was wirklich funktioniert.

Der ROKA-Rahmen (Rolle, Organisation, Konkrete Aufgabe, Ausgabeformat) ist meine eigene Methode, entwickelt aus der Praxis für die Praxis.

## Was du bekommst

- **12 Kapitel** – Vom absoluten Anfänger zum Prompt Engineering-Profi
- **50+ Prompt-Templates** – Kopieren, anpassen, loslegen
- **30-Tage-Lernplan** – Mit konkreten Übungen und Checkpoints
- **Ethik & Verantwortung** – Weil mächtige Tools Verantwortung erfordern

## Inhalt

### Teil 1: Grundlagen (Kapitel 1-4)
- Warum Prompt Engineering dein wichtigstes Skill wird
- Was Prompts wirklich sind
- Die 4 Säulen jedes guten Prompts
- Der ROKA-Rahmen

### Teil 2: Fortgeschrittene Techniken (Kapitel 5)
- Chain-of-Thought
- Few-Shot Prompting
- System-Prompts
- ReAct, Tree of Thoughts, Meta-Prompting
- Messbarkeit: KPIs für Prompt Success

### Teil 3: Praxis (Kapitel 6-10)
- Häufige Fehler (und wie du sie vermeidest)
- 20+ konkrete Anwendungsfälle
- Tools und Workflows
- 50+ Prompt-Templates für sofortigen Einsatz
- Der 30-Tage-Lernpfad

### Teil 4: Verantwortung & Skalierung (Kapitel 11-12)
- KI-Ethik, Bias, Transparenz, EU AI Act
- Team-Workflows und Enterprise-Einsatz

## Für wen dieses Buch ist

- **Content Creator**, die bessere Texte in weniger Zeit produzieren wollen
- **Gründer**, die KI für Marketing, Vertrieb und Produkt nutzen wollen
- **Marketing-Teams**, die ihre Produktivität verdreifachen wollen
- **Entwickler**, die KI für Code und Dokumentation einsetzen
- **Jeder**, der KI wirklich beherrschen will statt nur zu benutzen

## Verkaufsversionen

| Version | Preis | Enthält |
|---------|-------|---------|
| **Basic** | 29€ | E-Book (PDF/EPUB) |
| **Premium** ⭐Bestseller | 49€ | E-Book + Workbook + 50 Templates + Community |
| **Expert** | 149€ | Komplettpaket + Team-Materialien + Whitelabel-Lizenz + 1:1 Call |

## Format-Konvertierung

Das Buch ist in Markdown geschrieben. So erstellst du andere Formate:

### PDF (empfohlen für Druck)
```bash
# Mit pandoc + LaTeX
pandoc buch/*.md -o prompt-ingenieur.pdf \
  --pdf-engine=xelatex \
  -V geometry:margin=2.5cm \
  -V fontsize=11pt \
  --toc --toc-depth=2

# Alternative Tools:
# - md-to-pdf (Node.js): npx md-to-pdf buch/*.md
# - Typora: Export → PDF
# - VS Code: Markdown PDF Extension
```

### EPUB (für E-Reader)
```bash
# Mit pandoc
pandoc buch/*.md -o prompt-ingenieur.epub \
  --toc --toc-depth=2 \
  -V title="Der Prompt Ingenieur" \
  -V author="Belkis Aslani"

# Mit Calibre
# ebook-convert buch/*.md prompt-ingenieur.epub
```

### Word (DOCX)
```bash
# Mit pandoc
pandoc buch/*.md -o prompt-ingenieur.docx --toc

# Alternative: Typora → Export → Word
```

### HTML (für Web)
```bash
# Mit pandoc
pandoc buch/*.md -o prompt-ingenieur.html \
  --standalone --toc --css=style.css

# Alternative: grip (GitHub-Style Preview)
```

## Repository-Struktur

```
prompt-engineering-buch/
├── buch/                    # 12 Kapitel (Markdown)
├── versionen/               # Format-Spezifikationen
│   ├── ebook-epub/
│   ├── ebook-pdf/
│   ├── premium-workbook/
│   └── video-skript/
├── marketing/               # Sales Page, Emails, Social Posts
├── assets/                  # Templates, Checklisten, Übersichten
└── README.md               # Diese Datei
```

## Schnellstart

1. **Lesen**: Starte mit `buch/01-einleitung.md`
2. **Üben**: Folge dem 30-Tage-Plan in `buch/09-von-anfänger-zum-profi.md`
3. **Anwenden**: Nutze die 50+ Templates in `assets/prompt-templates/`
4. **Verkaufen**: Passe die Marketing-Materialien an

## Qualitätssicherung

Dieses Buch wurde mit einem Multi-LLM-System optimiert:
- Marketing-Analyse (GPT-4o)
- Inhalts-Review (GPT-4o)
- Qualitäts-Check (GPT-4o)
- 9 Verbesserungsregeln von Claude.ai angewendet

**Ergebnis:** 5/5 in allen Kategorien (Marketing, Inhalt, Qualität)

## Lizenz

© 2026 Belkis Aslani. Alle Rechte vorbehalten.

---

*Starte mit Kapitel 2 — nach 20 Minuten wirst du Prompts anders schreiben. Das verspreche ich dir.*
