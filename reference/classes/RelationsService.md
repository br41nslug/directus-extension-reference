[directus-monorepo](../README.md) / [Modules](../modules.md) / RelationsService

# Class: RelationsService

## Table of contents

### Constructors

- [constructor](RelationsService.md#constructor)

### Properties

- [accountability](RelationsService.md#accountability)
- [helpers](RelationsService.md#helpers)
- [knex](RelationsService.md#knex)
- [permissionsService](RelationsService.md#permissionsservice)
- [relationsItemService](RelationsService.md#relationsitemservice)
- [schema](RelationsService.md#schema)
- [schemaInspector](RelationsService.md#schemainspector)
- [systemCache](RelationsService.md#systemcache)

### Accessors

- [hasReadAccess](RelationsService.md#hasreadaccess)

### Methods

- [alterType](RelationsService.md#altertype)
- [createOne](RelationsService.md#createone)
- [deleteOne](RelationsService.md#deleteone)
- [filterForbidden](RelationsService.md#filterforbidden)
- [readAll](RelationsService.md#readall)
- [readOne](RelationsService.md#readone)
- [stitchRelations](RelationsService.md#stitchrelations)
- [updateOne](RelationsService.md#updateone)

## Constructors

### constructor

• **new RelationsService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/relations.ts:29](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L29)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Defined in

[api/src/services/relations.ts:23](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L23)

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

[api/src/services/relations.ts:27](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L27)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/relations.ts:20](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L20)

___

### permissionsService

• **permissionsService**: [`PermissionsService`](PermissionsService.md)

#### Defined in

[api/src/services/relations.ts:21](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L21)

___

### relationsItemService

• **relationsItemService**: [`ItemsService`](ItemsService.md)<`RelationMeta`\>

#### Defined in

[api/src/services/relations.ts:25](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L25)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/relations.ts:24](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L24)

___

### schemaInspector

• **schemaInspector**: `SchemaInspector`

#### Defined in

[api/src/services/relations.ts:22](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L22)

___

### systemCache

• **systemCache**: `Keyv`<`any`, `Record`<`string`, `unknown`\>\>

#### Defined in

[api/src/services/relations.ts:26](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L26)

## Accessors

### hasReadAccess

• `Private` `get` **hasReadAccess**(): `boolean`

Whether or not the current user has read access to relations

#### Returns

`boolean`

#### Defined in

[api/src/services/relations.ts:441](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L441)

## Methods

### alterType

▸ `Private` **alterType**(`table`, `relation`): `void`

MySQL Specific

MySQL doesn't accept FKs from `int` to `int unsigned`. `knex` defaults `.increments()` to
`unsigned`, but defaults regular `int` to `int`. This means that created m2o fields have the
wrong type. This step will force the m2o `int` field into `unsigned`, but only if both types are
integers, and only if we go from `int` to `int unsigned`.

**`TODO`**

This is a bit of a hack, and might be better of abstracted elsewhere

#### Parameters

| Name | Type |
| :------ | :------ |
| `table` | `TableBuilder` |
| `relation` | `Partial`<`Relation`\> |

#### Returns

`void`

#### Defined in

[api/src/services/relations.ts:559](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L559)

___

### createOne

▸ **createOne**(`relation`, `opts?`): `Promise`<`void`\>

Create a new relationship / foreign key constraint

#### Parameters

| Name | Type |
| :------ | :------ |
| `relation` | `Partial`<`Relation`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/relations.ts:128](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L128)

___

### deleteOne

▸ **deleteOne**(`collection`, `field`, `opts?`): `Promise`<`void`\>

Delete an existing relationship

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `field` | `string` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/relations.ts:357](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L357)

___

### filterForbidden

▸ `Private` **filterForbidden**(`relations`): `Promise`<`Relation`[]\>

Loop over all relations and filter out the ones that contain collections/fields you don't have
permissions to

#### Parameters

| Name | Type |
| :------ | :------ |
| `relations` | `Relation`[] |

#### Returns

`Promise`<`Relation`[]\>

#### Defined in

[api/src/services/relations.ts:494](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L494)

___

### readAll

▸ **readAll**(`collection?`, `opts?`): `Promise`<`Relation`[]\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection?` | `string` |
| `opts?` | [`QueryOptions`](../modules.md#queryoptions) |

#### Returns

`Promise`<`Relation`[]\>

#### Defined in

[api/src/services/relations.ts:47](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L47)

___

### readOne

▸ **readOne**(`collection`, `field`): `Promise`<`Relation`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `field` | `string` |

#### Returns

`Promise`<`Relation`\>

#### Defined in

[api/src/services/relations.ts:77](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L77)

___

### stitchRelations

▸ `Private` **stitchRelations**(`metaRows`, `schemaRows`): `Relation`[]

Combine raw schema foreign key information with Directus relations meta rows to form final
Relation objects

#### Parameters

| Name | Type |
| :------ | :------ |
| `metaRows` | `RelationMeta`[] |
| `schemaRows` | `ForeignKey`[] |

#### Returns

`Relation`[]

#### Defined in

[api/src/services/relations.ts:451](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L451)

___

### updateOne

▸ **updateOne**(`collection`, `field`, `relation`, `opts?`): `Promise`<`void`\>

Update an existing foreign key constraint

Note: You can update anything under meta, but only the `on_delete` trigger under schema

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `field` | `string` |
| `relation` | `Partial`<`Relation`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/relations.ts:242](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/relations.ts#L242)
