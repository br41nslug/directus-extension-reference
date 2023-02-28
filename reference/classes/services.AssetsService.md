[directus](../README.md) / [Modules](../modules.md) / [services](../modules/services.md) / AssetsService

# Class: AssetsService

[services](../modules/services.md).AssetsService

## Table of contents

### Constructors

- [constructor](services.AssetsService.md#constructor)

### Properties

- [accountability](services.AssetsService.md#accountability)
- [authorizationService](services.AssetsService.md#authorizationservice)
- [knex](services.AssetsService.md#knex)

### Methods

- [getAsset](services.AssetsService.md#getasset)

## Constructors

### constructor

• **new AssetsService**(`options`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options` | `AbstractServiceOptions` |

#### Defined in

[api/src/services/assets.ts:35](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/assets.ts#L35)

## Properties

### accountability

• **accountability**: `any`

#### Defined in

[api/src/services/assets.ts:32](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/assets.ts#L32)

___

### authorizationService

• **authorizationService**: [`AuthorizationService`](services.AuthorizationService.md)

#### Defined in

[api/src/services/assets.ts:33](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/assets.ts#L33)

___

### knex

• **knex**: `Knex`<`any`, `any`[]\>

#### Defined in

[api/src/services/assets.ts:31](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/assets.ts#L31)

## Methods

### getAsset

▸ **getAsset**(`id`, `transformation`, `range?`): `Promise`<{ `file`: `any` ; `stat`: `Stat` ; `stream`: `Readable`  }\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `string` |
| `transformation` | `TransformationParams` \| `TransformationPreset` |
| `range?` | `any` |

#### Returns

`Promise`<{ `file`: `any` ; `stat`: `Stat` ; `stream`: `Readable`  }\>

#### Defined in

[api/src/services/assets.ts:41](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/assets.ts#L41)
