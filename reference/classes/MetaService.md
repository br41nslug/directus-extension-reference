[directus-monorepo](../README.md) / [Modules](../modules.md) / MetaService

# Class: MetaService

## Table of contents

### Constructors

- [constructor](MetaService.md#constructor)

### Properties

- [accountability](MetaService.md#accountability)
- [knex](MetaService.md#knex)
- [schema](MetaService.md#schema)

### Methods

- [filterCount](MetaService.md#filtercount)
- [getMetaForQuery](MetaService.md#getmetaforquery)
- [totalCount](MetaService.md#totalcount)

## Constructors

### constructor

• **new MetaService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/meta.ts:13](https://github.com/directus/directus/blob/953c2f95d/api/src/services/meta.ts#L13)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Defined in

[api/src/services/meta.ts:10](https://github.com/directus/directus/blob/953c2f95d/api/src/services/meta.ts#L10)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/meta.ts:9](https://github.com/directus/directus/blob/953c2f95d/api/src/services/meta.ts#L9)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/meta.ts:11](https://github.com/directus/directus/blob/953c2f95d/api/src/services/meta.ts#L11)

## Methods

### filterCount

▸ **filterCount**(`collection`, `query`): `Promise`<`number`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `query` | `Query` |

#### Returns

`Promise`<`number`\>

#### Defined in

[api/src/services/meta.ts:59](https://github.com/directus/directus/blob/953c2f95d/api/src/services/meta.ts#L59)

___

### getMetaForQuery

▸ **getMetaForQuery**(`collection`, `query`): `Promise`<`undefined` \| `Record`<`string`, `any`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `query` | `any` |

#### Returns

`Promise`<`undefined` \| `Record`<`string`, `any`\>\>

#### Defined in

[api/src/services/meta.ts:20](https://github.com/directus/directus/blob/953c2f95d/api/src/services/meta.ts#L20)

___

### totalCount

▸ **totalCount**(`collection`): `Promise`<`number`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |

#### Returns

`Promise`<`number`\>

#### Defined in

[api/src/services/meta.ts:39](https://github.com/directus/directus/blob/953c2f95d/api/src/services/meta.ts#L39)
