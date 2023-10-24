---
sidebar_position: 3
id: API
title: API
sidebar_label: API
---
## `MoonSDK`

The `MoonSDK` class is the main class for interacting with the MoonUp platform. It provides a variety of functions for managing accounts, connecting to the MoonUp API, and handling messages.

### `constructor(config: MoonSDKConfig)`

Creates a new instance of the `MoonSDK` class with the specified configuration.

#### Parameters

- `config`: An object that contains the configuration for the `MoonSDK` class. The object should have the following properties:
  - `Auth`: An object that contains the authentication configuration for the MoonUp platform.
  - `Storage`: An object that contains the storage configuration for the MoonUp platform.
  - `Networks`: An optional array of supported networks for the MoonUp platform.

### `updateAccount(account: MoonAccount)`

Updates the current MoonUp account with the specified account object.

#### Parameters

- `account`: An object that contains the updated account information. The object should have the following properties:
  - `token`: The authentication token for the MoonUp platform.
  - `email`: The email address associated with the MoonUp account.
  - `expiry`: The expiry time for the authentication token.
  - `refreshToken`: The refresh token for the authentication token.
  - `wallet`: The wallet address associated with the MoonUp account.
  - `network`: The network associated with the MoonUp account.

### `connect()`

Connects to the MoonUp platform and fetches the current MoonUp account. This function must be called before any other functions that interact with the MoonUp platform.

### `getChain(network: string): Chain`

Returns the `Chain` object for the specified network.

#### Parameters

- `network`: A string that specifies the network to get the `Chain` object for.

### `initialiseConfig(config: MoonSDKConfig): MoonSDKConfig`

Initializes the configuration for the `MoonSDK` class.

#### Parameters

- `config`: An object that contains the configuration for the `MoonSDK` class. The object should have the following properties:
  - `Auth`: An object that contains the authentication configuration for the MoonUp platform.
  - `Storage`: An object that contains the storage configuration for the MoonUp platform.
  - `Networks`: An optional array of supported networks for the MoonUp platform.

#### Returns

- An object that contains the initialized configuration for the `MoonSDK` class.

### `MoonProvider: JsonRpcProvider | undefined`

A property that contains the `JsonRpcProvider` object for the MoonUp platform.

### `MoonApi: MoonApi`

A property that contains the `MoonApi` object for the MoonUp platform.

### `MoonSDKConfig: MoonSDKConfig`

A property that contains the configuration for the `MoonSDK` class.

### `MoonAccount: MoonAccount`

A property that contains the current MoonUp account.

### `MoonMessageHandler: MoonMessageHandler`

A property that contains the `MoonMessageHandler` object for handling MoonUp messages.

### `MoonIframe: IframeController | undefined`

A property that contains the `IframeController` object for the MoonUp platform.

That's a complete breakdown of all the available functions in the `MoonSDK` class. For more information on how to use the `@moonup/moon-sdk` library, see the [API documentation](api.md).