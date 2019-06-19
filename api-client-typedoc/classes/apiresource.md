> ## [@liskhq/lisk-api-client](../README.md)

[APIResource](apiresource.md) /

# Class: APIResource

## Hierarchy

* **APIResource**

  * [AccountsResource](accountsresource.md)

  * [BlocksResource](blocksresource.md)

  * [DappsResource](dappsresource.md)

  * [DelegatesResource](delegatesresource.md)

  * [NodeResource](noderesource.md)

  * [PeersResource](peersresource.md)

  * [SignaturesResource](signaturesresource.md)

  * [TransactionsResource](transactionsresource.md)

  * [VotersResource](votersresource.md)

  * [VotesResource](votesresource.md)

### Index

#### Constructors

* [constructor](apiresource.md#constructor)

#### Properties

* [apiClient](apiresource.md#apiclient)
* [path](apiresource.md#path)

#### Accessors

* [headers](apiresource.md#headers)
* [resourcePath](apiresource.md#resourcepath)

#### Methods

* [handleRetry](apiresource.md#handleretry)
* [request](apiresource.md#request)

## Constructors

###  constructor

\+ **new APIResource**(`apiClient`: [APIClient](apiclient.md)): *[APIResource](apiresource.md)*

*Defined in [api_resource.ts:26](url)*

**Parameters:**

Name | Type |
------ | ------ |
`apiClient` | [APIClient](apiclient.md) |

**Returns:** *[APIResource](apiresource.md)*

___

## Properties

###  apiClient

● **apiClient**: *[APIClient](apiclient.md)*

*Defined in [api_resource.ts:25](url)*

___

###  path

● **path**: *string*

*Defined in [api_resource.ts:26](url)*

___

## Accessors

###  headers

● **get headers**(): *[HashMap](../interfaces/hashmap.md)*

*Defined in [api_resource.ts:33](url)*

**Returns:** *[HashMap](../interfaces/hashmap.md)*

___

###  resourcePath

● **get resourcePath**(): *string*

*Defined in [api_resource.ts:37](url)*

**Returns:** *string*

___

## Methods

###  handleRetry

▸ **handleRetry**(`error`: `Error`, `req`: `AxiosRequestConfig`, `retryCount`: number): *`Promise<APIResponse>`*

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

*Defined in [api_resource.ts:66](url)*

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`req` | `AxiosRequestConfig` | - |
`retry` | boolean | - |
`retryCount` | number | 1 |

**Returns:** *`Promise<APIResponse>`*

___