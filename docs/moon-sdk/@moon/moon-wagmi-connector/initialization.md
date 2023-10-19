---
sidebar_position: 2
---


# Initialization 

```javascript
import { createConfig, mainnet } from 'wagmi'
 
import { MoonConnector } from '@moon/wagmi-connector'
 
const connector = new MoonConnector({
  chains: [mainnet],
  options: {
    // Custom connector options
  },
})
 
const config = createConfig({
  connectors: [connector],
})
```
