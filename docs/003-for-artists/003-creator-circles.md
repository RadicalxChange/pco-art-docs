# Creator Circles

**Creator Circles** are the individuals or entities deemed integral to the creation and ongoing value of a PCOArt work—by providing inspiration and context for the artwork,  participating in producing and maintaining the artwork, and/or contributing implicitly to the artwork's impact.

The initial Creator Circle template that we've created is a simple unit-based distribution list. 

The Artist should add the Ethereum address of each desired Creator Circle member to the list and then assign them the number of units proportional to the desired split of future Periodic Honorarium distributions. Creator Circle units are not tradeable and are simply an accounting/technical disbursement mechanism.

:::info

For example, Alice created a work and wants to include Bob, Charlie, and David in the Creator Circle. She could set it up as follows to reflect different contributions and ongoing involvement in the project:

- Alice (0x123...321): 4 Units
- Bob (0x456...032): 3 Unit
- Charlie (0x987...432): 2 Unit
- David (0x783...521): 1 Unit

Under this configuration, Alice would receive 40% of future Periodic Honorarium distributions, Bob 30%, Charlie 20%, and David 10%. 

:::

Upon the closing transaction of each [Stewardship Inauguration](stewardship-inauguration), the resulting Honorarium will be distributed to each _current_ member of the Creator Circle based on the number of units they hold at that time. Creator Circle membership can be updated (with optional [admin permissions](admin-permissions)), but changes will not impact previous distributions.

:::warning

For technical reasons, the total number of Creator Circle units outstanding must be less than the number of wei (the smallest denomination of ETH) to be distributed after a Stewardship Inauguration. This isn't likely relevant for most collections, but it's recommended to always assign units in the smallest denominations required to achieve your desired distribution. In the Alice example above, using 40, 30, 20, and 10 units would have an order of magnitude more units than necessary.

:::

PCOArt is designed with modularity top-of-mind. An unlimited number of alternative Creator Circle templates and functionality can be integrated with the core system. Artists and developers may create Creator Circle strategies that include voting, conditional distributions, 3rd-party allocation, etc.

:::note
For security purposes beyond the scope of this document, this initial disbursement module is implemented by depositing a wrapped version of ETH (identified as ETHx) rather than the _native_ ETH in which bids were placed and paid.&#x20;

Members of Creator Circles will need to execute a one-time `Approval` transaction of their units (this action can be done at any time) and then periodically withdraw (technically, "unwrap") their portion of the accumulated Honorarium to their ETH balance.&#x20;

They can send & use ETHx if desired, as well.
:::
