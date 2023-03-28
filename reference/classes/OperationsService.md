[directus-monorepo](../README.md) / [Modules](../modules.md) / OperationsService

# Class: OperationsService

## Hierarchy

- [`ItemsService`](ItemsService.md)<`OperationRaw`\>

  ↳ **`OperationsService`**

## Table of contents

### Constructors

- [constructor](OperationsService.md#constructor)

### Properties

- [accountability](OperationsService.md#accountability)
- [cache](OperationsService.md#cache)
- [collection](OperationsService.md#collection)
- [eventScope](OperationsService.md#eventscope)
- [knex](OperationsService.md#knex)
- [schema](OperationsService.md#schema)

### Methods

- [createMany](OperationsService.md#createmany)
- [createOne](OperationsService.md#createone)
- [deleteByQuery](OperationsService.md#deletebyquery)
- [deleteMany](OperationsService.md#deletemany)
- [deleteOne](OperationsService.md#deleteone)
- [getKeysByQuery](OperationsService.md#getkeysbyquery)
- [readByQuery](OperationsService.md#readbyquery)
- [readMany](OperationsService.md#readmany)
- [readOne](OperationsService.md#readone)
- [readSingleton](OperationsService.md#readsingleton)
- [updateBatch](OperationsService.md#updatebatch)
- [updateByQuery](OperationsService.md#updatebyquery)
- [updateMany](OperationsService.md#updatemany)
- [updateOne](OperationsService.md#updateone)
- [upsertMany](OperationsService.md#upsertmany)
- [upsertOne](OperationsService.md#upsertone)
- [upsertSingleton](OperationsService.md#upsertsingleton)

## Constructors

### constructor

• **new OperationsService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Overrides

[ItemsService](ItemsService.md).[constructor](ItemsService.md#constructor)

#### Defined in

[api/src/services/operations.ts:7](https://github.com/directus/directus/blob/953c2f95d/api/src/services/operations.ts#L7)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Inherited from

[ItemsService](ItemsService.md).[accountability](ItemsService.md#accountability)

#### Defined in

[api/src/services/items.ts:36](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L36)

___

### cache

• **cache**: ``null`` \| `Keyv`<`any`, `Record`<`string`, `unknown`\>\>

#### Inherited from

[ItemsService](ItemsService.md).[cache](ItemsService.md#cache)

#### Defined in

[api/src/services/items.ts:39](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L39)

___

### collection

• **collection**: `string`

#### Inherited from

[ItemsService](ItemsService.md).[collection](ItemsService.md#collection)

#### Defined in

[api/src/services/items.ts:34](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L34)

___

### eventScope

• **eventScope**: `string`

#### Inherited from

[ItemsService](ItemsService.md).[eventScope](ItemsService.md#eventscope)

#### Defined in

[api/src/services/items.ts:37](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L37)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Inherited from

[ItemsService](ItemsService.md).[knex](ItemsService.md#knex)

#### Defined in

[api/src/services/items.ts:35](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L35)

___

### schema

• **schema**: `SchemaOverview`

#### Inherited from

[ItemsService](ItemsService.md).[schema](ItemsService.md#schema)

#### Defined in

[api/src/services/items.ts:38](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L38)

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

[ItemsService](ItemsService.md).[createMany](ItemsService.md#createmany)

#### Defined in

[api/src/services/operations.ts:20](https://github.com/directus/directus/blob/953c2f95d/api/src/services/operations.ts#L20)

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

[ItemsService](ItemsService.md).[createOne](ItemsService.md#createone)

#### Defined in

[api/src/services/operations.ts:11](https://github.com/directus/directus/blob/953c2f95d/api/src/services/operations.ts#L11)

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

[ItemsService](ItemsService.md).[deleteByQuery](ItemsService.md#deletebyquery)

#### Defined in

[api/src/services/items.ts:768](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L768)

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

[ItemsService](ItemsService.md).[deleteMany](ItemsService.md#deletemany)

#### Defined in

[api/src/services/operations.ts:47](https://github.com/directus/directus/blob/953c2f95d/api/src/services/operations.ts#L47)

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

[ItemsService](ItemsService.md).[deleteOne](ItemsService.md#deleteone)

#### Defined in

[api/src/services/items.ts:780](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L780)

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

[ItemsService](ItemsService.md).[getKeysByQuery](ItemsService.md#getkeysbyquery)

#### Defined in

[api/src/services/items.ts:52](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L52)

___

### readByQuery

▸ **readByQuery**(`query`, `opts?`): `Promise`<`OperationRaw`[]\>

Get items by query

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`OperationRaw`[]\>

#### Inherited from

[ItemsService](ItemsService.md).[readByQuery](ItemsService.md#readbyquery)

#### Defined in

[api/src/services/items.ts:321](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L321)

___

### readMany

▸ **readMany**(`keys`, `query?`, `opts?`): `Promise`<`OperationRaw`[]\>

Get multiple items by primary keys

#### Parameters

| Name | Type |
| :------ | :------ |
| `keys` | `PrimaryKey`[] |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`OperationRaw`[]\>

#### Inherited from

[ItemsService](ItemsService.md).[readMany](ItemsService.md#readmany)

#### Defined in

[api/src/services/items.ts:427](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L427)

___

### readOne

▸ **readOne**(`key`, `query?`, `opts?`): `Promise`<`OperationRaw`\>

Get single item by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`OperationRaw`\>

#### Inherited from

[ItemsService](ItemsService.md).[readOne](ItemsService.md#readone)

#### Defined in

[api/src/services/items.ts:408](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L408)

___

### readSingleton

▸ **readSingleton**(`query`, `opts?`): `Promise`<`Partial`<`OperationRaw`\>\>

Read/treat collection as singleton

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`Partial`<`OperationRaw`\>\>

#### Inherited from

[ItemsService](ItemsService.md).[readSingleton](ItemsService.md#readsingleton)

#### Defined in

[api/src/services/items.ts:882](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L882)

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

[ItemsService](ItemsService.md).[updateBatch](ItemsService.md#updatebatch)

#### Defined in

[api/src/services/operations.ts:29](https://github.com/directus/directus/blob/953c2f95d/api/src/services/operations.ts#L29)

___

### updateByQuery

▸ **updateByQuery**(`query`, `data`, `opts?`): `Promise`<`PrimaryKey`[]\>

Update multiple items by query

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `data` | `Partial`<`OperationRaw`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Inherited from

[ItemsService](ItemsService.md).[updateByQuery](ItemsService.md#updatebyquery)

#### Defined in

[api/src/services/items.ts:447](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L447)

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

[ItemsService](ItemsService.md).[updateMany](ItemsService.md#updatemany)

#### Defined in

[api/src/services/operations.ts:38](https://github.com/directus/directus/blob/953c2f95d/api/src/services/operations.ts#L38)

___

### updateOne

▸ **updateOne**(`key`, `data`, `opts?`): `Promise`<`PrimaryKey`\>

Update a single item by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `data` | `Partial`<`OperationRaw`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Inherited from

[ItemsService](ItemsService.md).[updateOne](ItemsService.md#updateone)

#### Defined in

[api/src/services/items.ts:459](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L459)

___

### upsertMany

▸ **upsertMany**(`payloads`, `opts?`): `Promise`<`PrimaryKey`[]\>

Upsert many items

#### Parameters

| Name | Type |
| :------ | :------ |
| `payloads` | `Partial`<`OperationRaw`\>[] |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Inherited from

[ItemsService](ItemsService.md).[upsertMany](ItemsService.md#upsertmany)

#### Defined in

[api/src/services/items.ts:740](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L740)

___

### upsertOne

▸ **upsertOne**(`payload`, `opts?`): `Promise`<`PrimaryKey`\>

Upsert a single item

#### Parameters

| Name | Type |
| :------ | :------ |
| `payload` | `Partial`<`OperationRaw`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Inherited from

[ItemsService](ItemsService.md).[upsertOne](ItemsService.md#upsertone)

#### Defined in

[api/src/services/items.ts:714](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L714)

___

### upsertSingleton

▸ **upsertSingleton**(`data`, `opts?`): `Promise`<`PrimaryKey`\>

Upsert/treat collection as singleton

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Partial`<`OperationRaw`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Inherited from

[ItemsService](ItemsService.md).[upsertSingleton](ItemsService.md#upsertsingleton)

#### Defined in

[api/src/services/items.ts:918](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L918)
