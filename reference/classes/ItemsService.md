[directus-monorepo](../README.md) / [Modules](../modules.md) / ItemsService

# Class: ItemsService<Item\>

## Type parameters

| Name | Type |
| :------ | :------ |
| `Item` | extends `AnyItem` = `AnyItem` |

## Hierarchy

- **`ItemsService`**

  ↳ [`ActivityService`](ActivityService.md)

  ↳ [`DashboardsService`](DashboardsService.md)

  ↳ [`FilesService`](FilesService.md)

  ↳ [`FlowsService`](FlowsService.md)

  ↳ [`FoldersService`](FoldersService.md)

  ↳ [`NotificationsService`](NotificationsService.md)

  ↳ [`OperationsService`](OperationsService.md)

  ↳ [`PanelsService`](PanelsService.md)

  ↳ [`PermissionsService`](PermissionsService.md)

  ↳ [`PresetsService`](PresetsService.md)

  ↳ [`RevisionsService`](RevisionsService.md)

  ↳ [`RolesService`](RolesService.md)

  ↳ [`SettingsService`](SettingsService.md)

  ↳ [`UsersService`](UsersService.md)

  ↳ [`WebhooksService`](WebhooksService.md)

  ↳ [`SharesService`](SharesService.md)

## Implements

- `AbstractService`

## Table of contents

### Constructors

- [constructor](ItemsService.md#constructor)

### Properties

- [accountability](ItemsService.md#accountability)
- [cache](ItemsService.md#cache)
- [collection](ItemsService.md#collection)
- [eventScope](ItemsService.md#eventscope)
- [knex](ItemsService.md#knex)
- [schema](ItemsService.md#schema)

### Methods

- [createMany](ItemsService.md#createmany)
- [createOne](ItemsService.md#createone)
- [deleteByQuery](ItemsService.md#deletebyquery)
- [deleteMany](ItemsService.md#deletemany)
- [deleteOne](ItemsService.md#deleteone)
- [getKeysByQuery](ItemsService.md#getkeysbyquery)
- [readByQuery](ItemsService.md#readbyquery)
- [readMany](ItemsService.md#readmany)
- [readOne](ItemsService.md#readone)
- [readSingleton](ItemsService.md#readsingleton)
- [updateBatch](ItemsService.md#updatebatch)
- [updateByQuery](ItemsService.md#updatebyquery)
- [updateMany](ItemsService.md#updatemany)
- [updateOne](ItemsService.md#updateone)
- [upsertMany](ItemsService.md#upsertmany)
- [upsertOne](ItemsService.md#upsertone)
- [upsertSingleton](ItemsService.md#upsertsingleton)

## Constructors

### constructor

• **new ItemsService**<`Item`\>(`collection`, `options`)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `Item` | extends `Item` = `Item` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/items.ts:41](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L41)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Implementation of

AbstractService.accountability

#### Defined in

[api/src/services/items.ts:36](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L36)

___

### cache

• **cache**: ``null`` \| `Keyv`<`any`, `Record`<`string`, `unknown`\>\>

#### Defined in

[api/src/services/items.ts:39](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L39)

___

### collection

• **collection**: `string`

#### Defined in

[api/src/services/items.ts:34](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L34)

___

### eventScope

• **eventScope**: `string`

#### Defined in

[api/src/services/items.ts:37](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L37)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Implementation of

AbstractService.knex

#### Defined in

[api/src/services/items.ts:35](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L35)

___

### schema

• **schema**: `SchemaOverview`

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

#### Implementation of

AbstractService.createMany

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

#### Implementation of

AbstractService.createOne

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

#### Implementation of

AbstractService.deleteMany

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

#### Implementation of

AbstractService.deleteOne

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
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`Item`[]\>

#### Implementation of

AbstractService.readByQuery

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
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`Item`[]\>

#### Implementation of

AbstractService.readMany

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
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`Item`\>

#### Implementation of

AbstractService.readOne

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
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`Partial`<`Item`\>\>

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

#### Implementation of

AbstractService.updateMany

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

#### Implementation of

AbstractService.updateOne

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

#### Defined in

[api/src/services/items.ts:916](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L916)
