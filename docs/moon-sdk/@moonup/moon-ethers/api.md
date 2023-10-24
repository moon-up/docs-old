---
sidebar_position: 3
id: API
title: API
sidebar_label: API
---

# API Reference

## `MoonProvider`

The `MoonProvider` class provides a custom provider for the Ethers.js library, which allows you to interact with the Wagmi API using the Moon provider.

### Signature

```typescript
class MoonProvider extends ethers.providers.JsonRpcProvider {}
```

### Example

```typescript
import { MoonProvider } from '@moonup/ethers';

const provider = new MoonProvider({
  rpcUrl: 'https://rpc.moonup.com',
});

async function main() {
  const blockNumber = await provider.getBlockNumber();
  console.log(`Latest block number: ${blockNumber}`);
}

main();
```

In this example, we import the `MoonProvider` class from the `@moonup/ethers` library.

We create a new instance of the `MoonProvider` class with a configuration object that contains the URL of the Moon RPC endpoint.

We call the `getBlockNumber` method of the `MoonProvider` instance to retrieve the latest block number. We log the block number to the console.

Note that we import the `MoonProvider` class from the `@moonup/ethers` library and use the `getBlockNumber` method of the `MoonProvider` instance to retrieve the latest block number.

## `MoonSigner`

The `MoonSigner` class provides a custom signer for the Ethers.js library, which allows you to interact with the Wagmi API using the Moon provider.

### Signature

```typescript
class MoonSigner extends ethers.Wallet {}
```

### Example

```typescript
import { MoonSigner } from '@moonup/ethers';
import { ethers } from 'ethers';

const signer = new MoonSigner({
  rpcUrl: 'https://rpc.moonup.com',
  privateKey: '0x1234567890abcdef1234567890abcdef1234567890abcdef1234567890abcdef',
});

async function main() {
  const balance = await signer.getBalance();
  console.log(`Balance: ${ethers.utils.formatEther(balance)} ETH`);
}

main();
```

In this example, we import the `MoonSigner` class from the `@moonup/ethers` library and the `ethers` object from the Ethers.js library.

We create a new instance of the `MoonSigner` class with a configuration object that contains the URL of the Moon RPC endpoint and a private key.

We call the `getBalance` method of the `MoonSigner` instance to retrieve the balance of the account associated with the private key. We log the balance to the console.

Note that we import the `MoonSigner` class from the `@moonup/ethers` library and the `ethers` object from the Ethers.js library. We also use the `getBalance` method of the `MoonSigner` instance to retrieve the balance of the account associated with the private key.