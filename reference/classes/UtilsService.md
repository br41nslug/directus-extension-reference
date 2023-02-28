[directus-monorepo](../README.md) / [Modules](../modules.md) / UtilsService

# Class: UtilsService

## Table of contents

### Constructors

- [constructor](UtilsService.md#constructor)

### Properties

- [accountability](UtilsService.md#accountability)
- [knex](UtilsService.md#knex)
- [schema](UtilsService.md#schema)

### Methods

- [sort](UtilsService.md#sort)

## Constructors

### constructor

• **new UtilsService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/utils.ts:14](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/utils.ts#L14)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Defined in

[api/src/services/utils.ts:11](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/utils.ts#L11)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/utils.ts:10](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/utils.ts#L10)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/utils.ts:12](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/utils.ts#L12)

## Methods

### sort

▸ **sort**(`collection`, `«destructured»`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `«destructured»` | `Object` |
| › `item` | `PrimaryKey` |
| › `to` | `PrimaryKey` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/utils.ts:20](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/utils.ts#L20)
