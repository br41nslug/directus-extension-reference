[directus-monorepo](../README.md) / [Modules](../modules.md) / ExportService

# Class: ExportService

## Table of contents

### Constructors

- [constructor](ExportService.md#constructor)

### Properties

- [accountability](ExportService.md#accountability)
- [knex](ExportService.md#knex)
- [schema](ExportService.md#schema)

### Methods

- [exportToFile](ExportService.md#exporttofile)
- [transform](ExportService.md#transform)

## Constructors

### constructor

• **new ExportService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/import-export.ts:182](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L182)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Defined in

[api/src/services/import-export.ts:179](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L179)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/import-export.ts:178](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L178)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/import-export.ts:180](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L180)

## Methods

### exportToFile

▸ **exportToFile**(`collection`, `query`, `format`, `options?`): `Promise`<`void`\>

Export the query results as a named file. Will query in batches, and keep appending a tmp file
until all the data is retrieved. Uploads the result as a new file using the regular
FilesService upload method.

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `query` | `Partial`<`Query`\> |
| `format` | `ExportFormat` |
| `options?` | `Object` |
| `options.file?` | `Partial`<`File`\> |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/import-export.ts:193](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L193)

___

### transform

▸ **transform**(`input`, `format`, `options?`): `string`

Transform a given input object / array to the given type

#### Parameters

| Name | Type |
| :------ | :------ |
| `input` | `Record`<`string`, `any`\>[] |
| `format` | `ExportFormat` |
| `options?` | `Object` |
| `options.includeFooter?` | `boolean` |
| `options.includeHeader?` | `boolean` |

#### Returns

`string`

#### Defined in

[api/src/services/import-export.ts:321](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L321)
