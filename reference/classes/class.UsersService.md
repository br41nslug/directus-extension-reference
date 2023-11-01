[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > UsersService

# Class: UsersService

## Extends

- [`ItemsService`](class.ItemsService.md)

## Constructors

### constructor()

> **new UsersService**(`options`): [`UsersService`](class.UsersService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`UsersService`](class.UsersService.md)

#### Overrides

[`ItemsService`](class.ItemsService.md).[`constructor`](class.ItemsService.md#constructor)

#### Source

[api/src/services/users.ts:22](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L22)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/items.ts:43](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L43)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`accountability`](class.ItemsService.md#accountability)

---

### cache

> **cache**: `null` \| `Keyv`\< `any`, `Record`\< `string`, `unknown` \> \>

#### Source

[api/src/services/items.ts:46](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L46)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`cache`](class.ItemsService.md#cache)

---

### collection

> **collection**: `string`

#### Source

[api/src/services/items.ts:41](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L41)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`collection`](class.ItemsService.md#collection)

---

### eventScope

> **eventScope**: `string`

#### Source

[api/src/services/items.ts:44](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L44)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`eventScope`](class.ItemsService.md#eventscope)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/items.ts:42](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L42)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`knex`](class.ItemsService.md#knex)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/items.ts:45](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L45)

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`schema`](class.ItemsService.md#schema)

## Methods

### acceptInvite()

> **acceptInvite**(`token`, `password`): `Promise`\< `void` \>

#### Parameters

| Parameter  | Type     |
| :--------- | :------- |
| `token`    | `string` |
| `password` | `string` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/users.ts:410](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L410)

---

### checkPasswordPolicy()

> `private` **checkPasswordPolicy**(`passwords`): `Promise`\< `void` \>

Check if the provided password matches the strictness as configured in directus_settings.auth_password_policy

#### Parameters

| Parameter   | Type       |
| :---------- | :--------- |
| `passwords` | `string`[] |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/users.ts:69](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L69)

---

### checkRemainingActiveAdmin()

> `private` **checkRemainingActiveAdmin**(`excludeKeys`): `Promise`\< `void` \>

Make sure there's at least one active admin user when updating user status

#### Parameters

| Parameter     | Type           |
| :------------ | :------------- |
| `excludeKeys` | `PrimaryKey`[] |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/users.ts:122](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L122)

---

### checkRemainingAdminExistence()

> `private` **checkRemainingAdminExistence**(`excludeKeys`): `Promise`\< `void` \>

#### Parameters

| Parameter     | Type           |
| :------------ | :------------- |
| `excludeKeys` | `PrimaryKey`[] |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/users.ts:102](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L102)

---

### checkUniqueEmails()

> `private` **checkUniqueEmails**(`emails`, `excludeKey`?): `Promise`\< `void` \>

User email has to be unique case-insensitive. This is an additional check to make sure that the email is unique
regardless of casing

#### Parameters

| Parameter     | Type         |
| :------------ | :----------- |
| `emails`      | `string`[]   |
| `excludeKey`? | `PrimaryKey` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/users.ts:34](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L34)

---

### createMany()

> **createMany**(`data`, `opts`?): `Promise`\< `PrimaryKey`[] \>

Create multiple new users

#### Parameters

| Parameter | Type                    |
| :-------- | :---------------------- |
| `data`    | `Partial`\< `Item` \>[] |
| `opts`?   | `MutationOptions`       |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Overrides

