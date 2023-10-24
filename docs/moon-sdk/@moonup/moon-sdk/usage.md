---
sidebar_position: 2
id: usage
title: Usage
sidebar_label: Usage 
---

# Usage
To use the @moonup/moon-sdk library, you can import it into your TypeScript project like this:
```javascript
import { MoonSDK } from '@moonup/moon-sdk';
```

Then, you can create a new instance of the MoonSDK class and use its methods to interact with the MoonUp platform:

```javascript
const sdk = new MoonSDK({
  Auth: {
    clientId: 'YOUR_CLIENT_ID',
    clientSecret: 'YOUR_CLIENT_SECRET',
    redirectUri: 'YOUR_REDIRECT_URI',
  },
  Storage: {
    type: 'localStorage',
  },
});

sdk.connect();
```

For more information on how to use the @moonup/moon-sdk library, see the API documentation.

