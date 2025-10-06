# Qerun Testnet Docker

Simple Docker Compose setup for running a local Ethereum testnet (Anvil) to develop and test Qerun contracts.

## Prerequisites
- Docker 24+
- Docker Compose v2

## Usage
```bash
docker compose up -d
```
This starts an Anvil instance on `http://localhost:8545` with chain ID `1337`.

### Interacting with Hardhat
The `hardhat/` directory is mounted into the container at `/app`. You can:

```bash
# From host
docker compose exec hardhat-node npx hardhat accounts
```

Or run scripts against the local node:
```bash
npx hardhat run scripts/deploy.ts --network localhost
```

## Stopping
```bash
docker compose down
```

## Customisation
- Modify `docker-compose.yml` to add additional services (e.g., block explorer, indexer).
- Put your Hardhat project files inside `hardhat/`.

