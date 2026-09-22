# Artifact Quality Standards for Combined Role Architecture

**Memo.** Evidence standards for Product Engineer / Backend / SWE / Founding Engineer work.  
**Not a tutorial.** Specifies what a hiring-grade artifact *is*, with public primary sources.  
**Aligned with Route 5:** Kubernetes-for-one and event-sourcing-as-identity are theater at 1-person scale; this memo does not treat them as evidence.

**Tagging.** Every load-bearing claim is tagged:

- **[Evidence]** — observed in a named public source or repo file.
- **[Inference]** — reasoned from that evidence for Combined Role / Tower.
- **[Hypothesis]** — plausible but not independently verified here.

---

## 1. Architecture actually used at product companies

The public record for mid-market / startup *product* companies is **not** “microservices from day one.” It is **monolith first, modular monolith when team/code coupling hurts, services only when a specific pain pays the premium.**

### 1.1 Fowler: MonolithFirst + Microservice Premium

**[Evidence]** Fowler, *Monolith First* (3 Jun 2015): “Almost all the successful microservice stories have started with a monolith that got too big and was broken up.” “Almost all the cases where I’ve heard of a system that was built as a microservice system from scratch, it has ended up in serious trouble.” Two reasons: YAGNI (cycle time for feedback) and unstable Bounded Contexts (refactoring across network boundaries is “a layer of treacle”). He is explicit that even experienced architects get boundaries wrong at the start. https://martinfowler.com/bliki/MonolithFirst.html

**[Evidence]** Fowler, *Microservice Premium*: “don’t even consider microservices unless you have a system that’s too complex to manage as a monolith. The majority of software systems should be built as a single monolithic application. Do pay attention to good modularity within that monolith.” https://www.martinfowler.com/bliki/MicroservicePremium.html

**[Evidence]** Fowler, *Microservice Trade-Offs* (1 Jul 2015): the premium (failure handling, eventual consistency, independent contracts, extra pipelines) is only recouped in more complex systems. https://martinfowler.com/articles/microservice-trade-offs.html

### 1.2 Shopify: modular monolith as the *next* step after a working monolith

**[Evidence]** Westeinde, *Deconstructing the Monolith* (21 Feb 2019). Shopify is “one of the largest Ruby on Rails codebases,” decade+ of work, 1000+ developers. They rejected a microservice split because it would add per-service pipelines, infra, network latency, and data isolation they did not want. They kept **one codebase / one deployable** and introduced **enforced domain boundaries** (orders, shipping, billing, inventory) with public APIs between components and exclusive data ownership. Quote: “no architecture is often the best architecture in the early days”; “Designing a complex system of microservices before you have domain expertise is a risky move.” They cite Fowler’s Design Stamina Hypothesis: trade design quality for time-to-market until feature velocity actually slows. https://shopify.engineering/deconstructing-monolith-designing-software-maximizes-developer-productivity

**[Evidence]** Müller, *Under Deconstruction: The State of Shopify’s Monolith*. 18-month retrospective: they still stand by modular monolith; details changed; Packwerk/components exist because **people scale**, not because a 1-person shop needs package walls. https://shopify.engineering/shopify-monolith

**[Evidence]** *Enforcing Modularity in Rails Apps with Packwerk*. Component folders were a social contract; Packwerk adds walls (package visibility, acyclic deps). Later open-sourced as `Shopify/packwerk`. https://shopify.engineering/enforcing-modularity-rails-apps-packwerk · https://github.com/shopify/packwerk

### 1.3 Third and fourth primary sources (not Shopify/Fowler)

**[Evidence]** 37signals / DHH, *The Majestic Monolith* (2016): Basecamp 3 is one app, one database, ~12 programmers, hundreds of screens, 200 controllers / 190 models — “the necessity of this situation simply isn’t compatible with a highly labour intensive pattern like M/SOA.” “Stay in the majestic monolith as long as you can.” https://signalvnoise.com/svn3/the-majestic-monolith/

**[Evidence]** 37signals, *Vanilla Rails is plenty*: they do not split application vs domain layers as first-class architecture; they run Basecamp 4 on a ~9-year-old codebase (400 controllers, 500 models). Jobs are invoked from domain models. https://dev.37signals.com/vanilla-rails-is-plenty/

