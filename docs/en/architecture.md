---
title: "ΔΡΑΧ — Architecture"
description: "Monetary, technical, physical and institutional architecture"
---

[← Overview](/DRAX/en/) · [Deutsch](/DRAX/de/architecture.html) · [Ελληνικά](/DRAX/el/architecture.html) · [Dossier →](/DRAX/en/dossier.html)

# Architecture

> **Status:** Research architecture. Every amount and limit is a planning or test parameter. No production contract or mainnet asset exists.

## 1. One unit rather than four supplies

```text
S(t) = D(t) + P(t) + O(t) + E(t)
S(t) ≤ Mmax
```

- `D`: freely circulating digital bearer outputs;
- `P`: units locked in CashLots for notes and coins in circulation;
- `O`: units locked in OfflineLocks;
- `E`: narrowly defined exceptional states such as verified destruction or disputes.

Every valid transition is intended to satisfy: inputs plus permitted emissions equal outputs plus provable destruction. A wallet, bank or indexer must have no power to widen that invariant.

![Supply model](/DRAX/assets/images/architecture/en/supply-model.png)

## 2. Why this is not a collateralised stablecoin

The public DRAX design is separated from 1kUSD. There is no USD peg, PSM, mint against USDC/USDT/EURC or price oracle in the monetary core. BTC, ETH or gold could later be held in a separate voluntary liquidity or contingency fund, but such holdings would confer no minting right and promise no exchange rate.

This avoids importing a fiat peg into the money supply. The market price of ΔΡΑΧ against EUR, USD, BTC or goods would float. That makes the unit harder, but not automatically stable in purchasing power.

## 3. Kaspa Toccata as the proposed research substrate

Kaspa documentation describes Toccata as UTXO-native. A stateful covenant can validate its own successor when spent. The proposed architecture therefore uses many parallel bearer UTXOs rather than a global account with a mutable balance.

### Covenant families

| Family | Function | Intended immutable core |
|---|---|---|
| Constitution | genesis, `M0`, `Mmax`, schedule, sunset | no post-genesis discretionary mint authority |
| Bearer | split, merge, transfer | no administrative freeze function |
| CashLot | issue, return and destruction of physical cash | no physical nominal value without a digital lock |
| OfflineLock | prefunded offline allocation | no offline value without an on-chain lock |
| Recovery | narrowly scoped dispute states | no global pause or seizure switch |

### External dependencies

- KAS for network fees in the initial design;
- Kaspa consensus, miners and network upgrades;
- Silverscript and compiler maturity;
- wallets, indexers and hardware supply chains;
- market liquidity;
- a tested migration and exit path.

These dependencies rule out any claim of complete technical autarky.

## 4. Linking digital and physical forms

![CashLot cycle](/DRAX/assets/images/architecture/en/cashlot-cycle.png)

1. A legally defined Cash Utility or bank locks `x ΔΡΑΧ` in a CashLot.
2. The covenant provides a publicly verifiable production warrant for a batch.
3. An authorised printer or mint produces no more than the locked nominal amount.
4. After verification, the batch moves to `Issued`; its digital counterpart remains unspendable.
5. Returned notes or coins are authenticated, cancelled and destroyed under control.
6. Exactly `x ΔΡΑΧ` is released digitally only after the destruction proof.

When evidence is uncertain, the digital value remains locked. Liquidity may be delayed, but supply cannot increase. The physical arm remains institutional and needs serial controls, inventories, independent auditors, insurance and criminal counterfeit enforcement.

## 5. Offline payments without false promises

Offline value is prefunded. A user moves ΔΡΑΧ from `D` into an `OfflineLock`; a certified secure element manages bounded transfers until synchronisation.

**Phase-0 test parameters:**

- maximum 150 ΔΡΑΧ per device;
- maximum 50 ΔΡΑΧ per payment;
- maximum three offline hops;
- synchronisation within 72 hours;
- the merchant carries a disclosed residual risk until settlement.

These are not production recommendations. Unlimited trustless offline finality is explicitly not claimed.

## 6. Banking without unlimited money creation

Payment accounts are intended to be backed 100% in ΔΡΑΧ, segregated in insolvency and publicly attested. Credit would be funded by term deposits, bonds, equity or funds whose investors explicitly bear risk. A bank may not create an additional ΔΡΑΧ balance from a payment deposit.

The cost is real: credit may become more expensive and scarce in a crisis. Without an unlimited lender of last resort, liquidity reserves, deposit protection and resolution funds must be prefunded.

## 7. Public verifiability

At least three independently operated indexers should reconstruct total supply, genesis and emission state, CashLot balances, OfflineLock age, Steward-key status and differences between physical registers and on-chain commitments. An indexer is an observer, not the source of truth.

[Law and governance →](/DRAX/en/law-governance.html)

