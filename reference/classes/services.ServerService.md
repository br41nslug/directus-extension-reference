[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / ServerService

# Class: ServerService

[services](../modules/services.md).ServerService

## Table of contents

### Constructors

- [constructor](services.ServerService.md#constructor)

### Properties

- [accountability](services.ServerService.md#accountability)
- [knex](services.ServerService.md#knex)
- [schema](services.ServerService.md#schema)
- [settingsService](services.ServerService.md#settingsservice)

### Methods

- [health](services.ServerService.md#health)
- [serverInfo](services.ServerService.md#serverinfo)

## Constructors

### constructor

• **new ServerService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/server.ts:27](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/server.ts#L27)

## Properties

### accountability

• **accountability**: `any`

#### Defined in

[api/src/services/server.ts:23](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/server.ts#L23)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/server.ts:22](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/server.ts#L22)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/server.ts:25](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/server.ts#L25)

___

### settingsService

• **settingsService**: [`SettingsService`](services.SettingsService.md)

#### Defined in

[api/src/services/server.ts:24](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/server.ts#L24)

## Methods

### health

▸ **health**(): `Promise`<`Record`<`string`, `any`\>\>

#### Returns

`Promise`<`Record`<`string`, `any`\>\>

#### Defined in

[api/src/services/server.ts:91](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/server.ts#L91)

___

### serverInfo

▸ **serverInfo**(): `Promise`<`Record`<`string`, `any`\>\>

#### Returns

`Promise`<`Record`<`string`, `any`\>\>

#### Defined in

[api/src/services/server.ts:34](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/server.ts#L34)
