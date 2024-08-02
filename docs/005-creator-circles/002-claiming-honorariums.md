# Claiming Honorariums

## About Honorarium Balances
After your address is added to a Creator Circle, you'll begin receiving proportional payouts of all collected Periodic Honorariums automatically in a wrapped version of the ETH identified as ETHx. ETHx is a [Super Token](https://docs.superfluid.finance/docs/concepts/overview/super-tokens) on the Superfluid protocol. It has extra features that traditional tokens don't, like the ability to be natively streamed and distributed to an arbitrary number of addresses gas efficiently (which is why it's used in this PCOArt Module). You can check out [Superfluid's docs](https://docs.superfluid.finance/docs/concepts/superfluid) for more information.

## Checking Units and Balances
Every PCOArt collection has a publicly accessible Creator Circle page linked from its token pages.

![Creator Circle](https://github.com/user-attachments/assets/f40064e8-77fc-4647-95de-6237f222a203)

By design, anyone can see the current configuration and to-date payouts of a Creator Circle from this page. If you're a member of the Creator Circle, you'll also see the several ways to interact with the Creator Circle and your Honorarium Balance.

### Approving Distribution Units
While your Honorarium balance is already safely allocated to your address without any action, there is a one-time `connectPool` transaction per Creator Circle required to see your token balance updated in real-time. You can complete this transaction by clicking the **Approve Units** button next to your address in the Creator Circle Allocation Table and executing the transaction. 

If you don't complete this transaction, your past and future Honorariums are still safe, but you'll have to claim them periodically to see them reflected in your balance.

### Withdraw to ETH
ETHx and ETH are redeemable 1:1 (every ETHx token corresponds to a locked ETH in the Superfluid protocol contracts), but to your wallet (and exchanges!!!) they are distinct tokens. 

You can withdraw ETHx funds to ETH anytime on a Creator Circle page you're a member of or through the [Superfluid App](https://app.superfluid.finance/). Make sure to do this before trying to deposit your Honorarium to an exchange or another app expecting native ETH.

:::tip

You can add ETHx to your wallet (if it's not detected automatically) by copy/pasting these contract addresses into your wallet's Add Token feature:

- [Base ETHx](https://basescan.org/address/0x46fd5cfb4c12d87acd3a13e92baa53240c661d93) - 0x46fd5cfb4c12d87acd3a13e92baa53240c661d93
- [Optimism ETHx](https://optimistic.etherscan.io/address/0x4ac8bd1bdae47beef2d1c6aa62229509b962aa0d) - 0x4ac8bd1bdae47beef2d1c6aa62229509b962aa0d

:::
