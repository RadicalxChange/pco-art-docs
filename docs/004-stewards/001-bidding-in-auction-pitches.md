# Bidding in Auction Pitches

[English auctions](https://en.wikipedia.org/wiki/English_auction) are one of the most well-known auction types.&#x20;

Bidding starts at a low value and proceeds with ascending, public bids. The highest bid at the end of the auction wins.

PCOArt implements its English auction with a fixed (minimum) duration with optional parameters to extend the auction each time a bid is received within a configurable window. These extension parameters help discourage last-second races to submit the highest/winning bid (an important feature for blockchain-based auctions).

:::info
**Sample Auction Pitch Configuration**\

Auction Start: 12:00 UTC on October 24, 2023&#x20;

Duration: 24 Hours

Starting Bid: 0.001 ETH

Bid Increment: 0.001 ETH

Extension Window: 15 mintues

Extension Time: 5 minutes\

_The first bid received between 11:45 & 12:00 UTC on October 25th would extend the auction until 12:05 UTC. Each subsequent bid when the time left in the auction is less than 15 minutes would extend the auction another 5 minutes._
:::

### Bidding in a PCO English Auction

A bid submitted in PCOArt's English auction has two parts:

1. **Bid Value** - The price a prospective Steward is willing to pay the current Steward to assume control of the license (or in the case of a current Steward's bid, the payment value they'd be willing to forgo to retain control)
2. **Honorarium** - The monetary contribution passed to a work's Creator Circle based on a percentage of their Bid Value

These bids require full collateralization to ensure proper auction closing and funds distribution. For a work's current Steward and new prospective Stewards, this means two different things:

- Current Stewards set their Bid Value like everyone else, but submission of their bid _only requires a deposit of the implied Honorarium_. If the Steward were to win the auction, they wouldn't need to pay themselves, but they always need to contribute to the Creator Circle.
- Prospective Stewards must deposit funds to _cover both their Bid Value and corresponding Honorarium_. These bids are completed with a single, combined transaction. Upon auction close, the split of funds between the previous Steward (Bid Value) and the Creator Circle (Honorarium) happens automatically.

Once bids are submitted, they can be increased at any time with incremental deposits until the auction closes. Only bids that are no longer the highest bid can be canceled and their associated collateral withdrawn.&#x20;

Users will see separate "Locked" and "Available" balances for their collateral on a work's auction page along with the available actions that they can trigger.

:::caution
Not every Auction Pitch allows for open participation. Artists wishing to curate their Stewardship pool may optionally configure eligibility criteria for bidding on the work.
:::

### Closing an Auction

Once the clock on an auction reaches zero, no more bids are accepted. The highest bidder is in line to become the next Steward of the work but does not officially hold this role yet. The auction requires a Close Auction transaction.

This transaction can be executed by _any_ user—the Artist, Steward, bidder, or casual observer. It formally transitions the work from Auction Pitch to Stewardship Cycle by completing the following actions:

- Transferring the associated NFT from the now-former Steward to the winning bidder (if applicable)
- Releasing the winning Bid Value from the winning bidder's Locked Collateral to the former Steward's Available Collateral balance (if applicable)&#x20;
- Transferring the Honorarium from the winning bidder's Locked Collateral to the Creator Circle distribution mechanism
- Scheduling the start of the next Auction Pitch according to the Stewardship Cycle Duration
- Note: No action is taken on the losing bidders' collateral. As they had previously been outbid, they could already cancel and withdraw their bids.
