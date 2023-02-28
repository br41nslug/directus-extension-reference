[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / MailService

# Class: MailService

[services](../modules/services.md).MailService

## Table of contents

### Constructors

- [constructor](services.MailService.md#constructor)

### Properties

- [accountability](services.MailService.md#accountability)
- [knex](services.MailService.md#knex)
- [mailer](services.MailService.md#mailer)
- [schema](services.MailService.md#schema)

### Methods

- [getDefaultTemplateData](services.MailService.md#getdefaulttemplatedata)
- [renderTemplate](services.MailService.md#rendertemplate)
- [send](services.MailService.md#send)

## Constructors

### constructor

• **new MailService**(`opts`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/mail/index.ts:33](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/mail/index.ts#L33)

## Properties

### accountability

• **accountability**: `any`

#### Defined in

[api/src/services/mail/index.ts:29](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/mail/index.ts#L29)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/mail/index.ts:30](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/mail/index.ts#L30)

___

### mailer

• **mailer**: `Transporter`<`any`\>

#### Defined in

[api/src/services/mail/index.ts:31](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/mail/index.ts#L31)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/mail/index.ts:28](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/mail/index.ts#L28)

## Methods

### getDefaultTemplateData

▸ `Private` **getDefaultTemplateData**(): `Promise`<{ `projectColor`: `any` ; `projectLogo`: `string` ; `projectName`: `any` ; `projectUrl`: `any`  }\>

#### Returns

`Promise`<{ `projectColor`: `any` ; `projectLogo`: `string` ; `projectName`: `any` ; `projectUrl`: `any`  }\>

#### Defined in

[api/src/services/mail/index.ts:96](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/mail/index.ts#L96)

___

### renderTemplate

▸ `Private` **renderTemplate**(`template`, `variables`): `Promise`<`any`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `template` | `string` |
| `variables` | `Record`<`string`, `any`\> |

#### Returns

`Promise`<`any`\>

#### Defined in

[api/src/services/mail/index.ts:80](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/mail/index.ts#L80)

___

### send

▸ **send**<`T`\>(`options`): `Promise`<`T`\>

#### Type parameters

| Name |
| :------ |
| `T` |

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | [`EmailOptions`](../modules/services.md#emailoptions) |

#### Returns

`Promise`<`T`\>

#### Defined in

[api/src/services/mail/index.ts:49](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/mail/index.ts#L49)
