# Übersicht: Fortgeschrittene Techniken

```
┌─────────────────────────────────────────────────────────────┐
│           FORTGESCHRITTENE TECHNIKEN                        │
│                                                             │
│   Wann welche Technik nutzen?                               │
└─────────────────────────────────────────────────────────────┘
```

## Technik-Übersicht

### Chain-of-Thought (CoT)
```
┌─────────────────────────────────────┐
│  Wann: Komplexe Probleme            │
│  Wirkung: Bessere Logik             │
│                                     │
│  "Löse Schritt für Schritt:"        │
│  1. Analysieren                     │
│  2. Planen                          │
│  3. Ausführen                       │
│  4. Überprüfen                      │
└─────────────────────────────────────┘
```

### Few-Shot Prompting
```
┌─────────────────────────────────────┐
│  Wann: Klassifikation, Format       │
│  Wirkung: Konsistenz                │
│                                     │
│  Beispiel 1: Input → Output         │
│  Beispiel 2: Input → Output         │
│  Beispiel 3: Input → Output         │
│  Jetzt: Input → ?                   │
└─────────────────────────────────────┘
```

### System-Prompts
```
┌─────────────────────────────────────┐
│  Wann: Wiederholte Nutzung          │
│  Wirkung: Konsistentes Verhalten    │
│                                     │
│  "Du bist [Rolle].                  │
│   Dein Stil ist [X].                │
│   Deine Regeln: 1, 2, 3"            │
└─────────────────────────────────────┘
```

### Self-Consistency
```
┌─────────────────────────────────────┐
│  Wann: Wichtige Entscheidungen      │
│  Wirkung: Höhere Qualität           │
│                                     │
│  "Generiere 3 Varianten:            │
│   - Variante 1 (Ansatz A)           │
│   - Variante 2 (Ansatz B)           │
│   - Variante 3 (Ansatz C)"          │
└─────────────────────────────────────┘
```

### Tree of Thoughts
```
┌─────────────────────────────────────┐
│  Wann: Strategieentwicklung         │
│  Wirkung: Mehr Optionen             │
│                                     │
│  "Entwickle 3 Lösungswege:          │
│   Für jeden: Vor-/Nachteile,        │
│   Aufwand, Erfolgswahrscheinlichkeit│
│   Dann: Empfehlung"                 │
└─────────────────────────────────────┘
```

### Negative Prompting
```
┌─────────────────────────────────────┐
│  Wann: Klare Grenzen                │
│  Wirkung: Vermeidung von Fehlern    │
│                                     │
│  "Vermeide: X, Y, Z                 │
│   Stattdessen: A, B, C"             │
└─────────────────────────────────────┘
```

## Entscheidungsbaum

```
                    ┌─────────────────┐
                    │  Welche Technik?│
                    └────────┬────────┘
                             │
            ┌────────────────┼────────────────┐
            │                │                │
            ▼                ▼                ▼
    ┌──────────────┐ ┌──────────────┐ ┌──────────────┐
    │ Komplexes    │ │ Wiederholte  │ │ Format/      │
    │ Problem?     │ │ Aufgabe?     │ │ Klassifikation│
    └──────┬───────┘ └──────┬───────┘ └──────┬───────┘
           │                │                │
           ▼                ▼                ▼
    ┌──────────────┐ ┌──────────────┐ ┌──────────────┐
    │ Chain-of-    │ │ System-      │ │ Few-Shot     │
    │ Thought      │ │ Prompt       │ │ Prompting    │
    └──────────────┘ └──────────────┘ └──────────────┘
```

## Techniken kombinieren

```
┌─────────────────────────────────────────────────────────┐
│  EMPFOHLENE KOMBINATIONEN                               │
├─────────────────────────────────────────────────────────┤
│  System-Prompt + Few-Shot                               │
│  → Für konsistente, formatierte Ergebnisse             │
├─────────────────────────────────────────────────────────┤
│  Chain-of-Thought + Self-Consistency                    │
│  → Für wichtige, komplexe Entscheidungen               │
├─────────────────────────────────────────────────────────┤
│  Few-Shot + Negative Prompting                          │
│  → Für präzise Format-Vorgaben                         │
├─────────────────────────────────────────────────────────┤
│  Tree of Thoughts + Chain-of-Thought                    │
│  → Für strategische Planung                            │
└─────────────────────────────────────────────────────────┘
```

## Schnell-Referenz

| Situation | Primäre Technik | Sekundäre Technik |
|-----------|-----------------|-------------------|
| Mathe/Logik | Chain-of-Thought | - |
| Klassifikation | Few-Shot | - |
| Wiederholte Aufgaben | System-Prompt | Few-Shot |
| Wichtige Entscheidung | Self-Consistency | Chain-of-Thought |
| Strategie | Tree of Thoughts | - |
| Format-Probleme | Few-Shot | Negative Prompting |
| Unwanted Output | Negative Prompting | - |

---

*Wähle die Technik nach der Aufgabe. Kombiniere klug.*
