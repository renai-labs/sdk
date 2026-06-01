## v0.1.7 (2026-06-01)

## Changes

- feat(opencode): per-agent MCP scoping, default to sonnet-4-6, gh+aws in sandbox
- fix(app): default org logo to Ren mark
- feat(app): show version details in agent membership dialog
- chore: regenerate openapi, sdk and mcp tools
- feat(api): editable project agent membership


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.7

---

## v0.1.6 (2026-06-01)

## Changes

- rft(slack): prune via listChannels on reply failure
- rft(api): use conditional spread for project list user scope
- feat(slack): unified live channel-mapping API with auto-pruning
- fix(api): scope project list to caller, gate podId filter by pod membership
- rft(github): infer the org's single installation in routes
- feat(slack): expose install/channel management via SDK + CLI
- rft(slack): install flow should return json response
- feat(github): expose GitHub OAuth + management via SDK, JSON-based start
- fix(api): allow headless github oauth callback via state-bound vault


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.6

---

## v0.1.5 (2026-06-01)

## Changes

- fix(sandbox): build opencode-plugin during image assembly instead of copying stale dist
- feat(api): script to migrate pod-volume artifacts to slug-based keys
- chore(sdk): regenerate for slug-based manifest and session fields
- test(api): assert slug-based project paths and agent keys
- feat(api): materialize sandbox entities by slug instead of ULID
- refactor(slack): sender is email-match or channel fallback, else error
- feat(slack): per-channel fallback sender + richer channel-mapping UI
- refactor(api): drop dead exports surfaced by review
- refactor(api): share safeJsonParse, name artifact marker, improve slack copy
- refactor(opencode): centralize pod-volume IO and artifact read
- refactor(slack): clean up bolt ingress, drop retry, relocate provider types
- feat(slack): add channel-list endpoint for the install
- refactor(slack): split Slack out of the webhook-trigger provider abstraction
- feat(slack): drop thinking placeholder, post fresh reply on completion
- chore(api): squash slack-revamp migrations into one
- feat(slack): persist attachments to the pod volume and aggregate turn output
- feat(slack): add channel-mapping admin API
- feat(slack): route mentions via install channel mappings
- chore(api): auto-restart Temporal worker on file change
- fix(slack): request users:read.email scope for sender resolution
- refactor(slack): provider-pattern reply lifecycle, JSON channel mappings
- refactor(slack): simplify revamp — drop dead code, dedup reaction, fix query
- feat(slack): inbound files, error surfacing, retry Block Kit
- feat(slack): file reply pipeline — code blocks + showcase_artifact uploads
- feat(slack): streaming typing indicator, artifact extraction
- feat(slack): Bolt SDK migration, POST /api/slack/events, channel mapping dispatch
- feat(slack): add slack_channel_mapping domain
- feat(slack): add extractArtifacts, widen bot OAuth scopes
- feat(litellm): upgrade Anthropic flagship to Opus 4.8
- feat(sandbox): add Python 3 + uv to sandbox image


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.5

---

## v0.1.4 (2026-05-31)

## Changes

- refactor(api): extract pickPublic helper for registry view projection
- chore(sdk): regenerate after rebase onto dev
- refactor(api): consolidate public registry endpoints behind PublicView
- feat(api): expose session.create + session.url to MCP
- fix(api): build session URL with base64url directory segment
- feat(api/cli): expose session create + OpenCode URL to CLI
- fix(api): refresh pod artifacts volume creds like file/memory stores


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.4

---

## v0.1.3 (2026-05-27)

## Changes

- feat(opencode): gate ren CLI to ren agent, document volume purposes
- fix(model): scope agents to project dir, refresh base prompt
- refactor(agent): make create + initial version atomic
- feat(agent): create agent + initial version in one call
- fix(skill): return 409 on duplicate version instead of leaking SQL
- feat(cli): version flag, upgrade command, skill scope + publish
- refactor(sandbox): drop explanatory comment on findSandboxSessionPod
- refactor(token): extract randomToken, reuse for share tokens
- refactor(replay): address review — dedupe token read, clearer names
- refactor(replay): give sharing its own token, orthogonal to publishing
- fix(api): no-op sandbox session update for sessions Ren never registered
- fix(replay,auth): make share links resolve and correct invite URL path
- fix(github): preserve repo snapshots, fail loud on missing account, refresh status on focus
- test(mcp): update tool-name assertions to underscore-sanitized names
- chore(skill): remove explanatory comment from validator
- fix(skill): parse frontmatter with real YAML, stop rejecting valid skills
- fix(mcp): sanitize tool names to match MCP name pattern
- test(api): align identity + slug tests with current impl


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.3

---

## v0.1.2 (2026-05-26)

## Changes

- chore: prettier
- feat(api): hydrate agent latestVersion with skill + mcp refs
- feat(api): derive org defaults from email domain, smarter slugs
- feat(api): auto-create Default project for new teamspace pods
- chore: run generators
- chore(lint): fix all linting issues
- chore(api): merge migrations and generations
- feat(blueprint): persist project lineage and scope-filter the editor pickers
- feat(api): deprecation + autopublish for skill/agent/mcp/blueprint/replay
- feat(api): expose latestVersion on Agent.Info
- feat(api): make blueprint project/agent selection literal
- feat(app): publisher CRUD UI — per-asset listing + publish flow
- feat(api): replay update route + websiteMetadata editable on agent/mcp
- feat(api): allow editing publisher slug with uniqueness check
- feat(auth): auto-provision a publisher when an org is created
- feat(api): publish lifecycle for replay, skill, mcp, agent + publisher routes
- feat(blueprint): add install flow with batched forks and pinned-or-latest versions
- ft(api): Add parentId for allowing push updates later
- fix(pod): unify sandbox connection into one phase state machine
- refactor(session): scope data: truncation to tool attachments
- refactor(session): collapse data: truncation into one recursive walk
- refactor(session): inline transcript into OpencodeSession; truncate tool-attachment data URLs
- refactor(session): drop comments from transcript module
- refactor(session): simplify messages API
- perf(session): fetch single message via scoped event query
- feat(session): reject malformed pagination cursors with 400
- feat(session): paginated messages API for CLI/SDK/MCP
- rename: pushInvalidate -> pushInvalidateEventToSandbox
- refactor(pod): drop schedulePush debounce, fire pushInvalidate directly
- refactor(pod): fire-and-forget the invalidate POST, only await the sandbox lookup


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.2

---

# Changelog

## v0.1.1 (2026-05-24)

## Changes

- fix(ci): mirror ci.yml env block in release-package.yml
- fix(openapi): DATABASE_URL placeholder must parse as a URL
- fix(openapi): self-default storage env vars in openapi-generate


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.1
