[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > AuthenticationService

# Class: AuthenticationService

## Constructors

### constructor()

> **new AuthenticationService**(`options`): [`AuthenticationService`](class.AuthenticationService.md)

#### Parameters

| Parameter | Type                     |
| :-------- | :----------------------- |
| `options` | `AbstractServiceOptions` |

#### Returns

[`AuthenticationService`](class.AuthenticationService.md)

#### Source

[api/src/services/authentication.ts:30](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authentication.ts#L30)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/authentication.ts:26](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authentication.ts#L26)

---

### activityService

> **activityService**: [`ActivityService`](class.ActivityService.md)

#### Source

[api/src/services/authentication.ts:27](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authentication.ts#L27)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/authentication.ts:25](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authentication.ts#L25)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/authentication.ts:28](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authentication.ts#L28)

## Methods

### login()

> **login**( `providerName` = `DEFAULT_AUTH_PROVIDER`, `payload`, `otp`?): `Promise`\< `LoginResult` \>

Retrieve the tokens for a given user email.

Password is optional to allow usage of this function within the SSO flow and extensions. Make sure to handle password
existence checks elsewhere

#### Parameters

| Parameter      | Type                          | Default value           |
| :------------- | :---------------------------- | :---------------------- |
| `providerName` | `string`                      | `DEFAULT_AUTH_PROVIDER` |
| `payload`      | `Record`\< `string`, `any` \> | `undefined`             |
| `otp`?         | `string`                      | `undefined`             |

#### Returns

`Promise`\< `LoginResult` \>

#### Source

[api/src/services/authentication.ts:43](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authentication.ts#L43)

---

### logout()

> **logout**(`refreshToken`): `Promise`\< `void` \>

#### Parameters

| Parameter      | Type     |
| :------------- | :------- |
| `refreshToken` | `string` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/authentication.ts:401](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authentication.ts#L401)

---

### refresh()

> **refresh**(`refreshToken`): `Promise`\< `Record`\< `string`, `any` \> \>

#### Parameters

| Parameter      | Type     |
| :------------- | :------- |
| `refreshToken` | `string` |

#### Returns

`Promise`\< `Record`\< `string`, `any` \> \>

#### Source

[api/src/services/authentication.ts:252](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authentication.ts#L252)

---

### verifyPassword()

> **verifyPassword**(`userID`, `password`): `Promise`\< `void` \>

#### Parameters

| Parameter  | Type     |
| :--------- | :------- |
| `userID`   | `string` |
| `password` | `string` |

#### Returns

`Promise`\< `void` \>

#### Source

[api/src/services/authentication.ts:430](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/authentication.ts#L430)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
