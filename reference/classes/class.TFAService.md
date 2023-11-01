[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > TFAService

# Class: TFAService

## Constructors

### constructor()

> **new TFAService**(`options`): [`TFAService`](class.TFAService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`TFAService`](class.TFAService.md)

#### Source

[api/src/services/tfa.ts:12](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/tfa.ts#L12)

## Properties

### itemsService

> **itemsService**: [`ItemsService`](class.ItemsService.md)\< `Item` \>

#### Source

[api/src/services/tfa.ts:10](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/tfa.ts#L10)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/tfa.ts:9](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/tfa.ts#L9)

## Methods

### disableTFA()

> **disableTFA**(`key`): `Promise`\< `void` \>

#### Parameters

| Parameter | Type         |
| :-------- | :----------- |
| `key`     | `PrimaryKey` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/tfa.ts:65](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/tfa.ts#L65)

---

### enableTFA()

> **enableTFA**( `key`, `otp`, `secret`): `Promise`\< `void` \>

#### Parameters

| Parameter | Type         |
| :-------- | :----------- |
| `key`     | `PrimaryKey` |
| `otp`     | `string`     |
| `secret`  | `string`     |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/tfa.ts:51](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/tfa.ts#L51)

---

### generateTFA()

> **generateTFA**(`key`): `Promise`\< `Record`\< `string`, `string` \> \>

#### Parameters

| Parameter | Type         |
| :-------- | :----------- |
| `key`     | `PrimaryKey` |

#### Returns

`Promise`\< `Record`\< `string`, `string` \> \>

#### Source

[api/src/services/tfa.ts:31](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/tfa.ts#L31)

---

### verifyOTP()

> **verifyOTP**( `key`, `otp`, `secret`?): `Promise`\< `boolean` \>

#### Parameters

| Parameter | Type         |
| :-------- | :----------- |
| `key`     | `PrimaryKey` |
| `otp`     | `string`     |
| `secret`? | `string`     |

#### Returns

`Promise`\< `boolean` \>

#### Source

[api/src/services/tfa.ts:17](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/tfa.ts#L17)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
