[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / FlowsService

# Class: FlowsService

[services](../modules/services.md).FlowsService

## Hierarchy

- [`ItemsService`](services.ItemsService.md)<`FlowRaw`\>

  ↳ **`FlowsService`**

## Table of contents

### Constructors

- [constructor](services.FlowsService.md#constructor)

### Properties

- [accountability](services.FlowsService.md#accountability)
- [cache](services.FlowsService.md#cache)
- [collection](services.FlowsService.md#collection)
- [eventScope](services.FlowsService.md#eventscope)
- [knex](services.FlowsService.md#knex)
- [schema](services.FlowsService.md#schema)

### Methods

- [createMany](services.FlowsService.md#createmany)
- [createOne](services.FlowsService.md#createone)
- [deleteByQuery](services.FlowsService.md#deletebyquery)
- [deleteMany](services.FlowsService.md#deletemany)
- [deleteOne](services.FlowsService.md#deleteone)
- [getKeysByQuery](services.FlowsService.md#getkeysbyquery)
- [readByQuery](services.FlowsService.md#readbyquery)
- [readMany](services.FlowsService.md#readmany)
- [readOne](services.FlowsService.md#readone)
- [readSingleton](services.FlowsService.md#readsingleton)
- [updateBatch](services.FlowsService.md#updatebatch)
- [updateByQuery](services.FlowsService.md#updatebyquery)
- [updateMany](services.FlowsService.md#updatemany)
- [updateOne](services.FlowsService.md#updateone)
- [upsertMany](services.FlowsService.md#upsertmany)
- [upsertOne](services.FlowsService.md#upsertone)
- [upsertSingleton](services.FlowsService.md#upsertsingleton)

## Constructors

### constructor

• **new FlowsService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Overrides

[ItemsService](services.ItemsService.md).[constructor](services.ItemsService.md#constructor)

#### Defined in

[api/src/services/flows.ts:7](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/flows.ts#L7)

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

#### Overrides

[ItemsService](services.ItemsService.md).[createMany](services.ItemsService.md#createmany)

#### Defined in

[api/src/services/flows.ts:20](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/flows.ts#L20)

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

#### Overrides

[ItemsService](services.ItemsService.md).[createOne](services.ItemsService.md#createone)

#### Defined in

[api/src/services/flows.ts:11](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/flows.ts#L11)

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

#### Overrides

[ItemsService](services.ItemsService.md).[deleteMany](services.ItemsService.md#deletemany)

#### Defined in

[api/src/services/flows.ts:47](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/flows.ts#L47)

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

▸ **readByQuery**(`query`, `opts?`): `Promise`<`FlowRaw`[]\>

Get items by query

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules/services.md#queryoptions) |

#### Returns

`Promise`<`FlowRaw`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[readByQuery](services.ItemsService.md#readbyquery)

#### Defined in

[api/src/services/items.ts:319](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L319)

___

### readMany

▸ **readMany**(`keys`, `query?`, `opts?`): `Promise`<`FlowRaw`[]\>

Get multiple items by primary keys

#### Parameters

| Name | Type |
| :------ | :------ |
| `keys` | `PrimaryKey`[] |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules/services.md#queryoptions) |

#### Returns

`Promise`<`FlowRaw`[]\>

#### Inherited from

[ItemsService](services.ItemsService.md).[readMany](services.ItemsService.md#readmany)

#### Defined in

[api/src/services/items.ts:425](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L425)

___

### readOne

▸ **readOne**(`key`, `query?`, `opts?`): `Promise`<`FlowRaw`\>

Get single item by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules/services.md#queryoptions) |

#### Returns

`Promise`<`FlowRaw`\>

#### Inherited from

[ItemsService](services.ItemsService.md).[readOne](services.ItemsService.md#readone)

#### Defined in

[api/src/services/items.ts:406](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L406)

___

### readSingleton

▸ **readSingleton**(`query`, `opts?`): `Promise`<`FlowRaw`\>

Read/treat collection as singleton

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules/services.md#queryoptions) |

#### Returns

`Promise`<`FlowRaw`\>

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

#### Overrides

[ItemsService](services.ItemsService.md).[updateBatch](services.ItemsService.md#updatebatch)

#### Defined in

[api/src/services/flows.ts:29](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/flows.ts#L29)

___

### updateByQuery

▸ **updateByQuery**(`query`, `data`, `opts?`): `Promise`<`PrimaryKey`[]\>

Update multiple items by query

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `data` | `FlowRaw` |
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

#### Overrides

[ItemsService](services.ItemsService.md).[updateMany](services.ItemsService.md#updatemany)

#### Defined in

[api/src/services/flows.ts:38](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/flows.ts#L38)

___

### updateOne

▸ **updateOne**(`key`, `data`, `opts?`): `Promise`<`PrimaryKey`\>

Update a single item by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `data` | `FlowRaw` |
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
| `payloads` | `FlowRaw`[] |
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
| `payload` | `FlowRaw` |
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
| `data` | `FlowRaw` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Inherited from

[ItemsService](services.ItemsService.md).[upsertSingleton](services.ItemsService.md#upsertsingleton)

#### Defined in

[api/src/services/items.ts:916](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L916)
