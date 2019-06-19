> ## [@liskhq/lisk-api-client](README.md)

[Globals](globals.md) /

# @liskhq/lisk-api-client

### Index

#### Classes

* [APIClient](classes/apiclient.md)
* [APIError](classes/apierror.md)
* [APIResource](classes/apiresource.md)
* [AccountsResource](classes/accountsresource.md)
* [BlocksResource](classes/blocksresource.md)
* [DappsResource](classes/dappsresource.md)
* [DelegatesResource](classes/delegatesresource.md)
* [NodeResource](classes/noderesource.md)
* [PeersResource](classes/peersresource.md)
* [SignaturesResource](classes/signaturesresource.md)
* [TransactionsResource](classes/transactionsresource.md)
* [VotersResource](classes/votersresource.md)
* [VotesResource](classes/votesresource.md)

#### Interfaces

* [APIErrorContents](interfaces/apierrorcontents.md)
* [APIErrorData](interfaces/apierrordata.md)
* [APIErrorResponse](interfaces/apierrorresponse.md)
* [APIResponse](interfaces/apiresponse.md)
* [ClientOptions](interfaces/clientoptions.md)
* [HashMap](interfaces/hashmap.md)
* [InitOptions](interfaces/initoptions.md)
* [RequestConfig](interfaces/requestconfig.md)
* [Resource](interfaces/resource.md)

#### Type aliases

* [APIHandler](globals.md#apihandler)

#### Variables

* [GET](globals.md#const-get)
* [MAINNET_NETHASH](globals.md#const-mainnet_nethash)
* [MAINNET_NODES](globals.md#const-mainnet_nodes)
* [POST](globals.md#const-post)
* [PUT](globals.md#const-put)
* [TESTNET_NETHASH](globals.md#const-testnet_nethash)
* [TESTNET_NODES](globals.md#const-testnet_nodes)

#### Functions

* [apiMethod](globals.md#const-apimethod)
* [solveURLParams](globals.md#const-solveurlparams)
* [toQueryString](globals.md#const-toquerystring)

## Type aliases

###  APIHandler

Ƭ **APIHandler**: *function*

*Defined in [api_types.ts:18](url)*

#### Type declaration:

▸ (...`args`: `Array<number | string | object>`): *`Promise<APIResponse>`*

**Parameters:**

Name | Type |
------ | ------ |
`...args` | `Array<number \| string \| object>` |

___

## Variables

### `Const` GET

● **GET**: *"GET"* = "GET"

*Defined in [constants.ts:15](url)*

___

### `Const` MAINNET_NETHASH

● **MAINNET_NETHASH**: *"ed14889723f24ecc54871d058d98ce91ff2f973192075c0155ba2b7b70ad2511"* = "ed14889723f24ecc54871d058d98ce91ff2f973192075c0155ba2b7b70ad2511"

*Defined in [constants.ts:21](url)*

___

### `Const` MAINNET_NODES

● **MAINNET_NODES**: *`ReadonlyArray<string>`* =  [
	'https://node01.lisk.io:443',
	'https://node02.lisk.io:443',
	'https://node03.lisk.io:443',
	'https://node04.lisk.io:443',
	'https://node05.lisk.io:443',
	'https://node06.lisk.io:443',
	'https://node07.lisk.io:443',
	'https://node08.lisk.io:443',
]

*Defined in [constants.ts:27](url)*

___

### `Const` POST

● **POST**: *"POST"* = "POST"

*Defined in [constants.ts:16](url)*

___

### `Const` PUT

● **PUT**: *"PUT"* = "PUT"

*Defined in [constants.ts:17](url)*

___

### `Const` TESTNET_NETHASH

● **TESTNET_NETHASH**: *"da3ed6a45429278bac2666961289ca17ad86595d33b31037615d4b8e8f158bba"* = "da3ed6a45429278bac2666961289ca17ad86595d33b31037615d4b8e8f158bba"

*Defined in [constants.ts:19](url)*

___

### `Const` TESTNET_NODES

● **TESTNET_NODES**: *`ReadonlyArray<string>`* =  [
	'https://testnet.lisk.io:443',
]

*Defined in [constants.ts:24](url)*

___

## Functions

### `Const` apiMethod

▸ **apiMethod**(`options`: [RequestConfig](interfaces/requestconfig.md)): *[APIHandler](globals.md#apihandler)*

*Defined in [api_method.ts:27](url)*

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`options` | [RequestConfig](interfaces/requestconfig.md) |  {} |

**Returns:** *[APIHandler](globals.md#apihandler)*

___

### `Const` solveURLParams

▸ **solveURLParams**(`url`: string, `params`: [HashMap](interfaces/hashmap.md)): *string*

*Defined in [utils.ts:33](url)*

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`url` | string | - |
`params` | [HashMap](interfaces/hashmap.md) |  {} |

**Returns:** *string*

___

### `Const` toQueryString

▸ **toQueryString**(`obj`: [HashMap](interfaces/hashmap.md)): *string*

*Defined in [utils.ts:17](url)*

**Parameters:**

Name | Type |
------ | ------ |
`obj` | [HashMap](interfaces/hashmap.md) |

**Returns:** *string*

___