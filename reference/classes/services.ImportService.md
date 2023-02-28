[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / ImportService

# Class: ImportService

[services](../modules/services.md).ImportService

## Table of contents

### Constructors

- [constructor](services.ImportService.md#constructor)

### Properties

- [accountability](services.ImportService.md#accountability)
- [knex](services.ImportService.md#knex)
- [schema](services.ImportService.md#schema)

### Methods

- [import](services.ImportService.md#import)
- [importCSV](services.ImportService.md#importcsv)
- [importJSON](services.ImportService.md#importjson)

## Constructors

### constructor

• **new ImportService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/import-export.ts:39](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/import-export.ts#L39)

## Properties

### accountability

• **accountability**: `any`

#### Defined in

[api/src/services/import-export.ts:36](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/import-export.ts#L36)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/import-export.ts:35](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/import-export.ts#L35)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/import-export.ts:37](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/import-export.ts#L37)

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

[api/src/services/import-export.ts:45](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/import-export.ts#L45)

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

[api/src/services/import-export.ts:117](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/import-export.ts#L117)

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

[api/src/services/import-export.ts:71](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/import-export.ts#L71)
