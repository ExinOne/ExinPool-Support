---
layout: article
title: ExinPool Introduction
---

## Overview

ExinPool is a one-stop liquidity solution for users in the Mixin ecosystem. Currently, it supports the following public chains:

- Mixin Network (XIN)
- Ethereum (ETH)
- Axie Infinity (AXS)
- Solana (SOL)
- Polkadot (DOT)

## What is ExinPool?

ExinPool is a **Staking platform**, more precisely, not an investment platform, but a platform for staking coins to their respective network nodes. The consensus mechanism of these nodes is primarily PoS. After participating in record-keeping:
1. ExinPool receives the rewards distributed by the network
2. These earnings are distributed according to the users' shares
3. The entire process is denominated in coins

## Liquidity Management

ExinPool uses a queuing mechanism to address liquidity. Each coin will have an initial quota set based on the staking requirements of the public chain. The progress of the fundraising will determine whether to increase the fundraising quota.

## XIN Lifecycle Example

Participating in the fundraising for a specific coin (here we take XIN as an example) in ExinPool, XIN will have the following lifecycle:

1. **Initial Stage**: After the user pays for XIN and joins ExinPool
   - Status: XIN is in the queue
2. **Joining Stage**: When the queued XIN reaches the fundraising quota target
   - Status: XIN has successfully joined but is not yet effective
3. **Active Stage**: When the node generates income
   - Status: XIN has successfully joined and is in effect
   - Income is distributed according to the snapshot

## Queue Management

### Joining and Exiting Scenarios

* **Scenario 1**: User A wants to join, User B wants to exit
  - If queue number > 0 and exceeds queued exits:
    - User A enters join queue
    - User B can exit immediately
  
* **Scenario 2**: User A wants to join, User B wants to exit
  - If current queue number < 0:
    - They enter exit queue
    - User A can join
    - User B exits after other users join

> **Note**: Final decisions on joining/exiting depend on queue position and share quantities.

## Liquidity Priority

ExinPool always prioritizes 'liquidity' as the primary consideration. If a node has:
- Excessive queued exits
- No new users joining for a long time
- Expired and retrieved staking

Then a certain amount of sub-nodes or quantity will be dissolved to satisfy user liquidity.

## Exit Fees

- **Queue Exit**: 1 EPC fee required to cancel the queue
- **Active Exit**: Applies when user has successfully joined and generated income

## Earnings Distribution

The coins supported by ExinPool will be snapshotted by default at 8:00 AM Beijing time, and the earnings will be distributed after 15:00 PM Beijing time. The rules for distributing earnings vary across different public chains, so the frequency of snapshotting and sending earnings varies slightly.

## Conclusion

ExinPool is committed to providing a perfect one-stop liquidity solution for users in the Mixin ecosystem. Users participating in ExinPool can also use our other products, such as ExinOne, to solve different transaction scenarios.