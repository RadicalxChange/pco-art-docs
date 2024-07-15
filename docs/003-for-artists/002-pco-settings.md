# PCO Settings

A PCOArt Stewardship License at its core is defined by two variables:

- **Stewardship Cycle Duration**
- **Honorarium Rate**

The values that you set can change the relationship between your art, Stewards, and Creator Circle.

A **Stewardship Cycle** is the period in which a Steward is granted the right to possess, exhibit, and/or benefit from other rights relating to the artwork and its context(s). From a technical perspective, the Stewardship Cycle Duration determines the length of time between [Auction Pitches](auction-pitches) for your art.

You can set any duration consistent with the nature of the art, your goals, and practical considerations (e.g. installation/transport requirements). The longer the Stewardship Cycle, the more similar the market dynamics will be to traditional private ownership (Private ownership is effectively an indefinite Stewardship Cycle!).

The **Honorarium Rate** is the required percentage of a winning Auction Pitch bid that the Steward makes to the Creator Circle at the beginning of each Stewardship Cycle.&#x20;

:::tip

Winning  Bid  * Honorarium Rate = Periodic Honorarium$

:::

Lower Honorarium Rates will tend to lead to higher nominal Auction Prices: the capital commitment required of the Steward each cycle is lower given a valuation. A 0% Honorarium Rate effectively would mimic the dynamics of private ownership (with a periodic auction in which the Steward could set an arbitrarily high reserve price). The theoretically optimal rate to maximize the total Periodic Honorarium collected is equal to the probability that a new Steward emerges who values the work more than the current Steward (e.g. 1 new Steward in every 10 periods implies a 10% optimal rate). Revenue maximization isn't always the priority (and the theoretical turnover probability is likely difficult to determine), so don't get hung up on getting it "perfect." Set a rate that *feels right* for your art, community, and the dynamic you're attempting to create. 

The current implementation supports static rates (with [optional permissions](admin-permissions) to update them), but in the future, rates could be set dynamically or via an oracle that factors in market data like turnover rates.&#x20;

:::info
**Note: The Honorarium Rate is applied on a per-cycle basis and not as an annualized rate.**

A 3% Honorarium Rate paired with a 6-month Stewardship Cycle would produce the equivalent Honorarium to 6% with a 1-year cycle, all else equal.

These cycle durations may produce different Stewardship dynamics, however! &#x20;
:::
