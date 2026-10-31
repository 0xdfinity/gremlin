# Streak Gremlin

$GREMLIN is a NEAR-native ritual token concept, not a presale. A fixed 0.1 NEAR entry yields 1,000 GREMLIN from ritual allocation; deposits remain contract-held, not a team wallet.

built for the near hackathon memecoins with mechanics track

## Launch rules

10B fixed supply, zero team allocation, 75% ritual, 15% liquidity, 10% reserve. Target: 100 unique accounts daily. Met: distribute 1M from reserve equally. Miss: burn 1M and reset streaks. At streak day 7 burn 1% of account balance, at day 30 burn 3%, no oracle. One check-in per account/day/door (`near` or `intents`); one account counts once across doors. Demo-grade sybil limits, not personhood.

## Treasury

Deposits split immutably: 50% rewards, 30% milestone buyback bucket, 20% permanent burn bucket, rounding remainder to burn. No admin controls. Buyback execution is not implemented; 20% is a NEAR bucket, not token burn. NEAR-native contract door scaffold; `intents` is a label only, no EVM integration. Typed event log covers check-in, resolution, tier burns, treasury splits, transfer.

## Status and quickstart

Prototype adapter models NEP-141 metadata, balance, supply and transfer methods but lacks complete storage registration/transfer-call semantics. Engine Map/Set/BigInt state is not compatible with SDK JSON state serialization, and day is caller-supplied. Thus contract is **not deploy-ready**. No NEP-171 badges yet. Static UI has growing mascot states; testnet id is placeholder. Wallet signing UI remains scaffold. No deployment.

```sh
npm install
npm test
```

Tests compile and exercise deterministic TypeScript logic under Node, not NEAR sandbox. See `docs/SUPPLY_SIM.md` for day-by-day 90%-hit/worst-case simulation. Requires Node 20+, npm and SDK tarball one directory above checkout.
