[directus-monorepo](../README.md) / [Modules](../modules.md) / AssetsService

# Class: AssetsService

## Table of contents

### Constructors

- [constructor](AssetsService.md#constructor)

### Properties

- [accountability](AssetsService.md#accountability)
- [authorizationService](AssetsService.md#authorizationservice)
- [knex](AssetsService.md#knex)

### Methods

- [getAsset](AssetsService.md#getasset)

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

• **accountability**: ``null`` \| `Accountability`

#### Defined in

[api/src/services/assets.ts:32](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/assets.ts#L32)

___

### authorizationService

• **authorizationService**: [`AuthorizationService`](AuthorizationService.md)

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
| `range?` | `Range` |

#### Returns

`Promise`<{ `file`: `any` ; `stat`: `Stat` ; `stream`: `Readable`  }\>

#### Defined in

[api/src/services/assets.ts:41](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/assets.ts#L41)
