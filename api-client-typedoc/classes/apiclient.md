> ## [@liskhq/lisk-api-client](../README.md)

[Globals](../globals.md) / [APIClient](apiclient.md) /

# Class: APIClient

The Lisk Elements API Client provides a convenient wrapper for interacting with the public API of nodes on the Lisk network.

## Installation

Add Lisk Client as a dependency of your project:

```bash
$ npm install --save @liskhq/lisk-api-client
```

## Upgrade

```bash
npm update --save @liskhq/lisk-api-client
```

## APIClient

We expose a constructor, which takes an array of nodes, and optionally an options object. For convenience, we provide helper functions for creating API clients on specific networks with a default set of nodes. We recommend using these functions unless you operate your own nodes, or have good reasons to prefer nodes provided by a third party. *If you use the generic constructor, it is your responsibility to ensure that the nodes you specify are on the correct network.*

### Syntax

```js
new APIClient(nodes, [options])
APIClient.createMainnetAPIClient([options])
APIClient.createTestnetAPIClient([options])
```

### Examples

```js
import * as APIClient from '@liskhq/lisk-api-client';

const client = new APIClient(['https://node01.lisk.io:443', 'https://node02.lisk.io:443']);
const clientWithOptions = new APIClient(
['https://node01.lisk.io:443', 'https://node02.lisk.io:443'],
{
bannedNodes: ['https://my.faultynode.io:443'],
client: {
name: 'My Lisk Client',
version: '1.2.3',
engine: 'Some custom engine',
},
nethash: '9a9813156bf1d2355da31a171e37f97dfa7568187c3fd7f9c728de8f180c19c7',
node: 'https://my.preferrednode.io:443',
randomizeNodes: false,
});

const mainnetClient = APIClient.createMainnetAPIClient();
const testnetClient = APIClient.createTestnetAPIClient();
```

## Hierarchy

* **APIClient**

### Index

#### Constructors

