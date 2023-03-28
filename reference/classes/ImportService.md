[directus-monorepo](../README.md) / [Modules](../modules.md) / ImportService

# Class: ImportService

## Table of contents

### Constructors

- [constructor](ImportService.md#constructor)

### Properties

- [accountability](ImportService.md#accountability)
- [knex](ImportService.md#knex)
- [schema](ImportService.md#schema)

### Methods

- [import](ImportService.md#import)
- [importCSV](ImportService.md#importcsv)
- [importJSON](ImportService.md#importjson)

## Constructors

### constructor

• **new ImportService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/import-export.ts:39](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L39)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Defined in

[api/src/services/import-export.ts:36](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L36)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/import-export.ts:35](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L35)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/import-export.ts:37](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L37)

## Methods

### import

▸ **import**(`collection`, `mimetype`, `stream`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `mimetype` | `string` |
| `stream` | `Readable` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/import-export.ts:45](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L45)

___

### importCSV

▸ **importCSV**(`collection`, `stream`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `stream` | `Readable` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/import-export.ts:117](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L117)

___

### importJSON

▸ **importJSON**(`collection`, `stream`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `stream` | `Readable` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/import-export.ts:71](https://github.com/directus/directus/blob/953c2f95d/api/src/services/import-export.ts#L71)
