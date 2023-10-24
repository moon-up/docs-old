---
sidebar_position: 2
id: usage
title: Usage
sidebar_label: Usage 
---
# Usage

To use the `@moonup/types` library, you can import the types you need from the library:

```typescript
import { AccountResponse } from '@moonup/types';

const account: AccountResponse = {
  address: '0x1234567890123456789012345678901234567890',
  balance: BigNumber.from('1000000000000000000'),
  nonce: 0,
  transactions: [],
};
```

In this example, we import the `AccountResponse` type from the `@moonup/types` library and use it to define the structure of an object representing an account.

You can also import multiple types at once using the `*` wildcard:

```typescript
import * as MoonTypes from '@moonup/types';

const account: MoonTypes.AccountResponse = {
  address: '0x1234567890123456789012345678901234567890',
  balance: BigNumber.from('1000000000000000000'),
  nonce: 0,
  transactions: [],
};
```

This imports all of the types from the `@moonup/types` library and assigns them to the `MoonTypes` namespace.
