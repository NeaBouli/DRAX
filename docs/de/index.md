---
title: "Programm DRX — Unabhängige Drachme"
description: "Deutschsprachiger Einstieg in die öffentliche DRX-Machbarkeitsstudie"
---

[Deutsch](/DRAX/de/) · [English](/DRAX/en/) · [Ελληνικά](/DRAX/el/) · [GitHub](https://github.com/NeaBouli/DRAX)

# PROGRAMM DRX — UNABHÄNGIGE DRACHME

## Griechische Initiative für Währungstechnologie

**Währungseinheit:** dig Δραχμή · **Symbol:** ΔΡΑΧ · **Projektmarke:** DRX

Eine harte digitale, offline-fähige und physische Rechnungseinheit.

> **Öffentliche Forschungsfassung einer privaten Initiative von Vendetta Labs. Kein staatlicher Auftrag. Kein gesetzliches Zahlungsmittel. Kein existierender Coin. Kein Verkauf.**

ΔΡΑΧ untersucht, wie **eine einzige Geldmenge** gleichzeitig digital in Self-Custody, begrenzt offline, als Banknote und als Münze genutzt werden könnte. Griechenland ist der konkrete Anwendungsfall. Das Projekt behauptet nicht, dass Griechenland diese Währung beschlossen hat oder dass sie nach heutigem Eurozonenrecht als nationales gesetzliches Zahlungsmittel eingeführt werden kann.

## Der Prüfsatz

Ein Fischer auf Kalymnos erhält am Sonntag eine ΔΡΑΧ-Banknote. Am Montag zahlt er sie bei einer Bank ein und erhält denselben Nominalbetrag digital. Dabei darf weder die Bank noch ein Ministerium zusätzliche ΔΡΑΧ erzeugen, eine fremde Self-Custody-Wallet einfrieren oder die Maximalmenge verändern.

Dieser Satz ist ein **Prüfkriterium der Studie**, keine bereits bewiesene Systemeigenschaft.

## Was ΔΡΑΧ ist — und was nicht

| ΔΡΑΧ soll sein | ΔΡΑΧ soll nicht sein |
|---|---|
| eigenständige Rechnungseinheit | kein EUR- oder USD-Peg |
| digitaler Bearer Value in Self-Custody | keine CBDC mit Bürgerkonten bei einer Zentralbank |
| Banknoten und Münzen derselben Geldmenge | keine zweite Geldmenge für Bargeld |
| harte protokollseitige Obergrenze | kein Notfall-Mint durch Staat oder Governance |
| begrenzter, vorfinanzierter Offline-Wert | keine unbegrenzte trustlose Offline-Finalität |
| offene Marktpreisbildung | keine Stabilitäts- oder Renditegarantie |

## Die Geldverfassung in einer Formel

![Eine Geldmenge in vier Trägerformen](/DRAX/assets/images/architecture/de/supply-model.png)

`D`, `P`, `O` und `E` sind keine getrennten Währungen. Es sind Zustände derselben Einheit. Ein Wechsel von digital zu Bargeld oder offline darf die Summe nicht erhöhen.

## Warum Kaspa Toccata untersucht wird

Kaspa Toccata beschreibt ein UTXO-natives Modell, in dem ein Covenant beim Ausgeben nicht nur den aktuellen Spend, sondern auch zulässige Nachfolger prüfen kann. Das passt konzeptionell zu einem Bearer-System mit lokalen Split-, Merge- und Transferregeln. Die Studie behandelt Compiler, Wallets, Indexer, KAS-Gebühren, Netzwerk-Governance und Migration ausdrücklich als junge oder externe Abhängigkeiten. Kaspa ist damit Forschungsgrundlage, nicht Souveränitätsgarantie.

## Die fünf Bausteine

1. **Constitution:** Genesis-Menge, Emissionsschedule, `Mmax` und Sunset.
2. **Bearer:** digitale Split-, Merge- und Transferregeln ohne zentrale Kontoregistry.
3. **CashLot:** Sperre digitaler Einheiten als Voraussetzung für Banknoten und Münzen.
4. **OfflineLock:** vorfinanzierter, betrags- und zeitbegrenzter Offline-Wert.
5. **Recovery:** eng definierte Streit- und Vernichtungszustände ohne generelle Freeze-Macht.

## Wo Sie einsteigen können

- [Architektur](/DRAX/de/architecture.html) — Geldmenge, Kaspa, CashLot, OfflineLock und Bankenmodell.
- [Dossier](/DRAX/de/dossier.html) — Kapitelstruktur und vollständige Originaldokumente.
- [Recht und Governance](/DRAX/de/law-governance.html) — Eurozone, MiCA, Legal Tender, Genesis Steward und Key Burn.
- [Phase 0 und Risiken](/DRAX/de/phase-0-risks.html) — 18 Monate, Budget, Meilensteine, Abbruchkriterien und ehrliche Grenzen.
- [Folien und Downloads](/DRAX/de/slides.html) — Präsentation, Whitepaper, Memo und Ministeriumsvorlage.
- [Quellen](/DRAX/de/sources.html) — Primärquellen und Verifikationshinweise.

## Der beantragte nächste Schritt

Vorgeschlagen wird ausschließlich eine 12- bis 18-monatige **Phase 0** mit einer Mittelobergrenze von 1,6 Mio. Euro. Sie enthält Rechtsgutachten, Makrosimulation, einen wertlosen Testnet-Prototyp, CashLot-/Offline-Labortests und unabhängige Reviews. Nicht enthalten sind Mainnet-Wert, Banknoten mit Nennwert, Steuerannahme oder Legal Tender.

[Weiter zur Architektur →](/DRAX/de/architecture.html)
