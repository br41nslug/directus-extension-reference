[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > FieldsService

# Class: FieldsService

## Constructors

### constructor()

> **new FieldsService**(`options`): [`FieldsService`](class.FieldsService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`FieldsService`](class.FieldsService.md)

#### Source

[api/src/services/fields.ts:39](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L39)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/fields.ts:31](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L31)

---

### cache

> **cache**: `null` \| `Keyv`\< `any`, `Record`\< `string`, `unknown` \> \>

#### Source

[api/src/services/fields.ts:36](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L36)

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

[api/src/services/fields.ts:30](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L30)

---

### itemsService

> **itemsService**: [`ItemsService`](class.ItemsService.md)\< `Item` \>

#### Source

[api/src/services/fields.ts:32](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L32)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/fields.ts:29](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L29)

---

### payloadService

> **payloadService**: [`PayloadService`](class.PayloadService.md)

#### Source

[api/src/services/fields.ts:33](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L33)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/fields.ts:35](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L35)

---

### schemaInspector

> **schemaInspector**: `SchemaInspector`

#### Source

[api/src/services/fields.ts:34](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L34)

---

### systemCache

> **systemCache**: `Keyv`\< `any`, `Record`\< `string`, `unknown` \> \>

#### Source

[api/src/services/fields.ts:37](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L37)

## Accessors

### hasReadAccess

> `private` `get` hasReadAccess(): `boolean`

#### Source

[api/src/services/fields.ts:54](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L54)

## Methods

### addColumnToTable()

> **addColumnToTable**( `table`, `field`, `alter` = `null`): `void`

#### Parameters

| Parameter | Type                 | Default value |
| :-------- | :------------------- | :------------ |
| `table`   | `CreateTableBuilder` | `undefined`   |
| `field`   | `any`                | `undefined`   |
| `alter`   | `any`                | `null`        |

#### Returns

`void`

#### Source

[api/src/services/fields.ts:665](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L665)

---

### createField()

> **createField**( `collection`, `field`, `table`?, `opts`?): `Promise`\< `void` \>

#### Parameters

| Parameter    | Type                 |
| :----------- | :------------------- |
| `collection` | `string`             |
| `field`      | `any`                |
| `table`?     | `CreateTableBuilder` |
| `opts`?      | `MutationOptions`    |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/fields.ts:249](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L249)

---

### deleteField()

> **deleteField**( `collection`, `field`, `opts`?): `Promise`\< `void` \>

#### Parameters

| Parameter    | Type              |
| :----------- | :---------------- |
| `collection` | `string`          |
| `field`      | `string`          |
| `opts`?      | `MutationOptions` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/fields.ts:499](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L499)

---

### readAll()

> **readAll**(`collection`?): `Promise`\< `Field`[] \>

#### Parameters

| Parameter     | Type     |
| :------------ | :------- |
| `collection`? | `string` |

#### Returns

`Promise`\< `Field`[] \>

#### Source

[api/src/services/fields.ts:60](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L60)

---

### readOne()

> **readOne**(`collection`, `field`): `Promise`\< `Record`\< `string`, `any` \> \>

#### Parameters

| Parameter    | Type     |
| :----------- | :------- |
| `collection` | `string` |
| `field`      | `string` |

#### Returns

`Promise`\< `Record`\< `string`, `any` \> \>

#### Source

[api/src/services/fields.ts:192](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L192)

---

### updateField()

> **updateField**( `collection`, `field`, `opts`?): `Promise`\< `string` \>

#### Parameters

| Parameter    | Type              |
| :----------- | :---------------- |
| `collection` | `string`          |
| `field`      | `RawField`        |
| `opts`?      | `MutationOptions` |

#### Returns

`Promise`\< `string` \>

#### Source

[api/src/services/fields.ts:376](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/fields.ts#L376)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
