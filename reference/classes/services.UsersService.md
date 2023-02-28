[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / UsersService

# Class: UsersService

[services](../modules/services.md).UsersService

## Hierarchy

- [`ItemsService`](services.ItemsService.md)

  ↳ **`UsersService`**

## Table of contents

### Constructors

- [constructor](services.UsersService.md#constructor)

### Properties

- [accountability](services.UsersService.md#accountability)
- [cache](services.UsersService.md#cache)
- [collection](services.UsersService.md#collection)
- [eventScope](services.UsersService.md#eventscope)
- [knex](services.UsersService.md#knex)
- [schema](services.UsersService.md#schema)

### Methods

- [acceptInvite](services.UsersService.md#acceptinvite)
- [checkPasswordPolicy](services.UsersService.md#checkpasswordpolicy)
- [checkRemainingActiveAdmin](services.UsersService.md#checkremainingactiveadmin)
- [checkRemainingAdminExistence](services.UsersService.md#checkremainingadminexistence)
- [checkUniqueEmails](services.UsersService.md#checkuniqueemails)
- [createMany](services.UsersService.md#createmany)
- [createOne](services.UsersService.md#createone)
- [deleteByQuery](services.UsersService.md#deletebyquery)
- [deleteMany](services.UsersService.md#deletemany)
- [deleteOne](services.UsersService.md#deleteone)
- [getKeysByQuery](services.UsersService.md#getkeysbyquery)
- [inviteUser](services.UsersService.md#inviteuser)
- [readByQuery](services.UsersService.md#readbyquery)
- [readMany](services.UsersService.md#readmany)
- [readOne](services.UsersService.md#readone)
- [readSingleton](services.UsersService.md#readsingleton)
- [requestPasswordReset](services.UsersService.md#requestpasswordreset)
- [resetPassword](services.UsersService.md#resetpassword)
- [updateBatch](services.UsersService.md#updatebatch)
- [updateByQuery](services.UsersService.md#updatebyquery)
- [updateMany](services.UsersService.md#updatemany)
- [updateOne](services.UsersService.md#updateone)
- [upsertMany](services.UsersService.md#upsertmany)
- [upsertOne](services.UsersService.md#upsertone)
- [upsertSingleton](services.UsersService.md#upsertsingleton)

## Constructors

### constructor

• **new UsersService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Overrides

[ItemsService](services.ItemsService.md).[constructor](services.ItemsService.md#constructor)

#### Defined in

[api/src/services/users.ts:26](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L26)

## Properties

### accountability

• **accountability**: `any`

#### Overrides

[ItemsService](services.ItemsService.md).[accountability](services.ItemsService.md#accountability)

#### Defined in

[api/src/services/users.ts:23](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L23)

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

#### Overrides

[ItemsService](services.ItemsService.md).[knex](services.ItemsService.md#knex)

#### Defined in

[api/src/services/users.ts:22](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L22)

___

### schema

• **schema**: `SchemaOverview`

#### Overrides

[ItemsService](services.ItemsService.md).[schema](services.ItemsService.md#schema)

#### Defined in

[api/src/services/users.ts:24](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L24)

## Methods

### acceptInvite

▸ **acceptInvite**(`token`, `password`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `token` | `string` |
| `password` | `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/users.ts:355](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L355)

___

### checkPasswordPolicy

▸ `Private` **checkPasswordPolicy**(`passwords`): `Promise`<`void`\>

Check if the provided password matches the strictness as configured in
directus_settings.auth_password_policy

#### Parameters

| Name | Type |
| :------ | :------ |
| `passwords` | `string`[] |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/users.ts:75](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L75)

___

### checkRemainingActiveAdmin

▸ `Private` **checkRemainingActiveAdmin**(`excludeKeys`): `Promise`<`void`\>

Make sure there's at least one active admin user when updating user status

#### Parameters

| Name | Type |
| :------ | :------ |
| `excludeKeys` | `PrimaryKey`[] |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/users.ts:126](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L126)

___

### checkRemainingAdminExistence

▸ `Private` **checkRemainingAdminExistence**(`excludeKeys`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `excludeKeys` | `PrimaryKey`[] |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/users.ts:106](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L106)

___

### checkUniqueEmails

▸ `Private` **checkUniqueEmails**(`emails`, `excludeKey?`): `Promise`<`void`\>

User email has to be unique case-insensitive. This is an additional check to make sure that
the email is unique regardless of casing

#### Parameters

| Name | Type |
| :------ | :------ |
| `emails` | `string`[] |
| `excludeKey?` | `PrimaryKey` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/users.ts:38](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L38)

___

### createMany

▸ **createMany**(`data`, `opts?`): `Promise`<`PrimaryKey`[]\>

Create multiple new users

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

[api/src/services/users.ts:154](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L154)

___

### createOne

▸ **createOne**(`data`, `opts?`): `Promise`<`PrimaryKey`\>

Create a new user

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

[api/src/services/users.ts:146](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L146)

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

[api/src/services/users.ts:295](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L295)

___

### deleteMany

▸ **deleteMany**(`keys`, `opts?`): `Promise`<`PrimaryKey`[]\>

Delete multiple users by primary key

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

[api/src/services/users.ts:282](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L282)

___

### deleteOne

▸ **deleteOne**(`key`, `opts?`): `Promise`<`PrimaryKey`\>

Delete a single user by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Overrides

[ItemsService](services.ItemsService.md).[deleteOne](services.ItemsService.md#deleteone)

#### Defined in

[api/src/services/users.ts:274](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L274)

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

### inviteUser

▸ **inviteUser**(`email`, `role`, `url`, `subject?`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `email` | `string` \| `string`[] |
| `role` | `string` |
| `url` | ``null`` \| `string` |
| `subject?` | ``null`` \| `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/users.ts:314](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L314)

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

### requestPasswordReset

▸ **requestPasswordReset**(`email`, `url`, `subject?`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `email` | `string` |
| `url` | ``null`` \| `string` |
| `subject?` | ``null`` \| `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/users.ts:378](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L378)

___

### resetPassword

▸ **resetPassword**(`token`, `password`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `token` | `string` |
| `password` | `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/users.ts:425](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L425)

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

[api/src/services/users.ts:189](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L189)

___

### updateByQuery

▸ **updateByQuery**(`query`, `data`, `opts?`): `Promise`<`PrimaryKey`[]\>

Update many users by query

#### Parameters

| Name | Type |
| :------ | :------ |
| `query` | `Query` |
| `data` | `Partial`<`Item`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`[]\>

#### Overrides

[ItemsService](services.ItemsService.md).[updateByQuery](services.ItemsService.md#updatebyquery)

#### Defined in

[api/src/services/users.ts:176](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L176)

___

### updateMany

▸ **updateMany**(`keys`, `data`, `opts?`): `Promise`<`PrimaryKey`[]\>

Update many users by primary key

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

[api/src/services/users.ts:213](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L213)

___

### updateOne

▸ **updateOne**(`key`, `data`, `opts?`): `Promise`<`PrimaryKey`\>

Update a single user by primary key

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `data` | `Partial`<`Item`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`PrimaryKey`\>

#### Overrides

[ItemsService](services.ItemsService.md).[updateOne](services.ItemsService.md#updateone)

#### Defined in

[api/src/services/users.ts:184](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/users.ts#L184)

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
