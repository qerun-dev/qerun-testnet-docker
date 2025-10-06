# Hardhat Workspace (Optional)

This directory is mounted into the container at `/app` so you can run Hardhat tasks against the local Anvil testnet. If you want to execute scripts from the host machine, you can do so with:

```bash
npx hardhat run scripts/<script>.ts --network localhost
```

To execute within the container:

```bash
docker compose exec hardhat-node npx hardhat accounts
```

You can delete this README once you put your own project files here.
