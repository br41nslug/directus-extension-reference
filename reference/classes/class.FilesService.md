[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > FilesService

# Class: FilesService

## Extends

- [`ItemsService`](class.ItemsService.md)

## Constructors

### constructor()

> **new FilesService**(`options`): [`FilesService`](class.FilesService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`FilesService`](class.FilesService.md)

#### Overrides

[`ItemsService`](class.ItemsService.md).[`constructor`](class.ItemsService.md#constructor)

#### Source

[api/src/services/files.ts:26](https://github.com/directus/directus/blob/67c008df3/api/src/services/files.ts#L26)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/items.ts:43](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L43)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`accountability`](class.ItemsService.md#accountability)

---

### cache

> **cache**: `null` \| `Keyv`\< `any`, `Record`\< `string`, `unknown` \> \>

#### Source

[api/src/services/items.ts:46](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L46)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`cache`](class.ItemsService.md#cache)

---

### collection

> **collection**: `string`

#### Source

[api/src/services/items.ts:41](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L41)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`collection`](class.ItemsService.md#collection)

---

### eventScope

> **eventScope**: `string`

#### Source

[api/src/services/items.ts:44](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L44)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`eventScope`](class.ItemsService.md#eventscope)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/items.ts:42](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L42)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`knex`](class.ItemsService.md#knex)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/items.ts:45](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L45)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`schema`](class.ItemsService.md#schema)

## Methods

### createMany()

> **createMany**(`data`, `opts` = `{}`): `Promise`\< `PrimaryKey`[] \>

Create multiple new items at once. Inserts all provided records sequentially wrapped in a transaction.

#### Parameters

| Parameter | Type                    |
| :-------- | :---------------------- |
| `data`    | `Partial`\< `Item` \>[] |
| `opts`    | `MutationOptions`       |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`createMany`](class.ItemsService.md#createmany)

#### Source

[api/src/services/items.ts:313](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L313)

---

### createMutationTracker()

> **createMutationTracker**(`initialCount` = `0`): [`MutationTracker`](../type-aliases/type-alias.MutationTracker.md)

#### Parameters

| Parameter      | Type     | Default value |
| :------------- | :------- | :------------ |
| `initialCount` | `number` | `0`           |

#### Returns

[`MutationTracker`](../type-aliases/type-alias.MutationTracker.md)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`createMutationTracker`](class.ItemsService.md#createmutationtracker)

#### Source

[api/src/services/items.ts:59](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L59)

---

### createOne()

> **createOne**(`data`, `opts`?): `Promise`\< `PrimaryKey` \>

Create a file (only applicable when it is not a multipart/data POST request) Useful for associating metadata with
existing file in storage

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `data`    | `Partial`\< `File` \> |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Overrides

[`ItemsService`](class.ItemsService.md).[`createOne`](class.ItemsService.md#createone)

#### Source

[api/src/services/files.ts:304](https://github.com/directus/directus/blob/67c008df3/api/src/services/files.ts#L304)

---

### deleteByQuery()

> **deleteByQuery**(`query`, `opts`?): `Promise`\< `PrimaryKey`[] \>

Delete multiple items by query

#### Parameters

| Parameter | Type              |
| :-------- | :---------------- |
| `query`   | `Query`           |
| `opts`?   | `MutationOptions` |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`deleteByQuery`](class.ItemsService.md#deletebyquery)

#### Source

[api/src/services/items.ts:824](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L824)

---

### deleteMany()

> **deleteMany**(`keys`): `Promise`\< `PrimaryKey`[] \>

Delete multiple files

#### Parameters

| Parameter | Type           |
| :-------- | :------------- |
| `keys`    | `PrimaryKey`[] |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Overrides

[`ItemsService`](class.ItemsService.md).[`deleteMany`](class.ItemsService.md#deletemany)

#### Source

[api/src/services/files.ts:324](https://github.com/directus/directus/blob/67c008df3/api/src/services/files.ts#L324)

---

### deleteOne()

> **deleteOne**(`key`): `Promise`\< `PrimaryKey` \>

Delete a file

#### Parameters

| Parameter | Type         |
| :-------- | :----------- |
| `key`     | `PrimaryKey` |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Overrides

[`ItemsService`](class.ItemsService.md).[`deleteOne`](class.ItemsService.md#deleteone)

#### Source

[api/src/services/files.ts:316](https://github.com/directus/directus/blob/67c008df3/api/src/services/files.ts#L316)

---

### getKeysByQuery()

> **getKeysByQuery**(`query`): `Promise`\< `PrimaryKey`[] \>

#### Parameters

| Parameter | Type    |
| :-------- | :------ |
| `query`   | `Query` |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`getKeysByQuery`](class.ItemsService.md#getkeysbyquery)

#### Source

[api/src/services/items.ts:76](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L76)

---

### getMetadata()

> **getMetadata**(`stream`, `allowList` = `...`): `Promise`\< `Metadata` \>

Extract metadata from a buffer's content

#### Parameters

| Parameter   | Type       |
| :---------- | :--------- |
| `stream`    | `Readable` |
| `allowList` | `any`      |

#### Returns

`Promise`\< `Metadata` \>

#### Source

[api/src/services/files.ts:142](https://github.com/directus/directus/blob/67c008df3/api/src/services/files.ts#L142)

---

### importOne()

> **importOne**(`importURL`, `body`): `Promise`\< `PrimaryKey` \>

Import a single file from an external URL

#### Parameters

| Parameter   | Type                  |
| :---------- | :-------------------- |
| `importURL` | `string`              |
| `body`      | `Partial`\< `File` \> |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Source

[api/src/services/files.ts:261](https://github.com/directus/directus/blob/67c008df3/api/src/services/files.ts#L261)

---

### readByQuery()

> **readByQuery**(`query`, `opts`?): `Promise`\< `Item`[] \>

Get items by query

#### Parameters

| Parameter | Type                                                         |
| :-------- | :----------------------------------------------------------- |
| `query`   | `Query`                                                      |
| `opts`?   | [`QueryOptions`](../type-aliases/type-alias.QueryOptions.md) |

#### Returns

`Promise`\< `Item`[] \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`readByQuery`](class.ItemsService.md#readbyquery)

#### Source

[api/src/services/items.ts:360](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L360)

---

### readMany()

> **readMany**( `keys`, `query` = `{}`, `opts`?): `Promise`\< `Item`[] \>

Get multiple items by primary keys

#### Parameters

| Parameter | Type                                                         |
| :-------- | :----------------------------------------------------------- |
| `keys`    | `PrimaryKey`[]                                               |
| `query`   | `Query`                                                      |
| `opts`?   | [`QueryOptions`](../type-aliases/type-alias.QueryOptions.md) |

#### Returns

`Promise`\< `Item`[] \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`readMany`](class.ItemsService.md#readmany)

#### Source

[api/src/services/items.ts:466](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L466)

---

### readOne()

> **readOne**( `key`, `query` = `{}`, `opts`?): `Promise`\< `Item` \>

Get single item by primary key

#### Parameters

| Parameter | Type                                                         |
| :-------- | :----------------------------------------------------------- |
| `key`     | `PrimaryKey`                                                 |
| `query`   | `Query`                                                      |
| `opts`?   | [`QueryOptions`](../type-aliases/type-alias.QueryOptions.md) |

#### Returns

`Promise`\< `Item` \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`readOne`](class.ItemsService.md#readone)

#### Source

[api/src/services/items.ts:447](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L447)

---

### readSingleton()

> **readSingleton**(`query`, `opts`?): `Promise`\< `Partial`\< `Item` \> \>

Read/treat collection as singleton

#### Parameters

| Parameter | Type                                                         |
| :-------- | :----------------------------------------------------------- |
| `query`   | `Query`                                                      |
| `opts`?   | [`QueryOptions`](../type-aliases/type-alias.QueryOptions.md) |

#### Returns

`Promise`\< `Partial`\< `Item` \> \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`readSingleton`](class.ItemsService.md#readsingleton)

#### Source

[api/src/services/items.ts:947](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L947)

---

### updateBatch()

> **updateBatch**(`data`, `opts` = `{}`): `Promise`\< `PrimaryKey`[] \>

Update multiple items in a single transaction

#### Parameters

| Parameter | Type                    |
| :-------- | :---------------------- |
| `data`    | `Partial`\< `Item` \>[] |
| `opts`    | `MutationOptions`       |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`updateBatch`](class.ItemsService.md#updatebatch)

#### Source

[api/src/services/items.ts:509](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L509)

---

### updateByQuery()

> **updateByQuery**( `query`, `data`, `opts`?): `Promise`\< `PrimaryKey`[] \>

Update multiple items by query

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `query`   | `Query`               |
| `data`    | `Partial`\< `Item` \> |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`updateByQuery`](class.ItemsService.md#updatebyquery)

#### Source

[api/src/services/items.ts:486](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L486)

---

### updateMany()

> **updateMany**( `keys`, `data`, `opts` = `{}`): `Promise`\< `PrimaryKey`[] \>

Update many items by primary key, setting all items to the same change

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `keys`    | `PrimaryKey`[]        |
| `data`    | `Partial`\< `Item` \> |
| `opts`    | `MutationOptions`     |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`updateMany`](class.ItemsService.md#updatemany)

#### Source

[api/src/services/items.ts:546](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L546)

---

### updateOne()

> **updateOne**( `key`, `data`, `opts`?): `Promise`\< `PrimaryKey` \>

Update a single item by primary key

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `key`     | `PrimaryKey`          |
| `data`    | `Partial`\< `Item` \> |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`updateOne`](class.ItemsService.md#updateone)

#### Source

[api/src/services/items.ts:498](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L498)

---

### uploadOne()

> **uploadOne**( `stream`, `data`, `primaryKey`?, `opts`?): `Promise`\< `PrimaryKey` \>

Upload a single new file to the configured storage adapter

#### Parameters

| Parameter     | Type                                            |
| :------------ | :---------------------------------------------- |
| `stream`      | `Readable`                                      |
| `data`        | `Partial`\< `File` \> & \{`storage`: `string`;} |
| `primaryKey`? | `PrimaryKey`                                    |
| `opts`?       | `MutationOptions`                               |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Source

[api/src/services/files.ts:33](https://github.com/directus/directus/blob/67c008df3/api/src/services/files.ts#L33)

---

### upsertMany()

> **upsertMany**(`payloads`, `opts` = `{}`): `Promise`\< `PrimaryKey`[] \>

Upsert many items

#### Parameters

| Parameter  | Type                    |
| :--------- | :---------------------- |
| `payloads` | `Partial`\< `Item` \>[] |
| `opts`     | `MutationOptions`       |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`upsertMany`](class.ItemsService.md#upsertmany)

#### Source

[api/src/services/items.ts:794](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L794)

---

### upsertOne()

> **upsertOne**(`payload`, `opts`?): `Promise`\< `PrimaryKey` \>

Upsert a single item

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `payload` | `Partial`\< `Item` \> |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`upsertOne`](class.ItemsService.md#upsertone)

#### Source

[api/src/services/items.ts:768](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L768)

---

### upsertSingleton()

> **upsertSingleton**(`data`, `opts`?): `Promise`\< `PrimaryKey` \>

Upsert/treat collection as singleton

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `data`    | `Partial`\< `Item` \> |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`upsertSingleton`](class.ItemsService.md#upsertsingleton)

#### Source

[api/src/services/items.ts:983](https://github.com/directus/directus/blob/67c008df3/api/src/services/items.ts#L983)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
