[directus-monorepo](../README.md) / [Modules](../modules.md) / FilesService

# Class: FilesService

## Hierarchy

- [`ItemsService`](ItemsService.md)

  ↳ **`FilesService`**

## Table of contents

### Constructors

- [constructor](FilesService.md#constructor)

### Properties

- [accountability](FilesService.md#accountability)
- [cache](FilesService.md#cache)
- [collection](FilesService.md#collection)
- [eventScope](FilesService.md#eventscope)
- [knex](FilesService.md#knex)
- [schema](FilesService.md#schema)

### Methods

- [createMany](FilesService.md#createmany)
- [createOne](FilesService.md#createone)
- [deleteByQuery](FilesService.md#deletebyquery)
- [deleteMany](FilesService.md#deletemany)
- [deleteOne](FilesService.md#deleteone)
- [getKeysByQuery](FilesService.md#getkeysbyquery)
- [getMetadata](FilesService.md#getmetadata)
- [importOne](FilesService.md#importone)
- [readByQuery](FilesService.md#readbyquery)
- [readMany](FilesService.md#readmany)
- [readOne](FilesService.md#readone)
- [readSingleton](FilesService.md#readsingleton)
- [updateBatch](FilesService.md#updatebatch)
- [updateByQuery](FilesService.md#updatebyquery)
- [updateMany](FilesService.md#updatemany)
- [updateOne](FilesService.md#updateone)
- [uploadOne](FilesService.md#uploadone)
- [upsertMany](FilesService.md#upsertmany)
- [upsertOne](FilesService.md#upsertone)
- [upsertSingleton](FilesService.md#upsertsingleton)

## Constructors

### constructor

• **new FilesService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Overrides

[ItemsService](ItemsService.md).[constructor](ItemsService.md#constructor)

#### Defined in

[api/src/services/files.ts:26](https://github.com/directus/directus/blob/953c2f95d/api/src/services/files.ts#L26)

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

Create a file (only applicable when it is not a multipart/data POST request)
Useful for associating metadata with existing file in storage

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Partial`<`File`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Overrides

[ItemsService](ItemsService.md).[createOne](ItemsService.md#createone)

#### Defined in

[api/src/services/files.ts:293](https://github.com/directus/directus/blob/953c2f95d/api/src/services/files.ts#L293)

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

Delete multiple files

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

[api/src/services/files.ts:313](https://github.com/directus/directus/blob/953c2f95d/api/src/services/files.ts#L313)

___

### deleteOne

▸ **deleteOne**(`key`, `opts?`): `Promise`<`PrimaryKey`\>

Delete a file

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Overrides

[ItemsService](ItemsService.md).[deleteOne](ItemsService.md#deleteone)

#### Defined in

[api/src/services/files.ts:305](https://github.com/directus/directus/blob/953c2f95d/api/src/services/files.ts#L305)

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

### getMetadata

▸ **getMetadata**(`stream`, `allowList?`): `Promise`<`Metadata`\>

Extract metadata from a buffer's content

#### Parameters

| Name | Type |
| :------ | :------ |
| `stream` | `Readable` |
| `allowList` | `any` |

#### Returns

`Promise`<`Metadata`\>

#### Defined in

[api/src/services/files.ts:143](https://github.com/directus/directus/blob/953c2f95d/api/src/services/files.ts#L143)

___

### importOne

▸ **importOne**(`importURL`, `body`): `Promise`<`PrimaryKey`\>

Import a single file from an external URL

#### Parameters

| Name | Type |
| :------ | :------ |
| `importURL` | `string` |
| `body` | `Partial`<`File`\> |

#### Returns

`Promise`<`PrimaryKey`\>

#### Defined in

[api/src/services/files.ts:252](https://github.com/directus/directus/blob/953c2f95d/api/src/services/files.ts#L252)

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

### uploadOne

▸ **uploadOne**(`stream`, `data`, `primaryKey?`, `opts?`): `Promise`<`PrimaryKey`\>

Upload a single new file to the configured storage adapter

#### Parameters

| Name | Type |
| :------ | :------ |
| `stream` | `Readable` |
| `data` | `Partial`<`File`\> & { `storage`: `string`  } |
| `primaryKey?` | `PrimaryKey` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Defined in

[api/src/services/files.ts:33](https://github.com/directus/directus/blob/953c2f95d/api/src/services/files.ts#L33)

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
