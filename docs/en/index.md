---
title: "DRX Programme — Independent Drachma"
description: "English introduction to the public DRX feasibility study"
---

[Deutsch](/DRAX/de/) · [English](/DRAX/en/) · [Ελληνικά](/DRAX/el/) · [GitHub](https://github.com/NeaBouli/DRAX)

# DRX PROGRAMME — INDEPENDENT DRACHMA

## Hellenic Monetary Technology Initiative

**Digital designation:** dig Δραχμή (“digital Drachma”) · **Symbol:** ΔΡΑΧ · **Project mark:** DRX

A hard digital, offline-capable and physical unit of account.

> **Public research edition of an independent Vendetta Labs initiative. No government mandate. No legal-tender status. No existing coin. No sale.**

ΔΡΑΧ studies how **one money supply** could be used in self-custody, in a bounded offline mode, as banknotes and as coins. Greece is the concrete case study. The project does not claim that Greece has adopted this currency or that a second national legal tender could be introduced under current euro-area law.

## The test sentence

A fisher on Kalymnos receives a ΔΡΑΧ banknote on Sunday. On Monday, the fisher deposits it at a bank and receives the same nominal amount digitally. Neither the bank nor a ministry may thereby create additional ΔΡΑΧ, freeze an unrelated self-custody wallet or change the maximum supply.

This sentence is a **design test for the study**, not a proven property of a deployed system.

## What ΔΡΑΧ is — and is not

| ΔΡΑΧ is intended to be | ΔΡΑΧ is not intended to be |
|---|---|
| an independent unit of account | not pegged to EUR or USD |
| self-custodied digital bearer value | not a CBDC with central-bank citizen accounts |
| notes and coins from the same supply | not a second cash money supply |
| protected by a hard protocol cap | no emergency mint for government or governance |
| bounded and prefunded offline value | no unlimited trustless offline finality |
| freely priced by markets | no stability or return guarantee |

## The monetary constitution in one formula

![One money supply in four carrier forms](/DRAX/assets/images/architecture/en/supply-model.png)

`D`, `P`, `O` and `E` are not separate currencies. They are states of the same unit. Moving from digital to cash or offline form must never increase the sum.

## Why Kaspa Toccata is being studied

Kaspa Toccata describes a UTXO-native model in which a covenant can validate not only the current spend but also permitted successor outputs. This fits a bearer design with local split, merge and transfer rules. The study treats compiler maturity, wallets, indexers, KAS fees, network governance and migration as young or external dependencies. Kaspa is therefore a research substrate, not a guarantee of sovereignty.

## Five building blocks

1. **Constitution:** genesis supply, emission schedule, `Mmax` and sunset.
2. **Bearer:** digital split, merge and transfer rules without a central account registry.
3. **CashLot:** a digital lock required before issuing notes or coins.
4. **OfflineLock:** prefunded offline value with amount and time limits.
5. **Recovery:** narrowly defined dispute and destruction states without a general freeze power.

## Reading paths

- [Architecture](/DRAX/en/architecture.html) — supply, Kaspa, CashLot, OfflineLock and banking.
- [Dossier guide](/DRAX/en/dossier.html) — chapter map and complete original documents.
- [Law and governance](/DRAX/en/law-governance.html) — euro area, MiCA, legal tender, Genesis Steward and key burn.
- [Phase 0 and risks](/DRAX/en/phase-0-risks.html) — 18 months, budget, milestones, stop criteria and limitations.
- [Slides and downloads](/DRAX/en/slides.html) — presentation, whitepaper, memo and ministry template.
- [Sources](/DRAX/en/sources.html) — primary materials and verification notes.

## The proposed next step

Only a 12-to-18-month **Phase 0** is proposed, with a funding cap of €1.6 million. It covers legal opinions, macroeconomic simulation, a valueless testnet prototype, CashLot/offline laboratory tests and independent reviews. Mainnet value, notes with monetary value, tax acceptance and legal tender are explicitly excluded.

[Continue to the architecture →](/DRAX/en/architecture.html)
