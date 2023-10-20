---
sidebar_position: 3
id: API
title: API
sidebar_label: API
---
# API Reference

## `moonWallet`

The `moonWallet` function provides a custom connector for the RainbowKit library, which allows you to interact with the Wagmi API using the Moon provider.

### Signature

```typescript
function moonWallet(options: MyWalletOptions): Wallet;
```

### Parameters

- `options` (`MyWalletOptions`): An object containing the `chains` array and the `options` object.

### Returns

- `Wallet`: A `Wallet` instance that can be used to interact with the Wagmi API using the Moon provider.

### Example

```typescript
import { moonWallet } from '@moonup/moon-rainbowkit';
import { Chain } from '@rainbow-me/rainbowkit';

const chains: Chain[] = [{ chainId: 1, name: 'Ethereum', network: 'mainnet' }];

const wallet = moonWallet({
  chains,
  options: {
    rpcUrl: 'https://rpc.moonup.com',
  },
});

async function main() {
  const connector = wallet.createConnector().connector;
  await connector.connect();
  console.log('Connected to Moon provider');
}

main();
```

In this example, we import the `moonWallet` function from the `@moonup/moon-rainbowkit` library and the `Chain` type from the `@rainbow-me/rainbowkit` library.

We create an array of `Chain` objects that represent the Ethereum mainnet.

We then create a new instance of the `Wallet` class using the `moonWallet` function with a configuration object that contains the `chains` array and the URL of the Moon RPC endpoint.

We call the `createConnector` method of the `Wallet` instance to create a new `MoonConnector` instance. We then call the `connect` method of the `MoonConnector` instance to connect to the Moon provider. We log a message to the console indicating that we have connected to the Moon provider.

Note that we import the `moonWallet` function from the `@moonup/moon-rainbowkit` library and the `Chain` type from the `@rainbow-me/rainbowkit` library. We also use the `createConnector` method of the `Wallet` instance to create a new `MoonConnector` instance and the `connect` method of the `MoonConnector` instance to connect to the Moon provider.
