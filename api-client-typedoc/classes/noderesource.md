> ## [@liskhq/lisk-api-client](../README.md)

[NodeResource](noderesource.md) /

# Class: NodeResource

## Hierarchy

* [APIResource](apiresource.md)

  * **NodeResource**

### Index

#### Constructors

* [constructor](noderesource.md#constructor)

#### Properties

* [apiClient](noderesource.md#apiclient)
* [getConstants](noderesource.md#getconstants)
* [getForgingStatus](noderesource.md#getforgingstatus)
* [getStatus](noderesource.md#getstatus)
* [getTransactions](noderesource.md#gettransactions)
* [path](noderesource.md#path)
* [updateForgingStatus](noderesource.md#updateforgingstatus)

#### Accessors

* [headers](noderesource.md#headers)
* [resourcePath](noderesource.md#resourcepath)

#### Methods

* [handleRetry](noderesource.md#handleretry)
* [request](noderesource.md#request)

## Constructors

###  constructor

\+ **new NodeResource**(`apiClient`: [APIClient](apiclient.md)): *[NodeResource](noderesource.md)*

*Overrides [APIResource](apiresource.md).[constructor](apiresource.md#constructor)*

*Defined in [resources/node.ts:95](url)*

**Parameters:**

Name | Type |
------ | ------ |
`apiClient` | [APIClient](apiclient.md) |

**Returns:** *[NodeResource](noderesource.md)*

___

## Properties

###  apiClient

● **apiClient**: *[APIClient](apiclient.md)*

*Inherited from [APIResource](apiresource.md).[apiClient](apiresource.md#apiclient)*

*Defined in [api_resource.ts:25](url)*

___

###  getConstants

● **getConstants**: *[APIHandler](../README.md#apihandler)*

*Defined in [resources/node.ts:33](url)*

Returns all current constants data on the system, e.g. Lisk epoch time and version.

### Usage Example
```ts
client.accounts.getConstants()
.then(res => {
console.log(res.data);
});
```

___

###  getForgingStatus

● **getForgingStatus**: *[APIHandler](../README.md#apihandler)*

*Defined in [resources/node.ts:48](url)*

*Attention! This is a private endpoint only authorized to whitelisted IPs.*

Responds with the forging status of a delegate on a node.

### Usage Example
```ts
client.accounts.getForgingStatus()
.then(res => {
console.log(res.data);
});
```

___

###  getStatus

● **getStatus**: *[APIHandler](../README.md#apihandler)*

*Defined in [resources/node.ts:61](url)*

Returns all current status data of the node, e.g. height and broadhash.

### Usage Example
```ts
client.accounts.getStatus()
.then(res => {
console.log(res.data);
});
```

___

###  getTransactions

● **getTransactions**: *[APIHandler](../README.md#apihandler)*

*Defined in [resources/node.ts:74](url)*

By specifying the state of the transactions, you get a list of unprocessed transactions matching this state.

### Usage Example
```ts
client.accounts.getTransactions('unconfirmed')
.then(res => {
console.log(res.data);
});
```

___

###  path

● **path**: *string*

*Overrides [APIResource](apiresource.md).[path](apiresource.md#path)*

*Defined in [resources/node.ts:75](url)*

___

###  updateForgingStatus

● **updateForgingStatus**: *[APIHandler](../README.md#apihandler)*

*Defined in [resources/node.ts:95](url)*

*Attention! This is a private endpoint only authorized to whitelisted IPs.*

Upon passing the correct password and publicKey, forging will be enabled or disabled for the delegate of this particular node.
The password can be generated locally by encrypting your passphrase, either by using Lisk Commander or with Lisk Elements.

### Usage Example
```ts
client.accounts.updateForgingStatus({
forging: true,
password: 'happy tree friends',
publicKey: '968ba2fa993ea9dc27ed740da0daf49eddd740dbd7cb1cb4fc5db3a20baf341b',
})
.then(res => {
console.log(res.data);
});
```

___

## Accessors

###  headers

● **get headers**(): *[HashMap](../interfaces/hashmap.md)*

*Inherited from [APIResource](apiresource.md).[headers](apiresource.md#headers)*

*Defined in [api_resource.ts:33](url)*

**Returns:** *[HashMap](../interfaces/hashmap.md)*

___

###  resourcePath

● **get resourcePath**(): *string*

*Inherited from [APIResource](apiresource.md).[resourcePath](apiresource.md#resourcepath)*

*Defined in [api_resource.ts:37](url)*

**Returns:** *string*

___

## Methods

###  handleRetry

▸ **handleRetry**(`error`: `Error`, `req`: `AxiosRequestConfig`, `retryCount`: number): *`Promise<APIResponse>`*

*Inherited from [APIResource](apiresource.md).[handleRetry](apiresource.md#handleretry)*

*Defined in [api_resource.ts:41](url)*

**Parameters:**

Name | Type |
------ | ------ |
`error` | `Error` |
`req` | `AxiosRequestConfig` |
`retryCount` | number |

**Returns:** *`Promise<APIResponse>`*

___

###  request

▸ **request**(`req`: `AxiosRequestConfig`, `retry`: boolean, `retryCount`: number): *`Promise<APIResponse>`*

*Inherited from [APIResource](apiresource.md).[request](apiresource.md#request)*

*Defined in [api_resource.ts:66](url)*

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`req` | `AxiosRequestConfig` | - |
`retry` | boolean | - |
`retryCount` | number | 1 |

**Returns:** *`Promise<APIResponse>`*

___