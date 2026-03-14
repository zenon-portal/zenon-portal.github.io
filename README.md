# Zenon Portal v1.5 — Bitcoin Interoperability Blueprint

**Live site: [ebtc.wtf](https://ebtc.wtf)**

## What is this?

A visual explainer for **Zenon Portal v1.5**, a trust-reduced interoperability protocol that connects Bitcoin and Zenon Network. The site presents the full technical blueprint as a scrollable, slide-based document.

## What is Zenon Portal?

Zenon Portal enables Bitcoin holders to participate in the Zenon ecosystem without giving up custody of their BTC to a federated multisig. Instead of moving funds off the Bitcoin base layer, the protocol uses:

- **Taproot escrow scripts** to lock BTC on Bitcoin itself
- **SPV Merkle proofs** to cryptographically verify deposits on Zenon
- **FROST threshold signatures** (t-of-n Schnorr) for coordinated withdrawals
- **eBTC**, a Zenon-native accounting receipt backed 1:1 by base-layer Bitcoin UTXOs

Depositors choose between two escrow models — **Class R** (refund-protected, user retains full control) and **Class P** (pool-liquidity, delegates key-path authority for better UX) — making the security/efficiency trade-off explicit before capital is deployed.

## What the site covers

1. The UTXO → eBTC air-gap architecture
2. Settlement layer vs execution layer separation
3. The deposit → verify → mint → withdraw lifecycle
4. Class R and Class P escrow script trees (Taproot)
5. Security trade-off matrix
6. SPV verification and the genesis checkpoint
7. Relayer system and FROST coordination
8. UTXO consolidation and safety windows
9. Cross-layer withdrawal protocol
10. Economic security via attributable slashing
11. Unilateral refund paths
12. eBTC fungibility and secondary holder risks
13. Where Zenon Portal sits on the trust spectrum

## Source specification

The full technical spec lives at [zenon-developer-commons](https://github.com/TminusZ/zenon-developer-commons/tree/main/docs/specs/Zenon%20Portal).
