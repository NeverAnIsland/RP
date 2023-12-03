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
is always given to RPL holder bonding to a node (in the case of RPL pool it is unclear how to provide it).
