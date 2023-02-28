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

[api/src/services/fields.ts:38](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L38)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Defined in

[api/src/services/fields.ts:30](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L30)

___

### cache

• **cache**: ``null`` \| `Keyv`<`any`, `Record`<`string`, `unknown`\>\>

#### Defined in

[api/src/services/fields.ts:35](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L35)

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

[api/src/services/fields.ts:29](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L29)

___

### itemsService

• **itemsService**: [`ItemsService`](ItemsService.md)<`Item`\>

#### Defined in

[api/src/services/fields.ts:31](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L31)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/fields.ts:28](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L28)

___

### payloadService

• **payloadService**: [`PayloadService`](PayloadService.md)

#### Defined in

[api/src/services/fields.ts:32](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L32)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/fields.ts:34](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L34)

___

### schemaInspector

• **schemaInspector**: `SchemaInspector`

#### Defined in

[api/src/services/fields.ts:33](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L33)

___

### systemCache

• **systemCache**: `Keyv`<`any`, `Record`<`string`, `unknown`\>\>

#### Defined in

[api/src/services/fields.ts:36](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L36)

## Accessors

### hasReadAccess

• `Private` `get` **hasReadAccess**(): `boolean`

#### Returns

`boolean`

#### Defined in

[api/src/services/fields.ts:53](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L53)

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

[api/src/services/fields.ts:645](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L645)

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

[api/src/services/fields.ts:244](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L244)

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

[api/src/services/fields.ts:479](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L479)

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

[api/src/services/fields.ts:59](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L59)

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

[api/src/services/fields.ts:188](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L188)

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

[api/src/services/fields.ts:360](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L360)
