# Prompt-Template 35: API-Dokumentation

## Zweck
Entwickler-freundliche Dokumentation für APIs.

## Prompt
```
ROLLE: Als Technical Writer für Developer...

KONTEXT:
Endpoint: [Pfad]
Methode: [GET/POST/PUT/DELETE]
Zweck: [Was macht dieser Endpoint?]
Authentifizierung: [Wie authentifiziert man sich?]

AUFGABE: Dokumentiere den API Endpoint.

FORMAT:
- Endpoint: URL mit Parametern
- Methode: HTTP Verb
- Beschreibung: 2-3 Sätze zur Funktionalität
- Authentifizierung: Required/Optional + Methode
- Request: Parameter (Name, Typ, Required, Beschreibung)
- Response: Status Codes + Beispiel-JSON
- Error Handling: Häufige Fehler und Lösungen
- Beispiel: Kompletter cURL Request
```

## Variationen
- Für Public API: Rate Limits und Best Practices
- Für Internal API: Kontext und Architektur-Entscheidungen
- Für Webhook: Event-Struktur und Retry-Logik
