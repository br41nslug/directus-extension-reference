[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / FieldsService

# Class: FieldsService

[services](../modules/services.md).FieldsService

## Table of contents

### Constructors

- [constructor](services.FieldsService.md#constructor)

### Properties

- [accountability](services.FieldsService.md#accountability)
- [cache](services.FieldsService.md#cache)
- [helpers](services.FieldsService.md#helpers)
- [itemsService](services.FieldsService.md#itemsservice)
- [knex](services.FieldsService.md#knex)
- [payloadService](services.FieldsService.md#payloadservice)
- [schema](services.FieldsService.md#schema)
- [schemaInspector](services.FieldsService.md#schemainspector)
- [systemCache](services.FieldsService.md#systemcache)

### Accessors

- [hasReadAccess](services.FieldsService.md#hasreadaccess)

### Methods

- [addColumnToTable](services.FieldsService.md#addcolumntotable)
- [createField](services.FieldsService.md#createfield)
- [deleteField](services.FieldsService.md#deletefield)
- [readAll](services.FieldsService.md#readall)
- [readOne](services.FieldsService.md#readone)
- [updateField](services.FieldsService.md#updatefield)

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

• **accountability**: `any`

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

• **itemsService**: [`ItemsService`](services.ItemsService.md)<`Item`\>

#### Defined in

[api/src/services/fields.ts:31](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L31)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/fields.ts:28](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L28)

___

### payloadService

• **payloadService**: [`PayloadService`](services.PayloadService.md)

#### Defined in

[api/src/services/fields.ts:32](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L32)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/fields.ts:34](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/fields.ts#L34)

___

### schemaInspector

• **schemaInspector**: `any`

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
| `field` | `any` | `undefined` |
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
| `field` | `any` |
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
