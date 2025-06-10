---
icon: triangle-exclamation
---

# Impermanent Loss

## What is Impermanent Loss(IL)?

When you provide liquidity to an ETH/USDC pool, you can choose a price range, such as $1,500 – $2,500.&#x20;

* If ETH stays **within this range**: Your liquidity remains active, and you earn fees from trading.&#x20;
* If ETH moves toward the **high end ($2,500)**: You start holding more USDC and less ETH as the pool rebalances.
* If ETH moves toward the **low end ($1,500)**: You start holding more ETH and less USDC.&#x20;
* If ETH moves **outside your range**: Your liquidity is fully converted into one asset (all ETH at the bottom or all USDC at the top), and you stop earning fees.&#x20;

### **Why is This a Risk for Liquidity Providers?**

* You can still earn trading fees that offset IL.
* But if the price moves too much, IL can outweigh earnings—especially in volatile markets.

IL is most dangerous when:

* You provide liquidity to highly volatile asset pairs (e.g., ETH/MEMECOIN).
* The pool has low trading volume, meaning fewer fees to compensate for IL.
* You withdraw when asset prices are diverged, making the loss permanent.

### **When Does IL Become Permanent?**

IL remains "impermanent" as long as prices can revert. However, if you exit the pool while the price is still diverged, the loss is locked in.

#### **Key Takeaway: IL is Manageable but Must Be Watched**

IL is unavoidable in AMMs, but it's not always bad! If trading fees are high enough, they can offset IL and make liquidity provision very profitable. The goal is to keep price movements within a profitable range where fees outpace IL—which is where hedging strategies come in!
