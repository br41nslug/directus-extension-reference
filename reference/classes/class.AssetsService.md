[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > AssetsService

# Class: AssetsService

## Constructors

### constructor()

> **new AssetsService**(`options`): [`AssetsService`](class.AssetsService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`AssetsService`](class.AssetsService.md)

#### Source

[api/src/services/assets.ts:32](https://github.com/directus/directus/blob/67c008df3/api/src/services/assets.ts#L32)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/assets.ts:29](https://github.com/directus/directus/blob/67c008df3/api/src/services/assets.ts#L29)

---

### authorizationService

> **authorizationService**: [`AuthorizationService`](class.AuthorizationService.md)

#### Source

[api/src/services/assets.ts:30](https://github.com/directus/directus/blob/67c008df3/api/src/services/assets.ts#L30)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/assets.ts:28](https://github.com/directus/directus/blob/67c008df3/api/src/services/assets.ts#L28)

## Methods

### getAsset()

> **getAsset**( `id`, `transformation`, `range`?): `Promise`\< \{`file`: `any`; `stat`: `Stat`; `stream`: `Readable`;}
> \>

#### Parameters

| Parameter        | Type                |
| :--------------- | :------------------ |
| `id`             | `string`            |
| `transformation` | `TransformationSet` |
| `range`?         | `any`               |

#### Returns

`Promise`\< \{`file`: `any`; `stat`: `Stat`; `stream`: `Readable`;} \>

#### Source

[api/src/services/assets.ts:38](https://github.com/directus/directus/blob/67c008df3/api/src/services/assets.ts#L38)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
