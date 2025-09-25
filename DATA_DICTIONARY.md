# Data Dictionary

This repository provides two CSV files to help validators estimate DoubleZero fees.

> Fee policy: **5% of block rewards per epoch**.

## 1) `block_rewards_data.csv`
Historical block rewards by validator pubkey for epochs **830–853**.
The file computes:
- the average block rewards (second-to-last column),
- the average DoubleZero fees (last column).

**Columns (expected):**
- `pubkey` — string, validator public key (hex or base58-like, as provided in source data).
- `epoch` — integer, epoch number (e.g., 830 … 853).
- `block_rewards` — numeric, total block rewards for the validator in the given epoch (native units).
- `avg_block_rewards` — numeric, rolling or per-key average across the historical window (second-to-last column).
- `avg_doublezero_fee` — numeric, **5% of avg_block_rewards** (last column).

> Note: If actual column names differ, see README for the exact header row and adjust accordingly.

## 2) `earnings_epoch842.csv`
Deep-dive for **epoch 842**, listing all validator earnings that are active in **epoch 843**.

**Columns (expected):**
- `pubkey` — string, validator public key.
- `commission_rate` — numeric, current validator commission rate (fraction or percent).
- `inflation_rewards_epoch842` — numeric, total inflation rewards earned in epoch 842.
- `mev_rewards_epoch842` — numeric, total MEV rewards earned in epoch 842.
- `block_rewards_epoch842` — numeric, total block rewards earned in epoch 842.
- `doublezero_fee` — numeric, **5% of block_rewards_epoch842** (final column).

## Units and assumptions
- Rewards are expressed in the network’s native units unless otherwise noted.
- DoubleZero fee is computed per-epoch as 0.05 × block rewards of that epoch.
- If a validator does **not** have block rewards in an epoch, the fee for that epoch is 0.

## Notes
- For questions, contact `nihar@doublezero.us`.
- Consider adding a changelog / release tag when new epochs are appended.
