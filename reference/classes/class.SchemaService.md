[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > SchemaService

# Class: SchemaService

## Constructors

### constructor()

> **new SchemaService**(`options`): [`SchemaService`](class.SchemaService.md)

#### Parameters

| Parameter | Type                                             |
| :-------- | :----------------------------------------------- |
| `options` | `Omit`\< `AbstractServiceOptions`, `"schema"` \> |

#### Returns

[`SchemaService`](class.SchemaService.md)

#### Source

[api/src/services/schema.ts:23](https://github.com/directus/directus/blob/67c008df3/api/src/services/schema.ts#L23)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/schema.ts:21](https://github.com/directus/directus/blob/67c008df3/api/src/services/schema.ts#L21)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/schema.ts:20](https://github.com/directus/directus/blob/67c008df3/api/src/services/schema.ts#L20)

## Methods

### apply()

> **apply**(`payload`): `Promise`\< `void` \>

#### Parameters

| Parameter | Type                   |
| :-------- | :--------------------- |
| `payload` | `SnapshotDiffWithHash` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/schema.ts:36](https://github.com/directus/directus/blob/67c008df3/api/src/services/schema.ts#L36)

---

### diff()

> **diff**(`snapshot`, `options`?): `Promise`\< `null` \| `SnapshotDiff` \>

#### Parameters

| Parameter                  | Type       |
| :------------------------- | :--------- |
| `snapshot`                 | `Snapshot` |
| `options`?                 | `object`   |
| `options.currentSnapshot`? | `Snapshot` |
| `options.force`?           | `boolean`  |

#### Returns

`Promise`\< `null` \| `SnapshotDiff` \>

#### Source

[api/src/services/schema.ts:47](https://github.com/directus/directus/blob/67c008df3/api/src/services/schema.ts#L47)

---

### getHashedSnapshot()

> **getHashedSnapshot**(`snapshot`): `SnapshotWithHash`

#### Parameters

| Parameter  | Type       |
| :--------- | :--------- |
| `snapshot` | `Snapshot` |

#### Returns

`SnapshotWithHash`

#### Source

[api/src/services/schema.ts:65](https://github.com/directus/directus/blob/67c008df3/api/src/services/schema.ts#L65)

---

### snapshot()

> **snapshot**(): `Promise`\< `Snapshot` \>

#### Returns

`Promise`\< `Snapshot` \>

#### Source

[api/src/services/schema.ts:28](https://github.com/directus/directus/blob/67c008df3/api/src/services/schema.ts#L28)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
