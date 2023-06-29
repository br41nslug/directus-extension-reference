[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > ServerService

# Class: ServerService

## Constructors

### constructor()

> **new ServerService**(`options`): [`ServerService`](class.ServerService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`ServerService`](class.ServerService.md)

#### Source

[api/src/services/server.ts:27](https://github.com/directus/directus/blob/67c008df3/api/src/services/server.ts#L27)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/server.ts:23](https://github.com/directus/directus/blob/67c008df3/api/src/services/server.ts#L23)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/server.ts:22](https://github.com/directus/directus/blob/67c008df3/api/src/services/server.ts#L22)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/server.ts:25](https://github.com/directus/directus/blob/67c008df3/api/src/services/server.ts#L25)

---

### settingsService

> **settingsService**: [`SettingsService`](class.SettingsService.md)

#### Source

[api/src/services/server.ts:24](https://github.com/directus/directus/blob/67c008df3/api/src/services/server.ts#L24)

## Methods

### health()

> **health**(): `Promise`\< `Record`\< `string`, `any` \> \>

#### Returns

`Promise`\< `Record`\< `string`, `any` \> \>

#### Source

[api/src/services/server.ts:111](https://github.com/directus/directus/blob/67c008df3/api/src/services/server.ts#L111)

---

### serverInfo()

> **serverInfo**(): `Promise`\< `Record`\< `string`, `any` \> \>

#### Returns

`Promise`\< `Record`\< `string`, `any` \> \>

#### Source

[api/src/services/server.ts:34](https://github.com/directus/directus/blob/67c008df3/api/src/services/server.ts#L34)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
