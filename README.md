# cycer-deployment

[![cycer-deployments on npm](https://img.shields.io/npm/v/curie-deployments?style=flat-square)](https://www.npmjs.com/package/curie-deployments)

`cycer-deployments` contains the contract artifacts and metadata (deployed addresses) of all contracts in [cycer](https://cycer.io/).

## Contract Source Code

- [cycer-contract](https://github.com/cycer/cycer-contract)
- [cycer-periphery-contract](https://github.com/cycer/cycer-periphery-contract)
- [cycer-oracle-contract](https://github.com/cycer/cycer-oracle-contract)

## Contract Artifacts and Metadata

The folder structure of this package:

```bash
node_modules/cycer-deployments/
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

When using `git+ssh://git@github.com:cycer/cycer-xxx.git#GIT_COMMIT_SHA` to deploy contracts, **every time we deploy**, we must increase the version of `package.json` in `cycer-xxx` to avoid version conflicts of yarn install. For instance, change to `2.0.0-rc1`, `2.0.0-rc2` and so on. Otherwise, yarn might not install the correct version.

## Yarn Install
Please use `yarn --network-concurrency 1` to install packages.
You may encounter problem such as `ENOENT: no such file or directory...` if using `yarn` directly.
