> ## [@liskhq/lisk-api-client](../README.md)

[Globals](../globals.md) / [AccountsResource](accountsresource.md) /

# Class: AccountsResource

## Hierarchy

* [APIResource](apiresource.md)

  * **AccountsResource**

### Index

#### Constructors

* [constructor](accountsresource.md#constructor)

#### Properties

* [apiClient](accountsresource.md#apiclient)
* [get](accountsresource.md#get)
* [getMultisignatureGroups](accountsresource.md#getmultisignaturegroups)
* [getMultisignatureMemberships](accountsresource.md#getmultisignaturememberships)
* [path](accountsresource.md#path)

#### Accessors

* [headers](accountsresource.md#headers)
* [resourcePath](accountsresource.md#resourcepath)

#### Methods

* [handleRetry](accountsresource.md#handleretry)
* [request](accountsresource.md#request)

## Constructors

###  constructor

\+ **new AccountsResource**(`apiClient`: [APIClient](apiclient.md)): *[AccountsResource](accountsresource.md)*

*Overrides [APIResource](apiresource.md).[constructor](apiresource.md#constructor)*

*Defined in [resources/accounts.ts:60](url)*

**Parameters:**

Name | Type |
------ | ------ |
`apiClient` | [APIClient](apiclient.md) |

**Returns:** *[AccountsResource](accountsresource.md)*

___

## Properties

###  apiClient

● **apiClient**: *[APIClient](apiclient.md)*

*Inherited from [APIResource](apiresource.md).[apiClient](apiresource.md#apiclient)*

*Defined in [api_resource.ts:25](url)*

___

###  get

● **get**: *[APIHandler](../globals.md#apihandler)*

*Defined in [resources/accounts.ts:33](url)*

Searches for matching accounts in the system.

### Usage Example
```ts
client.accounts.get({ username: 'oliver' }
.then(res => {
console.log(res.data);
});
```

___

###  getMultisignatureGroups

● **getMultisignatureGroups**: *[APIHandler](../globals.md#apihandler)*

*Defined in [resources/accounts.ts:46](url)*

Searches for the specified account in the system and responds with a list of the multisignature groups that this account is a member of.

### Usage Example
```ts
client.accounts.getMultisignatureGroups('15434119221255134066L')
.then(res => {
console.log(res.data);
});
```

___

###  getMultisignatureMemberships

● **getMultisignatureMemberships**: *[APIHandler](../globals.md#apihandler)*

*Defined in [resources/accounts.ts:59](url)*

Searches for the specified multisignature group and responds with a list of all members of this particular multisignature group.

### Usage Example
```ts
client.accounts.getMultisignatureMemberships('15434119221255134066L')
.then(res => {
console.log(res.data);
});
```

___

###  path

● **path**: *string*

*Overrides [APIResource](apiresource.md).[path](apiresource.md#path)*

*Defined in [resources/accounts.ts:60](url)*

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