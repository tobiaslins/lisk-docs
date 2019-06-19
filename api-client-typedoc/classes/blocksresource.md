> ## [@liskhq/lisk-api-client](../README.md)

[BlocksResource](blocksresource.md) /

# Class: BlocksResource

Provides block related API endpoints.

## Hierarchy

* [APIResource](apiresource.md)

  * **BlocksResource**

### Index

#### Constructors

* [constructor](blocksresource.md#constructor)

#### Properties

* [apiClient](blocksresource.md#apiclient)
* [get](blocksresource.md#get)
* [path](blocksresource.md#path)

#### Accessors

* [headers](blocksresource.md#headers)
* [resourcePath](blocksresource.md#resourcepath)

#### Methods

* [handleRetry](blocksresource.md#handleretry)
* [request](blocksresource.md#request)

## Constructors

###  constructor

\+ **new BlocksResource**(`apiClient`: [APIClient](apiclient.md)): *[BlocksResource](blocksresource.md)*

*Overrides [APIResource](apiresource.md).[constructor](apiresource.md#constructor)*

*Defined in [resources/blocks.ts:38](url)*

**Parameters:**

Name | Type |
------ | ------ |
`apiClient` | [APIClient](apiclient.md) |

**Returns:** *[BlocksResource](blocksresource.md)*

___

## Properties

###  apiClient

● **apiClient**: *[APIClient](apiclient.md)*

*Inherited from [APIResource](apiresource.md).[apiClient](apiresource.md#apiclient)*

*Defined in [api_resource.ts:25](url)*

___

###  get

● **get**: *[APIHandler](../README.md#apihandler)*

*Defined in [resources/blocks.ts:37](url)*

Searches for a specified block in the system.

### Usage Example

```ts
client.accounts.get({ blockId: '17572751491778765213' })
.then(res => {
console.log(res.data);
});
```

___

###  path

● **path**: *string*

*Overrides [APIResource](apiresource.md).[path](apiresource.md#path)*

*Defined in [resources/blocks.ts:38](url)*

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