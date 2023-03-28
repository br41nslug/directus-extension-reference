[directus-monorepo](../README.md) / [Modules](../modules.md) / TFAService

# Class: TFAService

## Table of contents

### Constructors

- [constructor](TFAService.md#constructor)

### Properties

- [itemsService](TFAService.md#itemsservice)
- [knex](TFAService.md#knex)

### Methods

- [disableTFA](TFAService.md#disabletfa)
- [enableTFA](TFAService.md#enabletfa)
- [generateTFA](TFAService.md#generatetfa)
- [verifyOTP](TFAService.md#verifyotp)

## Constructors

### constructor

• **new TFAService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/tfa.ts:12](https://github.com/directus/directus/blob/953c2f95d/api/src/services/tfa.ts#L12)

## Properties

### itemsService

• **itemsService**: [`ItemsService`](ItemsService.md)<`Item`\>

#### Defined in

[api/src/services/tfa.ts:10](https://github.com/directus/directus/blob/953c2f95d/api/src/services/tfa.ts#L10)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/tfa.ts:9](https://github.com/directus/directus/blob/953c2f95d/api/src/services/tfa.ts#L9)

## Methods

### disableTFA

▸ **disableTFA**(`key`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/tfa.ts:65](https://github.com/directus/directus/blob/953c2f95d/api/src/services/tfa.ts#L65)

___

### enableTFA

▸ **enableTFA**(`key`, `otp`, `secret`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `otp` | `string` |
| `secret` | `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/tfa.ts:51](https://github.com/directus/directus/blob/953c2f95d/api/src/services/tfa.ts#L51)

___

### generateTFA

▸ **generateTFA**(`key`): `Promise`<`Record`<`string`, `string`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |

#### Returns

`Promise`<`Record`<`string`, `string`\>\>

#### Defined in

[api/src/services/tfa.ts:31](https://github.com/directus/directus/blob/953c2f95d/api/src/services/tfa.ts#L31)

___

### verifyOTP

▸ **verifyOTP**(`key`, `otp`, `secret?`): `Promise`<`boolean`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `PrimaryKey` |
| `otp` | `string` |
| `secret?` | `string` |

#### Returns

`Promise`<`boolean`\>

#### Defined in

[api/src/services/tfa.ts:17](https://github.com/directus/directus/blob/953c2f95d/api/src/services/tfa.ts#L17)