[`ItemsService`](class.ItemsService.md).[`createMany`](class.ItemsService.md#createmany)

#### Source

[api/src/services/users.ts:194](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L194)

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

[api/src/services/items.ts:59](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L59)

---

### createOne()

> **createOne**(`data`, `opts`?): `Promise`\< `PrimaryKey` \>

Create a new user

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `data`    | `Partial`\< `Item` \> |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Overrides

[`ItemsService`](class.ItemsService.md).[`createOne`](class.ItemsService.md#createone)

#### Source

[api/src/services/users.ts:186](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L186)

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

#### Overrides

[`ItemsService`](class.ItemsService.md).[`deleteByQuery`](class.ItemsService.md#deletebyquery)

#### Source

[api/src/services/users.ts:341](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L341)

---

### deleteMany()

> **deleteMany**(`keys`, `opts`?): `Promise`\< `PrimaryKey`[] \>

Delete multiple users by primary key

#### Parameters

| Parameter | Type              |
| :-------- | :---------------- |
| `keys`    | `PrimaryKey`[]    |
| `opts`?   | `MutationOptions` |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Overrides

[`ItemsService`](class.ItemsService.md).[`deleteMany`](class.ItemsService.md#deletemany)

#### Source

[api/src/services/users.ts:326](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L326)

---

### deleteOne()

> **deleteOne**(`key`, `opts`?): `Promise`\< `PrimaryKey` \>

Delete a single user by primary key

#### Parameters

| Parameter | Type              |
| :-------- | :---------------- |
| `key`     | `PrimaryKey`      |
| `opts`?   | `MutationOptions` |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Overrides

[`ItemsService`](class.ItemsService.md).[`deleteOne`](class.ItemsService.md#deleteone)

#### Source

[api/src/services/users.ts:318](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L318)

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

[api/src/services/items.ts:76](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L76)

---

### getUserByEmail()

> `private` **getUserByEmail**(`email`): `Promise`\< \{`id`: `string`; `password`: `string`; `role`: `string`; `status`:
> `string`;} \>

Get basic information of user identified by email

#### Parameters

| Parameter | Type     |
| :-------- | :------- |
| `email`   | `string` |

#### Returns

`Promise`\< \{`id`: `string`; `password`: `string`; `role`: `string`; `status`: `string`;} \>

#### Source

[api/src/services/users.ts:142](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L142)

---

### inviteUrl()

> `private` **inviteUrl**(`email`, `url`): `string`

Create url for inviting users

#### Parameters

| Parameter | Type               |
| :-------- | :----------------- |
| `email`   | `string`           |
| `url`     | `null` \| `string` |

#### Returns

`string`

#### Source

[api/src/services/users.ts:153](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L153)

---

### inviteUser()

> **inviteUser**( `email`, `role`, `url`, `subject`?): `Promise`\< `void` \>

#### Parameters

| Parameter  | Type                   |
| :--------- | :--------------------- |
| `email`    | `string` \| `string`[] |
| `role`     | `string`               |
| `url`      | `null` \| `string`     |
| `subject`? | `null` \| `string`     |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/users.ts:360](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L360)

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

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`readMany`](class.ItemsService.md#readmany)

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

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`readOne`](class.ItemsService.md#readone)

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

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`readSingleton`](class.ItemsService.md#readsingleton)

#### Source

[api/src/services/items.ts:982](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L982)

---

### requestPasswordReset()

> **requestPasswordReset**( `email`, `url`, `subject`?): `Promise`\< `void` \>

#### Parameters

| Parameter  | Type               |
| :--------- | :----------------- |
| `email`    | `string`           |
| `url`      | `null` \| `string` |
| `subject`? | `null` \| `string` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/users.ts:433](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L433)

---

### resetPassword()

> **resetPassword**(`token`, `password`): `Promise`\< `void` \>

#### Parameters

| Parameter  | Type     |
| :--------- | :------- |
| `token`    | `string` |
| `password` | `string` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/users.ts:478](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L478)

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

#### Overrides

[`ItemsService`](class.ItemsService.md).[`updateBatch`](class.ItemsService.md#updatebatch)

#### Source

[api/src/services/users.ts:230](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L230)

---

### updateByQuery()

> **updateByQuery**( `query`, `data`, `opts`?): `Promise`\< `PrimaryKey`[] \>

Update many users by query

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `query`   | `Query`               |
| `data`    | `Partial`\< `Item` \> |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Overrides

[`ItemsService`](class.ItemsService.md).[`updateByQuery`](class.ItemsService.md#updatebyquery)

#### Source

[api/src/services/users.ts:217](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L217)

---

### updateMany()

> **updateMany**( `keys`, `data`, `opts`?): `Promise`\< `PrimaryKey`[] \>

Update many users by primary key

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `keys`    | `PrimaryKey`[]        |
| `data`    | `Partial`\< `Item` \> |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< `PrimaryKey`[] \>

#### Overrides

[`ItemsService`](class.ItemsService.md).[`updateMany`](class.ItemsService.md#updatemany)

#### Source

[api/src/services/users.ts:256](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L256)

---

### updateOne()

> **updateOne**( `key`, `data`, `opts`?): `Promise`\< `PrimaryKey` \>

Update a single user by primary key

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `key`     | `PrimaryKey`          |
| `data`    | `Partial`\< `Item` \> |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< `PrimaryKey` \>

#### Overrides

[`ItemsService`](class.ItemsService.md).[`updateOne`](class.ItemsService.md#updateone)

#### Source

[api/src/services/users.ts:225](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L225)

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

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`upsertOne`](class.ItemsService.md#upsertone)

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

#### Inherited from

[`ItemsService`](class.ItemsService.md).[`upsertSingleton`](class.ItemsService.md#upsertsingleton)

#### Source

[api/src/services/items.ts:1018](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/items.ts#L1018)

---

### validateEmail()

> `private` **validateEmail**(`input`): `void`

Validate array of emails. Intended to be used with create/update users

#### Parameters

| Parameter | Type                   |
| :-------- | :--------------------- |
| `input`   | `string` \| `string`[] |

#### Returns

`void`

#### Source

[api/src/services/users.ts:166](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/users.ts#L166)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
