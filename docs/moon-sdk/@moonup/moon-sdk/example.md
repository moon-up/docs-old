---
sidebar_position: 4
id: example 
title: Example 
sidebar_label: Example 
---

```javascript
import { MoonSDK } from '@moonup/moon-sdk';

// Create a new instance of the MoonSDK class
const sdk = new MoonSDK({
  Auth: {
    clientId: 'YOUR_CLIENT_ID',
    clientSecret: 'YOUR_CLIENT_SECRET',
    redirectUri: 'YOUR_REDIRECT_URI',
  },
  Storage: {
    type: 'localStorage',
  },
  Networks: ['rinkeby', 'mainnet'],
});

// Update the current MoonUp account
const account = {
  token: 'YOUR_AUTH_TOKEN',
  email: 'YOUR_EMAIL_ADDRESS',
  expiry: 1234567890,
  refreshToken: 'YOUR_REFRESH_TOKEN',
  wallet: 'YOUR_WALLET_ADDRESS',
  network: 'rinkeby',
};
sdk.updateAccount(account);

// Connect to the MoonUp platform
await sdk.connect();

// Get the Chain object for the Rinkeby network
const chain = sdk.getChain('rinkeby');

// Initialize the configuration for the MoonSDK class
const config = sdk.initialiseConfig({
  Auth: {
    clientId: 'YOUR_CLIENT_ID',
    clientSecret: 'YOUR_CLIENT_SECRET',
    redirectUri: 'YOUR_REDIRECT_URI',
  },
  Storage: {
    type: 'localStorage',
  },
});

console.log(config);
```