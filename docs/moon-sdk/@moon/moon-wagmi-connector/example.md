---
sidebar_position: 4
id: example 
title: Example 
sidebar_label: Example 
---

# Examples

## Using the `MoonConnector` class

Here is an example of how you can use the `MoonConnector` class to interact with the Wagmi API:

```typescript
import { MoonConnector } from '@moonup/wagmi-connector';
import { MoonApi } from '@moonup/moon-api';
import { AccountResponse } from '@moonup/types';

const connector = new MoonConnector({
  options: {
    rpcUrl: 'https://rpc.moonup.com',
  },
});

async function main() {
  const moonApi = new MoonApi({
    connector,
  });

  const account: AccountResponse = await moonApi.getAccount('0x1234567890123456789012345678901234567890');
  console.log(account);
}

main();
```

In this example, we create a new instance of the `MoonConnector` class with a configuration object that contains the URL of the Moon RPC endpoint.

We then create a new instance of the `MoonApi` class with the `MoonConnector` instance as the `connector` option. We use the `getAccount` method of the `MoonApi` instance to retrieve information about an account with the Ethereum address `0x1234567890123456789012345678901234567890`. We log the account information to the console.

Note that we import the `MoonConnector` class from the `@moonup/wagmi-connector` library, the `MoonApi` class from the `@moonup/moon-api` library, and the `AccountResponse` type from the `@moonup/types` library.

## Importing the Wagmi library

Here is an example of how you can import the Wagmi library and use it to interact with the Wagmi API:

```typescript
import { MoonApi } from '@moonup/moon-api';
import { MoonConnector } from '@moonup/wagmi-connector';
import { AccountResponse } from '@moonup/types';

const connector = new MoonConnector({
  options: {
    rpcUrl: 'https://rpc.moonup.com',
  },
});

async function main() {
  const moonApi = new MoonApi({
    connector,
  });

  const account: AccountResponse = await moonApi.getAccount('0x1234567890123456789012345678901234567890');
  console.log(account);
}

main();
```

In this example, we import the `MoonApi` class from the `@moonup/moon-api` library, the `MoonConnector` class from the `@moonup/wagmi-connector` library, and the `AccountResponse` type from the `@moonup/types` library.

We then create a new instance of the `MoonConnector` class with a configuration object that contains the URL of the Moon RPC endpoint.

We create a new instance of the `MoonApi` class with the `MoonConnector` instance as the `connector` option. We use the `getAccount` method of the `MoonApi` instance to retrieve information about an account with the Ethereum address `0x1234567890123456789012345678901234567890`. We log the account information to the console.