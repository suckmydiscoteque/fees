# Example Usage

This example shows how to verify validator fees and block rewards.

---

## Step 1. Locate your validator pubkey
Each CSV file contains a column `pubkey` with the validator's public key.  
Search for your own validator pubkey in the file.

---

## Step 2. Find block rewards
From the file `block_rewards_data.csv`:
- `block_rewards`: total rewards for the validator in the given epoch.  
- Example: `block_rewards = 1000`.

---

## Step 3. Apply fee formula
The DoubleZero fee is defined as:
doublezero_fee = block_rewards * 0.05
```For the example above:```
doublezero_fee = 1000 * 0.05 = 50

---
## Step 4. Cross-check with `earnings_epochXYZ.csv`
In the `earnings_epochXYZ.csv` file:  
- Look for your `pubkey`.  
- Compare the column `doublezero_fee` with the calculated value.
