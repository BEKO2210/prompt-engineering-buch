# Das Prompt Engineering Handbuch

**Von Belkis Aslani**

---

## Über dieses Buch

Dieses Handbuch ist das Ergebnis von drei Jahren praktischer Arbeit mit KI-Systemen. Es enthält keine theoretischen Abhandlungen, keine Füllseiten – nur das, was wirklich funktioniert.

Der ROKA-Rahmen, der in diesem Buch vorgestellt wird, ist meine eigene Methode, die ich in hunderten Projekten entwickelt und verfeinert habe.

## Struktur

```
/tmp/prompt-engineering-buch/
├── README.md                    # Diese Datei
├── buch/                        # Hauptbuch (12 Kapitel)
│   ├── 01-einleitung.md
│   ├── 02-was-sind-prompts.md
│   ├── 03-die-anatomie-eines-guten-prompts.md
│   ├── 04-der-rahmen-rolle-kontext-aufgabe.md
│   ├── 05-fortgeschrittene-techniken.md
│   ├── 06-haeufige-fehler.md
│   ├── 07-praxisbeispiele.md
│   ├── 08-tools-und-workflows.md
│   ├── 09-von-anfänger-zum-profi.md
│   ├── 10-appendix-promptsammlung.md
│   ├── 11-ethik-und-verantwortung.md    # NEU
│   └── 12-team-workflows.md             # NEU
├── versionen/                   # Verschiedene Versionen
│   ├── ebook-epub/              # EPUB-Version
│   ├── ebook-pdf/               # PDF-Version
│   ├── premium-workbook/        # Premium-Version
│   └── video-skript/            # Video-Kurs-Skript
├── marketing/                   # Verkaufsmaterialien
│   ├── sales-page.md
│   ├── email-sequence.md
│   └── social-media-posts.md
└── assets/                      # Zusatzmaterialien
    ├── prompt-templates/        # 50+ Templates
    ├── checklisten/             # 4 Checklisten
    └── uebersichten/            # 4 Mindmaps/Übersichten
```

## Inhalt

### Teil 1: Grundlagen
- Was Prompts wirklich sind
- Die 4 Säulen jedes guten Prompts
- Der ROKA-Rahmen

### Teil 2: Fortgeschrittene Techniken
- Chain-of-Thought
- Few-Shot Prompting
- System-Prompts
- Self-Consistency
- Tree of Thoughts
- Negative Prompting
- Messbarkeit: KPIs für Prompt Success

### Teil 3: Praxis
- 20+ konkrete Anwendungsfälle
- 50+ sofort nutzbare Prompts
- Tools und Workflows
- Der 30-Tage-Lernpfad

### Teil 4: Ethik & Skalierung
- KI-Ethik und Verantwortung
- Team-Workflows und Enterprise-Einsatz

## Schreibstil

Dieses Buch ist geschrieben in:
- Direkter, ehrlicher Sprache
- Praxisnah mit echten Beispielen
- Ohne Floskeln
- Konkreten Anleitungen statt Theorie

## Verwendung

### Als E-Book
Die Markdown-Dateien im Ordner `buch/` können in EPUB oder PDF konvertiert werden.

**Tools:**
- Calibre (EPUB)
- Pandoc (PDF)
- Adobe InDesign (professionelles PDF)

### Als Kurs-Material
Die Inhalte können als Basis für einen Video-Kurs oder Workshop genutzt werden.

### Für Marketing
Die Materialien im Ordner `marketing/` können direkt verwendet oder angepasst werden.

## Format-Konvertierung

Dieses Buch ist in Markdown geschrieben. So wandelt du es in andere Formate:

### PDF
```bash
# Mit pandoc (empfohlen)
pandoc buch/*.md -o prompt-engineering-handbuch.pdf \
  --pdf-engine=xelatex \
  -V geometry:margin=2.5cm \
  -V fontsize=11pt \
  --toc \
  --toc-depth=2

# Alternative: Markdown to PDF Tools
# - md-to-pdf (Node.js)
# - grip (GitHub-style Markdown)
# - VS Code mit Markdown PDF Extension
```

### EPUB
```bash
# Mit pandoc
pandoc buch/*.md -o prompt-engineering-handbuch.epub \
  --toc \
  --toc-depth=2 \
  -V title="Das Prompt Engineering Handbuch" \
  -V author="Belkis Aslani"

# Mit Calibre (GUI oder CLI)
ebook-convert buch/*.md prompt-engineering-handbuch.epub
```

### Word (DOCX)
```bash
# Mit pandoc
pandoc buch/*.md -o prompt-engineering-handbuch.docx \
  --toc \
  --reference-doc=template.docx  # Optional: eigenes Template

# Alternative: Direkter Export
# - Typora (Export zu DOCX)
# - Obsidian (mit Community Plugins)
# - VS Code mit Pandoc Extension
```

### HTML
```bash
# Mit pandoc (Standalone-HTML)
pandoc buch/*.md -o prompt-engineering-handbuch.html \
  --standalone \
  --toc \
  --css=style.css  # Optional: eigenes CSS

# Alternative: Markdown-Renderer
# - grip (GitHub-Style)
# - marked (Node.js)
# - Python-Markdown
```

### Tipps für die Konvertierung

1. **Bilder**: Stelle sicher, dass Bildpfade relativ sind (`./assets/bild.png`)
2. **Tabellen**: Pandoc unterstützt Markdown-Tabellen gut, komplexe Layouts können angepasst werden
3. **Code-Blöcke**: Werden in den meisten Formaten korrekt dargestellt
4. **Schriften**: Für PDF mit LaTeX kannst du Systemschriften nutzen (`-V mainfont="Arial"`)

## Lizenz

Dieses Werk ist urheberrechtlich geschützt.

© 2026 Belkis Aslani

Alle Rechte vorbehalten.

## Kontakt

Bei Fragen oder Anregungen:
[Deine Kontaktdaten hier einfügen]

---

*Dieses Handbuch wurde mit KI-Unterstützung erstellt – unter Verwendung der im Buch beschriebenen Techniken.*
