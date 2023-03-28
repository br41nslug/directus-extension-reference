[directus-monorepo](../README.md) / [Modules](../modules.md) / SettingsService

# Class: SettingsService

## Hierarchy

- [`ItemsService`](ItemsService.md)

  ↳ **`SettingsService`**

## Table of contents

### Constructors

- [constructor](SettingsService.md#constructor)

### Properties

- [accountability](SettingsService.md#accountability)
- [cache](SettingsService.md#cache)
- [collection](SettingsService.md#collection)
- [eventScope](SettingsService.md#eventscope)
- [knex](SettingsService.md#knex)
- [schema](SettingsService.md#schema)

### Methods

- [createMany](SettingsService.md#createmany)
- [createOne](SettingsService.md#createone)
- [deleteByQuery](SettingsService.md#deletebyquery)
- [deleteMany](SettingsService.md#deletemany)
- [deleteOne](SettingsService.md#deleteone)
- [getKeysByQuery](SettingsService.md#getkeysbyquery)
- [readByQuery](SettingsService.md#readbyquery)
- [readMany](SettingsService.md#readmany)
- [readOne](SettingsService.md#readone)
- [readSingleton](SettingsService.md#readsingleton)
- [updateBatch](SettingsService.md#updatebatch)
- [updateByQuery](SettingsService.md#updatebyquery)
- [updateMany](SettingsService.md#updatemany)
- [updateOne](SettingsService.md#updateone)
- [upsertMany](SettingsService.md#upsertmany)
- [upsertOne](SettingsService.md#upsertone)
- [upsertSingleton](SettingsService.md#upsertsingleton)

## Constructors

### constructor

• **new SettingsService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Overrides

[ItemsService](ItemsService.md).[constructor](ItemsService.md#constructor)

#### Defined in

[api/src/services/settings.ts:5](https://github.com/directus/directus/blob/953c2f95d/api/src/services/settings.ts#L5)

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

#### Inherited from

[ItemsService](ItemsService.md).[createMany](ItemsService.md#createmany)

#### Defined in

[api/src/services/items.ts:278](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L278)

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

[ItemsService](ItemsService.md).[createOne](ItemsService.md#createone)

#### Defined in

[api/src/services/items.ts:72](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L72)

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

#### Inherited from

[ItemsService](ItemsService.md).[deleteMany](ItemsService.md#deletemany)

#### Defined in

[api/src/services/items.ts:791](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L791)

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

▸ **readByQuery**(`query`, `opts?`): `Promise`<`Item`[]\>

Get items by query

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`Item`[]\>

#### Inherited from

[ItemsService](ItemsService.md).[readByQuery](ItemsService.md#readbyquery)

#### Defined in

[api/src/services/items.ts:321](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L321)

___

### readMany

▸ **readMany**(`keys`, `query?`, `opts?`): `Promise`<`Item`[]\>

Get multiple items by primary keys

#### Parameters

| Name | Type |
| :------ | :------ |
| `keys` | `PrimaryKey`[] |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`Item`[]\>

#### Inherited from

[ItemsService](ItemsService.md).[readMany](ItemsService.md#readmany)

#### Defined in

[api/src/services/items.ts:427](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L427)

___

### readOne

▸ **readOne**(`key`, `query?`, `opts?`): `Promise`<`Item`\>

Get single item by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`Item`\>

#### Inherited from

[ItemsService](ItemsService.md).[readOne](ItemsService.md#readone)

#### Defined in

[api/src/services/items.ts:408](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L408)

___

### readSingleton

▸ **readSingleton**(`query`, `opts?`): `Promise`<`Partial`<`Item`\>\>

Read/treat collection as singleton

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`Partial`<`Item`\>\>

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

#### Inherited from

[ItemsService](ItemsService.md).[updateBatch](ItemsService.md#updatebatch)

#### Defined in

[api/src/services/items.ts:470](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L470)

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

#### Inherited from

[ItemsService](ItemsService.md).[updateMany](ItemsService.md#updatemany)

#### Defined in

[api/src/services/items.ts:505](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L505)

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
| `payloads` | `Partial`<`Item`\>[] |
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
| `payload` | `Partial`<`Item`\> |
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
| `data` | `Partial`<`Item`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Inherited from

[ItemsService](ItemsService.md).[upsertSingleton](ItemsService.md#upsertsingleton)

#### Defined in

[api/src/services/items.ts:918](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L918)
