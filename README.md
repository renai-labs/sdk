# @renai-labs/sdk

TypeScript SDK for the Ren API.

## Install

```bash
npm install @renai-labs/sdk
```

## Quick start

```ts
import { createRenClient, pat } from "@renai-labs/sdk"

const client = createRenClient({
  baseUrl: "https://api.ren.example",
  auth: pat(process.env.REN_PAT_TOKEN!),
})

const { data: skills } = await client.skill.list()
```

Calls are grouped by resource — `client.skill`, `client.agent`, `client.pod`, `client.routines`, `client.session`, `client.mcp`, `client.vault`, `client.credential`, `client.fileStore`, `client.memoryStore`, `client.environment`, `client.replay`, `client.registry`, `client.pat`. Each exposes the operations available on that resource.

Every method returns `{ data, error, request, response }`. `data` is typed to the success payload; `error` is the typed error body for non-2xx responses.

## Authentication

Pass an auth strategy to `createRenClient`:

```ts
import { createRenClient, pat } from "@renai-labs/sdk"

// Personal Access Token (server-side, CLIs, CI)
createRenClient({ baseUrl, auth: pat(token) })
```

Custom strategies implement `AuthStrategy`:

```ts
import type { AuthStrategy } from "@renai-labs/sdk"

const apiKey: AuthStrategy = {
  apply: ({ headers }) => headers.set("X-Api-Key", process.env.MY_KEY!),
}

createRenClient({ baseUrl, auth: apiKey })
```

## Types

For apps that only need the shapes (form validators, type exports), use the `/types` subpath to avoid pulling in the client runtime:

```ts
import type { Skill, SkillCreateData } from "@renai-labs/sdk/types"
```

## Errors

Non-2xx responses don't throw by default — check `error` or opt into throwing:

```ts
const { data, error } = await client.skill.get({ path: { id } })
if (error) {
  // error is typed to the operation's error schema
}

const { data } = await client.skill.get({
  path: { id },
  throwOnError: true,
})
```

## Configuration

`createRenClient` accepts any `@hey-api/client-fetch` `Config` option — `baseUrl`, `headers`, `fetch`, `credentials`, interceptors, etc.

```ts
createRenClient({
  baseUrl: "https://api.ren.example",
  auth: pat(token),
  headers: { "X-Request-Id": crypto.randomUUID() },
  fetch: customFetch,
})
```

## License

MIT
