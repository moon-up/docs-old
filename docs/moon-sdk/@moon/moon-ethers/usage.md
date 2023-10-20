---
sidebar_position: 2
id: usage
title: Usage
sidebar_label: Usage 
---

# Usage

To use the `@moonup/ethers` library, you can import the `MoonProvider` and `MoonSigner` classes from the library:

```typescript
import { MoonProvider, MoonSigner } from '@moonup/ethers';
import { ethers } from 'ethers';

const provider = new MoonProvider({
  rpcUrl: 'https://rpc.moonup.com',
});

const signer = new MoonSigner({
  rpcUrl: 'https://rpc.moonup.com',
});

async function main() {
  const blockNumber = await provider.getBlockNumber();
  console.log(`Latest block number: ${blockNumber}`);

  const balance = await signer.getBalance();
  console.log(`Balance: ${ethers.utils.formatEther(balance)} ETH`);
}

main();
```

In this example, we import the `MoonProvider` and `MoonSigner` classes from the `@moonup/ethers` library and the `ethers` object from the Ethers.js library.

We create a new instance of the `MoonProvider` class with a configuration object that contains the URL of the Moon RPC endpoint.

We create a new instance of the `MoonSigner` class with a configuration object that contains the URL of the Moon RPC endpoint and a private key.

We call the `getBlockNumber` method of the `MoonProvider` instance to retrieve the latest block number. We log the block number to the console.

We call the `getBalance` method of the `MoonSigner` instance to retrieve the balance of the account associated with the private key. We log the balance to the console.

Note that we import the `MoonProvider` and `MoonSigner` classes from the `@moonup/ethers` library and the `ethers` object from the Ethers.js library. We also use the `getBlockNumber` method of the `MoonProvider` instance to retrieve the latest block number and the `getBalance` method of the `MoonSigner` instance to retrieve the balance of the account associated with the private key.