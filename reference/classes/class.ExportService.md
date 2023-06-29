[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > ExportService

# Class: ExportService

## Constructors

### constructor()

> **new ExportService**(`options`): [`ExportService`](class.ExportService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`ExportService`](class.ExportService.md)

#### Source

[api/src/services/import-export.ts:184](https://github.com/directus/directus/blob/67c008df3/api/src/services/import-export.ts#L184)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/import-export.ts:181](https://github.com/directus/directus/blob/67c008df3/api/src/services/import-export.ts#L181)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/import-export.ts:180](https://github.com/directus/directus/blob/67c008df3/api/src/services/import-export.ts#L180)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/import-export.ts:182](https://github.com/directus/directus/blob/67c008df3/api/src/services/import-export.ts#L182)

## Methods

### exportToFile()

> **exportToFile**( `collection`, `query`, `format`, `options`?): `Promise`\< `void` \>

Export the query results as a named file. Will query in batches, and keep appending a tmp file until all the data is
retrieved. Uploads the result as a new file using the regular FilesService upload method.

#### Parameters

| Parameter       | Type                  |
| :-------------- | :-------------------- |
| `collection`    | `string`              |
| `query`         | `Query`               |
| `format`        | `ExportFormat`        |
| `options`?      | `object`              |
| `options.file`? | `Partial`\< `File` \> |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/import-export.ts:195](https://github.com/directus/directus/blob/67c008df3/api/src/services/import-export.ts#L195)

---

### transform()

> **transform**( `input`, `format`, `options`?): `string`

Transform a given input object / array to the given type

#### Parameters

| Parameter                | Type                            |
| :----------------------- | :------------------------------ |
| `input`                  | `Record`\< `string`, `any` \>[] |
| `format`                 | `ExportFormat`                  |
| `options`?               | `object`                        |
| `options.includeFooter`? | `boolean`                       |
| `options.includeHeader`? | `boolean`                       |

#### Returns

`string`

#### Source

[api/src/services/import-export.ts:323](https://github.com/directus/directus/blob/67c008df3/api/src/services/import-export.ts#L323)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
