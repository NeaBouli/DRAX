---
title: "ΔΡΑΧ — Architektur"
description: "Monetäre, technische, physische und institutionelle Architektur"
---

[← Überblick](/DRAX/de/) · [English](/DRAX/en/architecture.html) · [Ελληνικά](/DRAX/el/architecture.html) · [Dossier →](/DRAX/de/dossier.html)

# Architektur

> **Status:** Forschungsarchitektur. Alle Mengen und Limits sind Planungs- oder Testparameter. Es existiert kein produktiver Vertrag und kein Mainnet-Asset.

## 1. Eine Einheit statt vier Geldmengen

```text
S(t) = D(t) + P(t) + O(t) + E(t)
S(t) ≤ Mmax
```

- `D`: digital frei umlaufende Bearer-Outputs;
- `P`: in CashLots gesperrte Einheiten für ausgegebene Noten und Münzen;
- `O`: in OfflineLocks gesperrte Einheiten;
- `E`: eng definierte Sonderzustände, etwa nachgewiesene Vernichtung oder Streitfälle.

Für jede gültige Zustandsänderung soll formal gelten: Inputs plus erlaubte Emission entsprechen Outputs plus nachweislicher Vernichtung. Ein Wallet-Frontend, eine Bank oder ein Indexer darf diese Invariante nicht erweitern.

![Supply-Modell](/DRAX/assets/images/architecture/de/supply-model.png)

## 2. Warum kein kollateralisiertes Stablecoin-Modell

Die öffentliche DRAX-Fassung trennt die Landeswährung von 1kUSD. Es gibt keinen USD-Peg, kein PSM, keinen Mint gegen USDC/USDT/EURC und keinen Preis-Oracle im monetären Kern. BTC, ETH oder Gold können später in einem getrennten, freiwilligen Liquiditäts- oder Krisenfonds gehalten werden. Sie erzeugen aber kein Prägerecht und garantieren keinen Wechselkurs.

Damit wird ein systemischer Import des Fiat-Pegs vermieden. Der Preis von ΔΡΑΧ gegenüber EUR, USD, BTC oder Waren schwimmt am Markt. Das macht die Einheit härter, aber nicht automatisch preisstabil.

## 3. Kaspa Toccata als vorgeschlagene Forschungsbasis

Toccata ist laut Kaspa-Dokumentation UTXO-nativ. Ein zustandsbehafteter Covenant kann beim Spend den eigenen Nachfolger prüfen. Daraus folgt eine Architektur aus vielen parallel übertragbaren Bearer-UTXOs statt eines globalen Kontos mit veränderlicher Balance.

### Covenant-Familien

| Familie | Aufgabe | Unveränderlicher Zielkern |
|---|---|---|
| Constitution | Genesis, `M0`, `Mmax`, Schedule, Sunset | keine nachträgliche Mint-Autorität |
| Bearer | split, merge, transfer | keine administrative Freeze-Funktion |
| CashLot | physische Ausgabe, Rücknahme und Vernichtung | kein physischer Nominalwert ohne Lock |
| OfflineLock | vorfinanzierte Offline-Zuweisung | kein Offline-Wert ohne on-chain Sperre |
| Recovery | eng begrenzte Streitfälle | kein globaler Pause- oder Beschlagnahmeschalter |

### Externe Abhängigkeiten

- KAS für Netzwerkgebühren in der ersten Architektur;
- Konsens, Miner und Netzwerk-Upgrades von Kaspa;
- Silverscript-/Compiler-Reife;
- Wallets, Indexer und Hardware-Lieferketten;
- verfügbare Marktliquidität;
- ein getesteter Migrations- und Exit-Pfad.

Diese Abhängigkeiten schließen die Behauptung vollständiger technischer Autarkie aus.

## 4. Digitale und physische Form verheiraten

![CashLot-Zyklus](/DRAX/assets/images/architecture/de/cashlot-cycle.png)

1. Eine gesetzlich definierte Cash Utility oder Bank sperrt `x ΔΡΑΧ` in einem CashLot.
2. Der Covenant erzeugt einen öffentlich prüfbaren Warrant für eine Charge.
3. Eine autorisierte Druckerei oder Münzstätte produziert höchstens den gesperrten Nominalwert.
4. Nach Prüfung wechselt die Charge in den Zustand `Issued`; der digitale Gegenwert bleibt unübertragbar.
5. Bei Rückgabe werden Note oder Münze authentifiziert, entwertet und kontrolliert vernichtet.
6. Erst nach dem Vernichtungsnachweis werden exakt `x ΔΡΑΧ` wieder digital freigegeben.

Bei Unsicherheit bleibt der digitale Wert gesperrt. Dadurch kann Liquidität blockieren, die Geldmenge aber nicht wachsen. Der physische Arm bleibt institutionell und benötigt Serienkontrolle, Inventur, unabhängige Prüfer, Versicherungen und strafrechtlichen Fälschungsschutz.

## 5. Offline ohne falsche Versprechen

Der Offline-Wert ist vorfinanziert. Ein Nutzer verschiebt ΔΡΑΧ aus `D` in einen `OfflineLock`; ein zertifiziertes Secure Element verwaltet begrenzte Weitergaben bis zur nächsten Synchronisation.

**Testparameter für Phase 0:**

- maximal 150 ΔΡΑΧ je Gerät;
- maximal 50 ΔΡΑΧ je Zahlung;
- maximal drei Offline-Hops;
- Synchronisation spätestens nach 72 Stunden;
- Händler trägt bis zur Abrechnung ein klar ausgewiesenes Restrisiko.

Diese Werte sind keine Produktionsempfehlung. Unbegrenzte trustlose Offline-Finalität wird nicht behauptet.

## 6. Banken ohne unbeschränkte Geldschöpfung

Zahlungskonten sollen zu 100 % in ΔΡΑΧ gedeckt, insolvenzfest getrennt und öffentlich attestiert sein. Kredit entsteht aus Termineinlagen, Anleihen, Eigenkapital oder Fonds, deren Kapitalgeber ausdrücklich Risiko tragen. Eine Bank darf aus einem Zahlungsguthaben keinen zusätzlichen ΔΡΑΧ-Bestand erzeugen.

Der Preis dafür ist real: Kredit kann teurer und in Krisen knapper werden. Ohne unlimitierten Lender of Last Resort müssen Liquiditätspuffer, Einlagensicherung und Abwicklungsfonds vorfinanziert sein.

## 7. Öffentliche Nachprüfbarkeit

Mindestens drei unabhängig betriebene Indexer sollen Gesamtmenge, Genesis- und Emissionszustand, CashLot-Salden, OfflineLock-Alter, Steward-Schlüsselstatus und Abweichungen zwischen physischem Register und on-chain Commitments rekonstruieren. Ein Indexer ist Beobachter, nicht Quelle der Wahrheit.

[Recht und Governance →](/DRAX/de/law-governance.html)