**[Evidence]** 37signals, *Introducing Solid Queue* / *Solid Queue 1.0*: production jobs at HEY are ~20 million/day, DB-backed (not a Kafka identity), separate jobs DB, Kamal deploys. The craft object is **operable jobs**, not a message bus résumé line. https://dev.37signals.com/introducing-solid-queue/ · https://dev.37signals.com/solid-queue-v1-0/

**[Evidence]** Segment / Twilio, *Goodbye Microservices* (Alexandra Noonan, 10 Jul 2018): they split destinations into 140+ services/repos to isolate head-of-line blocking; operational overhead then scaled linearly (3 FTEs “keeping the system alive”). They **merged back to one service + one repo**, required a rock-solid test suite (Traffic Recorder), and accepted worse fault isolation / cache locality. “One engineer can deploy the service in a matter of minutes.” They still use microservices *elsewhere* where the trade-off paid. https://www.twilio.com/en-us/blog/developers/best-practices/goodbye-microservices

**[Evidence]** GitLab Handbook, *Rails Monolith Decomposition / Modular Monolith* (design doc, 2023–): 2.2M lines of Ruby, hundreds of daily contributors. Direction is modular monolith *with satellite services*, bounded contexts (`Ci::`, `MergeRequests::`), Packwerk, hexagonal adapters (Web / REST / GraphQL / Sidekiq), ADRs. Explicit: “Modularize broadly, extract selectively… a module is extracted into a separately deployed service only when the ROI is clear.” Data coupling (shared tables, cross-boundary FKs) is what actually blocks extraction. https://handbook.gitlab.com/handbook/engineering/architecture/design-documents/modular_monolith/

**[Inference]** For a Combined Role Architecture at 1-person / small-startup scale, the *professional* architecture claim is: **one deployable, modules by domain, Postgres as source of truth, a job runner, explicit public interfaces between modules.** The *unprofessional* claim is a mesh of empty services, Kubernetes, or event-sourcing-as-identity. Shopify’s componentization and GitLab’s Packwerk are **org-scale enforcement**, not a 1-person prerequisite; the transferable *idea* is named boundaries and exclusive data ownership, not the tooling.

**[Hypothesis]** Hiring managers who have operated a product will treat a 1-person microservice CV as a negative signal (Route 5 already states this). Hiring managers who have not operated a product may reward the logos. The Combined Role Architecture should specify evidence for the first audience.

---

## 2. What a professional application repo contains (vs a portfolio repo)

A portfolio repo proves **you can assemble a stack**. A professional repo proves **the system can be changed, operated, and not lie**. The difference is visible as *files that exist and are used*, not as a README claim.

Inspected public products that actually have **schema + jobs + API + tests + CI** (picked 3; Plane skipped — the three below already cover the checklist).

### 2.1 `chatwoot/chatwoot` — Rails modular monolith, SaaS + self-host

