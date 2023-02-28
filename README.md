# Unofficial Directus v9 Extension Reference

These docs are generated using TypeDoc for an easy reference of the Services and Exceptions exposed to backend extensions by Directus.

## Overview
- [All Services](reference/modules/services.md)
- [All Exceptions](reference/modules/exceptions.md)

## Shortcuts
- [ItemsService](reference/classes/services.ItemsService.md)
- [FilesService](reference/classes/services.FilesService.md)
- [MailService](reference/classes/services.MailService.md)

## How to generate the docs

After checking out the current repository and from it's root run:
- `git clone https://github.com/directus/directus directus`
- `cd directus`
- `pnpm i`
- `cd api`
- `pnpm -F directus i typedoc typedoc-plugin-markdown`
- `npx typedoc --plugin typedoc-plugin-markdown --skipErrorChecking --out ../../reference src/services/index.ts src/exceptions/index.ts`