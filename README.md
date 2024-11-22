### Renegade Token Mapping
This repo holds token mappings for various networks and chains onto which Renegade is deployed.

There is a separate mapping for each environment (e.g. Arbitrum testnet, Arbitrum mainnet) to which the Renegade protocol is deployed.

The schema for the token mapping object is as follows, using the testnet USDC token as an example:
```javascript
{
"tokens": [
  {
    /* The token name */
    "name": "USD Coin",
    /* The token ticker (symbol) */
    "ticker": "USDC",
    /*
     * The address at which the token is deployed for the given environment.
     * Note that these are _Arbitrum_ environments.
     */
    "address": "0xdf8d259c04020562717557f2b5a3cf28e92707d1",
    /*
     * The number of decimals used in the fixed-point representation
     * of the token.
     */
    "decimals": 6,
    /*
     * A (non-exhaustive) mapping of exchanges which list the token.
     * For each exchange, we map to the ticker listed on the exchange which
     * results in the highest-quality prices for the token.
     */
    "supported_exchanges": {
      "Binance": "USDC",
      "Coinbase": "USD",
      "Kraken": "USD",
      "Okx": "USDC"
    },
    /*
     * A mapping from chain ID -> address at which the token is deployed
     * to on that chain.
     */
    "chain_addresses": {
      "1": "0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48",
      "1151111081099710": "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v"
    },
    /* The URL at which the token's logo is hosted */
    "logo_url": "https://raw.githubusercontent.com/renegade-fi/token-mappings/refs/heads/main/testnet-token-logos/usdc.png"
  }
  // ...
]
}
```