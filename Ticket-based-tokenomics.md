# Ticket-based tokenomics

## Abstract
I propose a simple ticket-based tokenomics model as a substitute for a present model. It decouples node operators experience from RPL price issues thus stimulating protocol growth, and its simplicity allows for a better RPL price discovery.

## Rationale
Present tokenomics often criticized for the use of RPL token as an artificial requirement, which serves no other purpose than providing a base for RPL valuation, which is used to fund protocol development. At the same time a price of RPL is highly volatile, which creates excess complexity for both node operators and protocol developers, and hence hinders protocol growth. Which in turn makes a fair RPL price discovery hard and is part of the reason behind high volatility.
Simple tokenomics model, that removes RPL price dependence for node operators could better serve the protocol. 

## Model details
The protocol takes a fee from node operators for creating minipools (a _ticket_), this fee is paid in RPL and is burned. RPL is not used as collateral, ETH is used instead (like it is now) and can serve in all cases.

### Ticket price
It has been proposed in the past to consider RPL bond as an entrance ticket for a higher staking yield, however present tokenomics sets a high price for the ticket. Let's propose a fair entrance ticket price as an extra yield from using the protocol (NO APR - solo APR) for 1 year and 32 ETH investment. Currently it's about `2% * 32 = 0.64 ETH`.
This lowers a ticket price by ~4x and creates an incentive for a long-term commitment for node operators.

The ticket price can be lowered gradually with a protocol growth (please, explore a [chart](#numbers-by-examples) below), so that RP could still be attractive for new NOs within increasing competition in the LSP market.

### Inflation and protocol funding
Because RPL is not locked by node operators, the protocol doesn't have RPL rewards, and inflation is reduced to only cover protocol funding (pDAO, oDAO). This is `5% * 30% = 1.5%` RPL inflation.

In the future, when Protocol Owned Liquidity is enough to fund the protocol, inflation can be reduced to 0.

### RPL price impact
RPL price will be determined by a dynamic of new minipools creation. If a number of new minipools is high, RPL burned as a fee can surpass RPL inflation, reducing total RPL available; if the figure is low, then RPL monetary base will grow.

#### Numbers by examples
With current RPL price 0.014 ETH, 20M RPL issued, an equilibrium is this:
```
Annual inflation = 20,000,000 * 1.5% = 300,000 RPL
Number of annual tickets (new minipools) = 300,000 * 0.014 / 0.64 = 6562.5
Annual rETH growth (assuming LEB8) = 6562.5 * 24 = 157,500 rETH
This amounts for ~25% of current minipool/rETH base.
```

With historical numbers of average 15,000 minipools yearly, an equilibrium price is:
```
Annual inflation = 20,000,000 * 1.5% = 300,000 RPL
Total annual fee = 15,000 * 0.64 = 9,600 ETH
Equilibrium RPL price = 9,600 / 300,000 = 0.032 ETH/RPL
```

At protocol maturity with 66% ETH (of 100M total ETH) staked in LSP and 22% self-limit:

Look and play with numbers and a chart here: https://docs.google.com/spreadsheets/d/1-OFUf2phrPr5ewJcUsWzwiepeLg6SGQXvM6ICkU6z9E

#### Hodler / speculator perspective
It can be speculated that after protocol maturity:
- annual new minipools number is quite high to negate low RPL inflation;
- RPL inflation eventually reaches 0;

Hence, RPL becomes deflating asset and grows in price with time.
This assumption can result in removal of a big chunk of RPL from the market, affecting its price.

It's worth noting that while high RPL price does not affect node operators, it constrains further price growth through shifting an equilibrium and inflating an RPL token base.

### Currently staked RPL
These tokens are burned using historical ticket price at the date of each minipool creation. Excess RPL is unlocked.

### Voting eligibility criterium
Voting power is a square root of number of active minipools.

### Protocol fork opportunities
There are none. A fork would have almost the same protocol operational cost with a much smaller user base, so it's impossible to offer competitive ticket fee.
