[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > CollectionsService

# Class: CollectionsService

## Constructors

### constructor()

> **new CollectionsService**(`options`): [`CollectionsService`](class.CollectionsService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`CollectionsService`](class.CollectionsService.md)

#### Source

[api/src/services/collections.ts:45](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L45)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/collections.ts:39](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L39)

---

### cache

> **cache**: `null` \| `Keyv`\< `any`, `Record`\< `string`, `unknown` \> \>

#### Source

[api/src/services/collections.ts:42](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L42)

---

### helpers

> **helpers**: `object`

#### Type declaration

> ##### helpers.date
>
> **date**: `DateHelperMySQL` \| `DateHelperDefault` \| `DateHelperSQLite` \| `DateHelperOracle` \| `DateHelperMSSQL`
>
> ##### helpers.schema
>
> **schema**: `SchemaHelperMySQL` \| `SchemaHelperDefault` \| `SchemaHelperCockroachDb` \| `SchemaHelperSQLite` \|
> `SchemaHelperOracle` \| `SchemaHelperMSSQL`
>
> ##### helpers.sequence
>
> **sequence**: `AutoIncrementHelperDefault` \| `AutoIncrementHelperPostgres`
>
> ##### helpers.st
>
> **st**: `GeometryHelperMySQL` \| `GeometryHelperPostgres` \| `GeometryHelperSQLite` \| `GeometryHelperOracle` \|
> `GeometryHelperMSSQL` \| `GeometryHelperRedshift`

#### Source

[api/src/services/collections.ts:38](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L38)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/collections.ts:37](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L37)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/collections.ts:41](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L41)

---

### schemaInspector

> **schemaInspector**: `SchemaInspector`

#### Source

[api/src/services/collections.ts:40](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L40)

---

### systemCache

> **systemCache**: `Keyv`\< `any`, `Record`\< `string`, `unknown` \> \>

#### Source

[api/src/services/collections.ts:43](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L43)

## Methods

### createMany()

> **createMany**(`payloads`, `opts`?): `Promise`\< `string`[] \>

Create multiple new collections

#### Parameters

| Parameter  | Type                                                             |
| :--------- | :--------------------------------------------------------------- |
| `payloads` | [`RawCollection`](../type-aliases/type-alias.RawCollection.md)[] |
| `opts`?    | `MutationOptions`                                                |

#### Returns

`Promise`\< `string`[] \>

#### Source

[api/src/services/collections.ts:224](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L224)

---

### createOne()

> **createOne**(`payload`, `opts`?): `Promise`\< `string` \>

Create a single new collection

#### Parameters

| Parameter | Type                                                           |
| :-------- | :------------------------------------------------------------- |
| `payload` | [`RawCollection`](../type-aliases/type-alias.RawCollection.md) |
| `opts`?   | `MutationOptions`                                              |

#### Returns

`Promise`\< `string` \>

#### Source

[api/src/services/collections.ts:60](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L60)

---

### deleteMany()

> **deleteMany**(`collectionKeys`, `opts`?): `Promise`\< `string`[] \>

Delete multiple collections by key

#### Parameters

| Parameter        | Type              |
| :--------------- | :---------------- |
| `collectionKeys` | `string`[]        |
| `opts`?          | `MutationOptions` |

#### Returns

`Promise`\< `string`[] \>

#### Source

[api/src/services/collections.ts:702](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L702)

---

### deleteOne()

> **deleteOne**(`collectionKey`, `opts`?): `Promise`\< `string` \>

Delete a single collection This will delete the table and all records within. It'll also delete any fields, presets,
activity, revisions, and permissions relating to this collection

#### Parameters

| Parameter       | Type              |
| :-------------- | :---------------- |
| `collectionKey` | `string`          |
| `opts`?         | `MutationOptions` |

#### Returns

`Promise`\< `string` \>

#### Source

[api/src/services/collections.ts:567](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L567)

---

### readByQuery()

> **readByQuery**(): `Promise`\< `Collection`[] \>

Read all collections. Currently doesn't support any query.

#### Returns

`Promise`\< `Collection`[] \>

#### Source

[api/src/services/collections.ts:274](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L274)

---

### readMany()

> **readMany**(`collectionKeys`): `Promise`\< `Collection`[] \>

Read many collections by name

#### Parameters

| Parameter        | Type       |
| :--------------- | :--------- |
| `collectionKeys` | `string`[] |

#### Returns

`Promise`\< `Collection`[] \>

#### Source

[api/src/services/collections.ts:366](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L366)

---

### readOne()

> **readOne**(`collectionKey`): `Promise`\< `Collection` \>

Get a single collection by name

#### Parameters

| Parameter       | Type     |
| :-------------- | :------- |
| `collectionKey` | `string` |

#### Returns

`Promise`\< `Collection` \>

#### Source

[api/src/services/collections.ts:355](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L355)

---

### updateBatch()

> **updateBatch**(`data`, `opts`?): `Promise`\< `string`[] \>

Update multiple collections in a single transaction

#### Parameters

| Parameter | Type                          |
| :-------- | :---------------------------- |
| `data`    | `Partial`\< `Collection` \>[] |
| `opts`?   | `MutationOptions`             |

#### Returns

`Promise`\< `string`[] \>

#### Source

[api/src/services/collections.ts:457](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L457)

---

### updateMany()

> **updateMany**( `collectionKeys`, `data`, `opts`?): `Promise`\< `string`[] \>

Update multiple collections by name

#### Parameters

| Parameter        | Type                        |
| :--------------- | :-------------------------- |
| `collectionKeys` | `string`[]                  |
| `data`           | `Partial`\< `Collection` \> |
| `opts`?          | `MutationOptions`           |

#### Returns

`Promise`\< `string`[] \>

#### Source

[api/src/services/collections.ts:518](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L518)

---

### updateOne()

> **updateOne**( `collectionKey`, `data`, `opts`?): `Promise`\< `string` \>

Update a single collection by name

#### Parameters

| Parameter       | Type                        |
| :-------------- | :-------------------------- |
| `collectionKey` | `string`                    |
| `data`          | `Partial`\< `Collection` \> |
| `opts`?         | `MutationOptions`           |

#### Returns

`Promise`\< `string` \>

#### Source

[api/src/services/collections.ts:390](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/collections.ts#L390)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
