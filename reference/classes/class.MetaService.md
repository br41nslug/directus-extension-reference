[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > MetaService

# Class: MetaService

## Constructors

### constructor()

> **new MetaService**(`options`): [`MetaService`](class.MetaService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`MetaService`](class.MetaService.md)

#### Source

[api/src/services/meta.ts:13](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/meta.ts#L13)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/meta.ts:10](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/meta.ts#L10)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/meta.ts:9](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/meta.ts#L9)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/meta.ts:11](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/meta.ts#L11)

## Methods

### filterCount()

> **filterCount**(`collection`, `query`): `Promise`\< `number` \>

#### Parameters

| Parameter    | Type     |
| :----------- | :------- |
| `collection` | `string` |
| `query`      | `Query`  |

#### Returns

`Promise`\< `number` \>

#### Source

[api/src/services/meta.ts:58](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/meta.ts#L58)

---

### getMetaForQuery()

> **getMetaForQuery**(`collection`, `query`): `Promise`\< `undefined` \| `Record`\< `string`, `any` \> \>

#### Parameters

| Parameter    | Type     |
| :----------- | :------- |
| `collection` | `string` |
| `query`      | `any`    |

#### Returns

`Promise`\< `undefined` \| `Record`\< `string`, `any` \> \>

#### Source

[api/src/services/meta.ts:19](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/meta.ts#L19)

---

### totalCount()

> **totalCount**(`collection`): `Promise`\< `number` \>

#### Parameters

| Parameter    | Type     |
| :----------- | :------- |
| `collection` | `string` |

#### Returns

`Promise`\< `number` \>

#### Source

[api/src/services/meta.ts:38](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/meta.ts#L38)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
