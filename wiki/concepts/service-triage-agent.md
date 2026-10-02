---
title: Service-Triage-Agent
type: concept
created: 2026-10-02
updated: 2026-10-02
sources: [raw/alpstein/2026-08-21-kickoff-notes-agentic-ai-pilot.md]
tags: [ki, service, regeln]
---

# Service-Triage-Agent

**Was:** KI-Agent im [[agentic-ai-pilot]]. Er liest Service-Tickets aus [[alpmind]] und dem E-Mail-Postfach, klassiert sie (Störung, Wartung, Frage, Beschwerde), schlägt für Standardfälle eine Antwort aus der Wissensbasis vor (im Pilot gibt ein Mensch frei, siehe Tabelle und den Widerspruch auf [[agentic-ai-pilot]]) und gibt alles andere an Menschen weiter. (Quelle: [[2026-08-21-kickoff-notes-agentic-ai-pilot]])

## Was der Agent darf (erster Entwurf, Stand 21.08.2026)

| Aktion | Erlaubt? | Bemerkung |
|---|---|---|
| Ticket lesen und kategorisieren | ja | – |
| Antwort aus der Wissensbasis vorschlagen | ja | Ein Mensch gibt frei |
| Antwort direkt an Kunden senden | **nein** (Pilotphase) | Entscheid nach dem Pilot |
| Preisauskünfte geben | nein | Preisfragen gehen immer an den Verkauf |
| Gutschrift oder Entschädigung versprechen | **nie** | Lehre aus dem Fall [[ausfaelle-bergland-2026]] |
| Technikereinsatz auslösen | nur Vorschlag | Die Disposition entscheidet |
| Ticket schliessen | nein | – |

(Quelle: [[2026-08-21-kickoff-notes-agentic-ai-pilot]])

Grundsatz von [[nadia-frei]]: «The agent may suggest, not promise.» (Quelle: [[2026-08-21-kickoff-notes-agentic-ai-pilot]])

## Aufbau

- Ein einzelner Agent im Pilot, keine Multi-Agent-Lösung (Quelle: [[2026-08-21-kickoff-notes-agentic-ai-pilot]])
- Wissensbasis: Servicehandbücher und die letzten 2'000 gelösten Tickets, als Wiki aufbereitet (Quelle: [[2026-08-21-kickoff-notes-agentic-ai-pilot]])
- Jede Aktion wird protokolliert (Quelle: [[2026-08-21-kickoff-notes-agentic-ai-pilot]])
- Nach dem Pilot ist ein Prüf-Agent geplant (Quelle: [[2026-08-21-kickoff-notes-agentic-ai-pilot]])

> [!note] Uncertain
> Das Regelwerk ist ein Entwurf. Es sollte bis 05.09.2026 finalisiert werden ([[jonas-weber]], [[nadia-frei]]), ob das geschehen ist, weiss das Wiki nicht.