**Directory shape [Evidence]** (https://github.com/chatwoot/chatwoot, `develop`):

| Concern | Files that exist |
|---|---|
| HTTP / domain | `app/controllers`, `app/models`, `app/services`, `app/actions`, `app/listeners`, `app/builders` |
| Authz | `app/policies/` (Pundit-style policy objects — authorization as code, not a comment) |
| Jobs / queues | `app/jobs/`; `config/sidekiq.yml` (priority queues: `critical` … `async_database_migration`); `config/initializers/sidekiq.rb` (JSON logs in prod, `sidekiq-cron` loaded from schedule YAML, deleted cron entries cleaned on deploy) https://github.com/chatwoot/chatwoot/blob/master/config/sidekiq.yml · https://github.com/chatwoot/chatwoot/blob/master/config/initializers/sidekiq.rb |
| Schema / migrations | Rails `db:migrate` is the documented production update path https://developers.chatwoot.com/self-hosted/deployment/architecture |
| OpenAPI | `swagger/index.yml`, `swagger/paths/`, `swagger/definitions/`, committed `swagger/swagger.json` (~519 KB). PR #13623 adds Skooma validation so request specs assert the documented contract matches Rails behavior; CI detects Swagger drift (`rake swagger:build`, `spec/swagger/openapi_spec.rb`) https://github.com/chatwoot/chatwoot/pull/13623 |
| Tests | `spec/` mirrors app: `spec/jobs`, `spec/controllers`, `spec/integration`, `spec/factories`, `spec/fixtures`, plus enterprise strip in CE CI |
| CI | `.github/workflows/run_foss_spec.yml`: RuboCop, Brakeman (warn-only), `bundle-audit`, ESLint, frontend coverage, **16-way RSpec matrix** against Postgres (`pgvector/pgvector:pg16`) + Redis; `db:schema:load` before tests. Also `run_mfa_spec.yml`, Docker publish workflows, `deploy_check.yml` https://github.com/chatwoot/chatwoot/blob/develop/.github/workflows/run_foss_spec.yml |
| Deploy hints | Production architecture is **web + workers + Postgres + Redis + SMTP + object storage**, not a cluster of domain microservices. Recommended: Heroku / Docker / Linux; K8s is *an* option, not the identity. https://developers.chatwoot.com/self-hosted/deployment/architecture · `docker-compose.yaml` / `docker-compose.production.yaml` |

**[Inference]** Chatwoot is the closest public analogue to “Tower as a product”: one Rails app, Sidekiq as the clock, policies as authz, OpenAPI that CI tries to keep honest, migrations as the update ritual.

### 2.2 `calcom/cal.com` — Turborepo product monorepo (web + API + jobs)

**Directory shape [Evidence]** (https://github.com/calcom/cal.com):

| Concern | Files that exist |
|---|---|
| Apps | `apps/web` (Next.js), `apps/api/v1`, `apps/api/v2` |
| Shared domain | `packages/features/` (feature packages), `packages/trpc/`, `packages/lib/`, `packages/platform/` |
| Schema / migrations | `packages/prisma/schema.prisma` (~101 KB), `packages/prisma/migrations/`, `seed` / PBAC seed scripts, `auto-migrations.ts`, `zod-utils.ts` + `zod-utils.test.ts` |
| Authz | PBAC artifacts in Prisma (`seed-pbac-only.ts`, `cleanup-pbac.ts`) — permission is a schema concern, not a middleware afterthought |
| Jobs | Trigger.dev Tasker pattern: `packages/features/<domain>/lib/tasker/` with interface, async implementation, **sync fallback**, Zod schema, queue/retry/concurrency config. Documented in `agents/rules/patterns-trigger-dev.md`. Example domains: calendars, webhooks. Env `ENABLE_ASYNC_TASKER` selects async vs inline (E2E uses sync so tests do not wait for a cron). https://github.com/calcom/cal.com/blob/main/agents/rules/patterns-trigger-dev.md |
| Tests | Vitest unit; Playwright E2E (web 8 shards); API v2 Jest E2E (4 shards) with **Postgres + Redis services** in `.github/workflows/e2e-api-v2.yml` |
| CI | Path-filtered PR pipeline: prisma-change detection, trust-check gate before secrets, sharded E2E, dedicated `setup-db` to avoid cache races. They write about CI as an engineering product (30 min → 5 min). https://cal.com/blog/how-we-cut-our-ci-wall-time-from-30-minutes-to-5-minutes |
| Observability / deploy | Documented: Sentry, Vercel/Docker, GitHub Actions. Architecture wiki: unit = Vitest, E2E = Playwright, mocks = Prismock. https://calcom-cal-com.mintlify.app/developers/contributing/architecture |

**[Inference]** Cal.com shows the *TypeScript product* shape: schema package with migrations, feature packages (not per-entity services), jobs with explicit retry/concurrency, contract-ish Zod at the job boundary, CI that runs real Postgres.

### 2.3 `twentyhq/twenty` — NestJS + worker process + upgrade commands

**Directory shape [Evidence]** (https://github.com/twentyhq/twenty):

| Concern | Files that exist |
|---|---|
| Processes | Distinct **API server**, **BullMQ worker**, **CLI/command** (migrations/upgrades), **frontend**. README stack: NestJS, BullMQ, PostgreSQL, Redis. https://github.com/twentyhq/twenty |
| Jobs | `packages/twenty-server/src/engine/core-modules/message-queue/` — `BullMQDriver`, `jobs.module.ts`, worker lifecycle; Sentry isolation around job handlers. Cron via `cron-register-all.command.ts`. Worker is a separate prod target (`twenty-server:worker:prod`). |
| Schema / migrations | TypeORM core migrations; **versioned upgrade commands** that must not be rewritten for past versions. CI job `server-previous-version-upgrade-mutation-guard` fails if historical upgrade dirs change. CI also **generates a migration and fails if schema drift is uncommitted**. |
| API contract | GraphQL + REST OpenAPI (`/rest/open-api/core`, `/rest/open-api/metadata`). `.github/workflows/ci-breaking-changes.yaml` boots **two servers** (main vs PR) and diffs introspection + OpenAPI. |
| Tests / CI | `.github/workflows/ci-server.yaml`: Postgres + Redis services, health-check the server, **worker smoke** (start worker, timeout 30s = pass), pending-migration detection, sharded integration tests. Also `app-prod-parity-e2e-dispatch.yaml`, `cd-deploy-main.yaml`, `cd-deploy-tag.yaml`. |
| Deploy hints | `packages/twenty-docker/docker-compose.yml` runs server + worker as separate processes. |

**[Inference]** Twenty is the cleanest public example of “OpenAPI matching reality” as a **CI gate**, and of “jobs are a process you boot,” not a folder of TODOs.

### 2.4 `TryGhost/Ghost` — extra signal on *migrations as a reviewed ritual*

**[Evidence]** Ghost is a pnpm/Nx monorepo (`ghost/core`, `apps/*`, `packages/*`, `e2e/`). Tests are split: `pnpm test:unit` (Vitest), `test:integration` (DB), `test:e2e` (server-side webhooks/API — not browser), Playwright at repo root. Redis/MinIO/S3 suites skip locally, **always run in CI**. https://github.com/TryGhost/Ghost/blob/main/AGENTS.md

**[Evidence]** `.github/workflows/migration-review.yml` auto-labels PRs that touch `ghost/core/core/server/data/schema/**` or `migrations/versions/**` and posts a checklist: **idempotent `up()`/`down()`**, no mixed DDL/DML, batched mass updates, “defends against missing or invalid data,” performance on staging (local is not production), MySQL **and** SQLite. Separate `scripts/check-migration-integrity.cjs` in CI. https://github.com/TryGhost/Ghost/blob/main/.github/workflows/migration-review.yml

**[Inference]** Professional evidence for schema work is not “I have a `schema.prisma`.” It is **a review ritual that treats migrations as production events**.

### 2.5 Checklist: professional repo vs portfolio repo

| Artifact | Portfolio (typical) | Professional (observed above) |
|---|---|---|
| README / screenshots | Center of gravity | Exists, but is not the proof |
| Schema | `schema.sql` or ORM models only | Versioned migrations + integrity/drift CI (Ghost, Twenty, Cal Prisma) |
| Tests | A few unit tests or “how to run” | Layered: unit + DB-backed + job specs + E2E shards; factories/fixtures |
| CI | Badge or none | Path-filtered, real Postgres/Redis, lint + security scan + test matrix |
| Jobs | `setTimeout` or missing | Queue config, retries, worker process, cron registration, job tests |
| Authz | `if (user.id === …)` in controllers | Policy objects / PBAC tables / documented rules |
| API contract | Swagger generated once, stale | Committed spec + **drift/breaking-change CI** (Chatwoot Skooma, Twenty OpenAPI diff) |
| Observability | `console.log` | Structured prod logs (Chatwoot Sidekiq JSON), Sentry around workers (Twenty), Sentry in Cal |
| Docs / ADRs | Tutorial README | GitLab-style ADRs (context / decision / consequences / alternatives) https://handbook.gitlab.com/handbook/engineering/architecture/workflow/ |
| Incidents / runbooks | Absent | GitLab: runbooks repo, alert playbooks, blameless review, corrective-action issues. 1-person version is a dated incident note + “what I would run,” not incident.io. https://handbook.gitlab.com/handbook/engineering/infrastructure-platforms/incident-management/ |
| Deploy | “npm start” | Compose with **web + worker + db + cache**; migrate command in the release notes |

**[Hypothesis]** Public OSS under-represents private runbooks/incident notes (those live in company handbooks). A 1-person firm can still *have* them in-repo (`docs/incidents/`, `docs/runbooks/`). Their absence is a demo smell; their presence is uncommon and therefore high-signal.

---

## 3. Testing expectations: table-stakes vs excellent

### 3.1 What engineering orgs actually prescribe

**[Evidence]** *Software Engineering at Google*, ch. 11 (Adam Bender): aim ~**80% narrow unit / 15% integration / 5% E2E** by test *count*. Unit tests are the base because they are fast and localize failure. Ice-cream-cone (mostly E2E) and hourglass (unit + E2E, no integration) are named antipatterns. Tests exist to enable **change**, not just to catch bugs. GWS case: requiring tests on every change halved emergency pushes despite more changes. https://abseil.io/resources/swe-book/html/ch11.html

**[Evidence]** Same book, ch. 14: move to the pyramid in the first days; TAP (CI) only accepts **hermetic, single-change, time-bounded** tests — which is why unit tests dominate the *required* lane. Larger tests fill gaps but are not the submission gate. Prefer API-driven E2E over UI-through-backend multiplicative tests. https://abseil.io/resources/swe-book/html/ch14.html

**[Evidence]** Google Testing Blog, *How Much Testing is Enough?* (2021): after unit + integration, E2E covers **Critical User Journeys** (goal + path), not every feature. Feature/behavior coverage is a risk metric distinct from line coverage. https://testing.googleblog.com/2021/06/how-much-testing-is-enough.html

**[Evidence]** Fowler, *The Practical Test Pyramid*: integration tests are **narrow** (one integration point); contract tests (CDC / Pact) verify the stub against the real provider so mocks do not drift. https://martinfowler.com/articles/practical-test-pyramid.html

**[Evidence]** GitLab docs, *Sidekiq idempotent jobs*: workers must be safe to run twice; they ship `it_behaves_like 'an idempotent worker'` and a cop that fails if `idempotent!` is missing. Dedup (`until_executing` / `until_executed`) is **not** a substitute for idempotent effects. https://docs.gitlab.com/development/sidekiq/idempotent_jobs/

**[Evidence]** Chatwoot PR #13623 and Twenty `ci-breaking-changes.yaml` are the production form of “contract test”: the documented API is executed or diffed in CI.

### 3.2 What interviews actually score vs what blogs say is excellent

| Layer | Table-stakes (SWE / backend screen) | Excellent (owns a system) |
|---|---|---|
| Unit | Can write a test; talks edge cases; Google L3 coding is still DSA + correctness, not a test-strategy lecture. https://onsites.fyi/blog/article/google-L3-software-engineer-interview-questions | State-machine transition table tested **without** a DB; named invariants; no mock-heavy ice cream |
| Integration | Can say “I’d hit a real Postgres” | Testcontainers / CI Postgres; job + transaction + unique index; factories, isolated, order-independent (dhung.dev framework; Chatwoot `spec/jobs` + `spec/integration`) |
| Contract | Mentions OpenAPI | OpenAPI/Pact/Zod **gated**: drift fails the build (Chatwoot Skooma; Twenty OpenAPI diff; Fowler CDC) |
| E2E / CUJ | “Playwright for the happy path” | Few journeys; sharded; sync-fallback so E2E does not depend on a live queue (Cal Tasker) |
| Load | Recited in system-design loops (L4+) | Rarely table-stakes for mid product SWE. Excellent = one measured SLO on the CUJ you sell (eligibility check p95, job lag), not a k6 badge with no users |

**[Inference]** For Combined Role evidence, **excellent is not “all four layers plus load.”** Excellent is: (1) unit tests of the eligibility state machine, (2) integration tests of “job dies after commit,” (3) a contract that matches the HTTP API, (4) one or two CUJs. Load testing without production traffic is theater adjacent to Kubernetes-for-one.

**[Hypothesis]** FAANG/platform loops will still ask you to *talk* load/partitioning. The artifact that survives founder-discount is the integration/idempotency story, not the k6 repo.

---

## 4. Observability, security, CI/CD: 1-person production vs FAANG/platform

### 4.1 1-person production (table-stakes that are actually used)

**[Evidence]** Charity Majors: “Developing software with observability is better at ANY scale… tiny one-person teams.” Observability is inspecting production (debugger-for-systems), not a three-pillar platform. Hook the loop: the person who wrote the code is on-call for it. https://charitydotwtf.substack.com/p/questionable-advice-how-do-i-get-my-team-into-observability

**[Evidence]** Majors, *Observability 2.0*: “Your job as a developer isn’t done until you know it’s working in production. Deploying to production is the beginning…” Precision on “what happened when I deployed,” not dashboards of averages. https://www.honeycomb.io/blog/time-to-version-observability-signs-point-to-yes

**[Evidence]** Startup SRE guidance: a 12-person team does not need “Kubernetes-level observability.” Implement the practice that removes the current recurring pain. Under ~50 engineers: answers to “is it up / is it slow / is it erroring / is the job late,” Prometheus/Grafana or a hosted equivalent. https://thegoodshell.com/sre-practices-for-startups/

**[Evidence]** Chatwoot production Sidekiq uses JSON logs; Twenty wraps workers in Sentry; Cal documents Sentry. That is the *observed* 1-product bar.

**1-person should have [Inference]:**

- Structured logs with request/job IDs you have actually grepped at 2 a.m.
- Error reporting on the web process **and** the worker (Twenty’s split is the point).
- Uptime + one business signal (job lag, eligibility-check error rate) — not 40 RED dashboards.
- Backups you have restored once.
- CI that runs tests + migrations against real Postgres (all three repos).
- Dependency/security scan (Chatwoot `bundle-audit` + Brakeman; OWASP ASVS L1 as the *checklist*, not a certification).
- Secrets not in git; TLS; hashed passwords; **server-side authz** (ASVS V8: function- and object-level, deny-by-default, IDOR tests). https://asvs.dev/v5.0.0/V8-Authorization/ · https://github.com/OWASP/ASVS
- Deploy = build + migrate + restart web + restart worker + rollback note. Compose or a PaaS. Not a mesh.

### 4.2 FAANG / platform roles (different object)

**[Evidence]** Google SRE Workbook, *Alerting on SLOs*: multi-window, multi-burn-rate alerts on **error budget**, not “CPU > 80%.” This assumes SLIs, error budgets, and an on-call *organization*. https://sre.google/workbook/alerting-on-slos/

**[Evidence]** GitLab incident handbook: EOC + Incident Manager + CMOC, runbooks repo (mirrored to ops), alert playbooks with troubleshooting commands, blameless review within days, corrective-action issues with acceptance criteria. https://handbook.gitlab.com/handbook/engineering/infrastructure-platforms/incident-management/ · https://handbook.gitlab.com/handbook/engineering/infrastructure-platforms/alert-playbook-management/

**[Evidence]** Startup-vs-big-tech SRE writeups: at 10 SREs you fight for any instrumentation; at 50 you can make RED metrics a deploy gate. Platform roles exist to *standardize that path for other teams*. https://medium.com/developersglobal/sre-at-a-startup-vs-big-tech-what-actually-changes-cd496f90d905

**[Inference]** Copying FAANG platform artifacts (SLO burn-rate matrices, service mesh, golden-path platform) as a 1-person identity is the same category of theater as Kubernetes-for-one. Copying the **questions** (what is the CUJ, what do I page on, what did I write down after it broke) is professional.

**[Inference]** Security: ASVS L1 (authn, authz, validation, TLS, no default accounts) is the 1-person bar. L2/L3 (hardware MFA, contextual step-up, field-level authz docs) is what platform/security/fintech seats expect as *process evidence*, not as a solo checklist completed in a weekend.

---

## 5. What would make Omcoda / Tower look like professional evidence

Tower’s object (from Route 5): eligibility state machine + monitoring jobs + reactivation workflows + HTTP API + Postgres.

A demo is “I can POST an eligibility and get JSON.”  
Professional evidence is **correctness under failure**, with artifacts a hiring manager can read in an hour.

### 5.1 Required artifacts (specific)

| Artifact | Demo version | Professional version |
|---|---|---|
| **Schema + migrations** | Current models only | Linear migration history; constraints that encode invariants (`UNIQUE (case_id, pathway_id, window)`, CHECKs on state); a Ghost-like review note: idempotent, batched, not mixed DDL/DML; one story of a live migrate that did not destroy data |
| **State machine** | Enum column + `if` in a controller | Pure transition table (unit-tested: illegal transitions rejected); persistence tested with a real DB; “what must never be true” written down (ADR-length, not a blog) |
| **Idempotent jobs** | `MonitoringJob.perform_later(case_id)` | Deterministic **operation key** persisted with a **unique index**; retry resumes pending work (does not treat duplicate-key as success if the effect never ran). GitLab: `idempotent!` + shared example. Stripe-shaped webhook ingest: unique provider event ID at the door, separate key on the domain effect. Dedup locks are efficiency, not correctness. https://docs.gitlab.com/development/sidekiq/idempotent_jobs/ · https://eugenetheengineer.com/posts/billing-idempotency-webhooks-unique-indexes/ |
| **Poison / stuck jobs** | Default retry | Dead-letter or exhausted-retry path; metric/log for “job older than SLA”; a note on what a human does |
| **HTTP API + OpenAPI** | Hand-written swagger.yaml | Spec committed; at least one CI check that a real response matches (Chatwoot Skooma) or that the PR does not break the previous contract (Twenty). Versioning policy for fields caseworkers’ tools depend on |
| **Authz** | Logged-in user sees all cases | Tenant + role + object-level: caseworker A cannot read firm B; policy tests / PBAC rows; ASVS-shaped IDOR cases |
| **Observability you use** | Request logs | Job ID + case ID + pathway ID on every line; error tracker on worker; one alert: “monitoring lag > X” or “illegal transition attempted” |
| **Incident notes** | None | 2–5 dated notes: duplicate webhook, worker died after commit, partial migrate, bad IRCC payload. Format: what was true, what we thought, what we did, what we changed. GitLab review *shape*, 1-person length |
| **Runbook** | README “how to start” | “Eligibility wrong in UI”: which query, which job, which log field, how to re-enqueue **without** double-notify |
| **Case study** | “We used Postgres and Redis” | Framed as **correctness under failure**: “Worker died after writing `notified_at` but before ack; unique `(case_id, window, channel)` prevented the second email; here is the test.” Not “we used Kafka.” |
| **Users** | Seed data | At least one real firm / real pathway / real missed-window cost. Route 5: GitHub-only Tower collapses Chain A to Chain B |

### 5.2 Architecture restraint as evidence

**[Inference]** The professional design sentence is Shopify/Fowler-shaped: *one application; modules `pathways`, `eligibility`, `monitoring`, `reactivation`, `billing-if-any`; Postgres source of truth; job runner; structured logs; backups; migrations. The first cut boundary if a second consumer appears is X.*

**[Inference]** The demo/theater sentence is: event-sourced eligibility as identity, per-entity services, EKS, “event backbone.” Route 5 already forbids these as mastery objects. This memo treats them as **anti-evidence** for Combined Role.

### 5.3 What not to add to look “senior”

Do **not** add: Kubernetes-for-one, service mesh, Kafka-as-résumé, event-sourcing-as-identity, multi-region, 40-dashboard observability, load-test theater without users.  
**[Evidence]** Fowler premium + Shopify “no architecture in the early days” + Segment’s 140-service tax + 37signals majestic monolith.  
**[Inference]** A careful hiring manager will score the *refusal* as systems judgment.

---

## 6. Separation: portfolio-quality vs professional-quality

| | Portfolio-quality | Professional-quality |
|---|---|---|
| **Audience** | Recruiter skimming GitHub | Engineer who will own the next incident with you |
| **Center** | README, screenshots, tutorial CRUD, stack logos | Invariants, migrations, operability, users |
| **Proof of skill** | “I can build a CRUD app in X” | “I can change this next year without lying to a caseworker” |
| **Time** | Request/response | Jobs, schedules, replay, “what if it ran twice” |
| **Failure** | 500 + retry | Double-notify, lost eligibility window, split write/ack |
| **Data** | Rows | A model of a domain that outlives the framework |
| **API** | Postman collection | Contract that CI keeps honest |
| **Auth** | Login works | Authz: who must never see whose case |
| **Docs** | Getting started | ADR (why monolith, why this isolation level) + runbook + incident notes |
| **Users** | Optional | Load-bearing. Without users, Tower is a portfolio with extra folders |
| **CI** | Optional badge | The way merges happen; schema drift fails the build |
| **Career translation** | Agency “backend developer,” junior product | Mid product SWE / founding engineer: same object as Route 5 Chain A |

**[Inference]** Combined Role Architecture should treat portfolio artifacts as **eligibility to be screened** and professional artifacts as **eligibility to be trusted with a domain core**. Stacking more portfolio repos does not become professional. One operated core with the table in §5 does.

**[Hypothesis]** Founder-discount (recruiters coding Omcoda as “self-employed”) is best countered by *naming the artifacts* in the résumé the way this memo names them: “eligibility state machine, idempotent monitoring jobs, migration history, incident notes,” not “CEO / full-stack.”

---

## 7. Standards the Combined Role Architecture can adopt (normative, short)

A backend / product-engineer / founding-engineer workstream is **professional evidence** only if all of the following are true:

1. **One deployable** (modular monolith). Services only with a written reason. No K8s/event-sourcing identity.
2. **Schema is history**: migrations exist, are reviewed, and have been applied to a database that is not empty.
3. **Invariants are tests**: illegal state transitions fail in unit tests; job-twice fails in integration tests.
4. **Jobs are effects**: unique operation keys, retries, a worker process, a poison path.
5. **API is a contract**: OpenAPI (or equivalent) matches runtime, checked in CI.
6. **Authz is server-side and tested** (tenant + object).
7. **Operability**: logs you have used, one alert you would wake for, backups restored, a runbook, at least one incident note.
8. **Users**: at least one real consumer of the core. Screenshots without users remain portfolio.

Anything else is optional decoration.

---

## Source index

Architecture

- https://martinfowler.com/bliki/MonolithFirst.html
- https://www.martinfowler.com/bliki/MicroservicePremium.html
- https://martinfowler.com/articles/microservice-trade-offs.html
- https://shopify.engineering/deconstructing-monolith-designing-software-maximizes-developer-productivity
- https://shopify.engineering/shopify-monolith
- https://shopify.engineering/enforcing-modularity-rails-apps-packwerk
- https://github.com/shopify/packwerk
- https://signalvnoise.com/svn3/the-majestic-monolith/
- https://dev.37signals.com/vanilla-rails-is-plenty/
- https://dev.37signals.com/introducing-solid-queue/
- https://dev.37signals.com/solid-queue-v1-0/
- https://www.twilio.com/en-us/blog/developers/best-practices/goodbye-microservices
- https://handbook.gitlab.com/handbook/engineering/architecture/design-documents/modular_monolith/
- https://handbook.gitlab.com/handbook/engineering/architecture/workflow/

Repos inspected

- https://github.com/chatwoot/chatwoot
- https://github.com/chatwoot/chatwoot/blob/develop/.github/workflows/run_foss_spec.yml
- https://github.com/chatwoot/chatwoot/blob/master/config/sidekiq.yml
- https://github.com/chatwoot/chatwoot/pull/13623
- https://developers.chatwoot.com/self-hosted/deployment/architecture
- https://github.com/calcom/cal.com
- https://github.com/calcom/cal.com/blob/main/agents/rules/patterns-trigger-dev.md
- https://cal.com/blog/how-we-cut-our-ci-wall-time-from-30-minutes-to-5-minutes
- https://github.com/twentyhq/twenty
- https://github.com/TryGhost/Ghost
- https://github.com/TryGhost/Ghost/blob/main/.github/workflows/migration-review.yml
- https://github.com/TryGhost/Ghost/blob/main/AGENTS.md

Testing / jobs / security / observability

- https://abseil.io/resources/swe-book/html/ch11.html
- https://abseil.io/resources/swe-book/html/ch14.html
- https://testing.googleblog.com/2021/06/how-much-testing-is-enough.html
- https://martinfowler.com/articles/practical-test-pyramid.html
- https://docs.gitlab.com/development/sidekiq/idempotent_jobs/
- https://eugenetheengineer.com/posts/billing-idempotency-webhooks-unique-indexes/
- https://github.com/OWASP/ASVS
- https://asvs.dev/v5.0.0/V8-Authorization/
- https://charitydotwtf.substack.com/p/questionable-advice-how-do-i-get-my-team-into-observability
- https://www.honeycomb.io/blog/time-to-version-observability-signs-point-to-yes
- https://sre.google/workbook/alerting-on-slos/
- https://thegoodshell.com/sre-practices-for-startups/
- https://handbook.gitlab.com/handbook/engineering/infrastructure-platforms/incident-management/

Internal alignment

- `/workspace/research/evidence/route-5-backend-systems.md` (Chain A artifacts; over-engineering risk)
- `/workspace/research/role-architecture-deep-pass.md` §13.3 premature distribution
