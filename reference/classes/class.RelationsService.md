[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > RelationsService

# Class: RelationsService

## Constructors

### constructor()

> **new RelationsService**(`options`): [`RelationsService`](class.RelationsService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`RelationsService`](class.RelationsService.md)

#### Source

[api/src/services/relations.ts:31](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L31)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/relations.ts:25](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L25)

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
> ##### helpers.st
>
> **st**: `GeometryHelperMySQL` \| `GeometryHelperPostgres` \| `GeometryHelperSQLite` \| `GeometryHelperOracle` \|
> `GeometryHelperMSSQL` \| `GeometryHelperRedshift`

#### Source

[api/src/services/relations.ts:29](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L29)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/relations.ts:22](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L22)

---

### permissionsService

> **permissionsService**: [`PermissionsService`](class.PermissionsService.md)

#### Source

[api/src/services/relations.ts:23](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L23)

---

### relationsItemService

> **relationsItemService**: [`ItemsService`](class.ItemsService.md)\< `RelationMeta` \>

#### Source

[api/src/services/relations.ts:27](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L27)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/relations.ts:26](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L26)

---

### schemaInspector

> **schemaInspector**: `SchemaInspector`

#### Source

[api/src/services/relations.ts:24](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L24)

---

### systemCache

> **systemCache**: `Keyv`\< `any`, `Record`\< `string`, `unknown` \> \>

#### Source

[api/src/services/relations.ts:28](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L28)

## Accessors

### hasReadAccess

> `private` `get` hasReadAccess(): `boolean`

#### Source

[api/src/services/relations.ts:451](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L451)

## Methods

### alterType()

> `private` **alterType**(`table`, `relation`): `void`

MySQL Specific

MySQL doesn't accept FKs from `int` to `int unsigned`. `knex` defaults `.increments()` to `unsigned`, but defaults
regular `int` to `int`. This means that created m2o fields have the wrong type. This step will force the m2o `int` field
into `unsigned`, but only if both types are integers, and only if we go from `int` to `int unsigned`.

#### TODO

This is a bit of a hack, and might be better of abstracted elsewhere

#### Parameters

| Parameter  | Type           |
| :--------- | :------------- |
| `table`    | `TableBuilder` |
| `relation` | `Relation`     |

#### Returns

`void`

#### Source

[api/src/services/relations.ts:569](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L569)

---

### createOne()

> **createOne**(`relation`, `opts`?): `Promise`\< `void` \>

Create a new relationship / foreign key constraint

#### Parameters

| Parameter  | Type              |
| :--------- | :---------------- |
| `relation` | `Relation`        |
| `opts`?    | `MutationOptions` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/relations.ts:133](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L133)

---

### deleteOne()

> **deleteOne**( `collection`, `field`, `opts`?): `Promise`\< `void` \>

Delete an existing relationship

#### Parameters

| Parameter    | Type              |
| :----------- | :---------------- |
| `collection` | `string`          |
| `field`      | `string`          |
| `opts`?      | `MutationOptions` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/relations.ts:365](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L365)

---

### filterForbidden()

> `private` **filterForbidden**(`relations`): `Promise`\< `Relation`[] \>

Loop over all relations and filter out the ones that contain collections/fields you don't have permissions to

#### Parameters

| Parameter   | Type         |
| :---------- | :----------- |
| `relations` | `Relation`[] |

#### Returns

`Promise`\< `Relation`[] \>

#### Source

[api/src/services/relations.ts:504](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L504)

---

### readAll()

> **readAll**(`collection`?, `opts`?): `Promise`\< `Relation`[] \>

#### Parameters

| Parameter     | Type                                                         |
| :------------ | :----------------------------------------------------------- |
| `collection`? | `string`                                                     |
| `opts`?       | [`QueryOptions`](../type-aliases/type-alias.QueryOptions.md) |

#### Returns

`Promise`\< `Relation`[] \>

#### Source

[api/src/services/relations.ts:50](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L50)

---

### readOne()

> **readOne**(`collection`, `field`): `Promise`\< `Relation` \>

#### Parameters

| Parameter    | Type     |
| :----------- | :------- |
| `collection` | `string` |
| `field`      | `string` |

#### Returns

`Promise`\< `Relation` \>

#### Source

[api/src/services/relations.ts:80](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L80)

---

### stitchRelations()

> `private` **stitchRelations**(`metaRows`, `schemaRows`): `Relation`[]

Combine raw schema foreign key information with Directus relations meta rows to form final Relation objects

#### Parameters

| Parameter    | Type             |
| :----------- | :--------------- |
| `metaRows`   | `RelationMeta`[] |
| `schemaRows` | `ForeignKey`[]   |

#### Returns

`Relation`[]

#### Source

[api/src/services/relations.ts:461](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L461)

---

### updateOne()

> **updateOne**( `collection`, `field`, `relation`, `opts`?): `Promise`\< `void` \>

Update an existing foreign key constraint

Note: You can update anything under meta, but only the `on_delete` trigger under schema

#### Parameters

| Parameter    | Type              |
| :----------- | :---------------- |
| `collection` | `string`          |
| `field`      | `string`          |
| `relation`   | `Relation`        |
| `opts`?      | `MutationOptions` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/relations.ts:248](https://github.com/directus/directus/blob/67c008df3/api/src/services/relations.ts#L248)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
