[directus-monorepo](../README.md) / [Modules](../modules.md) / GraphQLValidationException

# Class: GraphQLValidationException

## Hierarchy

- `BaseException`

  ↳ **`GraphQLValidationException`**

## Table of contents

### Constructors

- [constructor](GraphQLValidationException.md#constructor)

### Properties

- [code](GraphQLValidationException.md#code)
- [extensions](GraphQLValidationException.md#extensions)
- [message](GraphQLValidationException.md#message)
- [name](GraphQLValidationException.md#name)
- [stack](GraphQLValidationException.md#stack)
- [status](GraphQLValidationException.md#status)
- [prepareStackTrace](GraphQLValidationException.md#preparestacktrace)
- [stackTraceLimit](GraphQLValidationException.md#stacktracelimit)

### Methods

- [captureStackTrace](GraphQLValidationException.md#capturestacktrace)

## Constructors

### constructor

• **new GraphQLValidationException**(`extensions`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `extensions` | `Record`<`string`, `any`\> |

#### Overrides

BaseException.constructor

#### Defined in

[api/src/exceptions/graphql-validation.ts:4](https://github.com/directus/directus/blob/9368dbd0c/api/src/exceptions/graphql-validation.ts#L4)

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
