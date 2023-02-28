[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / TFAService

# Class: TFAService

[services](../modules/services.md).TFAService

## Table of contents

### Constructors

- [constructor](services.TFAService.md#constructor)

### Properties

- [itemsService](services.TFAService.md#itemsservice)
- [knex](services.TFAService.md#knex)

### Methods

- [disableTFA](services.TFAService.md#disabletfa)
- [enableTFA](services.TFAService.md#enabletfa)
- [generateTFA](services.TFAService.md#generatetfa)
- [verifyOTP](services.TFAService.md#verifyotp)

## Constructors

### constructor

• **new TFAService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/tfa.ts:12](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/tfa.ts#L12)

## Properties

### itemsService

• **itemsService**: [`ItemsService`](services.ItemsService.md)<`Item`\>

#### Defined in

[api/src/services/tfa.ts:10](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/tfa.ts#L10)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/tfa.ts:9](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/tfa.ts#L9)

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

[api/src/services/tfa.ts:65](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/tfa.ts#L65)

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

[api/src/services/tfa.ts:51](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/tfa.ts#L51)

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

[api/src/services/tfa.ts:31](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/tfa.ts#L31)

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

[api/src/services/tfa.ts:17](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/tfa.ts#L17)
