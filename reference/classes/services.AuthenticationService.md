[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / AuthenticationService

# Class: AuthenticationService

[services](../modules/services.md).AuthenticationService

## Table of contents

### Constructors

- [constructor](services.AuthenticationService.md#constructor)

### Properties

- [accountability](services.AuthenticationService.md#accountability)
- [activityService](services.AuthenticationService.md#activityservice)
- [knex](services.AuthenticationService.md#knex)
- [schema](services.AuthenticationService.md#schema)

### Methods

- [login](services.AuthenticationService.md#login)
- [logout](services.AuthenticationService.md#logout)
- [refresh](services.AuthenticationService.md#refresh)
- [verifyPassword](services.AuthenticationService.md#verifypassword)

## Constructors

### constructor

• **new AuthenticationService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/authentication.ts:33](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authentication.ts#L33)

## Properties

### accountability

• **accountability**: `any`

#### Defined in

[api/src/services/authentication.ts:29](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authentication.ts#L29)

___

### activityService

• **activityService**: [`ActivityService`](services.ActivityService.md)

#### Defined in

[api/src/services/authentication.ts:30](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authentication.ts#L30)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/authentication.ts:28](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authentication.ts#L28)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/authentication.ts:31](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authentication.ts#L31)

## Methods

### login

▸ **login**(`providerName?`, `payload`, `otp?`): `Promise`<`LoginResult`\>

Retrieve the tokens for a given user email.

Password is optional to allow usage of this function within the SSO flow and extensions. Make sure
to handle password existence checks elsewhere

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `providerName` | `string` | `DEFAULT_AUTH_PROVIDER` |
| `payload` | `Record`<`string`, `any`\> | `undefined` |
| `otp?` | `string` | `undefined` |

#### Returns

`Promise`<`LoginResult`\>

#### Defined in

[api/src/services/authentication.ts:46](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authentication.ts#L46)

___

### logout

▸ **logout**(`refreshToken`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `refreshToken` | `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/authentication.ts:388](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authentication.ts#L388)

___

### refresh

▸ **refresh**(`refreshToken`): `Promise`<`Record`<`string`, `any`\>\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `refreshToken` | `string` |

#### Returns

`Promise`<`Record`<`string`, `any`\>\>

#### Defined in

[api/src/services/authentication.ts:255](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authentication.ts#L255)

___

### verifyPassword

▸ **verifyPassword**(`userID`, `password`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `userID` | `string` |
| `password` | `string` |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/authentication.ts:417](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authentication.ts#L417)
