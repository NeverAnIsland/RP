# (optional) Separation of roles for RPL owners and ETH owners

This is similar to no-RPL-bonded minipools idea, but different in some ways 👇

## Minipools stay the same
in the sence that they MUST consist of staked ETH and a bonded RPL to initialize and operate.

## Minipools change
because either ETH part or RPL part is provided by a NO depending on implementation.

### ETH-centric minipools and RPL pool
- node is registered by a person holding ETH
- RPL is borrowed from a RP operated RPL pool (like AAVE RPL pool but RP operated)
  - RPL pool is where RPL holders can deposit and benefit from the access to RPL inflation and a part of ETH comission
    - RPL inflation goes to the pool (calculated as always, individually for every node, depending on its collateral level)
- minipool ETH comission is divided into 3 parts
  - 1 part goes to NO
  - 1 part to RPL pool
  - 1 part to rETH contract (can be 0 at start)
  - shares can vary and are set by pDAO

### RPL-centric minipools and ETH pool (this is opposite to a previous and can utilize RPIP-32: Stake ETH on behalf of node)
- node is registered by a person holding RPL
- ETH is borrowed from a RP operated ETH pool
  - ETH pool is similar to AAVE pool where ETH holders can deposit and benefit from
    - rewards from staking
    - part of ETH commission
- minipool ETH comission is divided into 3 parts
  - 1 part goes to NO
  - 1 part to ETH pool
  - 1 part to rETH contract (can be 0 at start)
  - shares can vary and are set by pDAO

### Extreme version of RPL-centric minipools? 🤔
- All 32 ETH for minipools is taken from a deposit pool
- rETH gets higher APR
- this would require a much bigger RPL bond as collateral
- it makes it possible to lower RPL inflation, because RPL holders get way too much profit

## Voting right
is always given to RPL holder bonding to a node (in RPL-centric approach a voting can be implemented though a RPL pool vault, which accounts for RPL utilization to calc exact voting power).

Rationale? RPL holders are aligned with RPL and hence with RP the most, while ETH holders can use a variety of staking options.

## Numbers

### ETH-centric
TODO.

### RPL-centric
TODO.

### Extreme RPL-centric
Input: LEB8-like minipool, RPL collateral is 8 ETH worth of RPL.

With current PRL price `0.014` it would take `26,000 * 8 / 0.014 ~= 14,860,000` RPL to run all existing `26,000` minipools, or about 75% of current RPL supply.

For currently staked `10,140,000` RPL an equilibrium price would be `26,000 * 8 / 10,140,000 = 0.02`.

At the maturity, where 24M of RPL supply is staked, 66% of 120M ETH is staked and 22% of staked ETH is locked in RP, RPL price would be `120,000,000 * 0.66 * 0.22 / 32 * 8 / 24,000,000 = 0.18`.
