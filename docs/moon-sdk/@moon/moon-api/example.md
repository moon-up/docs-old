---
sidebar_position: 4
id: example
title: Example 
sidebar_label: Example 
---
# Example

Here is an example of how to use the `@moonup/moon-api` library to interact with the Moon API.

```typescript
import { MoonApi } from '@moonup/moon-api';
import { BigNumber } from '@ethersproject/bignumber';

const moonApi = new MoonApi({
  Auth: {
    securityWorker: () => Promise.resolve('test'),
  },
});

async function main() {
  const account = await moonApi.getAccount('0x1234567890123456789012345678901234567890');
  console.log(account);


  const transaction = {
    to: '0x1234567890123456789012345678901234567890',
    value: BigNumber.from('1000000000000000000'),
  };

  const response = await moonApi.sendTransaction(transaction);
  console.log(response);
}

main();
```

In this example, we create a new instance of the `MoonApi` class with a configuration object that contains a `securityWorker` function that returns a hardcoded authentication token.

We then use the `getAccount` method to retrieve information about an account with the Ethereum address `0x1234567890123456789012345678901234567890`. We log the account information to the console.

Finally, we use the `sendTransaction` method to send a transaction to the Ethereum address `0x1234567890123456789012345678901234567890` with a value of 1 ETH. We log the transaction response to the console.