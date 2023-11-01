[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > ExtensionsService

# Class: ExtensionsService

## Constructors

### constructor()

> **new ExtensionsService**(`options`): [`ExtensionsService`](class.ExtensionsService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`ExtensionsService`](class.ExtensionsService.md)

#### Source

[api/src/services/extensions.ts:31](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L31)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/extensions.ts:24](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L24)

---

### extensionsItemService

> **extensionsItemService**: [`ItemsService`](class.ItemsService.md)\< `ExtensionSettings` \>

#### Source

[api/src/services/extensions.ts:26](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L26)

---

### extensionsManager

> **extensionsManager**: `ExtensionManager`

#### Source

[api/src/services/extensions.ts:29](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L29)

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

[api/src/services/extensions.ts:28](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L28)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/extensions.ts:21](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L21)

---

### permissionsService

> **permissionsService**: [`PermissionsService`](class.PermissionsService.md)

#### Source

[api/src/services/extensions.ts:22](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L22)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/extensions.ts:25](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L25)

---

### schemaInspector

> **schemaInspector**: `SchemaInspector`

#### Source

[api/src/services/extensions.ts:23](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L23)

---

### systemCache

> **systemCache**: `Keyv`\< `any`, `Record`\< `string`, `unknown` \> \>

#### Source

[api/src/services/extensions.ts:27](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L27)

## Methods

### getKey()

> `private` **getKey**(`bundle`, `name`): `string`

#### Parameters

| Parameter | Type               |
| :-------- | :----------------- |
| `bundle`  | `null` \| `string` |
| `name`    | `string`           |

#### Returns

`string`

#### Source

[api/src/services/extensions.ts:103](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L103)

---

### readAll()

> **readAll**(): `Promise`\< `ApiOutput`[] \>

#### Returns

`Promise`\< `ApiOutput`[] \>

#### Source

[api/src/services/extensions.ts:49](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L49)

---

### readOne()

> **readOne**(`bundle`, `name`): `Promise`\< `any` \>

#### Parameters

| Parameter | Type               |
| :-------- | :----------------- |
| `bundle`  | `null` \| `string` |
| `name`    | `string`           |

#### Returns

`Promise`\< `any` \>

#### Source

[api/src/services/extensions.ts:60](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L60)

---

### stitch()

> `private` **stitch**(`installed`, `configured`): `ApiOutput`[]

Combine the settings stored in the database with the information available from the installed extensions into the
standardized extensions api output

#### Parameters

| Parameter    | Type                  |
| :----------- | :-------------------- |
| `installed`  | `Extension`[]         |
| `configured` | `ExtensionSettings`[] |

#### Returns

`ApiOutput`[]

#### Source

[api/src/services/extensions.ts:111](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L111)

---

### updateOne()

> **updateOne**( `bundle`, `name`, `data`): `Promise`\< `void` \>

#### Parameters

| Parameter | Type                           |
| :-------- | :----------------------------- |
| `bundle`  | `null` \| `string`             |
| `name`    | `string`                       |
| `data`    | `DeepPartial`\< `ApiOutput` \> |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/extensions.ts:77](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/extensions.ts#L77)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
