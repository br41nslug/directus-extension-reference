[directus-monorepo](README.md) / Modules

# directus-monorepo

## Table of contents

### Classes

- [ActivityService](classes/ActivityService.md)
- [AssetsService](classes/AssetsService.md)
- [AuthenticationService](classes/AuthenticationService.md)
- [AuthorizationService](classes/AuthorizationService.md)
- [CollectionsService](classes/CollectionsService.md)
- [DashboardsService](classes/DashboardsService.md)
- [ExportService](classes/ExportService.md)
- [FieldsService](classes/FieldsService.md)
- [FilesService](classes/FilesService.md)
- [FlowsService](classes/FlowsService.md)
- [FoldersService](classes/FoldersService.md)
- [ForbiddenException](classes/ForbiddenException.md)
- [GraphQLService](classes/GraphQLService.md)
- [GraphQLValidationException](classes/GraphQLValidationException.md)
- [HitRateLimitException](classes/HitRateLimitException.md)
- [IllegalAssetTransformation](classes/IllegalAssetTransformation.md)
- [ImportService](classes/ImportService.md)
- [InvalidConfigException](classes/InvalidConfigException.md)
- [InvalidCredentialsException](classes/InvalidCredentialsException.md)
- [InvalidIPException](classes/InvalidIPException.md)
- [InvalidOTPException](classes/InvalidOTPException.md)
- [InvalidPayloadException](classes/InvalidPayloadException.md)
- [InvalidProviderException](classes/InvalidProviderException.md)
- [InvalidQueryException](classes/InvalidQueryException.md)
- [InvalidTokenException](classes/InvalidTokenException.md)
- [ItemsService](classes/ItemsService.md)
- [MailService](classes/MailService.md)
- [MetaService](classes/MetaService.md)
- [MethodNotAllowedException](classes/MethodNotAllowedException.md)
- [NotificationsService](classes/NotificationsService.md)
- [OperationsService](classes/OperationsService.md)
- [PanelsService](classes/PanelsService.md)
- [PayloadService](classes/PayloadService.md)
- [PermissionsService](classes/PermissionsService.md)
- [PresetsService](classes/PresetsService.md)
- [RangeNotSatisfiableException](classes/RangeNotSatisfiableException.md)
- [RelationsService](classes/RelationsService.md)
- [RevisionsService](classes/RevisionsService.md)
- [RolesService](classes/RolesService.md)
- [RouteNotFoundException](classes/RouteNotFoundException.md)
- [SchemaService](classes/SchemaService.md)
- [ServerService](classes/ServerService.md)
- [ServiceUnavailableException](classes/ServiceUnavailableException.md)
- [SettingsService](classes/SettingsService.md)
- [SharesService](classes/SharesService.md)
- [SpecificationService](classes/SpecificationService.md)
- [TFAService](classes/TFAService.md)
- [TokenExpiredException](classes/TokenExpiredException.md)
- [UnexpectedResponseException](classes/UnexpectedResponseException.md)
- [UnprocessableEntityException](classes/UnprocessableEntityException.md)
- [UnsupportedMediaTypeException](classes/UnsupportedMediaTypeException.md)
- [UserSuspendedException](classes/UserSuspendedException.md)
- [UsersService](classes/UsersService.md)
- [UtilsService](classes/UtilsService.md)
- [WebhooksService](classes/WebhooksService.md)

### Type Aliases

- [EmailOptions](modules.md#emailoptions)
- [QueryOptions](modules.md#queryoptions)
- [RawCollection](modules.md#rawcollection)

### Functions

- [createApp](modules.md#createapp)

## Type Aliases

### EmailOptions

Ƭ **EmailOptions**: `SendMailOptions` & { `template?`: { `data`: `Record`<`string`, `any`\> ; `name`: `string`  }  }

#### Defined in

[api/src/services/mail/index.ts:20](https://github.com/directus/directus/blob/953c2f95d/api/src/services/mail/index.ts#L20)

___

### QueryOptions

Ƭ **QueryOptions**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `emitEvents?` | `boolean` |
| `permissionsAction?` | `PermissionsAction` |
| `stripNonRequested?` | `boolean` |

#### Defined in

[api/src/services/items.ts:27](https://github.com/directus/directus/blob/953c2f95d/api/src/services/items.ts#L27)

___

### RawCollection

Ƭ **RawCollection**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `collection` | `string` |
| `fields?` | `RawField`[] |
| `meta?` | `Partial`<`CollectionMeta`\> \| ``null`` |
| `schema?` | `Partial`<`Table`\> \| ``null`` |

#### Defined in

[api/src/services/collections.ts:21](https://github.com/directus/directus/blob/953c2f95d/api/src/services/collections.ts#L21)

## Functions

### createApp

▸ **createApp**(): `Promise`<`express.Application`\>

#### Returns

`Promise`<`express.Application`\>

#### Defined in

[api/src/app.ts:64](https://github.com/directus/directus/blob/953c2f95d/api/src/app.ts#L64)
