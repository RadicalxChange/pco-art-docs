# Admin Permissions

The PCOArt smart contracts do not have a centralized administrator.

Each current functional module (e.g. the v1 Extending English Auction) is deployed as an immutable instance.&#x20;

This does not mean that PCOArt collections are necessarily immutable though. We leave that decision up to the Artist. &#x20;

The PCOArt system offers two tiers of administrative permissions for each collection that Artists can retain, permanently relinquish, or delegate:

## 1. Collection Admin

This role is the "super admin" of the token collection.&#x20;

It retains the ability to change the designated smart contract address for _all_ modules leveraged in the collection system. This means the Collection Admin can effectively rewire the logic of core PCO functionality and indirectly update the configuration of components even if the Component Admin role is assigned to another address.

The Collection Admin can also reassign these second-tier admin roles at any time.

Operational security and care in exercising this power are tantamount to the ongoing viability of a PCOArt work. Artists may consider assigning this role to a multi-signature account.&#x20;

The primary reason for creating this role is to provide a method to gracefully respond to potential bugs/security flaws in the PCOArt contracts (or in the positive case, incorporate great new functionality!).&#x20;

This is especially important during the early public usage of the system. We've used battle-tested components like ERC-721 and tested and tested novel functionality we've developed, but bugs happen.

Should an issue with the deployed smart contracts arise, the PCOArt team and/or community can deploy a backward-compatible, patched version of the affected module and then work with Artists to migrate their collections to the new contracts as appropriate.

:::info
An admin can relinquish the role anytime by assigning the role to a "burn" address that can't be accessed (e.g. 0x000000000000000000000000000000000000dEaD).

Losing access to an admin wallet is the accidental equivalent!
:::

## 2. Component Admins

Each Component Admin permission has isolated control of the _configuration_ of a functional module, but not the ability to swap out the entire contract.&#x20;

This lowers the implied reach of administrative power, but configuration changes can still be very impactful on a PCOArt work implementation.&#x20;

The current Component Admin roles and their abilities follow:

- **Role Admin** - can change the address(es) assigned to other Component Admin roles
  - All changes will take immediate effect 
- **PCO Settings Admin** - can change the Stewardship Cycle Duration and the Honorarium Rate
  - Changes to either field will be applied to the _next_ Stewardship Cycle/Auction Pitch
- **Auction Pitch Admin** - can change all attributes of the collection's Auction Pitches (except for the initial auction date)
  - All changes will take immediate effect, including if an auction is in progress (exercise caution!)
- **Auction Pitch Eligibility Admin** - can flip between open or closed eligibility and update the eligibility criteria
  - All changes will take immediate effect
- **Creator Circle Admin** - can change Creator Circle membership units including removing/adding members
  - Changes will be applied when the next Auction Pitch is closed
- **Mint Additional Tokens Admin** - can add new tokens to a collection after the initial creation event
  - New tokens will be added to the collection sequentially and initial auction times will be set based on the existing offset (including setting an auction in the past).&#x20;

:::info
We've implemented the Configuration Admin abilities to try to avoid unexpected consequences that violate Steward expectations (e.g. if you change the Stewardship Cycle Duration, it won't shorten/lengthen the current Steward's period).&#x20;

But, just because you _can_ make a change, doesn't necessarily mean that you always _should_. Exercise caution!
:::