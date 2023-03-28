[directus-monorepo](../README.md) / [Modules](../modules.md) / SharesService

# Class: SharesService

## Hierarchy

- [`ItemsService`](ItemsService.md)

  ↳ **`SharesService`**

## Table of contents

### Constructors

- [constructor](SharesService.md#constructor)

### Properties

- [accountability](SharesService.md#accountability)
- [authorizationService](SharesService.md#authorizationservice)
- [cache](SharesService.md#cache)
- [collection](SharesService.md#collection)
- [eventScope](SharesService.md#eventscope)
- [knex](SharesService.md#knex)
- [schema](SharesService.md#schema)

### Methods

- [createMany](SharesService.md#createmany)
- [createOne](SharesService.md#createone)
- [deleteByQuery](SharesService.md#deletebyquery)
- [deleteMany](SharesService.md#deletemany)
- [deleteOne](SharesService.md#deleteone)
- [getKeysByQuery](SharesService.md#getkeysbyquery)
- [invite](SharesService.md#invite)
- [login](SharesService.md#login)
- [readByQuery](SharesService.md#readbyquery)
- [readMany](SharesService.md#readmany)
- [readOne](SharesService.md#readone)
- [readSingleton](SharesService.md#readsingleton)
- [updateBatch](SharesService.md#updatebatch)
- [updateByQuery](SharesService.md#updatebyquery)
- [updateMany](SharesService.md#updatemany)
- [updateOne](SharesService.md#updateone)
- [upsertMany](SharesService.md#upsertmany)
- [upsertOne](SharesService.md#upsertone)
- [upsertSingleton](SharesService.md#upsertsingleton)

## Constructors

### constructor

• **new SharesService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Overrides

[ItemsService](ItemsService.md).[constructor](ItemsService.md#constructor)

#### Defined in

[api/src/services/shares.ts:26](https://github.com/directus/directus/blob/953c2f95d/api/src/services/shares.ts#L26)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Inherited from

[ItemsService](ItemsService.md).[accountability](ItemsService.md#accountability)

#### Defined in

[api/src/services/items.ts:36](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L36)

___

### authorizationService

• **authorizationService**: [`AuthorizationService`](AuthorizationService.md)

#### Defined in

[api/src/services/shares.ts:24](https://github.com/directus/directus/blob/953c2f95d/api/src/services/shares.ts#L24)

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

#### Overrides

[ItemsService](ItemsService.md).[createOne](ItemsService.md#createone)

#### Defined in

[api/src/services/shares.ts:36](https://github.com/directus/directus/blob/953c2f95d/api/src/services/shares.ts#L36)

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

### invite

▸ **invite**(`payload`): `Promise`<`void`\>

Send a link to the given share ID to the given email(s). Note: you can only send a link to a share
if you have read access to that particular share

#### Parameters

| Name | Type |
| :------ | :------ |
| `payload` | `Object` |
| `payload.emails` | `string`[] |
| `payload.share` | `PrimaryKey` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/shares.ts:122](https://github.com/directus/directus/blob/953c2f95d/api/src/services/shares.ts#L122)

___

### login

▸ **login**(`payload`): `Promise`<`LoginResult`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `payload` | `Record`<`string`, `any`\> |

#### Returns

`Promise`<`LoginResult`\>

#### Defined in

[api/src/services/shares.ts:41](https://github.com/directus/directus/blob/953c2f95d/api/src/services/shares.ts#L41)

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
