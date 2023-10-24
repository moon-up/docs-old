---
sidebar_position: 4
id: example 
title: Example 
sidebar_label: Example 
---


# Example

Here is an example of how you can use the `@moonup/moon-rainbowkit` library to interact with the Wagmi API using the Moon provider:

```typescript
import { moonWallet } from '@moonup/moon-rainbowkit';
import { Chain } from '@rainbow-me/rainbowkit';
import { MoonApi } from '@moonup/moon-api';
import { AccountResponse } from '@moonup/types';

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

  const moonApi = new MoonApi({
    connector,
  });

  const account: AccountResponse = await moonApi.getAccount('0x1234567890123456789012345678901234567890');
  console.log(account);
}

main();
```

In this example, we import the `moonWallet` function from the `@moonup/moon-rainbowkit` library, the `Chain` type from the `@rainbow-me/rainbowkit` library, the `MoonApi` class from the `@moonup/moon-api` library, and the `AccountResponse` type from the `@moonup/types` library.

We create an array of `Chain` objects that represent the Ethereum mainnet.

We then create a new instance of the `Wallet` class using the `moonWallet` function with a configuration object that contains the `chains` array and the URL of the Moon RPC endpoint.

We call the `createConnector` method of the `Wallet` instance to create a new `MoonConnector` instance. We then call the `connect` method of the `MoonConnector` instance to connect to the Moon provider. We log a message to the console indicating that we have connected to the Moon provider.

We create a new instance of the `MoonApi` class with the `MoonConnector` instance as the `connector` option. We use the `getAccount` method of the `MoonApi` instance to retrieve information about an account with the Ethereum address `0x1234567890123456789012345678901234567890`. We log the account information to the console.

Note that we import the `moonWallet` function from the `@moonup/moon-rainbowkit` library, the `Chain` type from the `@rainbow-me/rainbowkit` library, the `MoonApi` class from the `@moonup/moon-api` library, and the `AccountResponse` type from the `@moonup/types` library. We also use the `createConnector` method of the `Wallet` instance to create a new `MoonConnector` instance, the `connect` method of the `MoonConnector` instance to connect to the Moon provider, and the `getAccount` method of the `MoonApi` instance to retrieve information about an account with the Ethereum address `0x1234567890123456789012345678901234567890`.