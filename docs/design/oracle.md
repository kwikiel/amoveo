Nakamoto consensus (invented in bitcoin) is a way for the network to make decisions. It incentivizes us to agree, because truth (following largest valid chain) is Schelling point for miners - they could obviosly mine "wrong" chain but in such case they are risking losing already spent computing power which is tied to real world resource - energy. 

Using Nakamoto consensus to answer questions like "Would it be better if block reward was increased?" is possible, but it is very expensive. The users and miners would have to manually answer that question as part of the process of syncing the blockchain. 

We use a market mechanism to allow the disagreement to escalate to the point where Nakamoto consensus can profitably answer the question.

For questions that are in the process of being answered, we store a market in the on-chain state. Market is essentially composed of "yes" and "no" shares, after truth has been discovered one kind of shares becomes worthless. 

To initiate a market - to put motion "for change" initial seeder has to provide liquidity for "yes" shares. 

The market remembers how many shares of each type have been sold, and it remembers what it's initial liquidity was, and it should have an order-book. 

The first order in the book needs to be as big as the initial liquidity.
Every order after that needs to be twice as big as the previous order.

There are 3 possible outcomes for an oracle:
True, False, Bad Question

the result of the oracle is determined by which side of the order book has open orders. If one side has open orders for a long enough period of time, then that side wins. "Long enough" is measured in number of blocks - and it's governance variable as well. 

The initial liquidity can be collected using a [dominant assurance contract](/docs/use-cases-and-ideas/dominant_assurance_contract.md) in a [market](/docs/use-cases-and-ideas/trustless_markets.md).

[to see the short and clear cryptoeconomic explanation for why this oracle will work, look at the bottom of the white paper](/docs/white_paper.md)

Oracles are stored in one of the consensus state merkle trees. [read more about these trees here](trees.md)

[motivations that lead to this oracle design](oracle_motivations.md)

[Explaining the oracle from a different perspective](oracle_simple.md)
