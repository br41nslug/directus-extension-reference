[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > GraphQLService

# Class: GraphQLService

## Constructors

### constructor()

> **new GraphQLService**(`options`): [`GraphQLService`](class.GraphQLService.md)

#### Parameters

| Parameter | Type                                                            |
| :-------- | :-------------------------------------------------------------- |
| `options` | `AbstractServiceOptions` & \{`scope`: `"items"` \| `"system"`;} |

#### Returns

[`GraphQLService`](class.GraphQLService.md)

#### Source

[api/src/services/graphql/index.ts:111](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L111)

## Properties

### accountability

> **accountability**: `any`

#### Source

[api/src/services/graphql/index.ts:106](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L106)

---

### knex

> **knex**: `Knex`\< `any`, `any`[] \>

#### Source

[api/src/services/graphql/index.ts:107](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L107)

---

### schema

> **schema**: `SchemaOverview`

#### Source

[api/src/services/graphql/index.ts:108](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L108)

---

### scope

> **scope**: `"items"` \| `"system"`

#### Source

[api/src/services/graphql/index.ts:109](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L109)

## Methods

### execute()

> **execute**(`__namedParameters`): `Promise`\< `FormattedExecutionResult`\< `ObjMap`\< `unknown` \>, `ObjMap`\<
> `unknown` \> \> \>

Execute a GraphQL structure

#### Parameters

| Parameter           | Type            |
| :------------------ | :-------------- |
| `__namedParameters` | `GraphQLParams` |

#### Returns

`Promise`\< `FormattedExecutionResult`\< `ObjMap`\< `unknown` \>, `ObjMap`\< `unknown` \> \> \>

#### Source

[api/src/services/graphql/index.ts:121](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L121)

---

### formatError()

> **formatError**(`error`): `GraphQLError`

Convert Directus-Exception into a GraphQL format, so it can be returned by GraphQL properly.

#### Parameters

| Parameter | Type  |
| :-------- | :---- |
| `error`   | `any` |

#### Returns

`GraphQLError`

#### Source

[api/src/services/graphql/index.ts:1781](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L1781)

---

### getAggregateQuery()

> **getAggregateQuery**(`rawQuery`, `selections`): `Query`

Resolve the aggregation query based on the requested aggregated fields

#### Parameters

| Parameter    | Type                         |
| :----------- | :--------------------------- |
| `rawQuery`   | `Query`                      |
| `selections` | _readonly_ `SelectionNode`[] |

#### Returns

`Query`

#### Source

[api/src/services/graphql/index.ts:1721](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L1721)

---

### getQuery()

> **getQuery**( `rawQuery`, `selections`, `variableValues`): `Query`

Get a Directus Query object from the parsed arguments (rawQuery) and GraphQL AST selectionSet. Converts SelectionSet
into Directus' `fields` query for use in the resolver. Also applies variables where appropriate.

#### Parameters

| Parameter        | Type                         |
| :--------------- | :--------------------------- |
| `rawQuery`       | `Query`                      |
| `selections`     | _readonly_ `SelectionNode`[] |
| `variableValues` | `object`                     |

#### Returns

`Query`

#### Source

[api/src/services/graphql/index.ts:1595](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L1595)

---

### getSchema()

> **getSchema**(): `GraphQLSchema`

Generate the GraphQL schema. Pulls from the schema information generated by the get-schema util.

#### Returns

`GraphQLSchema`

#### Source

[api/src/services/graphql/index.ts:167](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L167)

> **getSchema**(`type`): `GraphQLSchema`

#### Parameters

| Parameter | Type       |
| :-------- | :--------- |
| `type`    | `"schema"` |

#### Returns

`GraphQLSchema`

#### Source

[api/src/services/graphql/index.ts:168](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L168)

> **getSchema**(`type`): `string` \| `GraphQLSchema`

#### Parameters

| Parameter | Type    |
| :-------- | :------ |
| `type`    | `"sdl"` |

#### Returns

`string` \| `GraphQLSchema`

#### Source

[api/src/services/graphql/index.ts:169](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L169)

---

### injectSystemResolvers()

> **injectSystemResolvers**( `schemaComposer`, `__namedParameters`, `schema`): `SchemaComposer`\< `any` \>

#### Parameters

| Parameter                                 | Type                                                                                                                                                                                     |
| :---------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `schemaComposer`                          | `SchemaComposer`\< \{`req`: `Request`\< `ParamsDictionary`, `any`, `any`, `ParsedQs`, `Record`\< `string`, `any` \> \>; `res`: `Response`\< `any`, `Record`\< `string`, `any` \> \>;} \> |
| `__namedParameters`                       | `object`                                                                                                                                                                                 |
| `__namedParameters.CreateCollectionTypes` | `Record`\< `string`, `ObjectTypeComposer`\< `any`, `any` \> \>                                                                                                                           |
| `__namedParameters.DeleteCollectionTypes` | `Record`\< `string`, `ObjectTypeComposer`\< `any`, `any` \> \>                                                                                                                           |
| `__namedParameters.ReadCollectionTypes`   | `Record`\< `string`, `ObjectTypeComposer`\< `any`, `any` \> \>                                                                                                                           |
| `__namedParameters.UpdateCollectionTypes` | `Record`\< `string`, `ObjectTypeComposer`\< `any`, `any` \> \>                                                                                                                           |
| `schema`                                  | `object`                                                                                                                                                                                 |
| `schema.create`                           | `SchemaOverview`                                                                                                                                                                         |
| `schema.delete`                           | `SchemaOverview`                                                                                                                                                                         |
| `schema.read`                             | `SchemaOverview`                                                                                                                                                                         |
| `schema.update`                           | `SchemaOverview`                                                                                                                                                                         |

#### Returns

`SchemaComposer`\< `any` \>

#### Source

[api/src/services/graphql/index.ts:1823](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L1823)

---

### parseArgs()

> **parseArgs**(`args`, `variableValues`): `Record`\< `string`, `any` \>

GraphQL's regular resolver `args` variable only contains the "top-level" arguments. Seeing that we convert the whole
nested tree into one big query using Directus' own query resolver, we want to have a nested structure of arguments for
the whole resolving tree, which can later be transformed into Directus' AST using `deep`. In order to do that, we'll
parse over all ArgumentNodes and ObjectFieldNodes to manually recreate an object structure of arguments

#### Parameters

| Parameter        | Type                        |
| :--------------- | :-------------------------- |
| `args`           | _readonly_ `ArgumentNode`[] |
| `variableValues` | `object`                    |

#### Returns

`Record`\< `string`, `any` \>

#### Source

[api/src/services/graphql/index.ts:1560](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L1560)

---

### read()

> **read**(`collection`, `query`): `Promise`\< `Partial`\< `Item` \> \>

Execute the read action on the correct service. Checks for singleton as well.

#### Parameters

| Parameter    | Type     |
| :----------- | :------- |
| `collection` | `string` |
| `query`      | `Query`  |

#### Returns

`Promise`\< `Partial`\< `Item` \> \>

#### Source

[api/src/services/graphql/index.ts:1511](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L1511)

---

### replaceFragmentsInSelections()

> **replaceFragmentsInSelections**(`selections`, `fragments`): `null` \| _readonly_ `SelectionNode`[]

Replace all fragments in a selectionset for the actual selection set as defined in the fragment Effectively merges the
selections with the fragments used in those selections

#### Parameters

| Parameter    | Type                                             |
| :----------- | :----------------------------------------------- |
| `selections` | `undefined` \| _readonly_ `SelectionNode`[]      |
| `fragments`  | `Record`\< `string`, `FragmentDefinitionNode` \> |

#### Returns

`null` \| _readonly_ `SelectionNode`[]

#### Source

[api/src/services/graphql/index.ts:1795](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L1795)

---

### replaceFuncs()

> **replaceFuncs**(`filter`): `Filter`

Replace functions from GraphQL format to Directus-Filter format

#### Parameters

| Parameter | Type     |
| :-------- | :------- |
| `filter`  | `Filter` |

#### Returns

`Filter`

#### Source

[api/src/services/graphql/index.ts:1758](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L1758)

---

### resolveMutation()

> **resolveMutation**(`args`, `info`): `Promise`\< `undefined` \| `boolean` \| `Partial`\< `Item` \> \>

#### Parameters

| Parameter | Type                          |
| :-------- | :---------------------------- |
| `args`    | `Record`\< `string`, `any` \> |
| `info`    | `GraphQLResolveInfo`          |

#### Returns

`Promise`\< `undefined` \| `boolean` \| `Partial`\< `Item` \> \>

#### Source

[api/src/services/graphql/index.ts:1424](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L1424)

---

### resolveQuery()

> **resolveQuery**(`info`): `Promise`\< `null` \| `Partial`\< `Item` \> \>

Generic resolver that's used for every "regular" items/system query. Converts the incoming GraphQL AST / fragments into
Directus' query structure which is then executed by the services.

#### Parameters

| Parameter | Type                 |
| :-------- | :------------------- |
| `info`    | `GraphQLResolveInfo` |

#### Returns

`Promise`\< `null` \| `Partial`\< `Item` \> \>

#### Source

[api/src/services/graphql/index.ts:1361](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L1361)

---

### upsertSingleton()

> **upsertSingleton**( `collection`, `body`, `query`): `Promise`\< `boolean` \| `Partial`\< `Item` \> \>

Upsert and read singleton item

#### Parameters

| Parameter    | Type                                                             |
| :----------- | :--------------------------------------------------------------- |
| `collection` | `string`                                                         |
| `body`       | `Record`\< `string`, `any` \> \| `Record`\< `string`, `any` \>[] |
| `query`      | `Query`                                                          |

#### Returns

`Promise`\< `boolean` \| `Partial`\< `Item` \> \>

#### Source

[api/src/services/graphql/index.ts:1528](https://github.com/directus/directus/blob/67c008df3/api/src/services/graphql/index.ts#L1528)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)