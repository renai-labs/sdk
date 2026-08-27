## v0.1.25 (2026-08-27)

## Changes

- fix(inference): surface the failures these paths were swallowing
- fix(inference): bill Ren-pool usage at catalog rates
- chore(api): squash branch migrations into one
- fix(inference): harden subscription routing contracts
- chore(api): renumber the subscription migration onto main
- fix(billing): gate budgets on billable paths only, not customer subscriptions
- fix(inference): scope key models to the org, unify variant defaults, share crypto helpers
- chore: strip code comments from the subscription routing changes
- fix(bridge): name routing surfaces after the wire, not the vendor
- fix(inference): bill subscription usage from the API, not response headers
- feat(inference): provider-neutral subscription routing
- chore(api): squash branch migrations into one
- refactor(claude): reuse shared helpers in the subscription module
- feat(model): ModelSelection object, fold internal/claude-* aliases
- feat(model): default every variant to medium
- refactor(claude): simplify subscription pool code after review
- refactor(claude): simplify subscription pool routing
- chore(api): squash branch migrations into one
- feat(models): add dynamic Claude variants
- feat(opencode): use internal subscription pools locally
- feat(claude): add organization subscription pools
- feat(app,ui): refine the guided onboarding and session chat
- feat(blueprint): expose the icon in the browse listing
- perf(api): warm the pod sandbox before anyone reaches the composer
- feat(blueprint): carry the authored icon onto the row
- fix(outreach): repair the welcome message and drop a dead helper
- feat(outreach): Slack Connect channel per paying customer
- fix(api): grant skill folder access under both cache spellings
- fix(api,app,cli): gate credits before the sandbox and block broke teams
- refactor(api): make budget sync the single owner of cron billing pause


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.25

---

## v0.1.24 (2026-08-20)

## Changes

- fix(registry): address assets on the live cdn host
- fix(vault): key a requirement by whatever satisfies it
- chore(sdk): regenerate for the setup guide on auth requirements
- feat(vault): carry an app's setup guide onto its credential requirements
- chore(sdk): regenerate for the blueprint brand colour
- chore(api): squash this branch's migrations into one
- feat(blueprint): store the vendor's brand colour
- feat(blueprint): carry example prompts through to the composer
- feat(api): carry a setup guide on mcp and skill, and a type on blueprint
- feat: point shipped artifacts at useren.ai
- feat(api): let a git skill's source pointer be updated
- refactor(registry): move the meta agent and its skills into ren-meta/
- fix(api): fold a ref-only agent's live skills into its project on migrate
- fix(api): validate a blueprint's gitRepos against the installing org
- feat(registry): make the folder tree the only catalog
- feat(api): converge blueprints on spec v3 and compile them from registry folders
- feat(api): add a per-cron-trigger model override
- docs(api): correct the timeout-tuning note after the PodSandbox reuse
- refactor(api): reuse the PodSandbox lookups in sandbox timeout tuning
- chore(api): drop the explanatory comments from the resume timeout fix
- fix(api): stop sandbox resume from clobbering a busy timeout window
- revert(api): drop the special case for our own organisation
- feat(api): close the invite with a thanks
- fix(api): tighten the invite copy
- feat(api): send member invites as plain text
- feat(api): never email replies to automated senders
- feat(api): send member invites from a dedicated mail subdomain
- fix(api): replay the OAuth resource indicator instead of deriving it
- refactor(billing): let the plan picker state the amounts plainly
- perf(billing): stop caching the plan catalogue


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.24

---

## v0.1.23 (2026-08-12)

## Changes

- fix(registry,api): point the meta agent at the real credentials page
- fix(registry,api): correct meta-skill facts and cut prose padding
- feat(registry,api): one skill for the meta agent
- chore(api): renumber the skill agent_name migration to 0051 after rebase onto main
- refactor(api): name the per-project menu builder for what it returns
- fix(api): stop the skill menu rebuild re-reading SKILL.md from S3
- fix(api): scope session reads to the caller's pod membership
- feat(app,api,ui): revamp the web workspace and three-tier vault model


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.23

---

## v0.1.22 (2026-08-11)

## Changes

