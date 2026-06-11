## v0.1.12 (2026-06-11)

## Changes

- chore(sdk): regenerate for telegram sandbox document route
- refactor(telegram): drop explanatory comments
- feat(telegram): gate group replies on addressing; fix question custom-answer flag
- feat(telegram): expose telegram tools as a gated facade MCP
- refactor(telegram): migrate client to grammy + harden reply/error paths
- fix(telegram): honor a slash-command agent on a reply
- fix(telegram): multi-question prompts support custom answers
- fix(telegram): per-message session keying
- fix(channels): restore granular Slack session-degraded error messages
- refactor(telegram): address PR review round 2
- refactor(telegram): address PR review — route guards + plugin client DRY
- feat(telegram): settings UI, account link/unlink, revoke cleanup, command re-sync
- refactor(telegram): drop the agent create_topic action
- refactor(telegram): drop telegram_bot_message, reuse webhook_thread aliases
- feat: add telegram integration tables in single migration
- refactor: reset migrations to origin/dev baseline
- refactor: consolidate migrations and remove unwanted docs/config
- refactor(channels): share inbound run resolution + reply artifacts across slack/email/telegram
- feat(telegram): reach parity with slack/email — interactive flag + shared sender attribution
- feat(telegram): two-way Telegram integration via the webhook-provider pattern
- fix(observability): cut trace noise from auth, health checks, and poll loops


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.12

---

## v0.1.11 (2026-06-10)

## Changes

- fix(observability): keep PostHog error tracking alongside OpenTelemetry
- feat(observability): enrich trace metadata for debuggability (REN-586)
- feat(observability): OpenTelemetry tracing for platform + sandbox state machine (REN-586)
- feat(pod-sandbox): await resume refresh via invalidate-complete signal
- fix(slack): fully decouple the answer wake workflow from the request lifecycle
- fix(pod-sandbox): give the resume ren:invalidate publish time to await the refresh
- fix(slack): fire-and-forget the wake workflow so the handler never blocks
- fix(webhook): address review — error code, single callback, direct-first delivery
- fix(webhook): three races behind webhook + question failures
- fix(opencode): deny facade MCP tools unless the agent binds them
- refactor(topology): drop unused defaultAgent from email mailbox nodes
- feat(canvas): show email mailboxes as nodes, sort pods by project count
- fix(signup): unblock OAuth redirect; stop spurious billing ZodError
- fix(pod-sandbox): bump bootstrap timeout 60s→120s


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.11

---

## v0.1.10 (2026-06-08)

## Changes

- feat(session): make session-url API self-contained for sandbox auth
- feat(email): expose emails CRUD to MCP
- refactor(email): flat /api/emails CRUD, rename project-email → email
- feat: default exclude deprecated resources at query schema level
- refactor(topology-share): simplify get-or-create, remove race condition handling
- chore(topology): remove yaml response support from GET /api/topology
- feat(topology-share): idempotent create + unique index + smaller icon
- fix: run prettier after generation to eliminate formatting churn
- fix(scope): return 400 with descriptive reason for scope mismatches
- fix(topology): include non-registry skills not attached to agents
- fix(skill): remove yaml dependency from frontmatter parsing
- feat(topology): first-class file/memory store collections
- feat(canvas): render flat topology spec + desired-state draft schema
- chore: update tags and integrations
- feat(docs): integrations guide as MCP resource + ren docs integrations
- refactor(canvas): adapt flat topology spec into blueprint on the client
- refactor(topology): reshape GET /api/topology into a flat id+slug spec
- feat(cli): ren docs — offline command tree + data-model guide
- feat(triggers): render cron schedules as humane cadence + action
- fix(canvas): vault↔pod edges, private entities, credential logos, pod order + interaction
- fix(ci): add missing RESEND_INBOUND_WEBHOOK_SECRET and EMAIL_CHANNEL_DOMAIN to all generate-step env blocks
- feat(email): thread agent-originated mail via Reply-To token + SES-root backfill
- feat(email): gate email_send per-agent via plugin-backed MCP (Slack parity)
- refactor(email): inline marked.parse, drop markdownToHtml wrapper
- feat(email): proactive email_send parity with Slack (attachments + reply continuity)
- feat(email): route agent by leading body slug instead of subject prefix
- fix(email): preserve agent allow-exceptions in non-interactive ruleset
- feat(email): non-interactive permissions for email-triggered turns
- test(email): regression tests for References-JSON threading and slug routing
- feat(email): markdown→HTML replies, subject agent routing, properties UI


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.10

---

## v0.1.9 (2026-06-06)

## Changes

- fix(api): exclude deprecated items from owned lists by default; add slug + deprecation tests
- fix(api): pass slug on mcp and skill create to prevent duplicate entries
- test(agent): assert version list/get serialize skills and mcps
- fix(agent): surface configured skills and MCPs on version card
- feat(api): upsert Zoho CRM Contact on signup


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.9

---

## v0.1.8 (2026-06-05)

## Changes

- refactor(slack): address PR review — trim agent tool surface, DRY types
- feat(slack): bind agent-originated threads to sessions; move tools into plugin
- feat(slack): agent-facing Slack tool surface via local MCP
- refactor(google): address review — simplify provider, drop dead surface
- feat(google): per-user Google Workspace OAuth provider (BYO app)
- refactor(mcp): remove dead connectClient runtime dispatcher
- fix(mcp): materialize basic-auth credentials into MCP_<slug>_BASIC
- feat(mcp): apply api_key credentials via query param in connectClient
- feat(vault): support basic auth credentials for MCPs end-to-end
- fix(ci): unbreak main deploys after canvas + bot-id changes
- chore(sdk): regenerate for topology endpoint
- feat(api): add GET /api/topology aggregate (SDK-only)
- chore(github): strip explanatory comments from shared-pod repo changes
- fix(opencode-plugin): gate worktree create on materialization, not dir existence
- feat(github): allow repo attachment on shared pods
- refactor(enrichment): address PR review — extract date helpers to util, hoist REGIE_BASE
- refactor(enrichment): improve WHOAMI.md rendering — month-precision timestamps, safe parsing, drop description line
- refactor(test): rename msw-apollo → msw-regie, remove embedded worktree
- refactor(enrichment): replace Apollo with Regie as sole provider, add REGIE_BEARER_TOKEN
- feat(enrichment): add enrichment module with Regie provider, write WHOAMI.md on user provisioning
- chore(slack): reword thinking status to "is working on it…"
- chore: updated message on slackbot thinking
- refactor(slack,opencode): address PR #276 review feedback
- fix(slack): reply to subagent permissions/questions via the main turn session
- test(slack): cover interactive handlers with a Slack client mock
- refactor(slack): construct WebClient through a makeSlackClient seam
- feat(slack): post pending interactive requests from the webhook poll loop
- feat(slack): Block Kit interactivity for permission + question tools
- feat(webhook-provider): add optional postInteractive reply-provider seam
- feat(opencode): surface pending interactive requests + reply helpers


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.8

---

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
