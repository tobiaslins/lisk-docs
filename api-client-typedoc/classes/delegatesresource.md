> ## [@liskhq/lisk-api-client](../README.md)

[DelegatesResource](delegatesresource.md) /

# Class: DelegatesResource

## Hierarchy

* [APIResource](apiresource.md)

  * **DelegatesResource**

### Index

#### Constructors

* [constructor](delegatesresource.md#constructor)

#### Properties

* [apiClient](delegatesresource.md#apiclient)
* [get](delegatesresource.md#get)
* [getForgers](delegatesresource.md#getforgers)
* [getForgingStatistics](delegatesresource.md#getforgingstatistics)
* [getStandby](delegatesresource.md#getstandby)
* [path](delegatesresource.md#path)

#### Accessors

* [headers](delegatesresource.md#headers)
* [resourcePath](delegatesresource.md#resourcepath)

#### Methods

* [handleRetry](delegatesresource.md#handleretry)
* [request](delegatesresource.md#request)

## Constructors

###  constructor

\+ **new DelegatesResource**(`apiClient`: [APIClient](apiclient.md)): *[DelegatesResource](delegatesresource.md)*

*Overrides [APIResource](apiresource.md).[constructor](apiresource.md#constructor)*

*Defined in [resources/delegates.ts:74](url)*

**Parameters:**

Name | Type |
------ | ------ |
`apiClient` | [APIClient](apiclient.md) |

**Returns:** *[DelegatesResource](delegatesresource.md)*

___

## Properties

###  apiClient

● **apiClient**: *[APIClient](apiclient.md)*

*Inherited from [APIResource](apiresource.md).[apiClient](apiresource.md#apiclient)*

*Defined in [api_resource.ts:25](url)*

___

###  get

● **get**: *[APIHandler](../README.md#apihandler)*

*Defined in [resources/delegates.ts:33](url)*

Searches for a specified dapp in the system.

### Usage Example
```ts
client.accounts.get({ username: 'oliver' })
.then(res => {
console.log(res.data);
});
```

___

###  getForgers

● **getForgers**: *[APIHandler](../README.md#apihandler)*

*Defined in [resources/delegates.ts:46](url)*

Returns a list of the next forgers in this delegate round.

### Usage Example
```ts
client.accounts.getForgers()
.then(res => {
console.log(res.data);
});
```

___

###  getForgingStatistics

● **getForgingStatistics**: *[APIHandler](../README.md#apihandler)*

*Defined in [resources/delegates.ts:60](url)*

By passing an existing delegate address and the desired unix timestamps, you can get its forging statistics within the specified timespan.
If no timestamps are provided, it will use the timestamps from Lisk epoch to current date.

### Usage Example
```ts
client.accounts.getForgingStatistics('15434119221255134066L')
.then(res => {
console.log(res.data);
});
```

___

###  getStandby

● **getStandby**: *[APIHandler](../README.md#apihandler)*

*Defined in [resources/delegates.ts:73](url)*

Calls get with default parameters to retrieve delegates from rank 102 onwards.

### Usage Example
```ts
client.accounts.getStandby()
.then(res => {
console.log(res.data);
});
```

___

###  path

● **path**: *string*

*Overrides [APIResource](apiresource.md).[path](apiresource.md#path)*

*Defined in [resources/delegates.ts:74](url)*

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