- fix(api): correct the vault-attachment prose in the meta prompt and data model
- fix(api): only treat pod_id as a scope marker on pod-scoped tables
- refactor(api): rebuild the vault-tier migration on top of vault.pod_id
- fix(api): tighten vault provisioning, pod-vault oauth callbacks and fan-out
- fix(api): keep a vault in exactly one container tier
- style(api,app): drop the comments added by the vault-tiers change
- refactor(api): squash the vault-tier migrations into one
- feat(api,app): three-tier vaults replacing pod-vault attachment
- feat(api): add vault.pod_id ahead of the three-tier vault change
- test(api): assert the surviving store keeps its bytes, not its object count
- feat(api): put reference doctrine in the descriptions, seed store AGENTS.md
- fix(api): give every git reference a kind-bearing description
- refactor(api,plugin): drop the explanatory comments
- feat(api,plugin): consolidate agent context surfaces
- test(api): reset the skill caches after their suites, not just before each test
- refactor(api): trace the git mirror paths instead of counting them in-process
- docs(api): place the memory gauge in the documented middleware order
- feat(api): emit a process memory gauge with cache and mirror counters
- feat(api): trace the skill menu cache and git mirror path
- fix(api): sweep expired cache entries on read so they stop accumulating
- docs(api,plugin): the artifact template is not in the image (PR review)
- fix(api,cli,plugin): artifact defects found by the e2e pass
- fix(artifact): harden artifact workflows
- feat(api): auto-inject the ren-artifact skill into every project
- fix(cli): report the sandbox requirement before the template flag
- refactor(api,cli): move the artifact starter into the ren-artifact skill
- feat(api): give the artifact template shadcn/ui, Recharts and one theme file
- docs(api): document the artifact and pod-database entities
- feat(api): grant the artifacts tree to every agent in the pod
- feat(api): bake the artifact project template into the sandbox image


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.22

---

## v0.1.21 (2026-08-07)

## Changes

