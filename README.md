# MEV BOT Codebase written in Python, Javascript, and Rust

Current codebase includes **DEX flashloan arbitrage strategy** as a starting point. It is a simple demonstration and will need some tweaking to make it work (mostly in regards to order size optimization and gas bidding strategy), though it will work as a real DEX arbitrage bot by doing the following:

- Retrieving all historical events from the blockchain (PairCreated).

- Create a triangular arbitrage path with all the pools retrieved from above.

- Perform a multicall request of "getReserve" calls to all the pools we're trading (1 ~ 3 second to retrieve >=6000 pools).

- Stream new headers, new pending transactions, events asynchronously.

- Simulate Uniswap V2 3-hop paths offline.

- Sign transactions and create bundles to send to Flashbots (also supports sending transactions to the mempool).

For business inquiries, e-mail me directly at: slothbucksdev@gmail.com
