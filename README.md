This repo is designed to help validators estimate the fees they would pay to DoubleZero, which are assessed at 5% of block rewards per epoch.

block_rewards_data.csv has historical block rewards data, by pubkey, for epochs 830 - 852. It then computes average block rewards in the second-to-last column and average DoubleZero fees in the last column. A validator can find its pubkey in the file to understand its fees on a historical basis.

In addition, the repo currently has one deep-dive into epoch 842 into all validator earnings. That is, for each active validator in epoch 843, the file earnings_epoch842.csv lists the pubkeys, current commission rates, total inflation earned in epoch 842, total MEV rewards earned in epoch 842, and total block rewards earned in epoch 842. It then also notes the associated DoubleZero fee in the last column.

Please contact nihar@doublezero.us with questions.
[![CI](https://github.com/<owner>/<repo>/actions/workflows/<workflow>.yml/badge.svg)](https://github.com/<owner>/<repo>/actions/workflows/<workflow>.yml)
[![CI](https://github.com/<owner>/<repo>/actions/workflows/<workflow>.yml/badge.svg)](https://github.com/<owner>/<repo>/actions/workflows/<workflow>.yml)
