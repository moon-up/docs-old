---
sidebar_position: 4
id: example 
title: Example 
sidebar_label: Example 
---

# Example

```typescript
import { MoonApi } from '@moonup/moon-api';
import { AccountResponse } from '@moonup/types';

const moonApi = new MoonApi({
  Auth: {
    securityWorker: () => Promise.resolve('test'),
  },
});

async function main() {
  const account: AccountResponse = await moonApi.getAccount('0x1234567890123456789012345678901234567890');
  console.log(account);
}

main();
```

In this example, we create a new instance of the `MoonApi` class with a configuration object that contains a `securityWorker` function that returns a hardcoded authentication token.

We then use the `getAccount` method to retrieve information about an account with the Ethereum address `0x1234567890123456789012345678901234567890`. We log the account information to the console.

Note that we import the `AccountResponse` type from the `@moonup/types` library and use it to define the structure of the `account` object.