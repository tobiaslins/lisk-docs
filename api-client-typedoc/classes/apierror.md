> ## [@liskhq/lisk-api-client](../README.md)

[APIError](apierror.md) /

# Class: APIError

## Hierarchy

* `Error`

  * **APIError**

### Index

#### Constructors

* [constructor](apierror.md#constructor)

#### Properties

* [errno](apierror.md#errno)
* [errors](apierror.md#optional-errors)
* [message](apierror.md#message)
* [name](apierror.md#name)
* [stack](apierror.md#optional-stack)
* [Error](apierror.md#static-error)

## Constructors

###  constructor

\+ **new APIError**(`message`: string, `errno`: number, `errors?`: `ReadonlyArray<APIErrorData>`): *[APIError](apierror.md)*

*Defined in [errors.ts:10](url)*

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`message` | string | "" |
`errno` | number |  defaultErrorNo |
`errors?` | `ReadonlyArray<APIErrorData>` | - |

**Returns:** *[APIError](apierror.md)*

___

## Properties

###  errno

● **errno**: *number*

*Defined in [errors.ts:9](url)*

___

### `Optional` errors

● **errors**? : *`ReadonlyArray<APIErrorData>`*

*Defined in [errors.ts:10](url)*

___

###  message

● **message**: *string*

*Inherited from void*

Defined in /Users/mona/git/lisk-sdk/elements/lisk-api-client/node_modules/typedoc/node_modules/typescript/lib/lib.es5.d.ts:964

___

###  name

● **name**: *string*

*Inherited from void*

Defined in /Users/mona/git/lisk-sdk/elements/lisk-api-client/node_modules/typedoc/node_modules/typescript/lib/lib.es5.d.ts:963

___

### `Optional` stack

● **stack**? : *undefined | string*

*Inherited from void*

*Overrides void*

Defined in /Users/mona/git/lisk-sdk/elements/lisk-api-client/node_modules/typedoc/node_modules/typescript/lib/lib.es5.d.ts:965

___

### `Static` Error

■ **Error**: *`ErrorConstructor`*

Defined in /Users/mona/git/lisk-sdk/elements/lisk-api-client/node_modules/typedoc/node_modules/typescript/lib/lib.es5.d.ts:974

___