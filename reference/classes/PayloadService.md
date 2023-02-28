[directus-monorepo](../README.md) / [Modules](../modules.md) / PayloadService

# Class: PayloadService

Process a given payload for a collection to ensure the special fields (hash, uuid, date etc) are
handled correctly.

## Table of contents

### Constructors

- [constructor](PayloadService.md#constructor)

### Properties

- [accountability](PayloadService.md#accountability)
- [collection](PayloadService.md#collection)
- [helpers](PayloadService.md#helpers)
- [knex](PayloadService.md#knex)
- [schema](PayloadService.md#schema)
- [transformers](PayloadService.md#transformers)

### Methods

- [prepareDelta](PayloadService.md#preparedelta)
- [processA2O](PayloadService.md#processa2o)
- [processAggregates](PayloadService.md#processaggregates)
- [processDates](PayloadService.md#processdates)
- [processField](PayloadService.md#processfield)
- [processGeometries](PayloadService.md#processgeometries)
- [processM2O](PayloadService.md#processm2o)
- [processO2M](PayloadService.md#processo2m)
- [processValues](PayloadService.md#processvalues)

## Constructors

### constructor

• **new PayloadService**(`collection`, `options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/payload.ts:41](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L41)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Defined in

[api/src/services/payload.ts:35](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L35)

___

### collection

• **collection**: `string`

#### Defined in

[api/src/services/payload.ts:38](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L38)

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

[api/src/services/payload.ts:37](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L37)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/payload.ts:36](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L36)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/payload.ts:39](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L39)

___

### transformers

• **transformers**: `Transformers`

#### Defined in

[api/src/services/payload.ts:51](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L51)

## Methods

### prepareDelta

▸ **prepareDelta**(`data`): `Promise`<``null`` \| `string`\>

Transforms the input partial payload to match the output structure, to have consistency
between delta and data

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Partial`<`Item`\> |

#### Returns

`Promise`<``null`` \| `string`\>

#### Defined in

[api/src/services/payload.ts:789](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L789)

___

### processA2O

▸ **processA2O**(`data`, `opts?`): `Promise`<{ `nestedActionEvents`: `ActionEventParams`[] ; `payload`: `Partial`<`Item`\> ; `revisions`: `PrimaryKey`[]  }\>

Recursively save/update all nested related Any-to-One items

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Partial`<`Item`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<{ `nestedActionEvents`: `ActionEventParams`[] ; `payload`: `Partial`<`Item`\> ; `revisions`: `PrimaryKey`[]  }\>

#### Defined in

[api/src/services/payload.ts:369](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L369)

___

### processAggregates

▸ **processAggregates**(`payload`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `payload` | `Partial`<`Item`\>[] |

#### Returns

`void`

#### Defined in

[api/src/services/payload.ts:199](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L199)

___

### processDates

▸ **processDates**(`payloads`, `action`): `Partial`<`Record`<`string`, `any`\>\>[]

Knex returns `datetime` and `date` columns as Date.. This is wrong for date / datetime, as those
shouldn't return with time / timezone info respectively

#### Parameters

| Name | Type |
| :------ | :------ |
| `payloads` | `Partial`<`Record`<`string`, `any`\>\>[] |
| `action` | `Action` |

#### Returns

`Partial`<`Record`<`string`, `any`\>\>[]

#### Defined in

[api/src/services/payload.ts:265](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L265)

___

### processField

▸ **processField**(`field`, `payload`, `action`, `accountability`): `Promise`<`any`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `field` | `FieldOverview` |
| `payload` | `Partial`<`Item`\> |
| `action` | `Action` |
| `accountability` | ``null`` \| `Accountability` |

#### Returns

`Promise`<`any`\>

#### Defined in

[api/src/services/payload.ts:209](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L209)

___

### processGeometries

▸ **processGeometries**<`T`\>(`payloads`, `action`): `T`

Native geometries are stored in custom binary format. We need to insert them with
the function st_geomfromtext. For this to work, that function call must not be
escaped. It's therefore placed as a Knex.Raw object in the payload. Thus the need
to check if the value is a raw instance before stringifying it in the next step.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends `Partial`<`Record`<`string`, `any`\>\>[] |

#### Parameters

| Name | Type |
| :------ | :------ |
| `payloads` | `T` |
| `action` | `Action` |

#### Returns

`T`

#### Defined in

[api/src/services/payload.ts:242](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L242)

___

### processM2O

▸ **processM2O**(`data`, `opts?`): `Promise`<{ `nestedActionEvents`: `ActionEventParams`[] ; `payload`: `Partial`<`Item`\> ; `revisions`: `PrimaryKey`[]  }\>

Save/update all nested related m2o items inside the payload

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Partial`<`Item`\> |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<{ `nestedActionEvents`: `ActionEventParams`[] ; `payload`: `Partial`<`Item`\> ; `revisions`: `PrimaryKey`[]  }\>

#### Defined in

[api/src/services/payload.ts:461](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L461)

___

### processO2M

▸ **processO2M**(`data`, `parent`, `opts?`): `Promise`<{ `nestedActionEvents`: `ActionEventParams`[] ; `revisions`: `PrimaryKey`[]  }\>

Recursively save/update all nested related o2m items

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `Partial`<`Item`\> |
| `parent` | `PrimaryKey` |
| `opts?` | `MutationOptions` |

#### Returns

`Promise`<{ `nestedActionEvents`: `ActionEventParams`[] ; `revisions`: `PrimaryKey`[]  }\>

#### Defined in

[api/src/services/payload.ts:540](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L540)

___

### processValues

▸ **processValues**(`action`, `payloads`): `Promise`<`Partial`<`Item`\>[]\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `action` | `Action` |
| `payloads` | `Partial`<`Item`\>[] |

#### Returns

`Promise`<`Partial`<`Item`\>[]\>

#### Defined in

[api/src/services/payload.ts:140](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L140)

▸ **processValues**(`action`, `payload`): `Promise`<`Partial`<`Item`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `action` | `Action` |
| `payload` | `Partial`<`Item`\> |

#### Returns

`Promise`<`Partial`<`Item`\>\>

#### Defined in

[api/src/services/payload.ts:141](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/payload.ts#L141)
