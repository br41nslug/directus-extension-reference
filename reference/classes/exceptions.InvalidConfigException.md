[directus](../README.md) / [Modules](../modules.md) / [exceptions](../modules/exceptions.md) / InvalidConfigException

# Class: InvalidConfigException

[exceptions](../modules/exceptions.md).InvalidConfigException

## Hierarchy

- `unknown`

  ↳ **`InvalidConfigException`**

## Table of contents

### Constructors

- [constructor](exceptions.InvalidConfigException.md#constructor)

## Constructors

### constructor

• **new InvalidConfigException**(`message?`, `extensions?`)

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `message` | `string` | `'Invalid config'` |
| `extensions?` | `Record`<`string`, `any`\> | `undefined` |

#### Overrides

BaseException.constructor

#### Defined in

[api/src/exceptions/invalid-config.ts:4](https://github.com/directus/directus/blob/9368dbd0c/api/src/exceptions/invalid-config.ts#L4)
