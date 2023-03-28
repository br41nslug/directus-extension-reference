[directus-monorepo](../README.md) / [Modules](../modules.md) / InvalidCredentialsException

# Class: InvalidCredentialsException

## Hierarchy

- `BaseException`

  ↳ **`InvalidCredentialsException`**

## Table of contents

### Constructors

- [constructor](InvalidCredentialsException.md#constructor)

### Properties

- [cause](InvalidCredentialsException.md#cause)
- [code](InvalidCredentialsException.md#code)
- [extensions](InvalidCredentialsException.md#extensions)
- [message](InvalidCredentialsException.md#message)
- [name](InvalidCredentialsException.md#name)
- [stack](InvalidCredentialsException.md#stack)
- [status](InvalidCredentialsException.md#status)
- [prepareStackTrace](InvalidCredentialsException.md#preparestacktrace)
- [stackTraceLimit](InvalidCredentialsException.md#stacktracelimit)

### Methods

- [captureStackTrace](InvalidCredentialsException.md#capturestacktrace)

## Constructors

### constructor

• **new InvalidCredentialsException**(`message?`)

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `message` | `string` | `'Invalid user credentials.'` |

#### Overrides

BaseException.constructor

#### Defined in

[api/src/exceptions/invalid-credentials.ts:4](https://github.com/directus/directus/blob/953c2f95d/api/src/exceptions/invalid-credentials.ts#L4)

## Properties

### cause

• `Optional` **cause**: `unknown`

#### Inherited from

BaseException.cause

#### Defined in

node_modules/.pnpm/typescript@4.9.5/node_modules/typescript/lib/lib.es2022.error.d.ts:26

___

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

node_modules/.pnpm/@types+node@18.15.3/node_modules/@types/node/globals.d.ts:11

___

### stackTraceLimit

▪ `Static` **stackTraceLimit**: `number`

#### Inherited from

BaseException.stackTraceLimit

#### Defined in

node_modules/.pnpm/@types+node@18.15.3/node_modules/@types/node/globals.d.ts:13

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

node_modules/.pnpm/@types+node@18.15.3/node_modules/@types/node/globals.d.ts:4
