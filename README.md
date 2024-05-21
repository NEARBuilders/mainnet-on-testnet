# mainnet-on-testnet

Provides testnet deployments of requested NEAR Accounts.

Uses [bos-workspace](https://github.com/NEARBuilders/bos-workspace).

## Request a testnet deploy

To request an account's mainnet widgets to be deployed to "mainnet-on.testnet", create a pull request with the following changes:

1. From the root, clone the mainnet `yarn bw clone [mainnet account] ./apps`
2. Modify the `bos.config.json` to track aliases from the root directory, and configure the testnet override account to be "mainnet-on.testnet"
3. Create a new release workflow in `.github/workflows` for deploying the added "app"
4. Add the added account to the mainnet and testnet alias jsons -- testnet will be "mainnet-on.testnet", mainnet will be the linked account
