# Unofficial Directus v9 Extension Reference

These docs are generated using TypeDoc for an easy reference of the Services and Exceptions exposed to backend extensions by Directus.

## Commmonly used
- [ItemsService](reference/classes/ItemsService.md)
- [FilesService](reference/classes/FilesService.md)
- [MailService](reference/classes/MailService.md)

## Services
- [ActivityService](reference/classes/ActivityService.md)
- [AssetsService](reference/classes/AssetsService.md)
- [AuthenticationService](reference/classes/AuthenticationService.md)
- [AuthorizationService](reference/classes/AuthorizationService.md)
- [CollectionsService](reference/classes/CollectionsService.md)
- [DashboardsService](reference/classes/DashboardsService.md)
- [ExportService](reference/classes/ExportService.md)
- [FieldsService](reference/classes/FieldsService.md)
- [FilesService](reference/classes/FilesService.md)
- [FlowsService](reference/classes/FlowsService.md)
- [FoldersService](reference/classes/FoldersService.md)
- [GraphQLService](reference/classes/GraphQLService.md)
- [IllegalAssetTransformation](reference/classes/IllegalAssetTransformation.md)
- [ImportService](reference/classes/ImportService.md)
- [ItemsService](reference/classes/ItemsService.md)
- [MailService](reference/classes/MailService.md)
- [MetaService](reference/classes/MetaService.md)
- [NotificationsService](reference/classes/NotificationsService.md)
- [OperationsService](reference/classes/OperationsService.md)
- [PanelsService](reference/classes/PanelsService.md)
- [PayloadService](reference/classes/PayloadService.md)
- [PermissionsService](reference/classes/PermissionsService.md)
- [PresetsService](reference/classes/PresetsService.md)
- [RelationsService](reference/classes/RelationsService.md)
- [RevisionsService](reference/classes/RevisionsService.md)
- [RolesService](reference/classes/RolesService.md)
- [SchemaService](reference/classes/SchemaService.md)
- [ServerService](reference/classes/ServerService.md)
- [SettingsService](reference/classes/SettingsService.md)
- [SharesService](reference/classes/SharesService.md)
- [SpecificationService](reference/classes/SpecificationService.md)
- [TFAService](reference/classes/TFAService.md)
- [UsersService](reference/classes/UsersService.md)
- [UtilsService](reference/classes/UtilsService.md)
- [WebhooksService](reference/classes/WebhooksService.md)

## Exceptions
- [ForbiddenException](reference/classes/ForbiddenException.md)
- [GraphQLValidationException](reference/classes/GraphQLValidationException.md)
- [HitRateLimitException](reference/classes/HitRateLimitException.md)
- [InvalidConfigException](reference/classes/InvalidConfigException.md)
- [InvalidCredentialsException](reference/classes/InvalidCredentialsException.md)
- [InvalidIPException](reference/classes/InvalidIPException.md)
- [InvalidOTPException](reference/classes/InvalidOTPException.md)
- [InvalidPayloadException](reference/classes/InvalidPayloadException.md)
- [InvalidProviderException](reference/classes/InvalidProviderException.md)
- [InvalidQueryException](reference/classes/InvalidQueryException.md)
- [InvalidTokenException](reference/classes/InvalidTokenException.md)
- [MethodNotAllowedException](reference/classes/MethodNotAllowedException.md)
- [RangeNotSatisfiableException](reference/classes/RangeNotSatisfiableException.md)
- [RouteNotFoundException](reference/classes/RouteNotFoundException.md)
- [ServiceUnavailableException](reference/classes/ServiceUnavailableException.md)
- [TokenExpiredException](reference/classes/TokenExpiredException.md)
- [UnexpectedResponseException](reference/classes/UnexpectedResponseException.md)
- [UnprocessableEntityException](reference/classes/UnprocessableEntityException.md)
- [UnsupportedMediaTypeException](reference/classes/UnsupportedMediaTypeException.md)
- [UserSuspendedException](reference/classes/UserSuspendedException.md)

## How to generate the docs

After checking out the current repository and from it's root run:
- `git clone https://github.com/directus/directus directus`
- `cd directus`
- `pnpm i`
- `cd api`
- `pnpm -F directus i typedoc typedoc-plugin-markdown`
- `npx typedoc --plugin typedoc-plugin-markdown --skipErrorChecking --out ../../reference ../packages/shared/src/types/index.ts src/index.ts`