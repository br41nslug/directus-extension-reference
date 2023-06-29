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

[api/src/services/websocket.ts:11](https://github.com/directus/directus/blob/67c008df3/api/src/services/websocket.ts#L11)

## Properties

### controller

> `private` **controller**: `WebSocketController`

#### Source

[api/src/services/websocket.ts:9](https://github.com/directus/directus/blob/67c008df3/api/src/services/websocket.ts#L9)

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

[api/src/services/websocket.ts:23](https://github.com/directus/directus/blob/67c008df3/api/src/services/websocket.ts#L23)

---

### clients()

> **clients**(): `Set`\< `WebSocketClient` \>

#### Returns

`Set`\< `WebSocketClient` \>

#### Source

[api/src/services/websocket.ts:31](https://github.com/directus/directus/blob/67c008df3/api/src/services/websocket.ts#L31)

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

[api/src/services/websocket.ts:19](https://github.com/directus/directus/blob/67c008df3/api/src/services/websocket.ts#L19)

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

[api/src/services/websocket.ts:15](https://github.com/directus/directus/blob/67c008df3/api/src/services/websocket.ts#L15)

---

Generated using [TypeDoc](https://typedoc.org/) and
[typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown)
