---
title: "ΔΡΑΧ — Phase 0 und Risiken"
description: "Forschungsplan, Budget, Stop-Kriterien und ehrliches Restrisiko"
---

[← Dossier](/DRAX/de/dossier.html) · [English](/DRAX/en/phase-0-risks.html) · [Ελληνικά](/DRAX/el/phase-0-risks.html) · [Folien →](/DRAX/de/slides.html)

# Phase 0 und Risiken

## Der Beschluss bleibt bewusst klein

1. maximal 18 Monate;
2. Mittelobergrenze 1,6 Mio. Euro;
3. nur Gutachten, Simulation, wertloses Testnet und Laborarbeit;
4. Zwischenentscheidung nach neun Monaten;
5. automatisches Ende ohne neuen Fortsetzungsbeschluss.

Der Budgetkorridor von 0,95 bis 1,65 Mio. Euro ist ein **Vorschlag, keine Bewilligung**. Es gibt keine Produktionsinfrastruktur, keine Banknotenproduktion mit Nennwert und keine Mainnet-Liquidität.

## Zeitplan

| Monat | Nachweis |
|---|---|
| 0–3 | Rechtsfragen, Invarianten, Systemmodelle, Testnet-Umgebung |
| 4–6 | Constitution-/Bearer-PoC und Supply-Indexer |
| 7–9 | CashLot, Offline-Labor und Zwischenentscheidung |
| 10–12 | Angriffssimulation, Migrations- und Exit-Test |
| 13–15 | integrierte wertlose Demo und unabhängiges Red Team |
| 16–18 | Abschlussgutachten: Go, No-Go oder Research-Only |

## Budgetbänder

| Bereich | Band |
|---|---:|
| EU-/GR-Recht, MiCA, AML, Legal Tender | 140–220 Tsd. € |
| Makroökonomische Simulation | 120–200 Tsd. € |
| Toccata Covenant PoC | 220–380 Tsd. € |
| Wallet und öffentliche Indexer | 120–220 Tsd. € |
| Offline-/Secure-Element-Labor | 100–180 Tsd. € |
| Bargeldprozess-Design | 70–130 Tsd. € |
| Reviews und Bug Bounty | 120–220 Tsd. € |
| Programmsteuerung und Transparenz | 60–100 Tsd. € |

## Harte Abbruchkriterien

- Rechtsgutachten verneint einen sicheren Forschungs- oder Pilotpfad;
- `S ≤ Mmax` oder die Doppelzählungsfreiheit ist nicht unabhängig beweisbar;
- Compiler-, Wallet- oder Indexer-Reife reicht nicht aus;
- CashLot-Fälschung oder Offline-Double-Spend bleibt außerhalb genehmigter Verlustgrenzen;
- Genesis-Sunset oder Key Burn ist verlängerbar oder umgehbar;
- Kaspa-Abhängigkeit kann nicht mit einem realistischen Migrationspfad begrenzt werden;
- Datenschutz, AML oder physische Serienkontrolle erzeugen unvertretbare Risiken;
- das Projekt wird politisch als bereits beschlossene Parallelwährung dargestellt.

## Risikoregister in Kurzform

| Risiko | Frühindikator | Gegenmittel | Was bleibt |
|---|---|---|---|
| Covenant-/Compilerfehler | unterschiedliche Ausführung, Audit-Finding | formale Spezifikation, zwei unabhängige Audits | unbekannter Logikfehler |
| Kaspa-Reorg oder Gebührenabhängigkeit | hohe Reorgtiefe, Konzentration, Gebührenstress | Finalitätsfenster, Fee-Policy, Migrationstest | fremdes Netzwerk |
| CashLot-Betrug | Register-/Lock-Abweichung | unabhängige Inventur, Bond, Seriencommitments | physische Kollusion |
| Falschgeld | steigende Ablehnungsquote | Sicherheitsmerkmale, Maschinenprüfung, Austauschregeln | soziale Schäden |
| Offline Double Spend | Counter-Anomalien | Betrags-, Zeit- und Hop-Limits | begrenzter Händlerverlust |
| Governance Capture | Konzentration, schnelle Vorschläge | Sunset, Timelocks, unveränderlicher Kern | Einfluss an Systemrändern |
| Staatlicher Zugriff | Gesetzes-/Beschlagnahmerisiko | Self-Custody, Schlüsselvernichtung, Rechtsmittel | Nutzung kann reguliert werden |
| Bank-/Liquiditätskrise | Abflüsse, Laufzeitinkongruenz | 100%-Reserve, Fonds, geordnete Insolvenz | kein unbegrenzter LOLR |
| Soziale Ablehnung | „zweite Drachme = Krise“ | freiwilliger Test, transparente Sprache | Vertrauen ist nicht programmierbar |

## Ehrliches Restrisiko

Eine fixe Menge kann Deflation und reale Schuldenlast erhöhen. Narrow Banking kann Kredit verteuern. Papier und Metall bleiben von menschlichen Institutionen abhängig. Offline-Finalität ist begrenzt. Kaspa ersetzt keine nationale Rechtsordnung oder Migrationsstrategie. Technologie kann kein Verbot, keine Marktblockade und keine geopolitische Ablehnung unmöglich machen.

Phase 0 ist gerade deshalb vertretbar, weil ein **No-Go** ein zulässiges und nützliches Ergebnis ist.

