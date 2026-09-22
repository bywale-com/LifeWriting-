# Combined Role Architecture — Research Synthesis

**Document type:** LifeWriting research. Not a career decision and not Character Architecture.  
**Date:** 2026-09-22.  
**Subject (given):** Wale Omotayo, Greater Toronto Area. TSO archetype. Plan A = Omcoda as production laboratory. Plan B = independent operator work before a CS degree. Plan C = later employment where that work must count as the same craft, with the degree expanding access.  
**Company (given):** [Omcoda](https://www.omcoda.com/) — managed solutions provider, not a custom shop. Tower = eligibility monitoring + client reactivation. Explicit refusal: *we do not take briefs, build to spec, and hand off.* Marble Spaces was not researched.

**This file's job.** Re-synthesize the five route evidence files around one combined capability — Software / Product Engineering with a Backend / Systems spine — and state what becoming that person actually requires. It does **not** pick a winner among employment titles. It does **challenge** the proposed architecture wherever the existing evidence is thin or contradictory.

**Evidence base.** [`role-architecture-deep-pass.md`](role-architecture-deep-pass.md) plus [`evidence/`](evidence/) routes 1–5. Fresh 2026 Canada / GTA / remote-Canada posting scan: [`evidence/plan-c-market-2026.md`](evidence/plan-c-market-2026.md). Public-repo artifact standards: [`evidence/artifact-quality.md`](evidence/artifact-quality.md). Where this document is more certain than those files, that is a writing failure — trust the file.

**Epistemic tags.** **Evidence** = sourced, checkable. **Inference** = reasonable reading of evidence plus subject context. **Hypothesis** = decision-relevant and not established. **Working choice** = the architecture under interrogation, not a finding.

---

## 0. The working choice, and the first challenge

**Working choice (given, not established).** Do not pick one of the five routes as a career. Become a person who owns consequential software systems: understand a domain, encode it, keep its invariants, ship a usable product, operate it. Weight:

| Layer | Route | Weight in the working choice |
|---|---|---|
| Technical spine | R5 Backend / Systems | Very high |
| Product expression | R2 Software / Product | Very high |
| Operate the software | R1 Cloud / Infra | Supporting |
| Operational truth | R3 Data / Automation | Supporting |
| Field / organizations | R4 Solutions / FDE | Supporting / field capability |

ABC as given: Plan A is the flywheel (problem → domain model → core → product → truth → operate → integrate → observe → improve). Plan B must resemble Plan C craft. Plan C is the same craft plus a credential that expands the employment surface — not a new identity after graduation.

**What the prior pass already said.** The deep pass refused a route winner and then described a third architecture: own the core (R5), give it a product surface (R2), keep operational truth (R3), keep it trustworthy (R1), put it in the field without selling uniqueness (R4 restricted to FDE-of-own-product). Plan C is a *translation of that laboratory* ([`role-architecture-deep-pass.md`](role-architecture-deep-pass.md) §12.4). The working choice is that third architecture, now named as the thing to become.

**Challenge 1 — this is still an inference.** The combination is read off Omcoda's refusals and the B→C chain tables. **Tower's codebase, tenant count, and whether a real state machine exists were not inspected** (deep-pass §14.1; R5 §10.8). Every “continuous chain” below is conditional on that artifact.

**Challenge 2 — the labour market does not hire this combination as one job.** **Evidence.** Faire's Product Engineer posting permits *backend or frontend or mobile* (https://boards.greenhouse.io/faire/jobs/8654106002). Docebo's “Senior Product Engineer I — Automation” is Go/PHP/K8s backend (https://jobs.ashbyhq.com/docebo/f98c67f0-3ee3-4f3e-aaec-9b10c15d9f9d). Wealthsimple Cards is a payments-rail specialist under “Software Developer” (https://jobs.ashbyhq.com/wealthsimple/062a74c6-65e3-4210-bfb3-e0f1af9fe732). Bloomberry: ~30% of “FDE” postings are relabeled SE (https://bloomberry.com/blog/i-analyzed-1000-forward-deployed-engineer-jobs-what-i-learned/). **Inference.** Employers buy *slices*. The combined role is a **capability architecture** that several Plan C titles can *partially* employ. It is not a vacancy title.

**Challenge 3 — Plan B cash fights the center.** R5: the deepest object is employee-shaped; SMB buyers purchase integrations and CRUD, not a multi-year core (R5 §2). R2: Toronto custom-app bands (CA$30–80k) are the default commercial expression and the model Omcoda refuses (R2; deep-pass §6). R4: the market pays for the next workflow. **Inference.** A combined architecture that is not policed weekly by a refusal log will become a custom shop with a systems vocabulary.

**Verdict used in the rest of this file.** The working choice is **supported as the Omcoda / TSO operating system** and **supported as the Plan B object that later translates to mid-IC product/backend seats** — *if* Tower is a live domain core with users. It is **not** supported as “you will be hired to do all five routes,” as “FDE is a safe Plan C,” or as “the degree plus two years of freelance REST equals this person.”

---

## 1. Define the Combined Role

### 1.1 Capability statement

**Inference.** This person is a **domain-core product engineer**: they can take an organizational fact that must stay true over time (eligibility, money, identity, inventory), model it, persist it under transactions, change it through jobs that must not double-fire, expose it through an API and a product surface people actually use, deploy and restore it, and sit with the user when it is wrong.

They are not five specialists. They are one operator whose Tuesday changes costume: schema in the morning, a caseworker's workflow at noon, a failed job at 2 a.m., a deploy on Friday. The costume is not the craft. The craft is **keeping a domain true in software that ships and runs**.

### 1.2 Technical object(s) they own

**Primary object (R5 + R2, Inference).** One bounded context that is both a **system** and a **product**:

- A domain model (entities, states, invariants, “what must never be true”).
- A persistence story (relational source of truth, migrations, constraints).
- A time story (jobs, schedules, retries, idempotency keys).
- A contract story (HTTP API that matches reality).
- A use story (workflows a professional user can complete without you in the room).
- An operation story (deploy, logs you have grepped, one alert you would wake for, a restore).

For this subject the named instance is Tower: pathway model, eligibility state, monitoring jobs, reactivation workflows, APIs, a surface consultants use. The *portable* object is not immigration. It is **a live domain core with a product face**.

**Secondary objects (supporting, Inference).**

| Object | Route | Own it only insofar as… |
|---|---|---|
| Production control plane of *this* product (IAM, backup, deploy, cost, residency) | R1 | The product stays saleable. Not a platform for other engineers. |
| Operational truth (grain, valid time, reconciliation, activation) | R3 | Eligibility is a modeled fact, not a Zap. |
| Field productization (discovery, install, refusal of uniqueness) | R4 | You are FDE of *your* product. Not the client's vendor tenant. |

### 1.3 What they are responsible for keeping true

**Inference.** Not “the site is up.” Specific truths:

1. **Domain invariants.** A case is not eligible and ineligible in the same window. A reactivation does not fire twice. A migration does not invent or destroy legal state.
2. **Contract.** The API and the UI agree with the store. A caseworker is not shown a lie.
3. **Time.** Monitoring ran; if it failed, a human can see that and replay without double-notify.
4. **Tenancy / authz.** Firm A cannot read firm B.
5. **Restore.** Yesterday's store can come back.
6. **Use.** A real user can complete the journey the product claims to sell.

**Evidence (why this list, not “uptime”).** Mastering Backend: the data model is the most consequential backend work (https://blog.masteringbackend.com/what-does-a-backend-engineer-do). Kleppmann: transactions exist so partial failure is not a business event (https://dataintensive.net/). R5 §4.1: failure that matters is double-charge / lost eligibility, not HTTP 500. Chatwoot / Twenty / Cal.com production repos treat jobs, migrations, and contract drift as first-class (artifact memo).

### 1.4 Problems they can independently solve

**Competent (Inference).** Given a messy professional-services process: name the states; write a schema with constraints; ship an API and a thin product surface; run a worker; diagnose a wrong state from logs; migrate live data once; onboard a firm without taking a unique brief.

**Not yet (Evidence from all route §5 “not reachable”).** Multi-region consensus; a platform other teams cannot break casually; Staff/Principal technical strategy; OSFI-shaped bank change control; card-network authorization; Palantir-scale customer decomposition as an employed FDSE.

### 1.5 Where Product Engineering ends and Backend / Systems begins

**Working distinction (Inference), not an org chart.**

| Question | Backend / Systems (spine) | Product Engineering (expression) |
|---|---|---|
| What is being protected? | Invariants, schema, jobs, API contract, failure modes | Whether a human can complete a valuable journey, and whether the product should exist |
| Typical artifact | Transition table, migration, idempotent job, OpenAPI, incident note | Workflow, instrumentation, scope cut, UX for a professional user |
| Failure that matters | Worker dies after commit; illegal state persisted | User cannot finish; wrong problem shipped; state hidden in screens |
| Shared object | The domain model. R2's deepest object *is* the domain model (R2 §4; 37signals `Recording`). R5's deepest object is the same model plus time and failure. |

**The leak.** R5 §7.4: building Tower UI-first leaves the state machine implicit in screens. **Inference.** Product Engineering that does not force the model into schema + jobs is generic full-stack. Backend that never ships a user journey is a service without a product — Plan C-readable, TSO-incomplete.

**Boundary rule (Hypothesis, load-bearing).** If a week produces screens and no change to invariants, jobs, or contract, the spine was not exercised. If a week produces schema and no user can complete a journey, the product was not exercised. Both weeks are allowed; a quarter of only one is a failure mode.

### 1.6 How much Cloud, Data, and Solutions is actually necessary

**Inference — minimum supporting depth, not career identities.**

| Capability | Necessary amount | Too little | Too much (identity theft) |
|---|---|---|---|
| **Cloud / Infra** | Git → prod → rollback; locked secrets; backups restored; structured logs; one business alert; Canada-region / residency awareness; IAM that isolates tenants | SSH-and-hope; secrets in git; never restored | EKS, service mesh, platform-for-internal-devs as the résumé (R1 §7; Fowler/Shopify) |
| **Data / Automation** | Operational store with grain and valid time; jobs as activation; reconciliation; tests on transformations; CRM as *destination* | Spreadsheet or Zap as system of record | Warehouse specialist disconnected from users; Airflow/Spark identity; “real-time eligibility graph” as a title (R3 §4.3 Hypothesis) |
| **Solutions / field** | Diagnose a firm's bottleneck; map it onto *your* product; refuse a unique brief; watch a user fail; write the playbook | Never sit with a user; ship into a vacuum | Implementation Consultant / HubSpot-partner identity; pre-sales SE (56% demos — Consensus 2026); self-label FDE |

**Evidence.** EnzRossi: outsource periphery, not the core domain model (https://enzrossi.com/blog/outsourcing-solutions-for-startups). CNCF platforms serve *internal developers* — the wrong user for Omcoda (R1). Fairview: a Zapier workflow is not a pipeline (https://getfairview.com/blog/build-data-pipeline-small-business). Consensus 2026: SE Tuesday is sales (https://goconsensus.com/research/2026-sales-engineering-compensation-workload-report).

### 1.7 What should deliberately NOT be part of the capability

Treat these as **refusals**, not as humble gaps:

1. **CMS / theme / Shopify-as-identity** — R2 Chain A; maps to NOC 21234, Very limited, AI/low-code drag (Job Bank 21234).
2. **Zapier / Make mill** — R3 Chain A; Automation Specialist, not SWE.
3. **Vendor-certified consultant identity** (Salesforce/HubSpot/Clio as the mountain).
4. **Canadian “Systems Engineer” Linux/VMware contracts** (TMX R-6232).
5. **Distributed-systems theater** at 1-person scale (Kafka-as-identity, per-entity microservices, event-sourcing-as-identity).
6. **Platform Engineer meaning Kubernetes platform for other teams.**
7. **Data Scientist / ML Engineer** as Plan C (NOC 21211 master's-shaped; Uniflow founding 5+ ML).
8. **Pre-sales Solutions Engineer** as the job (11-year presales base rate).
9. **Technical Product / PM** (already out of scope).
10. **Custom-shop “we take briefs”** — incentive-incompatible with Omcoda even when the code is real.

### 1.8 Distinctions

| Nearby identity | What they own | How this person differs |
|---|---|---|
| **Generic full-stack developer** | Screens + CRUD + a framework fashion | This person owns invariants and time (jobs), not just request/response. Evidence of the difference is migrations, transition tests, incident notes — not “I used Next and Postgres.” |
| **Backend specialist (employed)** | A service or platform slice; Time Warp: almost no external client | This person also ships the product face and sits with the organization. Employed backend *amputates* TSO client diagnosis (R5 §9.1). Plan C FTE backend is a *slice* of this architecture, not the whole. |
| **DevOps / Platform** | Control plane for *other* engineers | This person operates *their* product. R1 supporting dose: deploy, IAM, restore. Not golden paths. |
| **Data Engineer** | Pipelines, warehouses, SLAs on data landing | This person models *operational* state and activation. Warehouse is optional. Grain/time/reconciliation are required. |
| **Analytics Engineer** | Meaning in the warehouse (dbt) | Adjacent if Tower's monitoring data becomes a semantic layer. Not the center. |
| **Solutions Engineer / Implementation Consultant** | Demo or go-live of a vendor product | This person owns the software. Overlap is field diagnosis only. |
| **True FDE (Type 1)** | Production code in a *customer's* environment that feeds a vendor product | Closest *employed* cousin. Differs: this person owns the product, not Palantir/Salesforce. Bloomberry feeder is SWE 45%, founder 8%. |
| **Technical PM / Product Manager** | Roadmap, not the runtime | Out of scope. This person decides *and* ships. Ashby PE explicitly wears PM/design hats *as an engineer* (https://jobs.ashbyhq.com/Ashby/272bc3f4-5af6-4c14-b797-a424b62d306c). |

### 1.9 Capability model (one picture)

```
                    field diagnosis (R4, restricted)
                              │
                              ▼
     users ◄── product surface (R2) ◄── domain core (R5) ──► jobs / time
                              │                │
                              │                ▼
                              │         operational truth (R3)
                              │                │
                              ▼                ▼
                         operate this product (R1 dose)
```

**What they can be hired as (Inference, after strong Plan B + later degree):** Product Engineer (Faire-shaped IC); Software Developer / Software Engineer at a product company (mid, not Wealthsimple Senior 5+); Backend Engineer where the JD wants a domain core, not a K8s platform; Founding Engineer (demo screen); engineering-heavy FDE *if* the coding interview passes and the output test is Type 1.

**What they should not claim:** Staff, Principal, bank senior, Distributed Systems Engineer, Platform Engineer, Implementation Consultant-as-identity, Data Engineer-from-Zaps.

---

## 2. Deep requirements analysis

This is the load-bearing section. Depth is **not** “complete a CS degree checklist.” Depth is **what must be true of the person** for the capability model in §1 to be honest.

**How to read each block.** Central = the spine dies without it. Supporting = required at a stated ceiling. Later = after the 1-year object exists. School = CS program as *access and DSA tutor*, not as the source of production taste (working choice; consistent with R5 §3.3).

### 2.1 Computer Science foundations

| Topic | Depth required | Why | Central? | When | Practice | Competent | Excellent | Evidence of it | Best gym |
|---|---|---|---|---|---|---|---|---|---|
| **Data structures & algorithms** | Working fluency in arrays/maps/trees/graphs/heaps; complexity as a habit; *interview* fluency as a **separate** block | Production: you pick the right store and notice O(n²) in a job. Plan C: Google-class and many SWE loops are DSA-first (R5 §3.2; https://www.youtube.com/watch?v=Ti5vfu9arXQ) | Central for Plan C screening. Supporting for Plan A (you can ship Tower without LeetCode) | Production habits now; interview block in the degree years | Tower jobs + later dedicated DSA | Can explain why a queue + unique index beats an in-memory list | Can pass a Docs/whiteboard medium and *also* refuse the wrong structure in prod | Interview pass; a job you rewrote after measuring | School + self; **not** Omcoda |
| **Relational model & transactions** | Isolation phenomena you have been bitten by; constraints as invariants; what a transaction is *for* | This *is* the spine (Kleppmann; R5 §4, §8) | **Central** | Immediately | Tower eligibility writes + job ack | “I wrap the state change in a DB transaction” | Named isolation choice; a story of a lost update you fixed | Schema constraints + incident note | **Plan A** |
| **Concurrency** | Races, idempotency, “died after commit,” at-least-once | Jobs *are* concurrency (R5 §8; GitLab idempotent workers) | **Central** | With the first job | Duplicate webhook tests | Job is safe to run twice | Unique operation key + resume-not-bail (artifact memo §5) | Integration test + unique index | **Plan A** |
| **Networking** | HTTP semantics, TLS, DNS, timeouts, idempotent methods | APIs and “it works on my machine” | Central-supporting | Year 1 | Public API + one integration | Correct status codes, timeouts, retries | Versioning without breaking a client; you have seen a retry storm | OpenAPI + an incident | Plan A |
| **OS / processes** | Process vs thread, files, signals, memory enough to debug a worker and a web process | Twenty's split (API + worker) is the production shape | Supporting | When you run two processes | Compose: web + worker + Postgres | You can tell which process died | You can reason about crash, restart, poison | Runbook: which process, which log | Plan A |
| **Distributed systems (Kleppmann sense)** | Reliability, consistency choices, derived data. **Not** Paxos, multi-region, consensus | 1-person Tower is a backend-systems problem (R5 §0 Hypothesis) | Supporting as *vocabulary*; not as a job | After year-1 core | Read DDIA against *your* failures | You can say why you did **not** distribute | You add a log when a second consumer is real | ADR: “modular monolith because X” | Plan A + reading |
| **Theory / compilers / graphics / numerical** | Not required | Does not keep eligibility true | Out | Never for this architecture | — | — | — | — | School elective only |

**Inference.** The CS degree's unique job in this architecture is **eligibility + DSA + (for some programs) OS/networks taught as a system**. It does not teach taste for invariants. Treating “I finished CS” as this table is the degree-as-magic failure (deep-pass §13.6).

### 2.2 Programming

| Topic | Depth | Why | Central? | When | Practice | Competent | Excellent | Evidence | Best gym |
|---|---|---|---|---|---|---|---|---|---|
| **One primary language, deeply** | Idioms, debugging, packaging, types-or-discipline, test runners | Banks want Java/Spring (Smile, Nue, TD — R5). Product PE often TS/React+Node (Ashby, Linear) or Java/Kotlin (Faire) or Rails (Wealthsimple). | **Central** (one language). Second language is supporting | Now | All of Tower in one stack | Ship and operate in it | Can read a foreign stack in a pairing interview (Ashby pairs in *their* repo) | Repo + production | Plan A |
| **Second language (reading)** | Enough to pass a pairing / bank screen later | Stack provincialism is a TSO failure (R5 §9.5). **Hypothesis:** primitives transfer; ATS may not | Supporting | After year-1; Java if banks stay in Plan C | Katas + a small service, not a Tower rewrite | Can modify a Spring/Rails controller without theater | Can explain isolation in that stack | A PR in the target stack | Plan C prep / school |
| **Debugging** | Prod-first: logs, bisect, bisect the *state* | Time Warp: debug is a real share; incident weeks 40–70% (R5 §1.1) | **Central** | Now | Every incident | Find a wrong eligibility from logs | Write the test that would have caught it | Incident notes | Plan A |
| **Testing** | Unit of the state machine; integration of job+DB; contract gated | Google SWE book ~80/15/5; Chatwoot/Twenty/Cal CI (artifact memo §3) | **Central** | With first invariant | CI on every merge | Tests exist and run in CI | Illegal transition + “job ran twice” fail the build | CI logs | Plan A |
| **Refactoring / modularity** | Named modules by domain, exclusive data ownership | Shopify modular monolith; not Packwerk-for-one | Central | After the core exists | Extract `eligibility` / `monitoring` | You can point at a boundary | You can say which boundary you would cut first | ADR + directory | Plan A |
| **Version control & review** | History as evidence; PR discipline even solo | Employers probe “worked on a team” (Wealthsimple: “senior contributor on a team”) | Supporting | Now | Solo PRs + ADRs; later staff-aug or OSS | Clean history, reversible commits | Review notes that teach | Git log + one external review | Plan A; **gap:** team review needs Plan C or OSS |
| **Performance** | Measure the CUJ you sell (eligibility p95, job lag) | Load-without-users is theater | Supporting | After users | One measured query/job | You have an EXPLAIN | You have a budget | A before/after | Plan A |
| **Tooling / AI-assisted coding** | Stated at Faire, Wealthsimple, Docebo, Dimely, Publicus (2026 scan) | Market token, not mastery | Supporting | Now | Use it; do not ship slop | Agents write drafts you can defend | You reject unsafe diffs | Publicus: “No AI slop” demo | Plan A/B |

**Hypothesis (R5 §8).** A person with these primitives and a live Tower learns Java/Spring for a bank loop faster than a Java graduate learns care. Do not assume ATS agrees.

### 2.3 Backend / Systems (spine)

This is the technical specialization. Depth here is what distinguishes the role from generic full-stack.

| Topic | Depth | Why | Central? | When | Competent | Excellent | Evidence | Gym |
|---|---|---|---|---|---|---|---|---|
| **Domain modeling** | Entities vs events; slowly changing pathways; “done” | R2+R5 shared object | **Central** | Week 1 | ERD that matches reality | Invariants written; illegal states unrepresentable | Schema + ADR | A |
| **HTTP APIs** | Methods, pagination, authn headers, versioning | Face of the model | **Central** | Year 1 | CRUD that is honest | Idempotent PUT; versioning; contract tests | OpenAPI + CI drift check | A |
| **Authn / authz** | Tenant + role + object; deny-by-default | ASVS V8; professional-services data | **Central** | Before a second firm | Login works; tenants isolated | IDOR tests; policy objects (Chatwoot `app/policies`) | Policy specs | A |
| **Databases** | Postgres (or equivalent) as source of truth; indexes you chose; constraints | R5 consistency choice | **Central** | Year 1 | Migrations apply | Drift CI; live migrate story | Migration history | A |
| **Transactions** | Atomicity of state+ack | Kleppmann | **Central** | With first job | Wrapped writes | Isolation story | Incident + test | A |
| **Jobs / queues** | At-least-once, keys, poison, backoff; queue ≠ log | Product's clock (R5 §7.1) | **Central** | Year 1 | Worker process exists | GitLab-shaped idempotent worker | Job specs + unique index | A |
| **Caching** | Know when *not* to | Stale eligibility is a lie | Supporting | After a measured pain | No cache, correctly | Cache with explicit invalidation | ADR | A |
| **Migrations** | Ritual, not a file | Ghost migration-review checklist | **Central** | First schema change in prod | `up` works | Idempotent `up`/`down`; no mixed DDL/DML | Review note + prod apply | A |
| **Observability** | Logs/metrics you used | Charity Majors: done when you know it's working in prod | **Central** | First user | Structured logs + worker errors | One business alert; job IDs on every line | Grep story | A |
| **Failure modes** | Retry storms, partial deploy, “exactly once” as a lie | R5 §8 | **Central** | First incident | You have one story | Catalogue from production | Incident notes | A |
| **Security** | ASVS L1: TLS, hashed secrets, server-side authz, validation | Immigration-adjacent data | **Central-supporting** | Before paying firms | No secrets in git | IDOR + tenancy tests | Checklist + tests | A |
| **Distributed systems at scale** | Replication, consensus, multi-region | Not the 1-person problem (R5 §0) | Out / later decade | After a real second consumer | — | — | — | C at infra-product cos |

### 2.4 Product Engineering (expression)

| Topic | Depth | Why | Central? | When | Competent | Excellent | Evidence | Gym |
|---|---|---|---|---|---|---|---|---|
| **User workflows** | Professional-user density, not consumer delight | Omcoda buyers are caseworkers, not shoppers | **Central** | With first user | A journey completes | You watched a user fail and changed the model | Session note + commit | A + field |
| **Frontend (necessary amount)** | Enough to ship and instrument the journeys you sell | Faire/Ashby/WS expect contribution across the stack; Linear hard systems are *not* Next.js (R2) | Supporting-central | Year 1 | Accessible, boring, correct | State not hidden in the client | UI talks to the API contract | A |
| **Product architecture** | Modules by user-visible capability that map to domain modules | Avoids UI-first leak | **Central** | Year 1 | Screens map to states | Cutting a screen does not orphan state | Directory + ADR | A |
| **Shipping / iteration** | Small releases, migrate+restart web+worker | Feature not done at merge (R2) | **Central** | Now | Weekly ship | Rollback note exists | Deploy log | A |
| **Instrumentation** | Did the CUJ happen? | Product feedback loop (R2 §8) | Supporting | After users | One event per CUJ | You killed a feature from data | Dashboard you used | A |
| **Quality / maintainability** | Change next year without lying | Artifact memo §6 | **Central** | Always | Tests + migrations | Constraint system others could extend | Time-to-change story | A |
| **Scope / “what is worth solving”** | Faire/Ashby stated responsibility | Distinguishes PE from ticket FS | **Central** | Plan B | You refused a brief | You wrote the spec *and* the code | Refusal log + spec | A/B |

**Frontend ceiling (Inference).** Learn the current product surface (likely React/TS if Plan C includes Ashby/Faire/Harvey). Do not become a CSS/framework specialist. Do not treat mobile as required (Faire lists it as optional).

### 2.5 Infrastructure / Operations (supporting)

| Topic | Depth | Why | Central? | When | Competent | Excellent | Evidence | Gym |
|---|---|---|---|---|---|---|---|---|
| **Linux** | Process, files, logs, ssh, permissions | Worker + web are Linux | Supporting | Year 1 | You can debug on the box | You wrote the runbook from the box | Runbook | A |
| **Containers** | Compose: web, worker, db, cache | Chatwoot/Twenty/Cal shape | Supporting | Year 1 | `compose up` is prod-like | Migrate is in the release | compose file | A |
| **CI/CD** | Test + migrate + deploy on merge | Professional vs portfolio (artifact §2.5) | Supporting-central | Year 1 | CI is the merge gate | Path-filtered; schema drift fails | Workflow YAML | A |
| **Cloud** | One provider, boring: compute, object storage, managed Postgres, secrets | Trust input (R1) | Supporting | When leaving localhost | Env exists | IAM least privilege; region chosen | Terraform or equivalent *for this app* | A |
| **IaC** | Enough to recreate the estate | R1 primitive | Supporting | Year 1–2 | Remote state locked | Recreate from zero | Repo + apply log | A |
| **Monitoring / incident** | Is it up / slow / erroring / is the job late | Startup SRE, not SLO burn-rate matrices | Supporting | First user | Uptime + job lag | Blameless 1-page review | Incident notes | A |
| **Security / tenancy / residency** | PIPEDA-aware hosting; backups | Professional-services data (R1 §7) | Supporting | Before paid tenants | Encrypted at rest; backups | Restore test dated | Restore note | A |
| **Scaling / cost** | Know the bill; vertical first | 1-person premium is cash (R5 §7.1) | Supporting | After users | You can explain the bill | You refused K8s on cost | Cost note | A |
| **K8s / service mesh / multi-region** | Not required | Theater at this scale | Out | Only if Plan C is platform | — | — | — | C only |

### 2.6 Data / Automation (supporting)

| Topic | Depth | Why | Central? | When | Competent | Excellent | Evidence | Gym |
|---|---|---|---|---|---|---|---|---|
| **SQL** | Joins, windows, EXPLAIN, transactions | Spine language | **Central** (shared with §2.3) | Now | Honest queries | Grain you would defend | Query + EXPLAIN | A |
| **Schemas / grain / time** | Event time vs valid time; SCD if needed | Eligibility is temporal (R3) | **Central-supporting** | Year 1 | Current state is correct | You can answer “were they eligible on date D?” | Table design | A |
| **Pipelines** | Ingest IRCC/status → store; not a warehouse | Tower product | Supporting | When a source exists | Idempotent ingest | Schema-drift test | Job + test | A |
| **ETL/ELT / warehouse** | Optional | Only if monitoring data is treated as a platform (R5 §6.1) | Out until a second consumer | Later | — | dbt tests on *derived* meaning | — | A later or C |
| **Events** | Outbox if a second consumer appears | Premature event backbone is a failure (R5 §7.3) | Supporting, delayed | After second consumer | — | — | ADR | A |
| **Workflow automation** | Durable jobs, not Zapier as store | R3 Chain A is the trap | Supporting as *engine*; Out as *identity* | Now as jobs | n8n may *call* the API | State lives in Postgres | Architecture picture | A |
| **Analytics / instrumentation** | CUJ events | Product loop | Supporting | After users | One trusted number | Semantic meaning named | Event spec | A |
| **Data quality** | Reconciliation: store vs source vs UI | Silent failure is the DE horror (R3) | Supporting-central | Year 1 | A recon job | You caught a lie before a client | Recon incident | A |

### 2.7 Field / organizational capability

| Topic | Depth | Why | Central? | When | Competent | Excellent | Evidence | Gym |
|---|---|---|---|---|---|---|---|---|
| **Problem diagnosis** | Why is *this firm* losing files / missing windows | TSO first verb; employed backend amputates it (R5 §9.1) | **Central for TSO / Plan A** | With first firm | You can name the bottleneck | You refused to automate the wrong step | Discovery note | **A/B field** |
| **Technical discovery** | Map process → states → what software should own | Prevents Zapier-as-OS | **Central** | Always | A process diagram that became a schema | The schema surprised the client usefully | Before/after | A |
| **Stakeholder communication** | Professional-services language, not Kafka | Buyers buy outcomes (R5 §2.3) | Central for Plan B cash | Now | Outcome sentence | Case study without logos-as-craft | Written case | B |
| **System mapping** | Their Clio/mailbox/IRCC vs your core | Integration is periphery | Supporting | First integration | A box diagram | Clear ownership of each fact | Diagram | A/B |
| **Integration work** | Webhooks, OAuth, retries | Sells; also Chain B trap if it *is* the product | Supporting | When a real consumer exists | A working connector | Idempotent, monitored | Code + incident | A/B |
| **Documentation** | Runbook, ADR, API, playbook | Handoff without taking a brief | Supporting | Year 1 | README that is true | Incident + runbook + ADR | `docs/` | A |
| **Deployment into orgs** | Onboarding a firm onto *Tower* | R4 restricted | Supporting | First customer | A playbook | Refusal of uniqueness is in the playbook | Playbook + refusal log | A/B |
| **User observation** | Watch, do not interview only | Ashby/Faire PE stated | Supporting-central | First user | One observed failure | Product change from observation | Note + commit | A |
| **Operating inside orgs** | Stand-ups, review, someone else's codebase | Wealthsimple “on a team”; R5 Chain C signal | Supporting for Plan C | Plan C or OSS/staff-aug | You can take review | You gave review | External PR | **C / OSS** (A cannot teach this) |

### 2.8 Dependencies (ordered mastery, not a calendar)

```
SQL + one language + git
        │
        ▼
domain model ──► schema + constraints ──► HTTP API + authz
        │                                      │
        ▼                                      ▼
transactions + jobs/idempotency          thin product surface
        │                                      │
        ▼                                      ▼
observability + CI + deploy/restore ◄── instrumentation
        │
        ▼
first real user / firm ──► incidents ──► migrations in anger
        │
        ├─► field diagnosis + refusal log          (Plan B cash that stays on-object)
        ├─► integrations as periphery              (do not become the product)
        ├─► DSA / system-design theater            (parallel; school + dedicated block)
        └─► second language / team review          (Plan C prep; not year-1)
```

**Do not start with:** Kubernetes, warehouse, vendor certs, microservices, LeetCode-only, CMS, a second language rewrite of Tower.

**Inference.** Until “first real user + one incident + one live migration” exists, additional supporting capabilities are decoration. That is the 1-year gate from R5 §4.2 and deep-pass §4.

### 2.9 What each environment uniquely trains

| Environment | Trains well | Cannot train |
|---|---|---|
| **Plan A (Omcoda/Tower)** | Invariants, jobs, product surface, ops of *this* system, field diagnosis, refusal, longitudinal ownership | Team review culture; someone else's mature codebase; OSFI; DSA; Staff influence; Java/Spring as default |
| **Plan B (independent, on-object)** | Closing, scoping, outcome language, integrations, cash | Same as A if A *is* B. Off-object B trains the wrong occupation |
| **Plan C (product-company IC)** | Review, shared code, leveling, design interviews as sport, collaboration evidence | TSO client diagnosis (amputated); founder ownership; Omcoda refusals |
| **School (CS)** | Eligibility at banks/gov; DSA reps; some OS/networks; peer cohort | Production taste; users; incidents; Omcoda economics |

---

## 3. Plan A requirements — Omcoda as professional evidence

**Question.** What must Omcoda *be* so that years in it are mid-IC evidence rather than a founder story?

### 3.1 Systems that must exist

**Inference** (R5 Chain A + artifact memo §5 + deep-pass 1-year tests):

1. **Eligibility / pathway core** — schema, constraints, tested transition table.
2. **HTTP API** — contract committed; at least one drift check.
3. **Job runner** — monitoring + reactivation as processes; unique operation keys; poison path.
4. **Product surface** — the journeys you sell, talking to the API, not holding state.
5. **Authz / tenancy** — firm isolation tested.
6. **Ingest** — status/source → store, idempotent (R3).
7. **Operate** — compose or PaaS; web + worker + Postgres; backups restored; structured logs; one business alert.
8. **Docs that are evidence** — ADRs, runbook, incident notes, refusal log, OpenAPI.

**Do not require:** warehouse, Kafka, K8s, per-entity services, mobile, a second product.

### 3.2 Technical complexity required

**Evidence.** Fowler Monolith First; Shopify “no architecture in the early days”; 37signals majestic monolith; Segment's 140-service tax. **Inference.** Required complexity is **correctness under failure in a real domain**, not distribution. A modular monolith with jobs is enough complexity to be mid-IC. Artificial complexity is anti-evidence to a careful hiring manager (R5 §7.3).

### 3.3 Production conditions required

| Condition | Why it is load-bearing |
|---|---|
| **Not localhost-only** | GitHub-only Tower collapses Chain A to Chain B (R5 §7.4) |
| **Migrations applied to non-empty data** | Ghost/Twenty treat this as the professional ritual |
| **Worker crashes in anger at least once** | R5 3-year object is operational stories |
| **Backup restore performed** | R1 trust input |
| **Secrets, TLS, tenant isolation** | Professional-services data |

### 3.4 Users / customers required

**Inference.** At least **one** real firm using Tower for a real pathway, with a real missed-window cost. Ten vanity tenants with no jobs running are still a demo. Conversion, ACV, and whether GTA immigration/legal will *buy operated software vs Clio+Zapier* are **unmeasured** (deep-pass §14.2). **Hypothesis.** One demanding firm teaches more than ten polite pilots.

### 3.5 Operational responsibility required

You are on-call for the code you wrote (Majors). Informal SLO: “monitoring finished by X” (R5 §8). A dated incident note. This is not GitLab EOC theater.

### 3.6 Artifacts generated (the résumé translation)

Name them as engineering, not as CEO (founder-discount Hypothesis, deep-pass §13.4):

- Eligibility state machine (tested).
- Idempotent monitoring / reactivation jobs.
- Migration history + one live migrate.
- OpenAPI matching runtime.
- Tenant authz tests.
- Incident notes (correctness-under-failure).
- Runbook.
- Refusal log (briefs declined).

### 3.7 Failures that create meaningful experience

Duplicate webhook; worker died after commit; partial migration; bad source payload; illegal transition attempted; job older than SLA; tenant leak caught in test (ideally) or in prod (expensive). **Inference.** If two years produce no such story, Plan A was a portfolio.

### 3.8 What Omcoda can teach well / cannot

**Teaches well (Inference, deep-pass §10):** domain core, product surface, operational truth, boring production, field diagnosis, TSO loop, restraint on distribution.

**Cannot teach:** team review; mature foreign codebase; bank/OSFI envelope; Staff influence; DSA; Java-as-default; Palantir-class customer decomposition at volume; “OS of the firm” as something *employers* hire (deep-pass §14.10).

---

## 4. Plan B requirements — independent operator

**Rule (given, restated as Inference from all five Chain tables).** Plan B compounds toward Plan C only when the next employer is buying the **same object**. Cash that trains a different occupation is allowed only as a short runway, and it must be labeled as such.

### 4.1 Sellable offers consistent with the central craft

**In order of realism (R5 §2.3 Hypothesis + deep-pass §6):**

1. **Operate Tower** for professional-services firms — outcome sale, R5 craft, R4-shaped conversation. Mastery path.
2. **A module that stays Omcoda's**, installed in a firm (FDE-of-own-product). Still (1).
3. **Scoped integration that talks to Tower's API** (periphery, cash, keep short).
4. **Staff-aug backend** later, if a network exists — B→C hinge, CRA risk if single-client employee-shaped (R5 §2.4).

**Not on this list:** “I will design your core APIs” as a pre-degree GTA product (buyers of that are Perimattic-shaped shops). Custom apps to spec. HubSpot/Clio implementations. Zapier retainers. CMS. Landing-zone/EKS for immigration firms.

### 4.2 Client / company profiles

| Fit | Who | Why |
|---|---|---|
| **Good** | Immigration / legal / financial firms that will *use* an operated eligibility/reactivation system | Same domain as Tower; field loop |
| **Acceptable cash, weak continuity** | SMBs wanting Stripe/CRM glue | R5 Chain B |
| **Wrong buyer for the spine** | Product companies wanting a contractor to own their core | They hire FTE (EnzRossi); you become staff-aug |
| **Wrong buyer for Omcoda** | Anyone sending a unique app brief | Custom-shop gravity |

### 4.3 Project types, depth, ownership, duration

| | Minimum to count as Plan B *of this architecture* |
|---|---|
| **Technical depth** | Schema + jobs + API + authz + deploy; not screens-on-CRM |
| **Ownership** | You chose the invariants and live with them after invoice |
| **Duration** | Longitudinal: months on the same core, not six unrelated MVPs |
| **Production** | You are the pager |
| **Evidence** | Artifacts in §3.6, dated |

**Hypothesis.** Two years of one core beats two years of twelve CRUD apps for every serious Plan C family in the 2026 scan except Implementation Consultant.

### 4.4 How to document

Rewrite as you go, not at application time: ADRs, incidents, OpenAPI, case studies framed as correctness-under-failure, refusal log. Résumé line is engineering responsibility, not “Founder/CEO, Omcoda” (deep-pass §15.3).

### 4.5 Work to reject (custom-shop / weak continuity)

- Unique application per brief (R2 betrayal).
- CMS / Shopify / WordPress as the product.
- Zapier/Make as system of record (R3 Chain A).
- Vendor implementation as the business (R4 default Plan C = Implementation Consultant).
- Linux “Systems Engineer” contracts (TMX trap).
- Microservices/Kafka showcases for buyers who needed a form.
- Single-client staff-aug that is a disguised FTE (CRA + no second customer).

### 4.6 Concrete examples

**Good Plan B (Inference).**

1. A Toronto immigration firm pays a monthly fee for Tower to watch IRCC-shaped status and reopen dead files. You model pathways, write jobs, sit with a caseworker when a window is missed, change the schema, write the incident. **Object:** R5+R2+R3+R1 dose+R4-of-own-product.
2. Same product, second firm, *no unique features* — a playbook change and a tenant. **Object:** product, not a shop.
3. A scoped connector: Tower emits a webhook the firm's Clio can consume. Connector is periphery; core stays yours.

**Bad / deceptively useful Plan B (Evidence-backed).**

1. **CA$40k custom portal** for one consultancy, handed off. Looks like full-stack. Plan C reads as agency work (R2 Chain A). Omcoda refusal broken.
2. **HubSpot + Make** “automation practice,” five retainers. Cash is real. Plan C title is Automation Specialist / Implementation Consultant (R3 §5.1, R4 §5).
3. **Freelance REST**: auth + Stripe + admin CRUD, six repos. R5 Chain B. Interviewers hear “I wrapped tables in Express.”
4. **“Founding Engineer” for a friend's idea** with no users. Demo interview at Publicus fails (“No AI slop” / no thing).
5. **TMX-style Linux contract** because the word “systems” matched. Craft becomes Route 1/IT.
6. **Salesforce “FDE” self-study + certs** without production code. Type 2 SE path; Consensus-shaped years.

---

## 5. Plan C — exact employment destinations

Fresh posting-level detail lives in [`evidence/plan-c-market-2026.md`](evidence/plan-c-market-2026.md). Compressed here. Labour weather: Ontario/Toronto NOC 21232 **Limited / Very limited + surplus**; COPS 2024–2033 **BALANCE** (76,300 openings vs 98,900 seekers); Indeed Canada Aug 2025: software-engineer postings **−51%** vs early 2020; junior/standard titles **−25%**, senior **+5%**. Plan C is a picky market.

### 5.1 Product Engineer

**Actual job (Evidence).** Faire Brand PE: plan and build features end-to-end with product/design/data; 2+ years; BA **or equivalent**; CA$129.5–178k; Java/Kotlin/JS; Toronto/KW hybrid (https://boards.greenhouse.io/faire/jobs/8654106002). Ashby Senior PE remote-Canada: own projects including specs/wireframes; filter architecture that compiles to SQL; **no LeetCode**, pair in their repo; CA$195–248k; anti-junior team (https://jobs.ashbyhq.com/Ashby/272bc3f4-5af6-4c14-b797-a424b62d306c). Docebo Toronto uses the title for both PHP product work and Go/K8s automation. Linear (US/EU only): 5+ at a “high-quality software company.”

**Canadian title reality.** Real at Faire/Docebo/Ashby. **Not** bank language. Wealthsimple does the job as **Software Developer — Product Engineering** (https://jobs.ashbyhq.com/wealthsimple/9f45d7bf-788e-456c-97d3-8fba8b88387d). Searching only “Product Engineer” under-counts.

**Degree.** Equivalent clause is real at Faire/Docebo. Absent at Ashby/Linear. Banks: N/A (they do not use the title).

**Plan B translation.** Continuous **if** Tower is end-to-end product + core (Faire “what is worth solving”; Ashby constraint-solver analog). **2 years clears Faire-shaped IC, not Docebo Senior 4+ / Ashby Senior / Linear 5+.** Gaps: team tenure, stack match (PHP/Go/Java), logo.

**Preserves combined architecture?** Faire/Ashby/Linear: yes, with a frontend-only *option* at Faire — filter JDs that never mention schema/jobs. Docebo Automation: no (backend/K8s specialization).

### 5.2 Software Engineer / Software Developer

**Actual job.** The Canadian default title for the same work. Wealthsimple Senior PE-org Developer: 5+ shipping production; “senior contributor **on a team**”; Rails + React; CA$151.2–189k; degree absent. Harvey Staff FS Toronto: 5+ **post-BS/MS**; CA$196.8–295k; no visa. RBC/BMO visible 2026 posts in the scan were **campus / enrollment-gated**, not experienced FTE.

**Degree.** Job Bank 21232: bachelor's or college CS **usually required**; 77% of Ontario incumbents are university-level. Harvey counts years post-degree. Campus doors closed without enrollment.

**Plan B translation.** Mid Developer at a product company is the honest level. Senior WS/Harvey is under the posted years. Bank FTE: conceptually similar (regulated-adjacent story) not continuous (Java/.NET, years, envelope). **Gap:** collaboration evidence; Harvey's years formula under-counts a no-degree founder.

**Ontario title law.** PEO restricts “Software Engineer.” Prefer Developer / Product Engineer / Backend Developer on self-description. Enforcement uneven; banks still post Engineer.

### 5.3 Backend Engineer / Backend Developer

**Actual job.** In the 2026 GTA product sample, this label was **senior/platform**: Harvey Senior Backend CA$164–225k, 4+ post-BS/MS, auth/flags/notifications platform; Docebo Automation (PE title, backend work); Wealthsimple Cards (domain years). No junior Backend Engineer title fetched. Intermediate backend is usually posted as Software Developer.

**Plan B translation.** Continuous if Tower's *backend is the product*. Discounted if résumé says microservices for one deployable. **Does not preserve full combined architecture** when the JD's first bullets are K8s/SLOs/DynamoDB.

### 5.4 Full-Stack Engineer

**Filter.** Only JDs that own API/schema/jobs *and* a surface. Wealthsimple PE-org, Faire, Harvey Staff FS, Ashby, Dimely founding (aggregator: C$100–120k, TypeScript, retries/idempotency, customer-facing — closest posted analog to Tower).

**Risk.** Enterprise “full stack” can mean API + UI in a PM-heavy estate at low cash (Element Fleet index; posting unavailable on refetch). Junior full-stack is the 21234/agency cage.

### 5.5 Founding Engineer

**Actual job.** Seed / first-10. Publicus Toronto: “Founding Builder,” 2–6 years, CA$100–150k + **0.5–2%**, demo interview, **not customer-facing** (https://hire.publicus.ai/). Dimely: fourth hire, customer + architecture + production. Uniflow: 5+ ML — wrong family. Degree **absent** on every founding JD that loaded.

**Plan B translation.** **Most literally in-distribution** if the demo is a live domain system. Cash near Job Bank high, below Faire/WS Senior — the bet is equity. **Gaps:** they want a #2 in the *room*, not another solo founder; Publicus amputates field; taking the job is leaving Omcoda.

**Preserves combined architecture?** Dimely-shaped: yes. Publicus: builder, not TSO-complete. Uniflow: no.

### 5.6 Forward-Deployed Engineer

**Split first (Evidence).** Bloomberry n≈1,000 (updated 2026-01-25): 60% Type 1 Builder / 30% SE+ / 10% internal; feeders SWE 45%, SE 22%, **founder 8%**; mode 3–5 years (https://bloomberry.com/blog/i-analyzed-1000-forward-deployed-engineer-jobs-what-i-learned/). Tandem: use the output test; FDE titles grew 800%+ with relabeling (https://usetandem.ai/blog/fde-vs-implementation-engineer-vs-solutions-engineer).

**Live Canada sample (thin).** Salesforce Toronto FDE: indexed Ontario base CA$95–145k (SE-band smell); body empty on fetch. Ethicrithm remote-Canada: Palantir-partner delivery. Palantir Toronto: closed. Palantir NY FDSE live: 1+ post-college, preferred STEM, USD $135–200k (https://jobs.lever.co/palantir/dab396d4-2f14-4796-aac0-0d82883dccf0).

**Plan B translation.** Continuous as **founder-FDE of Tower**. Conceptually similar to partner-FDE only with platform tenure you probably do not have. Palantir-by-default: no. Coding interview is the gate. **GTA true-FDE volume is not established** (deep-pass §14.6; scan §11).

**Preserves combined architecture?** Type 1 at a small product company: closest employed TSO cousin, still amputates *owning* the product. Type 2: destroys it.

### 5.7 Adjacent roles the evidence revealed

| Title | Keep as destination? | Why |
|---|---|---|
| Implementation Consultant | No (as identity) | Default Plan C of off-object Plan B |
| Cloud / Platform / SRE | Supporting competency; destination only if the JD is “operate our product,” not “pave roads” | R1 object is the account |
| Analytics / Data Engineer | Destination only if Tower internals are a real store + tests + recon | R3 Chains B/C |
| Web Developer (21234) | Cage | Official weather worse; AI/low-code drag |
| Staff / Principal / bank senior | Not after 2 years | Floor across all routes |

### 5.8 What Plan C develops that A/B cannot

**Evidence + Inference.** Review culture; working in a mature codebase; collaboration that Wealthsimple can score; design-interview sport; a manager reference; sometimes a regulated envelope (if not a bank, still “on a team”). **It will also untrain** client diagnosis and Omcoda refusals if the company has separate CS/SRE (R2 §9.1, R5 §9.1). That is a feature of employment, not a reason to avoid Plan C.

### 5.9 Realistic entry after strong Plan B + CS degree

**Inference, not a promise.**

| If Tower is real | Honest entry |
|---|---|
| Product company, equivalent-friendly | Intermediate Product Engineer / Software Developer (Faire-shaped). Not Ashby Senior, not WS Senior 5+ |
| Founding seat | In-distribution on demo (Publicus 2–6) |
| Bank / federal | Door *opens* (eligibility); screening is still DSA + stack; level junior-to-intermediate |
| Type 1 FDE | Possible at a small product co if the loop is coding-heavy; not Palantir-default |
| If Tower is thin | Junior Developer / Implementation / Automation — different occupation |

---

## 6. B → C translation

Rule: no match percentages. Continuous = same object. Conceptually similar = same words.

| Plan B activity | Capability demonstrated | Artifact | Employer interpretation | Qualifying Plan C |
|---|---|---|---|---|
| Operate Tower for a paying firm: states, jobs, API, surface, incidents | Domain-core product engineering | State machine tests, migrations, incident notes, OpenAPI, users | “Shipped and operated a production system” (WS language) | Mid PE / Software Developer / domain-backend; founding demo |
| Same, plus watched caseworkers and refused unique briefs | TSO + PE “what is worth solving” | Refusal log, playbook, session notes | Faire/Ashby PE; Dimely founding; Type 1 FDE feeder (8%) | Same + small-co FDE |
| Operate Tower infra (deploy, IAM, restore, cost) | Supporting reliability | Restore test, compose, CI | Mid Cloud at a *product* company if you want it; else “they can ship” | Optional Cloud IC; not bank cloud |
| Reconciliation + valid-time store | Operational truth | Recon job, grain ADR | AE / junior-mid DE *if* you want that slice | Not Staff Data Platform |
| Freelance REST / Stripe / CRUD | Shipping to a deadline | Many repos | Agency Backend Developer; “wrapped tables” | Junior–low-mid; **not** Nue/Harvey |
| Custom app to spec, handed off | Agency FS | Client folder | Web / 21234 / shop | Not PE |
| HubSpot/Clio/Zapier retainers | Implementation | Go-lives | Implementation Consultant | That occupation |
| Staff-aug on their product | Team + their stack | Manager ref, PRs | Continuous **at that company**; CRA if it looks like FTE | Convert, or next logo |
| LeetCode-only | Interview theater | Profiles | Big Tech screen, no craft | Not this architecture |
| Linux Systems Engineer contract | Infra/IT | TMX-shaped CV | Route 1/IT | Not PE/backend |

### 6.1 Where independent experience is discounted

**Evidence + Inference.**

1. **Founder/CEO coding** — recruiter under-count (Hypothesis, consistent across files).
2. **No team** — Wealthsimple Senior asks team tenure; review culture missing.
3. **Years formulas** — Harvey “post-BS/MS”; 4–5+ seniors; Indeed junior collapse.
4. **Stack** — PHP/Go/Java/Rails vs Tower in Node/Python.
5. **Logo / “high-quality software company”** — Linear.
6. **Theater résumé** — microservices/Kafka for one deployable (negative if the reader can tell).
7. **Empty education at bank Workday** — campus is enrollment-gated; FTE box **not directly observed** in the 2026 scan.
8. **Title “Product Engineer” at a bank ATS** — they hire Developers.

### 6.2 What makes it more legible

- Résumé as **responsibilities + artifacts**, not company narrative.
- Public professional-quality repo (or a shareable core) matching artifact memo §7.
- Case study: correctness under failure, not stack list.
- One external review (OSS PR or staff-aug) to blunt the team gap.
- Degree in progress/complete for bank/gov doors.
- Parallel DSA/system-design block if Big Tech / some SWE loops stay in scope (deep-pass §15.4).
- Title translation: “Software Developer — production eligibility systems,” not “Founder / Full-Stack / FDE.”

---

## 7. Employment-market reality

See [`evidence/plan-c-market-2026.md`](evidence/plan-c-market-2026.md) for posting-level tables. Cross-cut:

**Stated vs preferred vs hard (Inference across families).**

| Gate | Stated often | Preferred | Hard in practice |
|---|---|---|---|
| Degree | Job Bank “usually”; Faire/Docebo “or equivalent”; Ashby/founding absent; Harvey years post-BS/MS; bank campus enrollment | CS tokens | Campus = enrollment. Equivalent clause is real at some product cos. Bank FTE education box unobserved this pass |
| Years | Faire 2+; everyone else 4–5+ or anti-junior | “Shipped SaaS,” “on a team” | 2 years only clears Faire-shaped IC and founding 2–6. Senior product is 4–5+ |
| Stack | Language pinned at Docebo/Faire; “retrain” at Ashby/WS | AI-agentic coding now **stated** | Language match is a screen at PHP/Go shops |
| Domain | Cards = payments years; Harvey = legal SaaS | Regulated comfort | Tower ≠ card rails. Tower *is* closer to Dimely's “messy rules → validated state” |
| Interview | Ashby no-LC pair+product; Docebo system design; Publicus demo; Google-class DSA (prior evidence, not re-fetched as live FTE) | Production walkthrough | Theater is a separate ticket |

**Employer types that preserve the combination:** Canadian and Canada-hiring *product* companies (Faire, Wealthsimple PE-org, Ashby, Dimely-shaped founding).  

**Employer types that force specialization:** Cards/payments; Docebo Automation/K8s; bank Developer buckets; partner-FDE; 21234 web; ML founding.

**Industries that fit the domain story:** fintech (regulated-adjacent carefulness — asset *or* liability, unmeasured), legal-AI (Harvey), vertical SaaS, immigration-tech analogs. Banks: access later via degree, stack gap remains.

---

## 8. Repository / artifact investigation

Full memo: [`evidence/artifact-quality.md`](evidence/artifact-quality.md).

**Architecture actually used (Evidence).** Monolith first (Fowler); modular monolith when people-scale hurts (Shopify, GitLab); merge-back from microservice tax (Segment/Twilio); majestic monolith (37signals). Jobs as operable effects (Solid Queue; Sidekiq; BullMQ), not Kafka-as-identity.

**Repos inspected.**

| Repo | What “professional” looks like |
|---|---|
| [chatwoot/chatwoot](https://github.com/chatwoot/chatwoot) | Rails monolith; `app/jobs` + Sidekiq queues; Pundit `app/policies`; swagger + Skooma drift CI; 16-way RSpec on Postgres/Redis |
| [calcom/cal.com](https://github.com/calcom/cal.com) | Prisma migrations; feature packages; Trigger.dev Tasker with **sync fallback**, Zod, retry; sharded Playwright/Jest; path-filtered CI |
| [twentyhq/twenty](https://github.com/twentyhq/twenty) | API + BullMQ worker + CLI; CI fails on uncommitted migrations and OpenAPI/GraphQL breaking changes; worker smoke |
| [TryGhost/Ghost](https://github.com/TryGhost/Ghost) | Migration-review workflow: idempotent `up`/`down`, no mixed DDL/DML |

**Portfolio vs professional (Inference).** Portfolio proves you can assemble a stack. Professional proves the system can be changed, operated, and not lie. Center of gravity: invariants, migrations, jobs, contract CI, authz, users — not README screenshots.

**1-person bar vs FAANG bar.** Structured logs, worker errors, one business alert, restore-tested backups, ASVS L1 authz, CI against real Postgres. Not SLO burn-rate matrices or a platform golden path.

**Normative bar this architecture adopts** (artifact memo §7): one deployable; schema is history; invariants are tests; jobs are effects with keys; API is a contract; authz is server-side; operability you have used; at least one real user. Anything else is decoration.

---

## 9. Mastery horizon

Elapsed time ≠ seniority. These are **observable ownership tests**. They assume Plan A is real. If Tower is a prototype, the clock has not started (deep-pass §14.1).

### ~6 months

A language, a schema, an API, a worker, CI, compose. One journey authenticates, persists, stays up. Maybe no paying user yet. **Still glue if the domain is shallow.** Supporting cloud/data/field are embryonic. DSA not required yet.

### ~1 year

R5/R2 1-year object: one bounded context in production — schema, HTTP API, job runner, authz, logs you read; a product surface a human finished; migrations that did not destroy data; OpenAPI that matches; **one real consumer**; one incident note. Modular monolith, no theater. Field: one discovery → schema story. **This is the gate.** Below it, Plan C is junior/agency.

### ~2 years (end of planned Plan B)

Invariants under some failure (crashed worker, duplicate webhook, partial migrate) as *operational* stories. A playbook. A refusal log. Instrumentation on the CUJ. Maybe a second firm on the same product. Résumé can be rewritten as engineering. **Honest Plan C:** intermediate PE / Software Developer / founding demo. **Not:** Senior 5+, Staff, bank FTE, Palantir FDSE. Degree-in-progress may be opening campus/eligibility. Interview theater is a parallel block if those employers are in scope.

### ~3–5 years

Either (a) Omcoda is a domain core several surfaces share, or (b) Plan C IC ownership of a bounded context others cannot casually break. Optional event log because a second consumer appeared. Title translation: Senior Backend / Senior Software Developer / Product Engineer at a product company. **Still not Principal.** If these years were CRUD, Zapier, or CMS, you are still on year-1's object (R3; R5 Chain B). Team review now exists if Plan C or serious OSS happened.

**Principal / Staff-plus (decade-class, not this plan's promise).** Larson Architect: direction of a critical domain (https://staffeng.com/guides/staff-archetypes/). Requires org influence the 1-person firm cannot fake and two years cannot produce (R5 §4.2).

---

## 10. Final architecture

### Central craft

**Software / Product Engineering that exists to express a domain core** — not screens, not tickets, not CMS. Greatest mastery investment: making a valuable journey true in software people use, and iterating it while it is alive.

### Technical spine

**Backend / Systems:** domain model, schema, transactions, APIs, jobs, authz, failure, observability. This is what “consequential” means. Without it, Product Engineering collapses to generic full-stack.

### Supporting capabilities (ceilings)

| Capability | Required depth | Identity to refuse |
|---|---|---|
| Cloud / Infra | Deploy, IAM, restore, logs, one alert, boring cloud, CI | Platform / K8s / SRE-of-scale |
| Data / Automation | Grain, time, recon, jobs as activation, SQL | Zapier mill; warehouse/Spark identity |
| Frontend | Journeys + instrumentation | Framework fashion; 21234 |
| Field | Diagnosis, playbook, refusal, user observation | Implementation Consultant; Type 2 FDE; SE |

### Plan A function

Omcoda is the **studio**: the only realistic pre-degree way to own a core rather than a periphery (R5 §7.2). It compounds the craft when hours go to invariants, product journeys, and operability. It taxes the craft when hours go to Kubernetes-for-one, unique briefs, or UI-without-model.

### Plan B function

Independent operation exists to produce **users, incidents, longitudinal ownership, and cash without changing occupation**. The viable offer is operated Tower (and periphery that serves it). Off-object cash is a labeled runway, not the plan.

### Plan C function

The CS degree expands **eligibility and screening** (banks, federal, some ATS, campus/co-op, DSA reps). It does not create the capability. Employment surface to optimize for: **product-company mid IC** (Product Engineer / Software Developer / domain-backend) and **founding-engineer demo screens**. Optional: Type 1 FDE if the loop is engineering. Not the primary aim: Cloud/Data/Solutions identities, bank senior, Staff.

**Desired transition (supported as Inference, conditional on Tower):**  
Plan B operator of a live domain product → same object + degree as key → expanded mid-IC surface.  

**Unsupported transition:** Plan B custom-shop/Zapier/CMS → graduate → start an unrelated Plan C as if the years counted.

### Requirements map (inventory)

**Central, year-1:** one language; SQL; domain model; schema+constraints+migrations; HTTP API; authz/tenancy; transactions; idempotent jobs; tests (state machine + job-twice); CI; deploy/restore; thin product surface; structured logs; one user; one incident.

**Central, ongoing:** field diagnosis; refusal of briefs; instrumentation; migration-in-anger; case studies as correctness-under-failure.

**Supporting, timed:** boring cloud/IAM/cost; recon jobs; integrations as periphery; frontend sufficient for journeys; ASVS L1; ADRs/runbooks.

**Parallel, for Plan C access:** DSA + system-design theater; degree credentials; second-language *reading*; one external team signal (OSS or staff-aug).

**Out:** CMS identity; Zapier identity; vendor-consultant identity; Linux Systems Engineer identity; DS/ML identity; microservices theater; K8s-for-one; Staff-in-two-years; Technical PM.

**Dependencies:** §2.8. Gate: first real user + incident + live migration before adding supporting identities.

### Challenges that survive this pass

1. Combination is **capability architecture**, not a job title — employers hire slices.
2. Plan B **cash attractors** (custom, glue, vendor impl) fight the center.
3. Employed Plan C **amputates** TSO client diagnosis.
4. **Founder discount**, team-tenure gates, and post-BS/MS year formulas will under-count.
5. **Interview theater** is a separate ticket from Tower.
6. **Stack provincialism** (Java/Spring, PHP, Rails) vs a Node/Python Tower.
7. GTA **Very limited** weather — artifacts must be professional, not portfolio.
8. All continuous chains are **conditional on Tower actually being a core**.

### Open questions (before Character Architecture)

Load-bearing; do not paper over:

1. **Tower artifact inspection** against the 1-year tests (§9) and artifact memo §5. Until then Character Architecture would be designing a person for a laboratory that may not exist.
2. **Will GTA professional-services firms buy operated proprietary software** vs Clio+Zapier+impl? Conversion, ACV, cycle unknown.
3. **Can this subject close Plan B** at all, pre-degree? Rate cards ≠ a pipeline.
4. **Workday education-box behaviour** for *experienced* Canadian bank Developer reqs.
5. **Founder-discount survival rate** after 2 years of 1-person production (Bloomberry 8% feeder shows possibility, not rate).
6. **GTA Type-1 FDE volume** as a time series.
7. **Java/Spring as hard gate vs preference** at Toronto product companies outside banks.
8. **Immigration-data as asset vs liability** (cannot show the code).
9. **School choice / part-time feasibility** while operating Plan A — out of prior scope, now blocking if the degree is on the critical path for bank/gov.
10. **Tax / corp / IRAP / SR&ED** effects on Plan B leverage in Ontario.
11. **Whether “Product Engineer” remains a stable Canadian title** or stays a small SaaS cluster.
12. **Personal primitive depth today** — this file states requirements, not a skills inventory of the subject.

---

## What this file is for next

Character Architecture needs: an environment (Omcoda + GTA product-company Plan C + CS program as access), an organizational role (founder-operator now; mid-IC product/backend later), a technical object (live domain core with a product face), and professional requirements (the map in §2 and the artifact bar in §8). Those are now specified at research depth.

It still should **not** start until question 1 (Tower as artifact) is answered. Everything else in this file is reusable; that one fact decides whether the architecture is available or still hypothetical.

---

## Source index (compressed)

Route files and the prior synthesis: [`role-architecture-deep-pass.md`](role-architecture-deep-pass.md), [`evidence/route-1-cloud-infra.md`](evidence/route-1-cloud-infra.md), [`evidence/route-2-software-product.md`](evidence/route-2-software-product.md), [`evidence/route-3-data-automation.md`](evidence/route-3-data-automation.md), [`evidence/route-4-solutions-implementation.md`](evidence/route-4-solutions-implementation.md), [`evidence/route-5-backend-systems.md`](evidence/route-5-backend-systems.md).

2026 market scan and artifact memo: [`evidence/plan-c-market-2026.md`](evidence/plan-c-market-2026.md), [`evidence/artifact-quality.md`](evidence/artifact-quality.md).

Primary anchors used in this file: omcoda.com; Faire / Ashby / Docebo / Wealthsimple / Harvey / Publicus / Palantir JDs (URLs in the market file); Job Bank / COPS / Indeed Hiring Lab; Bloomberry; Tandem; Fowler MonolithFirst / Microservice Premium; Shopify modular monolith; 37signals; Segment/Twilio; Chatwoot, Cal.com, Twenty, Ghost; Kleppmann DDIA; Mastering Backend; EnzRossi; staffeng archetypes; Google Time Warp; Consensus 2026 SE report; PEO unlicensed-practice FAQ.

---

*End of Combined Role Architecture. No employment title is selected. No route is eliminated. The working choice is supported as an Omcoda/TSO capability architecture and is not supported as a single vacancy.*
