# Unofficial Directus v10 Extension Reference

These docs are generated using TypeDoc for an easy reference of the Services exposed to backend extensions by Directus.

## Commmonly used
- [ItemsService](reference/classes/class.ItemsService.md)
- [FilesService](reference/classes/class.FilesService.md)
- [MailService](reference/classes/class.MailService.md)

## Services
- [ActivityService](reference/classes/class.ActivityService.md)
- [AssetsService](reference/classes/class.AssetsService.md)
- [AuthenticationService](reference/classes/class.AuthenticationService.md)
- [AuthorizationService](reference/classes/class.AuthorizationService.md)
- [CollectionsService](reference/classes/class.CollectionsService.md)
- [DashboardsService](reference/classes/class.DashboardsService.md)
- [ExportService](reference/classes/class.ExportService.md)
- [ExtensionsService](reference/classes/class.ExtensionsService.md)
- [FieldsService](reference/classes/class.FieldsService.md)
- [FilesService](reference/classes/class.FilesService.md)
- [FlowsService](reference/classes/class.FlowsService.md)
- [FoldersService](reference/classes/class.FoldersService.md)
- [GraphQLService](reference/classes/class.GraphQLService.md)
- [ImportService](reference/classes/class.ImportService.md)
- [ItemsService](reference/classes/class.ItemsService.md)
- [MailService](reference/classes/class.MailService.md)
- [MetaService](reference/classes/class.MetaService.md)
- [NotificationsService](reference/classes/class.NotificationsService.md)
- [OperationsService](reference/classes/class.OperationsService.md)
- [PanelsService](reference/classes/class.PanelsService.md)
- [PayloadService](reference/classes/class.PayloadService.md)
- [PermissionsService](reference/classes/class.PermissionsService.md)
- [PresetsService](reference/classes/class.PresetsService.md)
- [RelationsService](reference/classes/class.RelationsService.md)
- [RevisionsService](reference/classes/class.RevisionsService.md)
- [RolesService](reference/classes/class.RolesService.md)
- [SchemaService](reference/classes/class.SchemaService.md)
- [ServerService](reference/classes/class.ServerService.md)
- [SettingsService](reference/classes/class.SettingsService.md)
- [SharesService](reference/classes/class.SharesService.md)
- [SpecificationService](reference/classes/class.SpecificationService.md)
- [TFAService](reference/classes/class.TFAService.md)
- [UsersService](reference/classes/class.UsersService.md)
- [UtilsService](reference/classes/class.UtilsService.md)
- [VersionsService](reference/classes/class.VersionsService.md)
- [WebhooksService](reference/classes/class.WebhooksService.md)
- [WebSocketService](reference/classes/class.WebSocketService.md)

## How to generate the docs

After checking out the current repository and from it's root run:
- `git clone https://github.com/directus/directus directus`
- `cd directus`
- `pnpm i`
- `cd api`
- `pnpm i typedoc typedoc-plugin-markdown`
- `npx typedoc --plugin typedoc-plugin-markdown --skipErrorChecking --out ../../reference src/services/index.ts`
