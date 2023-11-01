[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > ImportService

# Class: ImportService

## Constructors

### constructor()

> **new ImportService**(`options`): [`ImportService`](class.ImportService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`ImportService`](class.ImportService.md)

#### Source

[api/src/services/import-export/index.ts:40](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/import-export/index.ts#L40)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/import-export/index.ts:37](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/import-export/index.ts#L37)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/import-export/index.ts:36](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/import-export/index.ts#L36)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/import-export/index.ts:38](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/import-export/index.ts#L38)

## Methods

### import()

> **import**( `collection`, `mimetype`, `stream`): `Promise`\< `void` \>

#### Parameters

| Parameter    | Type       |
| :----------- | :--------- |
| `collection` | `string`   |
| `mimetype`   | `string`   |
| `stream`     | `Readable` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/import-export/index.ts:46](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/import-export/index.ts#L46)

---

### importCSV()

> **importCSV**(`collection`, `stream`): `Promise`\< `void` \>

#### Parameters

| Parameter    | Type       |
| :----------- | :--------- |
| `collection` | `string`   |
| `stream`     | `Readable` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/import-export/index.ts:118](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/import-export/index.ts#L118)

---

### importJSON()

> **importJSON**(`collection`, `stream`): `Promise`\< `void` \>

#### Parameters

| Parameter    | Type       |
| :----------- | :--------- |
| `collection` | `string`   |
| `stream`     | `Readable` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/import-export/index.ts:72](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/import-export/index.ts#L72)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
