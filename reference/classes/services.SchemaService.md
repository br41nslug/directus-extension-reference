[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / SchemaService

# Class: SchemaService

[services](../modules/services.md).SchemaService

## Table of contents

### Constructors

- [constructor](services.SchemaService.md#constructor)

### Properties

- [accountability](services.SchemaService.md#accountability)
- [knex](services.SchemaService.md#knex)

### Methods

- [apply](services.SchemaService.md#apply)
- [diff](services.SchemaService.md#diff)
- [getHashedSnapshot](services.SchemaService.md#gethashedsnapshot)
- [snapshot](services.SchemaService.md#snapshot)

## Constructors

### constructor

• **new SchemaService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `Omit`<`AbstractServiceOptions`, ``"schema"``\> |

#### Defined in

[api/src/services/schema.ts:17](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/schema.ts#L17)

## Properties

### accountability

• **accountability**: `any`

#### Defined in

[api/src/services/schema.ts:15](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/schema.ts#L15)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/schema.ts:14](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/schema.ts#L14)

## Methods

### apply

▸ **apply**(`payload`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `payload` | `SnapshotDiffWithHash` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/schema.ts:30](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/schema.ts#L30)

___

### diff

▸ **diff**(`snapshot`, `options?`): `Promise`<``null`` \| `SnapshotDiff`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `snapshot` | `Snapshot` |
| `options?` | `Object` |
| `options.currentSnapshot?` | `Snapshot` |
| `options.force?` | `boolean` |

#### Returns

`Promise`<``null`` \| `SnapshotDiff`\>

#### Defined in

[api/src/services/schema.ts:41](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/schema.ts#L41)

___

### getHashedSnapshot

▸ **getHashedSnapshot**(`snapshot`): `SnapshotWithHash`

#### Parameters

| Name | Type |
| :------ | :------ |
| `snapshot` | `Snapshot` |

#### Returns

`SnapshotWithHash`

#### Defined in

[api/src/services/schema.ts:59](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/schema.ts#L59)

___

### snapshot

▸ **snapshot**(): `Promise`<`Snapshot`\>

#### Returns

`Promise`<`Snapshot`\>

#### Defined in

[api/src/services/schema.ts:22](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/schema.ts#L22)
