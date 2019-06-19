> ## [@liskhq/lisk-api-client](../README.md)

[Globals](../globals.md) / [SignaturesResource](signaturesresource.md) /

# Class: SignaturesResource

## Hierarchy

* [APIResource](apiresource.md)

  * **SignaturesResource**

### Index

#### Constructors

* [constructor](signaturesresource.md#constructor)

#### Properties

* [apiClient](signaturesresource.md#apiclient)
* [broadcast](signaturesresource.md#broadcast)
* [path](signaturesresource.md#path)

#### Accessors

* [headers](signaturesresource.md#headers)
* [resourcePath](signaturesresource.md#resourcepath)

#### Methods

* [handleRetry](signaturesresource.md#handleretry)
* [request](signaturesresource.md#request)

## Constructors

###  constructor

\+ **new SignaturesResource**(`apiClient`: [APIClient](apiclient.md)): *[SignaturesResource](signaturesresource.md)*

*Overrides [APIResource](apiresource.md).[constructor](apiresource.md#constructor)*

*Defined in [resources/signatures.ts:39](url)*

**Parameters:**

Name | Type |
------ | ------ |
`apiClient` | [APIClient](apiclient.md) |

**Returns:** *[SignaturesResource](signaturesresource.md)*

___

## Properties

###  apiClient

● **apiClient**: *[APIClient](apiclient.md)*

*Inherited from [APIResource](apiresource.md).[apiClient](apiresource.md#apiclient)*

*Defined in [api_resource.ts:25](url)*

___

###  broadcast

● **broadcast**: *[APIHandler](../globals.md#apihandler)*

*Defined in [resources/signatures.ts:38](url)*

Submits a signature to sign a multisignature transaction.

### Usage Example
```ts
client.accounts.broadcast({
transactionId: '222675625422353767',
publicKey: '2ca9a7143fc721fdc540fef893b27e8d648d2288efa61e56264edf01a2c23079',
signature: '2821d93a742c4edf5fd960efad41a4def7bf0fd0f7c09869aed524f6f52bf9c97a617095e2c712bd28b4279078a29509b339ac55187854006591aa759784c205',
})
.then(res => {
console.log(res.data);
});
```

___

###  path

● **path**: *string*

*Overrides [APIResource](apiresource.md).[path](apiresource.md#path)*

*Defined in [resources/signatures.ts:39](url)*

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