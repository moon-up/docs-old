---
sidebar_position: 3
id: API
title: API
sidebar_label: API
---
# API Reference

## `MoonConnector`

The `MoonConnector` class provides a custom connector for the Wagmi library, which allows you to interact with the Wagmi API using the Moon provider.

### Properties

- `id` (`string`): The ID of the connector (`'moon'`).
- `name` (`string`): The name of the connector (`'Moon'`).
- `ready` (`boolean`): A boolean indicating whether the connector is ready to use (`true`).

### Methods

- `constructor(options: MoonConnectorOptions)`: Creates a new `MoonConnector` instance with the specified options.
- `connect(): Promise<void>`: Connects to the Wagmi API using the Moon provider.
- `getMoonAccount(): MoonAccount`: Returns a `MoonAccount` instance for interacting with the Wagmi API.

### Example

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

Note that we access the `MoonAccount` property of the `MoonConnector` instance to interact with the Wagmi API.