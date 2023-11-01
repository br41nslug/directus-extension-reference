[**directus-monorepo**](../README.md) ( [Readme](../README.md) \| [API](../API.md) )

---

[directus-monorepo](../API.md) > WebSocketService

# Class: WebSocketService

## Constructors

### constructor()

> **new WebSocketService**(): [`WebSocketService`](class.WebSocketService.md)

#### Returns

[`WebSocketService`](class.WebSocketService.md)

#### Source

[api/src/services/websocket.ts:14](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/websocket.ts#L14)

## Properties

### controller

> `private` **controller**: `WebSocketController`

#### Source

[api/src/services/websocket.ts:12](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/websocket.ts#L12)

## Methods

### broadcast()

> **broadcast**(`message`, `filter`?): `void`

#### Parameters

| Parameter      | Type                                                                                                                                                             |
| :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `message`      | `string` \| `objectOutputType`\< \{`type`: `ZodString`; `uid`: `ZodOptional`\< `ZodUnion`\< [`ZodString`, `ZodNumber`] \> \>;}, `ZodTypeAny`, `"passthrough"` \> |
| `filter`?      | `object`                                                                                                                                                         |
| `filter.role`? | `string`                                                                                                                                                         |
| `filter.user`? | `string`                                                                                                                                                         |

#### Returns

`void`

#### Source

[api/src/services/websocket.ts:36](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/websocket.ts#L36)

---

### clients()

> **clients**(): `Set`\< `WebSocketClient` \>

#### Returns

`Set`\< `WebSocketClient` \>

#### Source

[api/src/services/websocket.ts:44](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/websocket.ts#L44)

---

### off()

> **off**(`event`, `callback`): `void`

#### Parameters

| Parameter  | Type                                                 |
| :--------- | :--------------------------------------------------- |
| `event`    | `"connect"` \| `"message"` \| `"error"` \| `"close"` |
| `callback` | `ActionHandler`                                      |

#### Returns

`void`

#### Source

[api/src/services/websocket.ts:32](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/websocket.ts#L32)

---

### on()

> **on**(`event`, `callback`): `void`

#### Parameters

| Parameter  | Type                                                 |
| :--------- | :--------------------------------------------------- |
| `event`    | `"connect"` \| `"message"` \| `"error"` \| `"close"` |
| `callback` | `ActionHandler`                                      |

#### Returns

`void`

#### Source

[api/src/services/websocket.ts:28](https://github.com/directus/directus/blob/3a4abb10c/api/src/services/websocket.ts#L28)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
