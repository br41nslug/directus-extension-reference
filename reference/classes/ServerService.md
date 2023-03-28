[directus-monorepo](../README.md) / [Modules](../modules.md) / ServerService

# Class: ServerService

## Table of contents

### Constructors

- [constructor](ServerService.md#constructor)

### Properties

- [accountability](ServerService.md#accountability)
- [knex](ServerService.md#knex)
- [schema](ServerService.md#schema)
- [settingsService](ServerService.md#settingsservice)

### Methods

- [health](ServerService.md#health)
- [serverInfo](ServerService.md#serverinfo)

## Constructors

### constructor

• **new ServerService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/server.ts:28](https://github.com/directus/directus/blob/953c2f95d/api/src/services/server.ts#L28)

## Properties

### accountability

• **accountability**: ``null`` \| `Accountability`

#### Defined in

[api/src/services/server.ts:24](https://github.com/directus/directus/blob/953c2f95d/api/src/services/server.ts#L24)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/server.ts:23](https://github.com/directus/directus/blob/953c2f95d/api/src/services/server.ts#L23)

___

### schema

• **schema**: `SchemaOverview`

#### Defined in

[api/src/services/server.ts:26](https://github.com/directus/directus/blob/953c2f95d/api/src/services/server.ts#L26)

___

### settingsService

• **settingsService**: [`SettingsService`](SettingsService.md)

#### Defined in

[api/src/services/server.ts:25](https://github.com/directus/directus/blob/953c2f95d/api/src/services/server.ts#L25)

## Methods

### health

▸ **health**(): `Promise`<`Record`<`string`, `any`\>\>

#### Returns

`Promise`<`Record`<`string`, `any`\>\>

#### Defined in

[api/src/services/server.ts:100](https://github.com/directus/directus/blob/953c2f95d/api/src/services/server.ts#L100)

___

### serverInfo

▸ **serverInfo**(): `Promise`<`Record`<`string`, `any`\>\>

#### Returns

`Promise`<`Record`<`string`, `any`\>\>

#### Defined in

[api/src/services/server.ts:35](https://github.com/directus/directus/blob/953c2f95d/api/src/services/server.ts#L35)
