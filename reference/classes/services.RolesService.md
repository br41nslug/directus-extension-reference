[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / RolesService

# Class: RolesService

[services](../modules/services.md).RolesService

## Hierarchy

- [`ItemsService`](services.ItemsService.md)

  ↳ **`RolesService`**

## Table of contents

### Constructors

- [constructor](services.RolesService.md#constructor)

### Properties

- [accountability](services.RolesService.md#accountability)
- [cache](services.RolesService.md#cache)
- [collection](services.RolesService.md#collection)
- [eventScope](services.RolesService.md#eventscope)
- [knex](services.RolesService.md#knex)
- [schema](services.RolesService.md#schema)

### Methods

- [checkForOtherAdminRoles](services.RolesService.md#checkforotheradminroles)
- [checkForOtherAdminUsers](services.RolesService.md#checkforotheradminusers)
- [createMany](services.RolesService.md#createmany)
- [createOne](services.RolesService.md#createone)
- [deleteByQuery](services.RolesService.md#deletebyquery)
- [deleteMany](services.RolesService.md#deletemany)
- [deleteOne](services.RolesService.md#deleteone)
- [getKeysByQuery](services.RolesService.md#getkeysbyquery)
- [readByQuery](services.RolesService.md#readbyquery)
- [readMany](services.RolesService.md#readmany)
- [readOne](services.RolesService.md#readone)
- [readSingleton](services.RolesService.md#readsingleton)
- [updateBatch](services.RolesService.md#updatebatch)
- [updateByQuery](services.RolesService.md#updatebyquery)
- [updateMany](services.RolesService.md#updatemany)
- [updateOne](services.RolesService.md#updateone)
- [upsertMany](services.RolesService.md#upsertmany)
- [upsertOne](services.RolesService.md#upsertone)
- [upsertSingleton](services.RolesService.md#upsertsingleton)

## Constructors

### constructor

• **new RolesService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Overrides

[ItemsService](services.ItemsService.md).[constructor](services.ItemsService.md#constructor)

#### Defined in

[api/src/services/roles.ts:10](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/roles.ts#L10)

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

### checkForOtherAdminRoles

▸ `Private` **checkForOtherAdminRoles**(`excludeKeys`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `excludeKeys` | `PrimaryKey`[] |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/roles.ts:14](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/roles.ts#L14)

___

### checkForOtherAdminUsers

▸ `Private` **checkForOtherAdminUsers**(`key`, `users`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `users` | `Item`[] \| `Alterations` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/roles.ts:27](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/roles.ts#L27)

___

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

#### Overrides

[ItemsService](services.ItemsService.md).[deleteByQuery](services.ItemsService.md#deletebyquery)

#### Defined in

[api/src/services/roles.ts:185](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/roles.ts#L185)

___

### deleteMany

▸ **deleteMany**(`keys`): `Promise`<`PrimaryKey`[]\>

Delete multiple items by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `keys` | `PrimaryKey`[] |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Overrides

[ItemsService](services.ItemsService.md).[deleteMany](services.ItemsService.md#deletemany)

#### Defined in

[api/src/services/roles.ts:118](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/roles.ts#L118)

___

### deleteOne

▸ **deleteOne**(`key`): `Promise`<`PrimaryKey`\>

Delete a single item by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Overrides

[ItemsService](services.ItemsService.md).[deleteOne](services.ItemsService.md#deleteone)

#### Defined in

[api/src/services/roles.ts:113](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/roles.ts#L113)

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
| `data` | `Record`<`string`, `any`\>[] |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Overrides

[ItemsService](services.ItemsService.md).[updateBatch](services.ItemsService.md#updatebatch)

#### Defined in

[api/src/services/roles.ts:84](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/roles.ts#L84)

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
| `data` | `Record`<`string`, `any`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Overrides

[ItemsService](services.ItemsService.md).[updateMany](services.ItemsService.md#updatemany)

#### Defined in

[api/src/services/roles.ts:101](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/roles.ts#L101)

___

### updateOne

▸ **updateOne**(`key`, `data`, `opts?`): `Promise`<`PrimaryKey`\>

Update a single item by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `data` | `Record`<`string`, `any`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Overrides

[ItemsService](services.ItemsService.md).[updateOne](services.ItemsService.md#updateone)

#### Defined in

[api/src/services/roles.ts:72](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/roles.ts#L72)

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
