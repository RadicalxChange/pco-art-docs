# Creator Circles

**Creator Circles** are the individuals or entities that are deemed integral to the creation of a PCOArt work—by providing inspiration and context for the artwork, being implicit in the artwork’s value, and/or participating in producing and maintaining the artwork.

The initial Creator Circle template is a simple unit-based distribution list. The Artist should add the Ethereum address of each desired Creator Circle member to the list and then assign them the number of units.&#x20;

{% hint style="info" %}
Creator Circle units are not tradeable and are simply an accounting/technical disbursement mechanism.
{% endhint %}

Upon the closing transaction of each [Auction Pitch](auction-pitches.md), the resulting Honorarium will be proportionally distributed to each _current_ member of the Creator Circle. Creator Circle membership can be updated (with optional [admin permissions](admin-permissions.md)), but changes will not impact previous distributions.

{% hint style="warning" %}
For technical security purposes beyond the scope of this document, this initial disbursement strategy is implemented by depositing a wrapped version of ETH (identified as ETHx) rather than the _native_ ETH in which bids were placed and paid.&#x20;

Members of Creator Circles will need to execute a one-time `Approval` transaction of their units (this action can be done at any time) and then periodically withdraw (technically: unwrap) their portion of the accumulated Honorarium to their ETH balance.&#x20;

They are able to send & use ETHx if desired, as well.
{% endhint %}

PCOArt is designed modularly top-of-mind. An unlimited number of alternative Creator Circle templates and functionality can be integrated with the core system. Artists and developers may create Creator Circle strategies that include voting, conditional distributions, 3rd-party allocation, etc.
