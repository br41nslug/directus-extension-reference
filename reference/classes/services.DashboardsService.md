[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / DashboardsService

# Class: DashboardsService

[services](../modules/services.md).DashboardsService

## Hierarchy

- [`ItemsService`](services.ItemsService.md)

  ↳ **`DashboardsService`**

## Table of contents

### Constructors

- [constructor](services.DashboardsService.md#constructor)

### Properties

- [accountability](services.DashboardsService.md#accountability)
- [cache](services.DashboardsService.md#cache)
- [collection](services.DashboardsService.md#collection)
- [eventScope](services.DashboardsService.md#eventscope)
- [knex](services.DashboardsService.md#knex)
- [schema](services.DashboardsService.md#schema)

### Methods

- [createMany](services.DashboardsService.md#createmany)
- [createOne](services.DashboardsService.md#createone)
- [deleteByQuery](services.DashboardsService.md#deletebyquery)
- [deleteMany](services.DashboardsService.md#deletemany)
- [deleteOne](services.DashboardsService.md#deleteone)
- [getKeysByQuery](services.DashboardsService.md#getkeysbyquery)
- [readByQuery](services.DashboardsService.md#readbyquery)
- [readMany](services.DashboardsService.md#readmany)
- [readOne](services.DashboardsService.md#readone)
- [readSingleton](services.DashboardsService.md#readsingleton)
- [updateBatch](services.DashboardsService.md#updatebatch)
- [updateByQuery](services.DashboardsService.md#updatebyquery)
- [updateMany](services.DashboardsService.md#updatemany)
- [updateOne](services.DashboardsService.md#updateone)
- [upsertMany](services.DashboardsService.md#upsertmany)
- [upsertOne](services.DashboardsService.md#upsertone)
- [upsertSingleton](services.DashboardsService.md#upsertsingleton)

## Constructors

### constructor

• **new DashboardsService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Overrides

[ItemsService](services.ItemsService.md).[constructor](services.ItemsService.md#constructor)

#### Defined in

[api/src/services/dashboards.ts:5](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/dashboards.ts#L5)

## Properties

### accountability

• **accountability**: `any`

#### Inherited from

[ItemsService](services.ItemsService.md).[accountability](services.ItemsService.md#accountability)

#### Defined in

[api/src/services/items.ts:36](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L36)

___

### cache

• **cache**: ``null`` \| `Keyv`<`any`, `Record`<`string`, `unknown`\>\>

#### Inherited from

[ItemsService](services.ItemsService.md).[cache](services.ItemsService.md#cache)

#### Defined in

[api/src/services/items.ts:39](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L39)

___

### collection

• **collection**: `string`

#### Inherited from

[ItemsService](services.ItemsService.md).[collection](services.ItemsService.md#collection)

#### Defined in

[api/src/services/items.ts:34](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L34)

___

### eventScope

• **eventScope**: `string`

#### Inherited from

[ItemsService](services.ItemsService.md).[eventScope](services.ItemsService.md#eventscope)

#### Defined in

[api/src/services/items.ts:37](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L37)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[knex](services.ItemsService.md#knex)

#### Defined in

[api/src/services/items.ts:35](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L35)

___

### schema

• **schema**: `SchemaOverview`

#### Inherited from

[ItemsService](services.ItemsService.md).[schema](services.ItemsService.md#schema)

#### Defined in

[api/src/services/items.ts:38](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L38)

## Methods

### createMany

▸ **createMany**(`data`, `opts?`): `Promise`<`PrimaryKey`[]\>

Create multiple new items at once. Inserts all provided records sequentially wrapped in a transaction.

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Partial`<`Item`\>[] |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[createMany](services.ItemsService.md#createmany)

#### Defined in

[api/src/services/items.ts:276](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L276)

___

### createOne

▸ **createOne**(`data`, `opts?`): `Promise`<`PrimaryKey`\>

Create a single new item.

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Partial`<`Item`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Inherited from

[ItemsService](services.ItemsService.md).[createOne](services.ItemsService.md#createone)

#### Defined in

[api/src/services/items.ts:72](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L72)

___

### deleteByQuery

▸ **deleteByQuery**(`query`, `opts?`): `Promise`<`PrimaryKey`[]\>

Delete multiple items by query

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[deleteByQuery](services.ItemsService.md#deletebyquery)

#### Defined in

[api/src/services/items.ts:766](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L766)

___

### deleteMany

▸ **deleteMany**(`keys`, `opts?`): `Promise`<`PrimaryKey`[]\>

Delete multiple items by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `keys` | `PrimaryKey`[] |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[deleteMany](services.ItemsService.md#deletemany)

#### Defined in

[api/src/services/items.ts:789](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L789)

___

### deleteOne

▸ **deleteOne**(`key`, `opts?`): `Promise`<`PrimaryKey`\>

Delete a single item by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Inherited from

[ItemsService](services.ItemsService.md).[deleteOne](services.ItemsService.md#deleteone)

#### Defined in

[api/src/services/items.ts:778](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L778)

___

### getKeysByQuery

▸ **getKeysByQuery**(`query`): `Promise`<`PrimaryKey`[]\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[getKeysByQuery](services.ItemsService.md#getkeysbyquery)

#### Defined in

[api/src/services/items.ts:52](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L52)

___

### readByQuery

▸ **readByQuery**(`query`, `opts?`): `Promise`<`Item`[]\>

Get items by query

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules/services.md#queryoptions) |

#### Returns

`Promise`<`Item`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[readByQuery](services.ItemsService.md#readbyquery)

#### Defined in

[api/src/services/items.ts:319](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L319)

___

### readMany

▸ **readMany**(`keys`, `query?`, `opts?`): `Promise`<`Item`[]\>

Get multiple items by primary keys

#### Parameters

| Name | Type |
| :------ | :------ |
| `keys` | `PrimaryKey`[] |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules/services.md#queryoptions) |

#### Returns

`Promise`<`Item`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[readMany](services.ItemsService.md#readmany)

#### Defined in

[api/src/services/items.ts:425](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L425)

___

### readOne

▸ **readOne**(`key`, `query?`, `opts?`): `Promise`<`Item`\>

Get single item by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules/services.md#queryoptions) |

#### Returns

`Promise`<`Item`\>

#### Inherited from

[ItemsService](services.ItemsService.md).[readOne](services.ItemsService.md#readone)

#### Defined in

[api/src/services/items.ts:406](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L406)

___

### readSingleton

▸ **readSingleton**(`query`, `opts?`): `Promise`<`Partial`<`Item`\>\>

Read/treat collection as singleton

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules/services.md#queryoptions) |

#### Returns

`Promise`<`Partial`<`Item`\>\>

#### Inherited from

[ItemsService](services.ItemsService.md).[readSingleton](services.ItemsService.md#readsingleton)

#### Defined in

[api/src/services/items.ts:880](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L880)

___

### updateBatch

▸ **updateBatch**(`data`, `opts?`): `Promise`<`PrimaryKey`[]\>

Update multiple items in a single transaction

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Partial`<`Item`\>[] |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[updateBatch](services.ItemsService.md#updatebatch)

#### Defined in

[api/src/services/items.ts:468](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L468)

___

### updateByQuery

▸ **updateByQuery**(`query`, `data`, `opts?`): `Promise`<`PrimaryKey`[]\>

Update multiple items by query

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `data` | `Partial`<`Item`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[updateByQuery](services.ItemsService.md#updatebyquery)

#### Defined in

[api/src/services/items.ts:445](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L445)

___

### updateMany

▸ **updateMany**(`keys`, `data`, `opts?`): `Promise`<`PrimaryKey`[]\>

Update many items by primary key, setting all items to the same change

#### Parameters

| Name | Type |
| :------ | :------ |
| `keys` | `PrimaryKey`[] |
| `data` | `Partial`<`Item`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[updateMany](services.ItemsService.md#updatemany)

#### Defined in

[api/src/services/items.ts:503](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L503)

___

### updateOne

▸ **updateOne**(`key`, `data`, `opts?`): `Promise`<`PrimaryKey`\>

Update a single item by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `data` | `Partial`<`Item`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Inherited from

[ItemsService](services.ItemsService.md).[updateOne](services.ItemsService.md#updateone)

#### Defined in

[api/src/services/items.ts:457](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L457)

___

### upsertMany

▸ **upsertMany**(`payloads`, `opts?`): `Promise`<`PrimaryKey`[]\>

Upsert many items

#### Parameters

| Name | Type |
| :------ | :------ |
| `payloads` | `Partial`<`Item`\>[] |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[upsertMany](services.ItemsService.md#upsertmany)

#### Defined in

[api/src/services/items.ts:738](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L738)

___

### upsertOne

▸ **upsertOne**(`payload`, `opts?`): `Promise`<`PrimaryKey`\>

Upsert a single item

#### Parameters

| Name | Type |
| :------ | :------ |
| `payload` | `Partial`<`Item`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Inherited from

[ItemsService](services.ItemsService.md).[upsertOne](services.ItemsService.md#upsertone)

#### Defined in

[api/src/services/items.ts:712](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L712)

___

### upsertSingleton

▸ **upsertSingleton**(`data`, `opts?`): `Promise`<`PrimaryKey`\>

Upsert/treat collection as singleton

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Partial`<`Item`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Inherited from

[ItemsService](services.ItemsService.md).[upsertSingleton](services.ItemsService.md#upsertsingleton)

#### Defined in

[api/src/services/items.ts:916](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L916)
