> ## [@liskhq/lisk-api-client](../README.md)

[PeersResource](peersresource.md) /

# Class: PeersResource

## Hierarchy

* [APIResource](apiresource.md)

  * **PeersResource**

### Index

#### Constructors

* [constructor](peersresource.md#constructor)

#### Properties

* [apiClient](peersresource.md#apiclient)
* [get](peersresource.md#get)
* [path](peersresource.md#path)

#### Accessors

* [headers](peersresource.md#headers)
* [resourcePath](peersresource.md#resourcepath)

#### Methods

* [handleRetry](peersresource.md#handleretry)
* [request](peersresource.md#request)

## Constructors

###  constructor

\+ **new PeersResource**(`apiClient`: [APIClient](apiclient.md)): *[PeersResource](peersresource.md)*

*Overrides [APIResource](apiresource.md).[constructor](apiresource.md#constructor)*

*Defined in [resources/peers.ts:34](url)*

**Parameters:**

Name | Type |
------ | ------ |
`apiClient` | [APIClient](apiclient.md) |

**Returns:** *[PeersResource](peersresource.md)*

___

## Properties

###  apiClient

● **apiClient**: *[APIClient](apiclient.md)*

*Inherited from [APIResource](apiresource.md).[apiClient](apiresource.md#apiclient)*

*Defined in [api_resource.ts:25](url)*

___

###  get

● **get**: *[APIHandler](../README.md#apihandler)*

*Defined in [resources/peers.ts:33](url)*

Searches for specified peers.

### Usage Example
```ts
client.accounts.get({ height: 5509963 })
.then(res => {
console.log(res.data);
});
```

___

###  path

● **path**: *string*

*Overrides [APIResource](apiresource.md).[path](apiresource.md#path)*

*Defined in [resources/peers.ts:34](url)*

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