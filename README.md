<p align="center">
  <img src="https://www.mewccrypto.com/meowcoin.png" alt="Meowcoin Logo" width="150"/>
   <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Plus_symbol.svg/1707px-Plus_symbol.svg.png" alt="Plus Symbol" width="100"/>
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQo4umyYNRbBrKW7BYl3-DHwIbYj59CwBcumw&s" alt="Litecoin Logo" width="150"/>
</p>


# Meowcoin AuxPoW + Dual-PoW Upgrade: Test & Status Repo

**This repo tracks the current testing status of the Meowcoin AuxPoW + Dual-PoW chain upgrade.**  
All work and results are visible so the community can see exactly where things stand.  
Status will be updated as testing progresses through internal and public testnets.

## What Is Happening?

Meowcoin is preparing a major consensus upgrade to support **Auxiliary Proof-of-Work (AuxPoW)** alongside the existing MeowPoW algorithm.  
This will enable **merge-mining** with other Scrypt-based coins (like Litecoin, Dogecoin, Bellscoin) while retaining MeowPoW for GPU/ASIC resistance and community mining.

Key highlights of this upgrade:

- **Dual-PoW:** Meowcoin will accept both MeowPoW and Scrypt (AuxPoW) blocks, targeting a 50/50 split.
- **Merge Mining:** Pools and miners will be able to earn Meowcoin by merge-mining alongside Litecoin/Dogecoin with no loss of efficiency.
- **Fair Difficulty:** Uses LWMA difficulty adjustment to ensure neither algorithm dominates and rewards stay balanced.
- **Assets Remain Supported:** The Ravencoin-based asset system continues to work, both before and after the upgrade.
- **No Chain Split:** Existing chain data, balances, and assets are preserved and compatible with the new rules.
- **Open Testing:** This repo will transparently document every test and its status, so anyone can see what’s working and what needs more work.

## How to Use This Repo

- Check the current progress on core upgrade and integration tests.
- Follow along with internal, public testnet, and (eventually) mainnet rollout phases.
- See what areas are being tested, and what still needs attention.

## Status Legend

🔲 Not Started  🟡 In Progress  🟢 Complete  🟠 Blocked/Needs Help

## Test Matrix

| Status | Task                                                                 | Notes |
|:------:|:---------------------------------------------------------------------|:------|
| 🔲     | Sync node from genesis (legacy blocks)                               |       |
| 🔲     | Validate legacy blocks with AuxPoW-enabled node                      |       |
| 🔲     | AuxPoW activates at correct block/time                               |       |
| 🔲     | MeowPoW block acceptance after activation                            |       |
| 🔲     | AuxPoW (Scrypt) block acceptance after activation                    |       |
| 🔲     | 50/50 split: AuxPoW and MeowPoW enforced over time                   |       |
| 🔲     | LWMA retarget logic (difficulty) works as expected                   |       |
| 🔲     | Asset creation, transfer pre- and post-AuxPoW                        |       |
| 🔲     | Asset transfer under high network load                               |       |
| 🔲     | Wallet: rescan, recovery, key import (pre-/post-upgrade)             |       |
| 🔲     | UTXO set: consistency checks after upgrade and reindex               |       |
| 🔲     | Clean node upgrade from previous version                             |       |
| 🔲     | Stratum pool testing(AuxPoW, Scrypt)                                 |       |
| 🔲     | MeowPoW pool mining                                                  |       |
| 🔲     | Dual mining: concurrent Scrypt (AuxPoW) and MeowPoW                  |       |
| 🔲     | Litecoin pool merged mining with Meowcoin                            |       |
| 🔲     | Wallet compatibility (legacy and new)                                |       |
| 🔲     | Legacy wallet.dat loads                                              |       |
| 🔲     | RPC: all consensus/mining/asset calls work for both block types      |       |
| 🔲     | getblocktemplate returns correct for both mining algos               |       |
| 🔲     | getblock, getblockheader, getrawtransaction, etc, on new block types |       |
| 🔲     | Reorg handling with mixed block types (AuxPoW/MeowPoW, assets)       |       |
| 🔲     | Network performance under mining load                                |       |
| 🔲     | Sync and operation on low-end/old hardware                           |       |
| 🔲     | All RPC error codes correct (legacy/new edge cases)                  |       |
| 🔲     | Manual code review: consensus diffs                                  |       |

## High Level Objectives

| Status | Task                                                                 | Notes |
|:------:|:---------------------------------------------------------------------|:------|
| 🔲     | Define Mainnet Activation                                            |       |
| 🔲     | Prepare Electrum Changes                                             |       |
| 🔲     | Release Mainnet Core Wallet v3.0.0                                   |       |

## Current Status

**All items are pending initial smoke and regression testing.**  
First phase: closed/internal testnet  
Next: public testnet  
Mainnet activation follows after broad validation.

*This file will be updated regularly as work is completed and testing moves forward.*
