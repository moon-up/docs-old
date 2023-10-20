---
sidebar_position: 2
id: usage
title: Usage
sidebar_label: Usage 
---
# Usage

To use the `@moonup/wagmi-connector` library, you can import the `MoonConnector` class from the library:

```typescript
import { MoonConnector } from '@moonup/wagmi-connector';

const connector = new MoonConnector({
  options: {
    rpcUrl: 'https://rpc.moonup.com',
  },
});
```

Once you have created a `MoonConnector` instance, you can use it to interact with the Wagmi API using the Moon provider.

Here is an example of how you can use the `MoonConnector` class to retrieve information about an account:

```typescript
import { MoonConnector } from '@moonup/wagmi-connector';

const connector = new MoonConnector({
  options: {
    rpcUrl: 'https://rpc.moonup.com',
  },
});

async function main() {
  const account = await connector.MoonAccount.getAccount('0x1234567890123456789012345678901234567890');
  console.log(account);
}

main();
```

In this example, we create a new instance of the `MoonConnector` class with a configuration object that contains the URL of the Moon RPC endpoint.

We then use the `getAccount` method of the `MoonAccount` property to retrieve information about an account with the Ethereum address `0x1234567890123456789012345678901234567890`. We log the account information to the console.

Note that we import the `MoonConnector` class from the `@moonup/wagmi-connector` library and use it to create a new instance of the `MoonConnector` class. We also access the `MoonAccount` property of the `MoonConnector` instance to interact with the Wagmi API.

# Initialization 

```javascript
import { createConfig, mainnet } from 'wagmi'
 
import { MoonConnector } from '@moon/wagmi-connector'
 
const connector = new MoonConnector({
  chains: [mainnet],
  options: {
    // Custom connector options
  },
})
 
const config = createConfig({
  connectors: [connector],
})
```
