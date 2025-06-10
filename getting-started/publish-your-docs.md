---
description: >-
  Understand the end-to-end process of creating a sophisticated, cross-protocol
  position in HedgeHogs. This example shows how you can supply collateral,
  borrow against it, and then use the borrowed fund
icon: rocket-launch
---

# Core User Flow

#### **1. Initial Setup**

First, you need to create your personal **HH Proxy** contract and grant it the necessary approvals to act on your behalf.

graph LR\
A\[You] --> B\[HHFactory.createHH()]\
B --> C\[New HH Proxy Deployed]\
C --> D\[Approve Proxy for Aave V3]\
D --> E\[Approve Proxy for Uniswap V3]

This setup ensures that all future actions are securely managed through your single proxy contract.

#### **2. Position Creation Flow**

Once set up, you can create a chain of linked positions across different protocols.

1. **Supply Collateral:** You start by supplying an asset (e.g., ETH) to a lending protocol like Aave V3. This creates your first position, a **Supply Position**.
2. **Borrow Against Collateral:** You then borrow another asset (e.g., USDC) against your supplied collateral. This creates a **Borrow Position**, which is automatically linked as a child of your Supply Position.
3. **Provide Liquidity:** Finally, you can use the borrowed USDC to provide liquidity on Uniswap V3. Using our **Zap feature**, you can deposit the single asset (USDC), and HedgeHogs will automatically swap it for the correct ratio of assets needed for the LP position. This creates a **Uniswap V3 LP Position**, which is linked as a child of the Borrow Position.

#### **3. Final Position Structure**

The result is a sophisticated, linked structure that is easy to manage and automate from your HedgeHogs dashboard.

Supply Position (Aave V3)\
└── Borrow Position (Aave V3) \[child of Supply]\
└── LP Position (Uniswap V3) \[child of Borrow]

From here, you can apply automation strategies to any position in the chain, such as using the fees earned from your LP position to automatically repay your Aave debt.

You can publish your site and find related settings from your docs site's homepage.

<figure><img src="https://gitbookio.github.io/onboarding-template-images/publish-hero.png" alt=""><figcaption></figcaption></figure>

