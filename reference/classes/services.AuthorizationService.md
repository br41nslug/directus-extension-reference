[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / AuthorizationService

# Class: AuthorizationService

[services](../modules/services.md).AuthorizationService

## Table of contents

### Constructors

- [constructor](services.AuthorizationService.md#constructor)

### Properties

- [accountability](services.AuthorizationService.md#accountability)
- [knex](services.AuthorizationService.md#knex)
- [payloadService](services.AuthorizationService.md#payloadservice)
- [schema](services.AuthorizationService.md#schema)

### Methods

- [checkAccess](services.AuthorizationService.md#checkaccess)
- [processAST](services.AuthorizationService.md#processast)
- [validatePayload](services.AuthorizationService.md#validatepayload)

## Constructors

### constructor

• **new AuthorizationService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/authorization.ts:37](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authorization.ts#L37)

## Properties

### accountability

• **accountability**: `any`

#### Defined in

[api/src/services/authorization.ts:33](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authorization.ts#L33)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/authorization.ts:32](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authorization.ts#L32)

___

### payloadService

• **payloadService**: [`PayloadService`](services.PayloadService.md)

#### Defined in

[api/src/services/authorization.ts:34](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authorization.ts#L34)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/authorization.ts:35](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authorization.ts#L35)

## Methods

### checkAccess

▸ **checkAccess**(`action`, `collection`, `pk`): `Promise`<`void`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `action` | `PermissionsAction` |
| `collection` | `string` |
| `pk` | `PrimaryKey` \| `PrimaryKey`[] |

#### Returns

`Promise`<`void`\>

#### Defined in

[api/src/services/authorization.ts:583](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authorization.ts#L583)

___

### processAST

▸ **processAST**(`ast`, `action?`): `Promise`<`AST`\>

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `ast` | `AST` | `undefined` |
| `action` | `PermissionsAction` | `'read'` |

#### Returns

`Promise`<`AST`\>

#### Defined in

[api/src/services/authorization.ts:47](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authorization.ts#L47)

___

### validatePayload

▸ **validatePayload**(`action`, `collection`, `data`): `Partial`<`Item`\>

Checks if the provided payload matches the configured permissions, and adds the presets to the payload.

#### Parameters

| Name | Type |
| :------ | :------ |
| `action` | `PermissionsAction` |
| `collection` | `string` |
| `data` | `Partial`<`Item`\> |

#### Returns

`Partial`<`Item`\>

#### Defined in

[api/src/services/authorization.ts:472](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/authorization.ts#L472)
