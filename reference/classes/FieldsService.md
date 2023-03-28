[directus-monorepo](../README.md) / [Modules](../modules.md) / FieldsService

# Class: FieldsService

## Table of contents

### Constructors

- [constructor](FieldsService.md#constructor)

### Properties

- [accountability](FieldsService.md#accountability)
- [cache](FieldsService.md#cache)
- [helpers](FieldsService.md#helpers)
- [itemsService](FieldsService.md#itemsservice)
- [knex](FieldsService.md#knex)
- [payloadService](FieldsService.md#payloadservice)
- [schema](FieldsService.md#schema)
- [schemaInspector](FieldsService.md#schemainspector)
- [systemCache](FieldsService.md#systemcache)

### Accessors

- [hasReadAccess](FieldsService.md#hasreadaccess)

### Methods

- [addColumnToTable](FieldsService.md#addcolumntotable)
- [createField](FieldsService.md#createfield)
- [deleteField](FieldsService.md#deletefield)
- [readAll](FieldsService.md#readall)
- [readOne](FieldsService.md#readone)
- [updateField](FieldsService.md#updatefield)

## Constructors

### constructor

• **new FieldsService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/fields.ts:37](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L37)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Defined in

[api/src/services/fields.ts:29](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L29)

___

### cache

• **cache**: ``null`` \| `Keyv`<`any`, `Record`<`string`, `unknown`\>\>

#### Defined in

[api/src/services/fields.ts:34](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L34)

___

### helpers

• **helpers**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `date` | `DateHelperMySQL` \| `DateHelperDefault` \| `DateHelperSQLite` \| `DateHelperOracle` \| `DateHelperMSSQL` |
| `schema` | `SchemaHelperMySQL` \| `SchemaHelperDefault` \| `SchemaHelperCockroachDb` \| `SchemaHelperSQLite` \| `SchemaHelperOracle` \| `SchemaHelperMSSQL` |
| `st` | `GeometryHelperMySQL` \| `GeometryHelperPostgres` \| `GeometryHelperSQLite` \| `GeometryHelperOracle` \| `GeometryHelperMSSQL` \| `GeometryHelperRedshift` |

#### Defined in

[api/src/services/fields.ts:28](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L28)

___

### itemsService

• **itemsService**: [`ItemsService`](ItemsService.md)<`Item`\>

#### Defined in

[api/src/services/fields.ts:30](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L30)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/fields.ts:27](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L27)

___

### payloadService

• **payloadService**: [`PayloadService`](PayloadService.md)

#### Defined in

[api/src/services/fields.ts:31](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L31)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/fields.ts:33](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L33)

___

### schemaInspector

• **schemaInspector**: `SchemaInspector`

#### Defined in

[api/src/services/fields.ts:32](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L32)

___

### systemCache

• **systemCache**: `Keyv`<`any`, `Record`<`string`, `unknown`\>\>

#### Defined in

[api/src/services/fields.ts:35](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L35)

## Accessors

### hasReadAccess

• `Private` `get` **hasReadAccess**(): `boolean`

#### Returns

`boolean`

#### Defined in

[api/src/services/fields.ts:52](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L52)

## Methods

### addColumnToTable

▸ **addColumnToTable**(`table`, `field`, `alter?`): `void`

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `table` | `CreateTableBuilder` | `undefined` |
| `field` | `Field` \| `RawField` | `undefined` |
| `alter` | ``null`` \| `Column` | `null` |

#### Returns

`void`

#### Defined in

[api/src/services/fields.ts:644](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L644)

___

### createField

▸ **createField**(`collection`, `field`, `table?`, `opts?`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `field` | `Partial`<`Field`\> & { `field`: `string` ; `type`: ``null`` \| ``"string"`` \| ``"boolean"`` \| ``"bigInteger"`` \| ``"date"`` \| ``"dateTime"`` \| ``"decimal"`` \| ``"float"`` \| ``"integer"`` \| ``"json"`` \| ``"text"`` \| ``"time"`` \| ``"timestamp"`` \| ``"binary"`` \| ``"uuid"`` \| ``"alias"`` \| ``"hash"`` \| ``"csv"`` \| ``"geometry"`` \| ``"geometry.Point"`` \| ``"geometry.LineString"`` \| ``"geometry.Polygon"`` \| ``"geometry.MultiPoint"`` \| ``"geometry.MultiLineString"`` \| ``"geometry.MultiPolygon"`` \| ``"unknown"``  } |
| `table?` | `CreateTableBuilder` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/fields.ts:243](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L243)

___

### deleteField

▸ **deleteField**(`collection`, `field`, `opts?`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `field` | `string` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/fields.ts:478](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L478)

___

### readAll

▸ **readAll**(`collection?`): `Promise`<`Field`[]\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection?` | `string` |

#### Returns

`Promise`<`Field`[]\>

#### Defined in

[api/src/services/fields.ts:58](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L58)

___

### readOne

▸ **readOne**(`collection`, `field`): `Promise`<`Record`<`string`, `any`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `field` | `string` |

#### Returns

`Promise`<`Record`<`string`, `any`\>\>

#### Defined in

[api/src/services/fields.ts:187](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L187)

___

### updateField

▸ **updateField**(`collection`, `field`, `opts?`): `Promise`<`string`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `field` | `RawField` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`string`\>

#### Defined in

[api/src/services/fields.ts:359](https://github.com/directus/directus/blob/953c2f95d/api/src/services/fields.ts#L359)
