# perp-curie-deployment

[![@perp/curie-deployments on npm](https://img.shields.io/npm/v/@perp/curie-deployments?style=flat-square)](https://www.npmjs.com/package/@perp/curie-deployments)

`@perp/curie-deployments` contains the contract artifacts and metadata (deployed addresses) of all contracts in [Perpetual Protocol Curie (v2)](https://perp.com/).

## Contract Source Code

- [perp-curie-contract](https://github.com/perpetual-protocol/perp-curie-contract)
- [perp-curie-periphery-contract](https://github.com/perpetual-protocol/perp-curie-periphery-contract)
- [perp-oracle-contract](https://github.com/perpetual-protocol/perp-oracle-contract)

## Contract Artifacts and Metadata

The folder structure of this package:

```bash
node_modules/@perp/curie-deployments/
├── optimism/
│   ├── core/
│   │   ├── artifacts/
│   │   │   └── contracts/
│   │   ├── dependencies.json
│   │   └── metadata.json
│   ├── periphery/
│   │   ├── artifacts/
│   │   │   └── contracts/
│   │   ├── dependencies.json
│   │   └── metadata.json
│   └── liquidity-mining
│       ├── artifacts/
│       │   └── contracts/
│       ├── dependencies.json
│       └── metadata.json
├── optimism-goerli
    └── ...
```

You could find the deployed contract addresses inside `metadata.json` under each network.

## Package Versions

If possible, it's recommended to publish a new npm version first and use that version to deploy contracts.

When using `git+ssh://git@github.com:perpetual-protocol/perp-xxx.git#GIT_COMMIT_SHA` to deploy contracts, **every time we deploy**, we must increase the version of `package.json` in `perp-xxx` to avoid version conflicts of yarn install. For instance, change to `2.0.0-rc1`, `2.0.0-rc2` and so on. Otherwise, yarn might not install the correct version.

## Yarn Install
Please use `yarn --network-concurrency 1` to install packages.
You may encounter problem such as `ENOENT: no such file or directory...` if using `yarn` directly.
