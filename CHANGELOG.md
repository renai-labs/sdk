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
