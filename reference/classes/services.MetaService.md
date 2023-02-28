[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / MetaService

# Class: MetaService

[services](../modules/services.md).MetaService

## Table of contents

### Constructors

- [constructor](services.MetaService.md#constructor)

### Properties

- [accountability](services.MetaService.md#accountability)
- [knex](services.MetaService.md#knex)
- [schema](services.MetaService.md#schema)

### Methods

- [filterCount](services.MetaService.md#filtercount)
- [getMetaForQuery](services.MetaService.md#getmetaforquery)
- [totalCount](services.MetaService.md#totalcount)

## Constructors

### constructor

• **new MetaService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/meta.ts:13](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/meta.ts#L13)

## Properties

### accountability

• **accountability**: `any`

#### Defined in

[api/src/services/meta.ts:10](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/meta.ts#L10)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/meta.ts:9](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/meta.ts#L9)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/meta.ts:11](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/meta.ts#L11)

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

[api/src/services/meta.ts:58](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/meta.ts#L58)

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

[api/src/services/meta.ts:20](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/meta.ts#L20)

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

[api/src/services/meta.ts:38](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/meta.ts#L38)
