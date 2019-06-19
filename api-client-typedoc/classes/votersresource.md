> ## [@liskhq/lisk-api-client](../README.md)

[Globals](../globals.md) / [VotersResource](votersresource.md) /

# Class: VotersResource

## Hierarchy

* [APIResource](apiresource.md)

  * **VotersResource**

### Index

#### Constructors

* [constructor](votersresource.md#constructor)

#### Properties

* [apiClient](votersresource.md#apiclient)
* [get](votersresource.md#get)
* [path](votersresource.md#path)

#### Accessors

* [headers](votersresource.md#headers)
* [resourcePath](votersresource.md#resourcepath)

#### Methods

* [handleRetry](votersresource.md#handleretry)
* [request](votersresource.md#request)

## Constructors

###  constructor

\+ **new VotersResource**(`apiClient`: [APIClient](apiclient.md)): *[VotersResource](votersresource.md)*

*Overrides [APIResource](apiresource.md).[constructor](apiresource.md#constructor)*

*Defined in [resources/voters.ts:35](url)*

**Parameters:**

Name | Type |
------ | ------ |
`apiClient` | [APIClient](apiclient.md) |

**Returns:** *[VotersResource](votersresource.md)*

___

## Properties

###  apiClient

● **apiClient**: *[APIClient](apiclient.md)*

*Inherited from [APIResource](apiresource.md).[apiClient](apiresource.md#apiclient)*

*Defined in [api_resource.ts:25](url)*

___

###  get

● **get**: *[APIHandler](../globals.md#apihandler)*

*Defined in [resources/voters.ts:34](url)*

Returns all votes received by a delegate.

### Usage Example
```ts
client.accounts.get({ username: 'oliver' })
.then(res => {
console.log(res.data);
});
```

___

###  path

● **path**: *string*

*Overrides [APIResource](apiresource.md).[path](apiresource.md#path)*

*Defined in [resources/voters.ts:35](url)*

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