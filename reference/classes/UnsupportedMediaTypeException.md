[directus-monorepo](../README.md) / [Modules](../modules.md) / UnsupportedMediaTypeException

# Class: UnsupportedMediaTypeException

## Hierarchy

- `BaseException`

  ↳ **`UnsupportedMediaTypeException`**

## Table of contents

### Constructors

- [constructor](UnsupportedMediaTypeException.md#constructor)

### Properties

- [code](UnsupportedMediaTypeException.md#code)
- [extensions](UnsupportedMediaTypeException.md#extensions)
- [message](UnsupportedMediaTypeException.md#message)
- [name](UnsupportedMediaTypeException.md#name)
- [stack](UnsupportedMediaTypeException.md#stack)
- [status](UnsupportedMediaTypeException.md#status)
- [prepareStackTrace](UnsupportedMediaTypeException.md#preparestacktrace)
- [stackTraceLimit](UnsupportedMediaTypeException.md#stacktracelimit)

### Methods

- [captureStackTrace](UnsupportedMediaTypeException.md#capturestacktrace)

## Constructors

### constructor

• **new UnsupportedMediaTypeException**(`message`, `extensions?`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `message` | `string` |
| `extensions?` | `Record`<`string`, `unknown`\> |

#### Overrides

BaseException.constructor

#### Defined in

[api/src/exceptions/unsupported-media-type.ts:4](https://github.com/directus/directus/blob/9368dbd0c/api/src/exceptions/unsupported-media-type.ts#L4)

## Properties

### code

• **code**: `string`

#### Inherited from

BaseException.code

#### Defined in

packages/shared/dist/cjs/exceptions/base.d.ts:3

___

### extensions

• **extensions**: `Record`<`string`, `any`\>

#### Inherited from

BaseException.extensions

#### Defined in

packages/shared/dist/cjs/exceptions/base.d.ts:4

___

### message

• **message**: `string`

#### Inherited from

BaseException.message

#### Defined in

node_modules/.pnpm/typescript@4.9.5/node_modules/typescript/lib/lib.es5.d.ts:1054

___

### name

• **name**: `string`

#### Inherited from

BaseException.name

#### Defined in

node_modules/.pnpm/typescript@4.9.5/node_modules/typescript/lib/lib.es5.d.ts:1053

___

### stack

• `Optional` **stack**: `string`

#### Inherited from

BaseException.stack

#### Defined in

node_modules/.pnpm/typescript@4.9.5/node_modules/typescript/lib/lib.es5.d.ts:1055

___

### status

• **status**: `number`

#### Inherited from

BaseException.status

#### Defined in

packages/shared/dist/cjs/exceptions/base.d.ts:2

___

### prepareStackTrace

▪ `Static` `Optional` **prepareStackTrace**: (`err`: `Error`, `stackTraces`: `CallSite`[]) => `any`

#### Type declaration

▸ (`err`, `stackTraces`): `any`

Optional override for formatting stack traces

**`See`**

https://v8.dev/docs/stack-trace-api#customizing-stack-traces

##### Parameters

| Name | Type |
| :------ | :------ |
| `err` | `Error` |
| `stackTraces` | `CallSite`[] |

##### Returns

`any`

#### Inherited from

BaseException.prepareStackTrace

#### Defined in

node_modules/.pnpm/@types+node@18.13.0/node_modules/@types/node/globals.d.ts:11

___

### stackTraceLimit

▪ `Static` **stackTraceLimit**: `number`

#### Inherited from

BaseException.stackTraceLimit

#### Defined in

node_modules/.pnpm/@types+node@18.13.0/node_modules/@types/node/globals.d.ts:13

## Methods

### captureStackTrace

▸ `Static` **captureStackTrace**(`targetObject`, `constructorOpt?`): `void`

Create .stack property on a target object

#### Parameters

| Name | Type |
| :------ | :------ |
| `targetObject` | `object` |
| `constructorOpt?` | `Function` |

#### Returns

`void`

#### Inherited from

BaseException.captureStackTrace

#### Defined in

node_modules/.pnpm/@types+node@18.13.0/node_modules/@types/node/globals.d.ts:4