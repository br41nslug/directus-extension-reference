[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > AuthorizationService

# Class: AuthorizationService

## Constructors

### constructor()

> **new AuthorizationService**(`options`): [`AuthorizationService`](class.AuthorizationService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`AuthorizationService`](class.AuthorizationService.md)

#### Source

[api/src/services/authorization.ts:37](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authorization.ts#L37)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/authorization.ts:33](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authorization.ts#L33)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/authorization.ts:32](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authorization.ts#L32)

---

### payloadService

> **payloadService**: [`PayloadService`](class.PayloadService.md)

#### Source

[api/src/services/authorization.ts:34](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authorization.ts#L34)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/authorization.ts:35](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authorization.ts#L35)

## Methods

### checkAccess()

> **checkAccess**( `action`, `collection`, `pk`): `Promise`\< `void` \>

#### Parameters

| Parameter    | Type                           |
| :----------- | :----------------------------- |
| `action`     | `PermissionsAction`            |
| `collection` | `string`                       |
| `pk`         | `PrimaryKey` \| `PrimaryKey`[] |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/authorization.ts:592](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authorization.ts#L592)

---

### processAST()

> **processAST**(`ast`, `action` = `'read'`): `Promise`\< `AST` \>

#### Parameters

| Parameter | Type                | Default value |
| :-------- | :------------------ | :------------ |
| `ast`     | `AST`               | `undefined`   |
| `action`  | `PermissionsAction` | `'read'`      |

#### Returns

`Promise`\< `AST` \>

#### Source

[api/src/services/authorization.ts:48](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authorization.ts#L48)

---

### validatePayload()

> **validatePayload**( `action`, `collection`, `data`): `Partial`\< `Item` \>

Checks if the provided payload matches the configured permissions, and adds the presets to the payload.

#### Parameters

| Parameter    | Type                  |
| :----------- | :-------------------- |
| `action`     | `PermissionsAction`   |
| `collection` | `string`              |
| `data`       | `Partial`\< `Item` \> |

#### Returns

`Partial`\< `Item` \>

#### Source

[api/src/services/authorization.ts:481](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authorization.ts#L481)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
