---
title: "DRX Programme — Phase 0 and risks"
description: "Research plan, budget, stop criteria and honest residual risk"
---

[← Dossier](/DRAX/en/dossier.html) · [Deutsch](/DRAX/de/phase-0-risks.html) · [Ελληνικά](/DRAX/el/phase-0-risks.html) · [Slides →](/DRAX/en/slides.html)

# Phase 0 and risks

## A deliberately small decision

1. no more than 18 months;
2. funding cap of €1.6 million;
3. legal opinions, simulations, a valueless testnet and laboratory work only;
4. an interim decision after nine months;
5. automatic termination without a new continuation decision.

The €0.95–1.65 million range is **a proposal, not approved funding**. It contains no production infrastructure, monetary banknote production or mainnet liquidity.

## Timeline

| Month | Required evidence |
|---|---|
| 0–3 | legal questions, invariants, system models, testnet environment |
| 4–6 | Constitution/Bearer proof of concept and supply indexer |
| 7–9 | CashLot, offline laboratory and interim decision |
| 10–12 | attack simulation, migration and exit test |
| 13–15 | integrated valueless demonstration and independent red team |
| 16–18 | final opinion: Go, No-Go or Research-Only |

## Budget bands

| Area | Band |
|---|---:|
| EU/Greek law, MiCA, AML, legal tender | €140–220k |
| Macroeconomic simulation | €120–200k |
| Toccata covenant proof of concept | €220–380k |
| Wallet and public indexers | €120–220k |
| Offline/secure-element laboratory | €100–180k |
| Cash-process design | €70–130k |
| Reviews and bug bounty | €120–220k |
| Programme governance and transparency | €60–100k |

## Hard stop criteria

- legal analysis finds no safe research or pilot path;
- `S ≤ Mmax` or absence of double counting cannot be independently proven;
- compiler, wallet or indexer maturity is inadequate;
- CashLot fraud or offline double spend exceeds the approved loss envelope;
- the Genesis sunset or key burn can be extended or bypassed;
- Kaspa dependency lacks a credible migration path;
- privacy, AML or physical serial controls create unacceptable risk;
- the project is politically presented as an already decided parallel currency.

## Condensed risk register

| Risk | Early signal | Mitigation | Residual risk |
|---|---|---|---|
| covenant/compiler error | divergent execution, audit finding | formal specification, two independent audits | unknown logic flaw |
| Kaspa reorg or fee dependency | deep reorg, concentration, fee stress | finality window, fee policy, migration test | external network |
| CashLot fraud | register/lock mismatch | inventory, bonds, serial commitments | physical collusion |
| counterfeiting | rising rejection rate | security features, machine checks, exchange rules | social damage |
| offline double spend | counter anomalies | amount, time and hop limits | bounded merchant loss |
| governance capture | concentration, rushed proposals | sunset, timelocks, immutable core | edge influence |
| state pressure | seizure or prohibition proposals | self-custody, destroyed keys, legal remedy | use can be regulated |
| banking/liquidity crisis | outflows, maturity mismatch | 100% reserve, funds, orderly insolvency | no unlimited LOLR |
| social rejection | “second drachma means crisis” | voluntary testing, transparent language | trust cannot be programmed |

## Honest residual risk

A fixed supply can amplify deflation and real debt burdens. Narrow banking can make credit more expensive. Notes and coins still depend on human institutions. Offline finality is bounded. Kaspa does not replace national law or a migration strategy. Technology cannot make prohibition, market exclusion or geopolitical rejection impossible.

Phase 0 is defensible precisely because **No-Go** is an acceptable and useful outcome.
