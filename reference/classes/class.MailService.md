[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > MailService

# Class: MailService

## Constructors

### constructor()

> **new MailService**(`opts`): [`MailService`](class.MailService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `opts`    | `AbstractServiceOptions` |

#### Returns

[`MailService`](class.MailService.md)

#### Source

[api/src/services/mail/index.ts:36](https://github.com/directus/directus/blob/67c008df3/api/src/services/mail/index.ts#L36)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/mail/index.ts:32](https://github.com/directus/directus/blob/67c008df3/api/src/services/mail/index.ts#L32)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/mail/index.ts:33](https://github.com/directus/directus/blob/67c008df3/api/src/services/mail/index.ts#L33)

---

### mailer

> **mailer**: `Transporter`

#### Source

[api/src/services/mail/index.ts:34](https://github.com/directus/directus/blob/67c008df3/api/src/services/mail/index.ts#L34)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/mail/index.ts:31](https://github.com/directus/directus/blob/67c008df3/api/src/services/mail/index.ts#L31)

## Methods

### getDefaultTemplateData()

> `private` **getDefaultTemplateData**(): `Promise`\< \{`projectColor`: `any`; `projectLogo`: `string`; `projectName`:
> `any`; `projectUrl`: `any`;} \>

#### Returns

`Promise`\< \{`projectColor`: `any`; `projectLogo`: `string`; `projectName`: `any`; `projectUrl`: `any`;} \>

#### Source

[api/src/services/mail/index.ts:99](https://github.com/directus/directus/blob/67c008df3/api/src/services/mail/index.ts#L99)

---

### renderTemplate()

> `private` **renderTemplate**(`template`, `variables`): `Promise`\< `any` \>

#### Parameters

| Parameter   | Type                          |
| :---------- | :---------------------------- |
| `template`  | `string`                      |
| `variables` | `Record`\< `string`, `any` \> |

#### Returns

`Promise`\< `any` \>

#### Source

[api/src/services/mail/index.ts:83](https://github.com/directus/directus/blob/67c008df3/api/src/services/mail/index.ts#L83)

---

### send()

> **send**\<`T`\>(`options`): `Promise`\< `T` \>

#### Type parameters

| Parameter |
| :-------- |
| `T`       |

#### Parameters

| Parameter | Type                                                         |
| :-------- | :----------------------------------------------------------- |
| `options` | [`EmailOptions`](../type-aliases/type-alias.EmailOptions.md) |

#### Returns

`Promise`\< `T` \>

#### Source

[api/src/services/mail/index.ts:52](https://github.com/directus/directus/blob/67c008df3/api/src/services/mail/index.ts#L52)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
