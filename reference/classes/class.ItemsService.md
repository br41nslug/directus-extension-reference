[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > ItemsService

# Class: ItemsService`<Item>`

## Extended By

- [`ActivityService`](class.ActivityService.md)
- [`DashboardsService`](class.DashboardsService.md)
- [`FilesService`](class.FilesService.md)
- [`FlowsService`](class.FlowsService.md)
- [`FoldersService`](class.FoldersService.md)
- [`NotificationsService`](class.NotificationsService.md)
- [`OperationsService`](class.OperationsService.md)
- [`PanelsService`](class.PanelsService.md)
- [`PermissionsService`](class.PermissionsService.md)
- [`PresetsService`](class.PresetsService.md)
- [`RevisionsService`](class.RevisionsService.md)
- [`RolesService`](class.RolesService.md)
- [`SettingsService`](class.SettingsService.md)
- [`SharesService`](class.SharesService.md)
- [`TranslationsService`](class.TranslationsService.md)
- [`UsersService`](class.UsersService.md)
- [`VersionsService`](class.VersionsService.md)
- [`WebhooksService`](class.WebhooksService.md)

## Type parameters

| Parameter                  | Default   |
| :------------------------- | :-------- |
| `Item` _extends_ `AnyItem` | `AnyItem` |

## Implements

- `AbstractService`

## Constructors

### constructor()

> **new ItemsService**\<`Item`\>(`collection`, `options`): [`ItemsService`](class.ItemsService.md)\< `Item` \>

#### Type parameters

| Parameter               | Default |
| :---------------------- | :------ |
| `Item` _extends_ `Item` | `Item`  |

#### Parameters

| Parameter    | Type                     |
| :----------- | :----------------------- |
| `collection` | `string`                 |
| `options`    | `AbstractServiceOptions` |

#### Returns

[`ItemsService`](class.ItemsService.md)\< `Item` \>

#### Source

[api/src/services/items.ts:48](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L48)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/items.ts:43](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L43)

#### Implementation of

AbstractService.accountability

---

### cache

> **cache**: `null` \| `Keyv`\< `any`, `Record`\< `string`, `unknown` \> \>

#### Source

[api/src/services/items.ts:46](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L46)

---

### collection

> **collection**: `string`

#### Source

[api/src/services/items.ts:41](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L41)

---

### eventScope

> **eventScope**: `string`

#### Source

[api/src/services/items.ts:44](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L44)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/items.ts:42](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L42)

#### Implementation of

AbstractService.knex

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/items.ts:45](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L45)

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

#### Implementation of

AbstractService.createMany

#### Source

[api/src/services/items.ts:337](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L337)

---

### createMutationTracker()

> **createMutationTracker**(`initialCount` = `0`): [`MutationTracker`](../type-aliases/type-alias.MutationTracker.md)

#### Parameters

| Parameter      | Type     | Default value |
| :------------- | :------- | :------------ |
| `initialCount` | `number` | `0`           |

#### Returns

[`MutationTracker`](../type-aliases/type-alias.MutationTracker.md)

#### Source

[api/src/services/items.ts:59](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L59)

---

### createOne()

> **createOne**(`data`, `opts` = `{}`): `Promise`\< `PrimaryKey` \>

Create a single new item.

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `data`    | `Partial`\< `Item` \> |
| `opts`    | `MutationOptions`     |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Implementation of

AbstractService.createOne

#### Source

[api/src/services/items.ts:96](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L96)

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

#### Source

[api/src/services/items.ts:859](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L859)

---

### deleteMany()

> **deleteMany**(`keys`, `opts` = `{}`): `Promise`\< `PrimaryKey`[] \>

Delete multiple items by primary key

#### Parameters

| Parameter | Type              |
| :-------- | :---------------- |
| `keys`    | `PrimaryKey`[]    |
| `opts`    | `MutationOptions` |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Implementation of

AbstractService.deleteMany

#### Source

[api/src/services/items.ts:882](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L882)

---

### deleteOne()

> **deleteOne**(`key`, `opts`?): `Promise`\< `PrimaryKey` \>

Delete a single item by primary key

#### Parameters

| Parameter | Type              |
| :-------- | :---------------- |
| `key`     | `PrimaryKey`      |
| `opts`?   | `MutationOptions` |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Implementation of

AbstractService.deleteOne

#### Source

[api/src/services/items.ts:871](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L871)

---

### getKeysByQuery()

> **getKeysByQuery**(`query`): `Promise`\< `PrimaryKey`[] \>

#### Parameters

| Parameter | Type    |
| :-------- | :------ |
| `query`   | `Query` |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Source

[api/src/services/items.ts:76](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L76)

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

#### Implementation of

AbstractService.readByQuery

#### Source

[api/src/services/items.ts:395](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L395)

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

#### Implementation of

AbstractService.readMany

#### Source

[api/src/services/items.ts:501](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L501)

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

#### Implementation of

AbstractService.readOne

#### Source

[api/src/services/items.ts:482](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L482)

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

#### Source

[api/src/services/items.ts:982](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L982)

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

#### Source

[api/src/services/items.ts:544](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L544)

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

#### Source

[api/src/services/items.ts:521](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L521)

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

#### Implementation of

AbstractService.updateMany

#### Source

[api/src/services/items.ts:581](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L581)

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

#### Implementation of

AbstractService.updateOne

#### Source

[api/src/services/items.ts:533](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L533)

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

#### Source

[api/src/services/items.ts:829](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L829)

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

#### Source

[api/src/services/items.ts:803](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L803)

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

#### Source

[api/src/services/items.ts:1018](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L1018)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