- fix(deploy): copy skill-md node_modules into the api runtime image
- fix(deploy): add @ren/skill-md workspace to api and site Dockerfiles
- docs: catch token-auth, auth-and-state, manifest-and-hot-reload up to skill-read serving (review)
- feat: opencode-exact SKILL.md parsing + skill-folder permissions that mirror load access
- refactor(api): fold the skill storage backfill into its migration script
- fix: align sandbox permission composition with skill serving
- fix: E2E-found fixes — opencode menu contract, skill-read rotation, CLI positionals/arrays, resource-check removal
- fix: strict review pass — token kind-scoped revoke, mirror completeness marker, discriminated version.data, tag parity, monitoring captures
- fix: review hardening pass + comment sweep
- feat(api): drop the legacy manifest skills field, serve skills only via the menu
- chore(gen): regenerate for project.skill.resolution + pod.resourceCheck (PR final)
- feat: one shared SKILL.md validator (@ren/skill-md) imported by API and CLI (PR 4)
- feat(api): /resource-check reads the sandbox status file (decision 9, PR 3)
- feat(opencode-plugin): consume skillMenuPath via opencode skills.urls, delete downloader (decision 6/9, Materialise #6)
- docs(api): document publish-no-fanout + deprecation-not-materialisation, rewrite skill AGENTS.md (Publish #3)
- feat(api): surface pin conflicts on project read + reach pin-archived + drop captures (decision 5, Edge F, Materialise #7)
- feat(api): publish of a git skill requires a publicly cloneable repo (decision 11, Publish #2)
- chore(gen): regenerate SDK/MCP/CLI + adapt first-party consumers (chunk 13)
- feat(api): manifest carries both legacy skills and new skillMenuPath (chunk 13)
- feat(api): skill monitoring sweep — mutation + fan-out failure captures (chunk 12)
- feat(api): harden skill-read serving auth — both-direction rejection, redaction, rate limit (chunk 9)
- feat(api): per-project skill serving — menu routes, 302 delivery, skill-read token (chunk 8/9)
- feat(api): per-file S3 skill storage, merged reads, one-shape data (chunk 7+10)
- feat(api): validate git skills at create, git skills are versionless (decision 1/2/3)
- feat(api): git skill mirror module + local git fixtures (decision 2/10, edge C/K)
- feat(api): JSON+base64 skill upload body, SKILL.md-authoritative overrides
- fix(api): archive skill + versions in one transaction, report blast radius
- refactor(api): one shared copy/fork column-mapper + broken-pin errors
- fix(api): atomic version archive, strict publish 409, race-safe conflicts
- refactor(api): rename SkillValidationError, drop unused contentHash, fix as-laundering


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.21

---

## v0.1.20 (2026-08-06)

## Changes

- refactor(api): split 0037 into pure-DDL migration + one-time scripts
- chore(api): renumber migration to 0037 + regenerate after main rebase
- chore(gen): regenerate for search summary rewording
- fix(api,cli): audit follow-ups — pod-member 400 mapping, migration owner backfill, explicit false predicate, transactional archive sweep, stale copy
- fix(api): topology share stays org-scoped at create (pre-union behavior)
- chore(api): renumber migration to 0035 + migrate new project binding routes to role guards
- fix(api): publish completes the ratchet in place + pin cross-org published mutation denials
- feat(clients): visibility filters replace ?scope=user across app, CLI, client-core, tui-plugin
- fix(api): gate mutations with owned guards + guard skill copy source (canOwn-on-mutation)
- chore(api): strip review-pass code comments + tighten user-lifecycle/pat types
- chore(api): collapse authz-pass migrations into one self-contained 0033
- feat(api): remove ?scope=user OpenAPI param + B25 surface assertions (A1, stage 11)
- feat(api): archive-before-delete + UnauthorizedError + auth monitoring (A15,E1-E6,E8,B22,B23,B26, stage 10)
- feat(api): pod visibility ceiling + sole-member invariant + defaults-follow-ceiling (A9,A10,A13,A16,B19, stage 9)
- fix(api): org-wide memory-store mountSlug uniqueness + dedupe migration (A11,A12,B20, stage 8)
- feat(api): in-place cascading promote replaces copyToOrg + ratchet pins (A6,A7,B16,B17,B8, stage 7)
- feat(api): guard split into visible/owned/load factories + rename cleanup (A8,D2,D3,D4,D5,N3,N4,N5,B18, stage 6)
- feat(api): union visibility + delete OwnerContext + visibility field (A1,N2,N6,B15,B6,B21, stage 5)
- test(api): retitle sandbox act-as test to role vocabulary (B4)
- feat(api): replace 40-scope catalog with rank-ordered Role + requireMinRole (A2-A5,C1-C3,D1,D6,N1,N7, stages 3-4)
- feat(api): add Role union + RenClaims Zod schema (D1, D2, B24, stage 2)
- test(api): pin resolver precedence + PAT authz matrix (B14, stage 1)
- feat(api): expose LiteLLM model IDs
- fix(api): address PR review comments on scoped instructions
- docs(api): blueprint docs for spec additions
- chore: regenerate sdk + openapi
- chore(api): blueprint spec test coverage
- feat(api): authored instructions/initialPrompt on blueprint create/update
- feat(api): blueprint install applies instructions, references, and project attachments
- feat(api): blueprint build captures project instructions, references, and attachments


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.20

---

## v0.1.19 (2026-07-15)

## Changes

- refactor(api): reset agent copy to 0.0.1 + carry skill metadata on copy
- refactor(api): simplify copy-to-org via toOrg + single transaction (REN-722)
- feat(api): replace promote-to-org with copy-to-org clone (REN-722)
- tdlr REN-722 done - added promote endpoint to move a private skill/agent/mcp to org scope
- fix(mcp): skip URL dedupe for gateway (mcp_provider) and plugin-backed MCPs
- refactor(mcp): simplify findDuplicateUrl to sequential precedence lookups
- fix(mcp): dedupe MCPs by URL within an org's accessible scope (REN-773)
- fix(linear): attribute agent session to comment author (REN-798)
- docs(api): update module CLAUDE.md for 13/14 Jul releases
- fix(vault): proactive MCP OAuth refresh sweeper + archive-on-fatal (REN-788)


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.19

---

## v0.1.18 (2026-07-13)

## Changes

- chore(api): squash 0018-0021 migrations into a single 0018
- refactor(api): remove Composio MCP seeding (moved to registry)
- feat(api): proxy Composio MCP traffic so the account key never enters the sandbox
- refactor(api): drop code comments from Composio integration
- feat(api): session-based Composio MCPs + Gmail/Google toolkits
- feat(api): add Composio-backed Outlook MCP as a vault-native provider credential
- feat(cron-trigger): support until boundaries
- fix(topology): gate Canvas pods on membership (REN-717)
- fix(migration): restore repo_mappings in 0019 snapshot
- refactor(linear): rename MCP slug to linear-ren and resolve project via issue
- refactor(linear): drop code comments per repo convention
- chore(linear): regenerate SDK/ops + fix tests after rebase onto dev
- docs(linear): document prod deployment + wire LINEAR_* prod secrets
- feat(linear): connect + project mapping from the web UI
- docs(linear): add SETUP.md for the Linear agent integration
- fix(linear): request write scope so the agent can post activities
- fix(linear): harden inbound dispatch, decouple oauth state secret
- feat(linear): store refresh token and auto-refresh expired access tokens
- feat(linear): add inbound Linear agent webhook channel (REN-511)
- refactor(github): address PR review on the PR agent
- refactor(github): split repo references from PR-agent channel mappings
- feat(github): PR mention ack reactions + senior-engineer prompt
- chore(github): drop local webhook test scripts from the PR
- fix(sandbox): add host.docker.internal mapping for local Docker provider
- feat(github): PR agent — @Ren mentions and opt-in auto-run
- chore(api): trim comments from undelete-poisoned-sessions script (REN-730)
- chore(api): add REN-730 undelete-poisoned-sessions remediation script
- test(api): assert exact 400 body for facade MCP binding error (REN-727)
- fix(api): return actionable message for facade MCP binding error (REN-727)
- refactor(api): move timezone helpers into util/date


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.18

---

## v0.1.17 (2026-07-05)

## Changes

- fix(docker): copy tui-plugin manifest so frozen install matches lockfile
- fix(docker): copy client-core manifest for frozen install
- fix(tui): attach session command
- refactor(api): drop the cli expose tag; client surface derives from sdk
- refactor(api): unify replay + topology share tokens onto sharing module (REN-706)


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.17

---

## v0.1.16 (2026-07-05)

## Changes

- feat(scripts): re-point channel-posting crons to the meta agent
- refactor(manifest): stop force-injecting facade MCPs onto the meta agent
- refactor(migration): unify channel-agent migrations, extract data cleanups to scripts
- refactor(meta-agent): trim the originated-turn topology section
- feat(meta-agent): guard topology changes on originated turns
- refactor(subagent): address PR review
- fix(subagent): persist and rehydrate subagent session messages
- fix(triggers): blast-radius fixes for nullable trigger agent
- refactor(triggers): give cron/webhook their own trigger_message envelope
- feat(triggers): default cron/webhook to ren meta agent with handback
- fix(prompts): explain channel handback in meta-agent routing
- fix(slack): process file_share DMs so attachments reach the sandbox
- refactor(prompts): handle missing-integration and tangential requests; drop config comment
- fix(permissions): grant handoff explicitly to ren instead of relying on default
- refactor(prompts): name the channel MCPs (Slack/email/Telegram) instead of "facade channels"
- refactor(meta-agent): drop cross-agent MCP reach; gate handoff to Ren only
- refactor(channel-prompts): unify per-turn injection into one <channel_message> tag
- refactor(channel-prompts): gate channel-bound reply guidance on the reply_channel marker
- refactor(prompts): reframe meta-agent situational prompt and enrich roster
- feat: pin models for opencode default agents in pod sandboxes
- refactor: inline facade-mcp load into manifest; facade.ts is just resolveChannelPromptSections (REN-711)
- refactor: rename metaFor→getMetaAgentForProject, handBackToRen→handBackToMetaAgent; drop explanatory comments (REN-711)
- refactor: simplify channel→meta routing per review (REN-711)
- feat: route user channels to the project meta agent (REN-711)
- docs(api): tell meta agent to use --output json and --fields for session traces (REN-662)
- fix(api): correct ren CLI traces command form in meta-agent prompt (REN-662)
- feat(api): session execution traces endpoint for meta agent self-observability (REN-662)
- refactor(api): address REN-662 review — scoped meta-prompt, ids, version note
- feat(api): per-project Ren meta agent — auto-attach, situational prompt, reach (REN-662)
- refactor(slack): reply-channel wording + one-clarification/hyphen prompt rules (REN-707)


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.16

---

## v0.1.15 (2026-06-15)

## Changes

- fix(sandbox): make attached-environment package installs work
- feat(sandbox): offload Langfuse media server-side in the OTLP forwarder
- feat(sandbox): bootstrap-once runtime setup + sandbox recreate kill switch
- feat(sandbox): install attached environment packages on bootstrap
- refactor(sandbox): drop LANGFUSE_ENVIRONMENT and explanatory comments
- feat(sandbox): forward OTEL traces to Langfuse via server-side proxy
- fix(slack): ingest snippets/links cleanly + add question dismiss


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.15

---

## v0.1.14 (2026-06-15)

## Changes

- fix(sandbox): re-apply idle timeout on resume
- fix(sandbox): forward POSTHOG_API_KEY/HOST into sandbox bootstrap env
- fix(sdk): throw real ApiError instead of plain object
- fix(docker): copy experiments/video manifest for frozen install
- fix(test): stub mailer in invitation suite to stop real Resend calls in CI
- chore: prettier-format invitation.test.ts
- fix(auth): unblock invitation accept and normalize pending-invite lookup (REN-613)
- fix(opencode): advertise model attachment + image modalities to opencode (REN-624)


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.14

---

## v0.1.13 (2026-06-11)

## Changes

- feat(telegram): allow setting fallback sender at claim time


Published to npm: https://www.npmjs.com/package/@renai-labs/sdk/v/0.1.13

---

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
