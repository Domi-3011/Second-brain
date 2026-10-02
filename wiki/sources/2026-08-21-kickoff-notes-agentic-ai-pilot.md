---
title: Kickoff-Notizen Pilot «Agentic AI im Service»
type: source
created: 2026-10-02
updated: 2026-10-02
sources: [raw/alpstein/2026-08-21-kickoff-notes-agentic-ai-pilot.md, raw/alpstein/2026-05-05-strategy-memo-service-first.md]
tags: [ki, service, pilot]
---

# Kickoff-Notizen Pilot «Agentic AI im Service»

**Art:** Sitzungsnotizen zum Kickoff des [[agentic-ai-pilot]]
**Datum:** 21. August 2026, 14:00–15:30
**Teilnehmende:** [[jonas-weber]] (Projektleitung), [[priya-raman]] (Technik), [[nadia-frei]] (Teamleiterin Service Desk), [[lukas-amrein]] (Softwareentwicklung), [[marco-steiner]] (Gast, Finanzen)
**Notizen:** [[lukas-amrein]]
**Original:** `raw/alpstein/2026-08-21-kickoff-notes-agentic-ai-pilot.md`

## Zusammenfassung

Der [[service-triage-agent]] soll Service-Tickets aus [[alpmind]] und dem E-Mail-Postfach lesen, klassieren, Standardfälle mit einer Antwort aus der Wissensbasis lösen und alles andere an Menschen weitergeben. Ziel ist eine Reaktionszeit unter 10 Minuten im Standardfall, heute sind es im Schnitt 3 Stunden. Der Pilot läuft von September bis November 2026 mit einem genehmigten Budget von CHF 180'000. Ein erster Regelentwurf legt fest, was der Agent darf: Er darf vorschlagen, aber nichts versprechen, und nie eine Gutschrift zusagen (Lehre aus dem Fall [[ausfaelle-bergland-2026]]). Offen sind Haftung, Qualitätsmessung, Datenschutz und der Rückfall auf den heutigen Prozess.

## Kernpunkte

- **Klassierung:** Störung, Wartung, Frage, Beschwerde
- **Ziel:** unter 10 Minuten im Standardfall, heute im Schnitt 3 Stunden (Stand 21.08.2026)
- **Pilot:** September bis November 2026, Budget CHF 180'000 (genehmigt)
- **Regeln, erster Entwurf:** siehe [[service-triage-agent]]
  - Ticket lesen und kategorisieren: ja
  - Antwort aus der Wissensbasis vorschlagen: ja, ein Mensch gibt frei
  - Antwort direkt an Kunden senden: **nein** in der Pilotphase, Entscheid nach dem Pilot
  - Preisauskünfte: nein, Preisfragen gehen immer an den Verkauf
  - Gutschrift oder Entschädigung versprechen: **nie** («Lesson from the Bergland case»)
  - Technikereinsatz auslösen: nur vorschlagen, die Disposition entscheidet
  - Ticket schliessen: nein
- **Zitat [[nadia-frei]]:** «The agent may suggest, not promise.»
- **Architektur ([[priya-raman]]):**
  - ein einzelner Agent, keine Multi-Agent-Lösung im Pilot
  - Wissensbasis: Servicehandbücher und die letzten 2'000 gelösten Tickets, aufbereitet als Wiki
  - jede Aktion wird protokolliert, das Protokoll ist Teil der Auswertung
  - zweite Ausbaustufe nach dem Pilot: ein Prüf-Agent kontrolliert die Vorschläge, bevor ein Mensch sie sieht

## Offene Fragen

1. Wer ist verantwortlich, wenn der Agent ein Ticket falsch klassiert und ein Ausfall dadurch länger dauert? ([[marco-steiner]])
2. Wie wird Qualität gemessen, nicht nur Tempo? Vorschlag von [[nadia-frei]]: 10 % der Tickets als Stichprobe durch das Team prüfen.
3. Dürfen Kundendaten aus Tickets ins Sprachmodell? Klärung mit dem Datenschutz bis 15.09.2026.
4. Was passiert, wenn der Agent ausfällt? Der Rückfall auf den heutigen Prozess muss jederzeit möglich sein.

## Nächste Schritte

| Was | Wer | Bis |
|---|---|---|
| Regelwerk «Was der Agent darf» finalisieren | [[jonas-weber]], [[nadia-frei]] | 05.09.2026 |
| Wissensbasis aufbauen | [[lukas-amrein]] | 19.09.2026 |
| Datenschutz klären | [[priya-raman]] | 15.09.2026 |
| Konzept Qualitätsmessung | [[nadia-frei]] | 12.09.2026 |
| Statusbericht an die GL | [[jonas-weber]] | 30.09.2026 |

> [!note] Uncertain
> Alle Termine sind vorbei (heute 02.10.2026). Ob sie eingehalten wurden, weiss das Wiki nicht.

> [!warning] Contradiction
> **Standardfälle direkt lösen:** Das Strategie-Memo sieht vor, dass der Agent Standardfälle «directly» löst (Quelle: [[2026-05-05-strategy-memo-service-first]]). Der Regelentwurf erlaubt im Pilot keine Antwort direkt an Kunden, ein Mensch gibt frei.

## Beteiligte Personen

- [[jonas-weber]], [[priya-raman]], [[nadia-frei]], [[lukas-amrein]], [[marco-steiner]]
