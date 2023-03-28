[directus-monorepo](../README.md) / [Modules](../modules.md) / CollectionsService

# Class: CollectionsService

## Table of contents

### Constructors

- [constructor](CollectionsService.md#constructor)

### Properties

- [accountability](CollectionsService.md#accountability)
- [cache](CollectionsService.md#cache)
- [helpers](CollectionsService.md#helpers)
- [knex](CollectionsService.md#knex)
- [schema](CollectionsService.md#schema)
- [schemaInspector](CollectionsService.md#schemainspector)
- [systemCache](CollectionsService.md#systemcache)

### Methods

- [createMany](CollectionsService.md#createmany)
- [createOne](CollectionsService.md#createone)
- [deleteMany](CollectionsService.md#deletemany)
- [deleteOne](CollectionsService.md#deleteone)
- [readByQuery](CollectionsService.md#readbyquery)
- [readMany](CollectionsService.md#readmany)
- [readOne](CollectionsService.md#readone)
- [updateBatch](CollectionsService.md#updatebatch)
- [updateMany](CollectionsService.md#updatemany)
- [updateOne](CollectionsService.md#updateone)

## Constructors

### constructor

• **new CollectionsService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/collections.ts:37](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L37)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Defined in

[api/src/services/collections.ts:31](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L31)

___

### cache

• **cache**: ``null`` \| `Keyv`<`any`, `Record`<`string`, `unknown`\>\>

#### Defined in

[api/src/services/collections.ts:34](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L34)

___

### helpers

• **helpers**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `date` | `DateHelperMySQL` \| `DateHelperDefault` \| `DateHelperSQLite` \| `DateHelperOracle` \| `DateHelperMSSQL` |
| `schema` | `SchemaHelperMySQL` \| `SchemaHelperDefault` \| `SchemaHelperCockroachDb` \| `SchemaHelperSQLite` \| `SchemaHelperOracle` \| `SchemaHelperMSSQL` |
| `st` | `GeometryHelperMySQL` \| `GeometryHelperPostgres` \| `GeometryHelperSQLite` \| `GeometryHelperOracle` \| `GeometryHelperMSSQL` \| `GeometryHelperRedshift` |

#### Defined in

[api/src/services/collections.ts:30](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L30)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/collections.ts:29](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L29)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/collections.ts:33](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L33)

___

### schemaInspector

• **schemaInspector**: `SchemaInspector`

#### Defined in

[api/src/services/collections.ts:32](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L32)

___

### systemCache

• **systemCache**: `Keyv`<`any`, `Record`<`string`, `unknown`\>\>

#### Defined in

[api/src/services/collections.ts:35](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L35)

## Methods

### createMany

▸ **createMany**(`payloads`, `opts?`): `Promise`<`string`[]\>

Create multiple new collections

#### Parameters

| Name | Type |
| :------ | :------ |
| `payloads` | [`RawCollection`](../modules.md#rawcollection)[] |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`string`[]\>

#### Defined in

[api/src/services/collections.ts:189](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L189)

___

### createOne

▸ **createOne**(`payload`, `opts?`): `Promise`<`string`\>

Create a single new collection

#### Parameters

| Name | Type |
| :------ | :------ |
| `payload` | [`RawCollection`](../modules.md#rawcollection) |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`string`\>

#### Defined in

[api/src/services/collections.ts:52](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L52)

___

### deleteMany

▸ **deleteMany**(`collectionKeys`, `opts?`): `Promise`<`string`[]\>

Delete multiple collections by key

#### Parameters

| Name | Type |
| :------ | :------ |
| `collectionKeys` | `string`[] |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`string`[]\>

#### Defined in

[api/src/services/collections.ts:656](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L656)

___

### deleteOne

▸ **deleteOne**(`collectionKey`, `opts?`): `Promise`<`string`\>

Delete a single collection This will delete the table and all records within. It'll also
delete any fields, presets, activity, revisions, and permissions relating to this collection

#### Parameters

| Name | Type |
| :------ | :------ |
| `collectionKey` | `string` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`string`\>

#### Defined in

[api/src/services/collections.ts:528](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L528)

___

### readByQuery

▸ **readByQuery**(): `Promise`<`Collection`[]\>

Read all collections. Currently doesn't support any query.

#### Returns

`Promise`<`Collection`[]\>

#### Defined in

[api/src/services/collections.ts:238](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L238)

___

### readMany

▸ **readMany**(`collectionKeys`): `Promise`<`Collection`[]\>

Read many collections by name

#### Parameters

| Name | Type |
| :------ | :------ |
| `collectionKeys` | `string`[] |

#### Returns

`Promise`<`Collection`[]\>

#### Defined in

[api/src/services/collections.ts:330](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L330)

___

### readOne

▸ **readOne**(`collectionKey`): `Promise`<`Collection`\>

Get a single collection by name

#### Parameters

| Name | Type |
| :------ | :------ |
| `collectionKey` | `string` |

#### Returns

`Promise`<`Collection`\>

#### Defined in

[api/src/services/collections.ts:319](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L319)

___

### updateBatch

▸ **updateBatch**(`data`, `opts?`): `Promise`<`string`[]\>

Update multiple collections in a single transaction

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Partial`<`Collection`\>[] |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`string`[]\>

#### Defined in

[api/src/services/collections.ts:421](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L421)

___

### updateMany

▸ **updateMany**(`collectionKeys`, `data`, `opts?`): `Promise`<`string`[]\>

Update multiple collections by name

#### Parameters

| Name | Type |
| :------ | :------ |
| `collectionKeys` | `string`[] |
| `data` | `Partial`<`Collection`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`string`[]\>

#### Defined in

[api/src/services/collections.ts:479](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L479)

___

### updateOne

▸ **updateOne**(`collectionKey`, `data`, `opts?`): `Promise`<`string`\>

Update a single collection by name

#### Parameters

| Name | Type |
| :------ | :------ |
| `collectionKey` | `string` |
| `data` | `Partial`<`Collection`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`string`\>

#### Defined in

[api/src/services/collections.ts:354](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L354)
