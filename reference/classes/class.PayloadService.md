[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > PayloadService

# Class: PayloadService

Process a given payload for a collection to ensure the special fields (hash, uuid, date etc) are handled correctly.

## Constructors

### constructor()

> **new PayloadService**(`collection`, `options`): [`PayloadService`](class.PayloadService.md)

#### Parameters

| Parameter    | Type                     |
| :----------- | :----------------------- |
| `collection` | `string`                 |
| `options`    | `AbstractServiceOptions` |

#### Returns

[`PayloadService`](class.PayloadService.md)

#### Source

[api/src/services/payload.ts:49](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L49)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/payload.ts:43](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L43)

---

### collection

> **collection**: `string`

#### Source

[api/src/services/payload.ts:46](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L46)

---

### helpers

> **helpers**: `object`

#### Type declaration

> ##### helpers.date
>
> **date**: `DateHelperMySQL` \| `DateHelperDefault` \| `DateHelperSQLite` \| `DateHelperOracle` \| `DateHelperMSSQL`
>
> ##### helpers.schema
>
> **schema**: `SchemaHelperMySQL` \| `SchemaHelperDefault` \| `SchemaHelperCockroachDb` \| `SchemaHelperSQLite` \|
> `SchemaHelperOracle` \| `SchemaHelperMSSQL`
>
> ##### helpers.st
>
> **st**: `GeometryHelperMySQL` \| `GeometryHelperPostgres` \| `GeometryHelperSQLite` \| `GeometryHelperOracle` \|
> `GeometryHelperMSSQL` \| `GeometryHelperRedshift`

#### Source

[api/src/services/payload.ts:45](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L45)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/payload.ts:44](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L44)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/payload.ts:47](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L47)

---

### transformers

> **transformers**: `Transformers`

#### Source

[api/src/services/payload.ts:59](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L59)

## Methods

### prepareDelta()

> **prepareDelta**(`data`): `Promise`\< `null` \| `string` \>

Transforms the input partial payload to match the output structure, to have consistency between delta and data

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `data`    | `Partial`\< `Item` \> |

#### Returns

`Promise`\< `null` \| `string` \>

#### Source

[api/src/services/payload.ts:817](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L817)

---

### processA2O()

> **processA2O**(`data`, `opts`?): `Promise`\< \{`nestedActionEvents`: `ActionEventParams`[]; `payload`: `Partial`\<
> `Item` \>; `revisions`: `PrimaryKey`[];} \>

Recursively save/update all nested related Any-to-One items

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `data`    | `Partial`\< `Item` \> |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< \{`nestedActionEvents`: `ActionEventParams`[]; `payload`: `Partial`\< `Item` \>; `revisions`:
`PrimaryKey`[];} \>

#### Source

[api/src/services/payload.ts:384](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L384)

---

### processAggregates()

> **processAggregates**(`payload`): `void`

#### Parameters

| Parameter | Type                    |
| :-------- | :---------------------- |
| `payload` | `Partial`\< `Item` \>[] |

#### Returns

`void`

#### Source

[api/src/services/payload.ts:208](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L208)

---

### processDates()

> **processDates**(`payloads`, `action`): `Partial`\< `Record`\< `string`, `any` \> \>[]

Knex returns `datetime` and `date` columns as Date.. This is wrong for date / datetime, as those shouldn't return with
time / timezone info respectively

#### Parameters

| Parameter  | Type                                           |
| :--------- | :--------------------------------------------- |
| `payloads` | `Partial`\< `Record`\< `string`, `any` \> \>[] |
| `action`   | `Action`                                       |

#### Returns

`Partial`\< `Record`\< `string`, `any` \> \>[]

#### Source

[api/src/services/payload.ts:276](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L276)

---

### processField()

> **processField**( `field`, `payload`, `action`, `accountability`): `Promise`\< `any` \>

#### Parameters

| Parameter        | Type                  |
| :--------------- | :-------------------- |
| `field`          | `SchemaOverview`      |
| `payload`        | `Partial`\< `Item` \> |
| `action`         | `Action`              |
| `accountability` | `any`                 |

#### Returns

`Promise`\< `any` \>

#### Source

[api/src/services/payload.ts:219](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L219)

---

### processGeometries()

> **processGeometries**\<`T`\>(`payloads`, `action`): `T`

Native geometries are stored in custom binary format. We need to insert them with the function st_geomfromtext. For this
to work, that function call must not be escaped. It's therefore placed as a Knex.Raw object in the payload. Thus the
need to check if the value is a raw instance before stringifying it in the next step.

#### Type parameters

| Parameter                                                    |
| :----------------------------------------------------------- |
| `T` _extends_ `Partial`\< `Record`\< `string`, `any` \> \>[] |

#### Parameters

| Parameter  | Type     |
| :--------- | :------- |
| `payloads` | `T`      |
| `action`   | `Action` |

#### Returns

`T`

#### Source

[api/src/services/payload.ts:252](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L252)

---

### processM2O()

> **processM2O**(`data`, `opts`?): `Promise`\< \{`nestedActionEvents`: `ActionEventParams`[]; `payload`: `Partial`\<
> `Item` \>; `revisions`: `PrimaryKey`[];} \>

Save/update all nested related m2o items inside the payload

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `data`    | `Partial`\< `Item` \> |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< \{`nestedActionEvents`: `ActionEventParams`[]; `payload`: `Partial`\< `Item` \>; `revisions`:
`PrimaryKey`[];} \>

#### Source

[api/src/services/payload.ts:478](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L478)

---

### processO2M()

> **processO2M**( `data`, `parent`, `opts`?): `Promise`\< \{`nestedActionEvents`: `ActionEventParams`[]; `revisions`:
> `PrimaryKey`[];} \>

Recursively save/update all nested related o2m items

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `data`    | `Partial`\< `Item` \> |
| `parent`  | `PrimaryKey`          |
| `opts`?   | `MutationOptions`     |

#### Returns

`Promise`\< \{`nestedActionEvents`: `ActionEventParams`[]; `revisions`: `PrimaryKey`[];} \>

#### Source

[api/src/services/payload.ts:559](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L559)

---

### processValues()

> **processValues**(`action`, `payloads`): `Promise`\< `Partial`\< `Item` \>[] \>

#### Parameters

| Parameter  | Type                    |
| :--------- | :---------------------- |
| `action`   | `Action`                |
| `payloads` | `Partial`\< `Item` \>[] |

#### Returns

`Promise`\< `Partial`\< `Item` \>[] \>

#### Source

[api/src/services/payload.ts:149](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L149)

> **processValues**(`action`, `payload`): `Promise`\< `Partial`\< `Item` \> \>

#### Parameters

| Parameter | Type                  |
| :-------- | :-------------------- |
| `action`  | `Action`              |
| `payload` | `Partial`\< `Item` \> |

#### Returns

`Promise`\< `Partial`\< `Item` \> \>

#### Source

[api/src/services/payload.ts:150](https://github.com/directus/directus/blob/67c008df3/api/src/services/payload.ts#L150)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
