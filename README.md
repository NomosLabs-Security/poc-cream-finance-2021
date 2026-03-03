# CREAM Finance Flash Loan Exploit — PoC

> **Educational Purpose Only** — This PoC is created for security research and education
> purposes only. It runs against a fork, not mainnet.

## Quick Start

```bash
git clone https://github.com/NomosLabs-Security/poc-cream-finance-2021
cd poc-cream-finance-2021
forge install foundry-rs/forge-std --no-git
forge test -vvvv
```

## Details

- **Exploit Date:** 2021-10-27
- **Fork Block:** #13499798
- **Expected Output:** Flash loan re-enter via crETH, price manipulation via yUSD collateral
- **Full Analysis:** [NomosLabs Security Intelligence Archive](https://nomoslabs.io/archive/cream-finance-2021)

## Description

CREAM Finance's third exploit used a flash loan to manipulate the price of yUSD
(a Yearn vault token used as collateral). The attacker:

1. Flash-borrowed a large amount of ETH
2. Minted crYUSD by depositing manipulated yUSD
3. Inflated yUSD price by depositing into underlying Yearn vault
4. Borrowed all available assets against inflated crYUSD collateral
5. Drained $130M from the protocol

## RPC Providers

```
Alchemy:   https://eth-mainnet.alchemyapi.io/v2/YOUR_KEY
Infura:    https://mainnet.infura.io/v3/YOUR_KEY
QuickNode: https://YOUR_ENDPOINT.quiknode.pro/YOUR_KEY
```

## License

MIT — For educational use only.
