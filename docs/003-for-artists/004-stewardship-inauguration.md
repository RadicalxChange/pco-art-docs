# Stewardship Inaugurations

_**Stewardship Inaugurations**_ are the periodic ritual for the artwork to enter and re-enter circulation, thereby allowing Stewards to either recommit or for the artwork to pass to a subsequent Steward.

The first Stewardship Inauguration module implemented uses an extending English auction format. This type of auction opens with a low initial bid and accepts increasingly higher bids. The highest bid at the end of the auction time wins. The PCOArt implementation sets an initial auction length that can be configured to automatically extend if a new bid is received within a designated period at the end of the auction. This helps eliminate the incentive to sneak in last-second winning bids.&#x20;

:::tip
Other Stewardship Inauguration formats such as [Dutch](https://en.wikipedia.org/wiki/Dutch_auction), [Vickery](https://en.wikipedia.org/wiki/Vickrey_auction), and continuous auctions can be integrated into the PCOArt system. Mechanisms that use social and other non-finanical factors to effect ownership transfer can be considered as well.

Each option will have a different user experience, technical complexity, and dynamics tradeoffs to fit Artist needs.
:::

Regardless of type or configuration, the Stewardship Inauguration module always should produce the following actions:

1. The winning bidder assumes Stewardship of the work (or maintains it if the previous Steward wins the auction).
2. The Periodic Honorarium is released to the Creator Circle.
3. The winning bid proceeds are released to the previous Steward.
   - If the previous cycle's Steward wins the Stewardship Inauguration, they don't "pay themselves."

:::info
By default, the winning bid proceeds of a work's initial auction will be released to the Artist. They are the "previous Steward" in this scenario. If an Artist wants to allocate the initial auction proceeds elsewhere (like to a Creator Circle member), they can select the option to mint tokens at creation and transfer the work(s) to the desired wallet address before the initial auction.&#x20;
:::

## Configuring an extending English auction

While PCOArt is not focused on maximizing auction prices, Stewardship Inaugurations should be configured to promote participation and avoid "surprise" results.&#x20;

Artists can set their **Initial Stewardship Inauguration Date** to any future time that allows sufficient time to raise awareness, help onboard Creator Circle members, etc.&#x20;

Artists that wish to launch their PCOArt without a standard Stewardship Inauguration can set the initial Stewardship Inauguration date to the equivalent of one Stewardship Cycle into the future and manually transfer the token to the desired initial Steward (e.g. an offline auction winner). 

PCOArt that is created as part of a collection can utilize a **Collection Offset** so that individual Stewardship Inaugurations are staggered by a fixed period (e.g. a 1-day offset could be used to release a collection of 7 with an Stewardship Inauguration starting at 12:00 UTC each day of the week).

The remaining English Auction Configuration fields are likely familiar:

- **Auction Duration** (can be extended)
- **Starting Bid** (set to any number greater than 0)
- **Minimum Bid Increment** (must be set greater than 0 to ensure that bids actually increase)
- **Extension Window** (bids within this period will extend the auction)
- **Extension Length** (how much time each bid during the extension window adds)

:::info
A work's next Stewardship Inauguration start time is set based on when the previous one is closed.&#x20;

Closing an English Stewardship Inauguration requires a manual transaction that _any user_ can trigger after the Stewardship Inauguration clock has reached zero.&#x20;

A Steward will always receive their full Stewardship Cycle, so Stewardship Inauguration extensions or other delays in closing the Stewardship Inauguration will result in a "drift" in the next Stewardship Inaugurationn's start time relative to other works in the collection.
:::
