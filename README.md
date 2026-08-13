# Avail Emission Control

An interactive model of Avail's validator economics — tune the levers of issuance, validator set size, commission, treasury split, token price and more, and watch validator profitability, emissions, and the reward split update instantly.

Built as a decision-support / demo tool for evaluating how to reduce token issuance while keeping validators sustainable.

## What it shows

- **Total minted / day & effective inflation** under a dynamic reward curve (today's model) or a Polkadot-style fixed-issuance model that auto-decays.
- **Per-operator income** vs server cost, with a live Profitable / Unprofitable indicator.
- **Where the emission goes** — operators vs nominators (~74% Foundation) vs Treasury.
- **Per-operator income vs token price** and **effective inflation over 10 years**.
- A full before/after breakdown table vs today's baseline.

## Levers

Emission model (dynamic curve / fixed issuance), fixed issuance rate, active validator count, commission (capped at 20% per AIP-8), treasury split, a fixed per-validator reward "escape hatch", AVAIL price, and monthly server cost.

## Preset scenarios

Today (status quo) · Recommended · Aggressive cut · Deep cut + fixed reward · Stop inflation.

## Data

Baseline figures were measured on-chain (Avail mainnet, era 768) and from the runtime:
total issuance ~11.09B AVAIL, ~4.69B staked (42.3%), 80 validators, 24h eras,
reward curve (min 1% / max 5% / ideal 50%), ~74% of nominator stake in Foundation-program
accounts, self-bond ~0.48%, and negligible transaction-fee revenue (~126 AVAIL/day to validators).

## Run locally

It's a static site — no build step. Just serve the folder:

```bash
python3 -m http.server 8099
# open http://localhost:8099
```

Chart.js is bundled locally (`chart.umd.min.js`), so it works fully offline.
