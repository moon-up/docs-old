---
sidebar_position: 2
id: usage
title: Usage
sidebar_label: Usage 
---

# Usage


Once you have installed the library, you can import the `MoonApi` class and create an instance of it:

```typescript
import { MoonApi } from '@moonup/moon-api';

const moonApi = new MoonApi({
  Auth: {
    securityWorker: () => Promise.resolve('test'),
  },
});
```

The `MoonApi` constructor takes a configuration object as its argument. The configuration object should have an `Auth` property, which is an object that contains a `securityWorker` function. The `securityWorker` function should return a Promise that resolves to a string, which is used as the authentication token for requests to the Moon API.

Once you have an instance of the `MoonApi` class, you can use its methods to interact with the Moon API. For example, to get information about an account, you can use the `getAccount` method:

```typescript
const account = await moonApi.getAccount('0x1234567890123456789012345678901234567890');
console.log(account);
```

The `getAccount` method takes an Ethereum address as its argument and returns an object that contains information about the account, including its balance and transaction history.

You can also use the `sendTransaction` method to send a transaction to the Moon API:

```typescript
const transaction: Transaction = {
  to: '0x1234567890123456789012345678901234567890',
  value: BigNumber.from('1000000000000000000'),
};

const response = await moonApi.sendTransaction(transaction);
console.log(response);
```

The `sendTransaction` method takes a `Transaction` object as its argument and returns a `TransactionResponse` object, which contains information about the transaction, including its hash and status.

