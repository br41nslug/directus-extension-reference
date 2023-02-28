[directus](../README.md) / [Modules](../modules.md) / services

# Module: services

## Table of contents

### Classes

- [ActivityService](../classes/services.ActivityService.md)
- [AssetsService](../classes/services.AssetsService.md)
- [AuthenticationService](../classes/services.AuthenticationService.md)
- [AuthorizationService](../classes/services.AuthorizationService.md)
- [CollectionsService](../classes/services.CollectionsService.md)
- [DashboardsService](../classes/services.DashboardsService.md)
- [ExportService](../classes/services.ExportService.md)
- [FieldsService](../classes/services.FieldsService.md)
- [FilesService](../classes/services.FilesService.md)
- [FlowsService](../classes/services.FlowsService.md)
- [FoldersService](../classes/services.FoldersService.md)
- [GraphQLService](../classes/services.GraphQLService.md)
- [ImportService](../classes/services.ImportService.md)
- [ItemsService](../classes/services.ItemsService.md)
- [MailService](../classes/services.MailService.md)
- [MetaService](../classes/services.MetaService.md)
- [NotificationsService](../classes/services.NotificationsService.md)
- [OperationsService](../classes/services.OperationsService.md)
- [PanelsService](../classes/services.PanelsService.md)
- [PayloadService](../classes/services.PayloadService.md)
- [PermissionsService](../classes/services.PermissionsService.md)
- [PresetsService](../classes/services.PresetsService.md)
- [RelationsService](../classes/services.RelationsService.md)
- [RevisionsService](../classes/services.RevisionsService.md)
- [RolesService](../classes/services.RolesService.md)
- [SchemaService](../classes/services.SchemaService.md)
- [ServerService](../classes/services.ServerService.md)
- [SettingsService](../classes/services.SettingsService.md)
- [SharesService](../classes/services.SharesService.md)
- [SpecificationService](../classes/services.SpecificationService.md)
- [TFAService](../classes/services.TFAService.md)
- [UsersService](../classes/services.UsersService.md)
- [UtilsService](../classes/services.UtilsService.md)
- [WebhooksService](../classes/services.WebhooksService.md)

### Type Aliases

- [EmailOptions](services.md#emailoptions)
- [QueryOptions](services.md#queryoptions)
- [RawCollection](services.md#rawcollection)

## Type Aliases

### EmailOptions

Ƭ **EmailOptions**: `SendMailOptions` & { `template?`: { `data`: `Record`<`string`, `any`\> ; `name`: `string`  }  }

#### Defined in

[api/src/services/mail/index.ts:20](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/mail/index.ts#L20)

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

[api/src/services/items.ts:27](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/items.ts#L27)

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

[api/src/services/collections.ts:21](https://github.com/directus/directus/blob/9368dbd0c/api/src/services/collections.ts#L21)
