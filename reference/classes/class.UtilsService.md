[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > UtilsService

# Class: UtilsService

## Constructors

### constructor()

> **new UtilsService**(`options`): [`UtilsService`](class.UtilsService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`UtilsService`](class.UtilsService.md)

#### Source

[api/src/services/utils.ts:16](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/utils.ts#L16)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/utils.ts:13](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/utils.ts#L13)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/utils.ts:12](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/utils.ts#L12)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/utils.ts:14](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/utils.ts#L14)

## Methods

### clearCache()

> **clearCache**(): `Promise`\< `void` \>

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/utils.ts:151](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/utils.ts#L151)

---

### sort()

> **sort**(`collection`, `__namedParameters`): `Promise`\< `void` \>

#### Parameters

| Parameter                | Type         |
| :----------------------- | :----------- |
| `collection`             | `string`     |
| `__namedParameters`      | `object`     |
| `__namedParameters.item` | `PrimaryKey` |
| `__namedParameters.to`   | `PrimaryKey` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/utils.ts:22](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/utils.ts#L22)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