* [constructor](apiclient.md#constructor)

#### Properties

* [accounts](apiclient.md#accounts)
* [bannedNodes](apiclient.md#bannednodes)
* [blocks](apiclient.md#blocks)
* [currentNode](apiclient.md#currentnode)
* [dapps](apiclient.md#dapps)
* [delegates](apiclient.md#delegates)
* [headers](apiclient.md#headers)
* [node](apiclient.md#node)
* [nodes](apiclient.md#nodes)
* [peers](apiclient.md#peers)
* [randomizeNodes](apiclient.md#randomizenodes)
* [signatures](apiclient.md#signatures)
* [transactions](apiclient.md#transactions)
* [voters](apiclient.md#voters)
* [votes](apiclient.md#votes)

#### Accessors

* [constants](apiclient.md#static-constants)

#### Methods

* [banActiveNode](apiclient.md#banactivenode)
* [banActiveNodeAndSelect](apiclient.md#banactivenodeandselect)
* [banNode](apiclient.md#bannode)
* [getNewNode](apiclient.md#getnewnode)
* [hasAvailableNodes](apiclient.md#hasavailablenodes)
* [initialize](apiclient.md#initialize)
* [isBanned](apiclient.md#isbanned)
* [createMainnetAPIClient](apiclient.md#static-createmainnetapiclient)
* [createTestnetAPIClient](apiclient.md#static-createtestnetapiclient)

## Constructors

###  constructor

\+ **new APIClient**(`nodes`: `ReadonlyArray<string>`, `providedOptions`: [InitOptions](../interfaces/initoptions.md)): *[APIClient](apiclient.md)*

*Defined in [api_client.ts:173](url)*

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`nodes` | `ReadonlyArray<string>` | - |
`providedOptions` | [InitOptions](../interfaces/initoptions.md) |  {} |

**Returns:** *[APIClient](apiclient.md)*

___

## Properties

###  accounts

● **accounts**: *[AccountsResource](accountsresource.md)*

*Defined in [api_client.ts:159](url)*

___

###  bannedNodes

● **bannedNodes**: *`ReadonlyArray<string>`*

*Defined in [api_client.ts:160](url)*

___

###  blocks

● **blocks**: *[BlocksResource](blocksresource.md)*

*Defined in [api_client.ts:161](url)*

___

###  currentNode

● **currentNode**: *string*

*Defined in [api_client.ts:162](url)*

___

###  dapps

● **dapps**: *[DappsResource](dappsresource.md)*

*Defined in [api_client.ts:163](url)*

___

###  delegates

● **delegates**: *[DelegatesResource](delegatesresource.md)*

*Defined in [api_client.ts:164](url)*

___

###  headers

● **headers**: *[HashMap](../interfaces/hashmap.md)*

*Defined in [api_client.ts:165](url)*

___

###  node

● **node**: *[NodeResource](noderesource.md)*

*Defined in [api_client.ts:166](url)*

___

###  nodes

● **nodes**: *`ReadonlyArray<string>`*

*Defined in [api_client.ts:167](url)*

___

###  peers

● **peers**: *[PeersResource](peersresource.md)*

*Defined in [api_client.ts:168](url)*

___

###  randomizeNodes

● **randomizeNodes**: *boolean*

*Defined in [api_client.ts:169](url)*

___

###  signatures

● **signatures**: *[SignaturesResource](signaturesresource.md)*

*Defined in [api_client.ts:170](url)*

___

###  transactions

● **transactions**: *[TransactionsResource](transactionsresource.md)*

*Defined in [api_client.ts:171](url)*

___

###  voters

● **voters**: *[VotersResource](votersresource.md)*

*Defined in [api_client.ts:172](url)*

___

###  votes

● **votes**: *[VotesResource](votesresource.md)*

*Defined in [api_client.ts:173](url)*

___

## Accessors

### `Static` constants

● **get constants**(): *`"/Users/mona/git/lisk-sdk/elements/lisk-api-client/src/constants"`*

*Defined in [api_client.ts:141](url)*

## Constants

API-specific constants are available via the `APIClient` constructor, and include relevant HTTP methods and lists of default nodes.

### Examples

```js
import APIClient from '@liskhq/lisk-api-client';

APIClient.constants.GET; // 'GET'
APIClient.constants.POST; // 'POST'
APIClient.constants.PUT; // 'PUT'

APIClient.constants.TESTNET_NETHASH; // Nethash for Testnet.
APIClient.constants.MAINNET_NETHASH; // Nethash for Mainnet.

APIClient.constants.TESTNET_NODES; // Array of default Testnet nodes.
APIClient.constants.MAINNET_NODES; // Array of default Mainnet nodes.
```

**Returns:** *`"/Users/mona/git/lisk-sdk/elements/lisk-api-client/src/constants"`*

___

## Methods

###  banActiveNode

▸ **banActiveNode**(): *boolean*

*Defined in [api_client.ts:192](url)*

**Returns:** *boolean*

___

###  banActiveNodeAndSelect

▸ **banActiveNodeAndSelect**(): *boolean*

*Defined in [api_client.ts:205](url)*

Bans the current node and selects a new random (non-banned) node.

### Usage Exmaple

```ts
client.banActiveNodeAndSelect()
```

**Returns:** *boolean*

___

###  banNode

▸ **banNode**(`node`: string): *boolean*

*Defined in [api_client.ts:223](url)*

Adds a node to the list of banned nodes. Banned nodes will not be chosen to replace an unreachable node.

### Usage Exmaple

```ts
client.banNode('https://my.faultynode.io:443');
```

**Parameters:**

Name | Type |
------ | ------ |
`node` | string |

**Returns:** *boolean*

___

###  getNewNode

▸ **getNewNode**(): *string*

*Defined in [api_client.ts:242](url)*

Selects a random node that has not been banned.

### Usage Exmaple

```ts
const randomNode = client.getNewNode();
```

**Returns:** *string*

___

###  hasAvailableNodes

▸ **hasAvailableNodes**(): *boolean*

*Defined in [api_client.ts:265](url)*

Tells you whether all the nodes have been banned or not.

### Usage Exmaple

```ts
const moreNodesNeeded = !client.hasAvailableNodes();
```

**Returns:** *boolean*

___

###  initialize

▸ **initialize**(`nodes`: `ReadonlyArray<string>`, `providedOptions`: [InitOptions](../interfaces/initoptions.md)): *void*

*Defined in [api_client.ts:293](url)*

Initialises the client instance with an array of nodes and an optional configuration object.
This is called in the constructor, but can be called again later if necessary.
(Note that in practice it is usually easier just to create a new instance.)

### Usage Exmaple

```ts
client.initialize(['https://node01.lisk.io:443', 'https://node02.lisk.io:443']);
client.initialize(
['https://node01.lisk.io:443', 'https://node02.lisk.io:443'],
{
bannedNodes: ['https://my.faultynode.io:443'],
client: {
name: 'My Lisk Client',
version: '1.2.3',
engine: 'Some custom engine',
},
nethash: '9a9813156bf1d2355da31a171e37f97dfa7568187c3fd7f9c728de8f180c19c7',
node: 'https://my.preferrednode.io:443',
randomizeNodes: false,
});
```

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`nodes` | `ReadonlyArray<string>` | - |
`providedOptions` | [InitOptions](../interfaces/initoptions.md) |  {} |

**Returns:** *void*

___

###  isBanned

▸ **isBanned**(`node`: string): *boolean*

*Defined in [api_client.ts:330](url)*

Tells you whether a specific node has been banned or not.

### Usage Exmaple

```ts
const banned = client.isBanned('https://node01.lisk.io:443');
```

**Parameters:**

Name | Type |
------ | ------ |
`node` | string |

**Returns:** *boolean*

___

### `Static` createMainnetAPIClient

▸ **createMainnetAPIClient**(`options?`: [InitOptions](../interfaces/initoptions.md)): *[APIClient](apiclient.md)*

*Defined in [api_client.ts:145](url)*

**Parameters:**

Name | Type |
------ | ------ |
`options?` | [InitOptions](../interfaces/initoptions.md) |

**Returns:** *[APIClient](apiclient.md)*

___

### `Static` createTestnetAPIClient

▸ **createTestnetAPIClient**(`options?`: [InitOptions](../interfaces/initoptions.md)): *[APIClient](apiclient.md)*

*Defined in [api_client.ts:152](url)*

**Parameters:**

Name | Type |
------ | ------ |
`options?` | [InitOptions](../interfaces/initoptions.md) |

**Returns:** *[APIClient](apiclient.md)*

___