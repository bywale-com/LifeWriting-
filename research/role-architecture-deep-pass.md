# Technical Systems Operator — Role Architecture Deep Pass

**Document type:** LifeWriting research. Not a career decision.  
**Date:** 2026-09-22  
**Subject:** Wale Omotayo, Greater Toronto Area. Plan B = independent operator work before a CS degree. Plan C = later full-time engineering in which that work must count as real experience.  
**Archetype:** Technical Systems Operator — diagnose organizational bottlenecks, architect technical solutions, write or integrate software, automate processes, and maintain live systems end-to-end.  
**Company in the flywheel:** [Omcoda](https://www.omcoda.com/) — a managed solutions provider, not a custom software shop. Identifies gaps in professional-services markets (immigration, legal, financial), builds proprietary software, and operates it for firms. Current product: Tower (eligibility monitoring and client reactivation). Explicit refusal: *we do not take briefs, build to spec, and hand off.*

This pass does not pick a winner. It does the three things the revision asked for, across all five remaining routes, then compares architectures rather than intuitions.

Evidence files with sources, epistemic tags, and the full chains live in [`research/evidence/`](evidence/). Claims here are compressed from those files. Where this document is more certain than the evidence, that is a writing failure — trust the file.

---

## 0. What this pass was asked to do

The locked protocol already had five sections per route: work composition, leverage, B→C plus degree mechanisms, Omcoda flywheel, mastery horizon.

Routes 1 and 4 had been characterized. The revision said that characterization had surfaced a deeper question than “which route scores higher,” and named three additions *before* any comparison:

1. **Deepest technical object.** Not “how technical?” What do you eventually get to own?
2. **A real B→C chain.** Not a match percentage. Independent work → responsibilities → evidence → exact title → employer type → expected level → degree effect. Continuous, or only conceptually similar?
3. **Career optionality.** After excellence, what can you become? What cages you? This is a decade-scale capability base, not a first job.

It also said: take Route 4 seriously as a possible Omcoda laboratory; do not eliminate Cloud/Infra; run the same evidence for the other routes; then compare architectures.

Candidate #6 (Technical Product / Product Engineering as PM) stays dropped. The five routes in the pool:

| Category | Route | Stated focus |
|---|---|---|
| Infrastructure & Operations | **1** Cloud & Infrastructure (Platform / DevOps) | Cloud, IaC, containers, CI/CD, pipelines |
| Application Engineering | **2** Software & Product (Full-Stack / App Building) | End-to-end user-facing applications |
| Application Engineering | **5** Backend & Systems (Distributed Systems / Core APIs) | APIs, schemas, jobs, reliability, scale |
| Data & Automation | **3** Data & Automation (ETL / Workflow Automation) | Pipelines, workflow scripts, warehouses, dashboards |
| Field & Client Engineering | **4** Solutions & Implementation (Technical Consulting / Integration) | Translate friction, integrate APIs, glue, automate for non-technical stakeholders |

---

## 1. How to read claims

- **Evidence** — a posting, survey, official guideline, or named practitioner source. URLs in the evidence files.
- **Inference** — a conclusion from several pieces of evidence plus the subject context.
- **Hypothesis** — decision-relevant and not established.

The earlier **90%+ (Cloud)** and **80%+ (Solutions)** B→C figures are **not findings**. They are hypotheses this pass was written to retire.

Tuesday percentages, where given, are ranges. They are not a time-and-motion study of this subject.

GTA labour-market weather, 2025–2027: Ontario Job Bank outlook for software engineers and designers (NOC 21231) and software developers and programmers (NOC 21232) is **Very limited**. Plan C is not entering a shortage. Artifacts have to be better than “I also used the tools.”

---

## 2. Subject architecture that every route is scored against

Three facts about the subject, not about the labour market:

1. **Mastery is the asset.** A route that pays well while leaving you owning someone else’s Salesforce org, a ticket queue, or a CMS theme has failed the brief even if Plan B cash is easy.
2. **Omcoda is specified by its refusals.** Verbs that match “understand → design → integrate → deploy” are not enough. Custom shops and HubSpot partners use those verbs. Omcoda owns the software and operates it. A route that trains you to say yes to the next brief is incentive-incompatible even when the skill overlap looks perfect.
3. **Plan B must close before a degree, and later be readable as engineering.** Those two jobs are not the same buyer. What an immigration consultancy will pay for this quarter is not what a hiring manager at a product company or a Canadian bank will credit in two years.

Omcoda’s own site names three disciplines: solutions architecture, market development, managed operations. Tower is a production system whose core is an eligibility state machine plus reactivation workflows. That is the laboratory. It is not an infrastructure company, not a Zapier agency, and not a distributed-systems showcase.

---

## 3. The finding that changes the comparison

**Every route name hides more than one job.** Comparing “Cloud vs Solutions” as two occupations was the original error. The revision’s object / chain / optionality questions only resolve after the labels are split.

| Route label | Distinct jobs the market actually hires | The job that matches the TSO + Omcoda architecture |
|---|---|---|
| **1 Cloud / Infra** | Ticket-ops “DevOps”; MSP; product-company platform/SRE; bank Azure/OpenShift; independent landing-zone/CI seller | Production control plane of a live product (Tower’s runtime), not EKS-as-identity |
| **2 Full-stack / Product** | CMS/theme freelance; agency ticket full-stack; product engineer at a product company; founding engineer | Building and operating a domain-specific product (Tower), not taking app briefs |
| **3 Data / Automation** | Zapier/Make consultant; analytics engineer (dbt/warehouse); platform data engineer (Airflow/Spark); leftover RPA | Operational state system: ingest → model → detect → activate. Not a dashboard. Not a Zap. |
| **4 Solutions / Implementation** | Pre-sales SE; post-sales implementation consultant; vendor-certified consultant; true FDE; independent glue | Founder-FDE of *your* product. The base-rate jobs are implementation of *someone else’s* product. |
| **5 Backend / Systems** | SMB CRUD APIs; staff-aug on someone else’s core; product-company backend; “distributed systems” at Big Tech; Canadian “Systems Engineer” as Linux/infra | Domain core and its invariants. Not microservices theatre. Not TMX-style Systems Engineer. |

Once the labels are split, a second finding appears:

**The Plan B that is continuous with serious Plan C, in every route, is the same shape: Tower (or an equivalent) running in production for real firms.** Freelance glue, CMS, ClickOps, and “I used Terraform” are cash or conceptually similar experience. They are not the same object.

That is not a vote for “just do Omcoda and ignore routes.” It is a statement about evidence. The routes still differ in **which object inside Tower you make your mastery**, how independently that object can be sold, how Plan C interviews read it, and how easily the market pulls you off the product.

---

## 4. Deepest technical object

The revision: *don’t just ask how much technical. Ask what is the deepest technical object I eventually get to own.*

Surface work is what Tuesdays look like. The object is what is still valuable if every brand name on the résumé dies.

| Route | Surface | Object of mastery, if the route is walked in earnest | Object you actually own if you follow the base-rate market |
|---|---|---|---|
| **1** | YAML, `kubectl`, Terraform apply, red pipelines | **A production control plane**: desired-state reconciliation of an estate under identity, network, failure, cost, and change control (K8s controllers, Terraform state, IAM graph, SLOs) | Tickets against someone else’s modules; or a small landing zone you no longer own after handoff |
| **2** | Screens, repos, “the app” | **The domain model of a live product** plus the operated runtime that keeps it true (37signals’ `Recording` is the craft analog of Tower’s eligibility machine) | A folder of client codebases, or a CMS |
| **3** | Zaps, DAGs, dashboards | **A production eligibility (or analog) state system**: grain + valid time + tests + a durable activation loop. Warehouse and workflow engine are layers of that object, not the object | Other people’s Zapier orgs, or a reporting ghetto |
| **4** | Demos, SOWs, HubSpot portals, Zaps | **How a product is made real in the field** — only in true FDE or founder-operator form. “OS of the firm” is founder language, not a hired principal object | The client’s vendor tenant |
| **5** | REST endpoints, “we have Kafka” | **The domain core and its invariants**: schema, API contract, jobs, what must never be true, what happens if the worker dies after commit | CRUD mill, or a microservice CV with no users |

Horizon, compressed. These are observable tests, not titles.

**~1 year**

- R1: one workload, git push → prod → rollback, remote state locked, one incident write-up. Kubernetes is not required.
- R2: one user journey that authenticates, persists, and stays up. Glue, not a domain.
- R3: a live pipeline *or* a live workflow with error handling. Depth is still “I can keep data moving.”
- R4: you can map a messy process onto a tool and get a cheque. You do not own a system.
- R5: one bounded context in production: schema, API, idempotent jobs, logs you actually read.

**~3 years**

- R1: a golden path other humans can ship on; SLO; identity/network graph from memory.
- R2: a domain model that survives feature churn, plus a UX grammar. Tower-shaped: eligibility states, permissions, jobs.
- R3: a warehouse or operational store whose grain you would defend, plus orchestration you can page. If the three years were Zapier, you are still on year-1’s object.
- R4: either senior implementer of vendor orgs, or founder-FDE of one product across several firms. Those are different objects.
- R5: invariants under failure — crashed worker, duplicate webhook, partial migration — as operational stories, not CAP recitation.

**~5 years / principal**

- R1 principal object: the production *institution* (how the company is allowed to change machines).
- R2 principal object: a constraint system other engineers can extend without you in every PR.
- R3 principal object: a data architecture others cannot quietly violate. Staff data-platform postings ask 8–10+ years of *that class of system*.
- R4 principal object, base rate: CTA / MuleSoft / Microsoft SA — vendor-platform architecture. Founder principal object: the product + its operating layer across firms, not each firm’s OS.
- R5 principal object: technical strategy for a core domain (Larson Architect). Two years of Plan B cannot produce this.

**Direct answer to the Cloud vs Solutions contrast in the revision.** Cloud’s mountain is production infrastructure / platform / reliability architecture. Solutions’ advertised mountain was “technical architecture of an organization’s workflows and integrations.” Evidence says that second mountain is **mostly a vendor org** (Salesforce, HubSpot, Clio, Zapier) unless you are true FDE or you own the product. Those are different forms of mastery. The original contrast was right about the *aspirations* and too generous about what Route 4 actually awards.

---

## 5. Work composition (what a Tuesday is)

The original 30/30/20/20 (Cloud) and 35/25/20/20 (Solutions) mixes are **too tidy**. They are mid-level target shapes for one sub-job each, not occupation means.

| Route | What a healthy employed Tuesday is actually made of | Independent / 1-person shape | What it feels like |
|---|---|---|---|
| **1** | Interrupts 25–50%; IaC 15–35%; CI/CD 10–25%; design 5–20%; meetings/docs 15–35% (higher in banks). Google SRE *average* toil ~33%, individual range 0–80%. | Whatever is on fire plus whatever ships the product. Infra can be 10% or 80% in a given week. | Interrupt-shaped systems work. You restore desired state. Developers ping you when “the environment” is wrong. |
| **2** | New behaviour 20–45%; maintenance 20–40%; user/product judgement 3–20% (culture-dependent); meetings 15–40%. Clockwise: ICs ~10.9 meeting hours/week; Tuesday is the worst focus day. | Hunter-freelancer: 20–40% selling/PM. Operator-founder: product engineering superimposed on sales, onboarding, and ops. | Feature not done at merge. At large firms the day is chopped. At product-engineer cultures you are also PM and support. |
| **3** | Platform DE: production health 15–35%, maintenance 15–25%, new ingestion 10–25%, modeling 10–20%. AE: dbt 30–50% plus semantic governance. Low-code: discovery 15–30%, building scenarios 25–40%, break-fix 15–30%. | SMBs buy workflows; they rarely buy Snowflake. Two Tuesdays share a name. | Schema/API drift and silent failure in both crafts. The *object* that failed is not the same (a missed CRM row vs three weeks of dropped orders). |
| **4** | **Pre-sales SE (n=423 Consensus 2026): 56% demos/discovery/POCs, 14% implementation, ~0–15% production code.** Implementation: workshops 25–45%, vendor config 25–45%, glue 10–30%. True FDE: ~50/50 customer and production code. | 30–50% selling if you have no AE. Draft 35/25/20/20 is only a hypothesis for this sub-job, and “system design 20%” is generous. | SE is a sales-technical job. Implementation is go-live of a product that already exists. FDE is software with a customer in the room. Do not mix them. |
| **5** | Microsoft Time Warp (484 ICs): coding ~11% actual vs ~20% wanted; debugging ~9%; design ~6% vs ~15% wanted. Re-binned guess for backend: code 25–40%, diagnosis 15–30%, internal contact 15–25%, external client 0–5% on a non-incident week. | Clients buy integrations, CRUD+auth+payments, firefighting, short architecture docs. They rarely buy a multi-year domain core. | Diagnosis, review, and living with last year’s schema. Client contact is mostly internal unless you are the founder. |

**Implication.** Route 4’s original mix described an independent integrator and was **false for employed Solutions Engineer**. Route 1’s mix is a mid-level platform target in a healthy org, not junior ticket-ops and not a 1-person founder week.

---

## 6. Independence and leverage

Three economic roles, not a slider.

| Route | Employee | Contractor / packaged sale | Independent operator (Omcoda-shaped) |
|---|---|---|---|
| **1** | High leverage *for the employer* if you own a platform; low for you if TicketOps. Same title: RBC DevOps median ~CA$102k vs Shopify L5–L7 ~CA$154–267k. | Senior K8s/Terraform **$110–$160/hr** is a senior market, not pre-degree Plan B. Sellable before a degree: CI/CD, landing zone, Dockerize+observe, cost sprint — if you can show a live system. Professional-services firms do not buy EKS. | Infra is a **trust input** to Tower, not the sale. Draft “Operator High” overstates this route’s economics for this subject. |
| **2** | Scope of system, not hours. Staff is a different job (GitLab, Shopify). Ontario: “Software Engineer” is a restricted P.Eng. title; market still uses it. | Complete apps *are* the default commercial expression (Toronto MVP bands ~CA$30–80k). That is also the model Omcoda refuses. | One system × N firms. Compatible with Omcoda. Custom-app gravity is the well. |
| **3** | DE/AE seats buy production models, SLAs, incidents. Bank DE bands are professional, not US-SaaS lottery (BMO ~CA$62–114k; TD DE median ~CA$102k). | Two markets: packaged workflow automation (closeable, car-payment prices) vs mini-warehouse (harder first sale, much closer to Plan C). | Tower productizes monitoring+reactivation as software rather than as a custom Zap. Craft underneath still decides what GitHub looks like. |
| **4** | Vendor SE/SA pay is real and high (Salesforce Canada SE CA$95–145k base; Microsoft D365 SE IC4 CA$96–178k; Snowflake SA GTA median TC ~CA$262k). Canadian implementation ~CA$70–120k. Consensus: average SE has ~11 years presales. | Rate spread is violent: Make Community CA$25–40/hr vs Salesforce CA$85–160/hr vs packaged $500–$8k/workflow. “Contractor Extremely High” is a ceiling, not a default. Unpaid selling is 30–50% of a 1-person shop. | Very high **only if** the software is proprietary and the wrapper is operating that software. Route 4’s market pays you to say yes to the next workflow. |
| **5** | Deepest work is **employee-shaped**. Product companies keep the domain core in-house (EnzRossi: outsource periphery, not the core). | Discrete integrations sell. “I will design your core APIs” sells as boutique architecture to teams that already have engineers — not as a pre-degree GTA product. | Selling backend *as backend* to SMBs collapses to CRUD. Selling the **outcome** (eligibility monitored) and owning the engine is Omcoda, which uses this craft. |

**Contractor viability, three-way (not a ranking of careers):**

| | What the buyer inspects | Independent package? | Employee gravity of the deepest work |
|---|---|---|---|
| Route 1 | Cloud account works | High, for the right buyer (tech, not immigration firms) | Medium |
| Route 4 | A process now happens | High | Medium (some work is forever contractor) |
| Route 5 | Invariants hold over years | Low for the core; medium for periphery | High |
| Route 2 | An app exists | High — and that sale is the custom shop | Medium |
| Route 3 | A workflow fires, or a number is trusted | High for workflows; medium for warehouses | High for platform DE |

CRA treats IT consultants as a class where control is hard to read; a single-client “contractor” on someone else’s laptop is economically an employee. Bank DevOps contracts via staffing firms are usually that shape, and they want the years Plan B is trying to create.

---

## 7. Degree mechanisms (three, separately)

A CS degree is not one thing. Split eligibility / screening / progression. Split employer type.

### Compact verdict

| Route | Eligibility (can you apply?) | Screening (do you get seen / through the loop?) | Progression (Senior → Staff/Director) |
|---|---|---|---|
| **1** | **Low** for private-sector DevOps (“or equivalent” is common). Harder gates: years, Azure/OpenShift, on-site, credit/criminal, clearance — not CS. FINTRAC/GC is essential-experience essays + clearance. | **Medium**, not the folklore “High.” Burning Glass/HBS: dropping BA requirements raised non-BA hires only ~3.5pp; ~45% of firms were in name only. After two years of Plan B, **missing logos** likely screen harder than missing BA. | Degree is hygiene at bank director; impact/scope at startups. **“Progression High” for the degree is not well supported.** Years of platform outcomes dominate. |
| **2** | Startups: rarely a hard bar once shipped product exists. Banks/gov **co-op doors are enrollment-gated**. Federal IT: two-year credential by default; experience alternative is per-competition and does not travel. | High at banks/Workday and federal essential-education boxes. Weak at startups. Medium at Big Tech *campus*; after credible production, the hidden value of the degree is **DSA prep**, not the PDF. | Low for IC Staff at product companies. Medium-high for bank/gov Director+. Opposite shape of Plan B value. |
| **3** | Bank intern machines and many FTE posts want a bachelor’s. Federal IT: two-year credential. Data science is worse (master’s “usually required”) — do not use DS as the Plan C. | Stack tokens (dbt, Snowflake, Airflow, Spark) and title match. “Automation consultant” applying to “Senior Data Engineer” dies on title before keywords. | 8–10+ years of the *same class of system* for Staff data platform. Two years of n8n do not start that clock. |
| **4** | Low for indie and vendor-consultant (certs substitute). Low-moderate for SE/FDE (“or equivalent” common). Some implementation jobs list a bachelor’s with no equivalent clause. | **Depends on destination.** Low for more freelance/certs. Medium for vendor SE (tenure in the motion). Medium-high to high for FDE/SWE — the coding interview is the gate. Average SE has 11 years presales; that is the screen, not the diploma. | High *inside* a vendor ladder. Weak as a bridge to product engineering. |
| **5** | Often the hardest of the five. NOC 21232 is TEER 1, “usually” a degree. Smile-class hard-requires it. Wealthsimple-class omits it. Google says “or equivalent”; campus still behaves like a degree pipeline. | **The sharp gate.** DSA + system design. Coding decides whether you can do the job; design decides the level. A live Tower does not skip LeetCode. | Once inside, degree residual is small vs ownership. Degree is a key, not a ladder. |

**Inference for timing.** A Canadian CS degree earned *while* operating Tower helps mechanism 2 at banks/gov without being required to close Plan B. It does not convert a Zapier year into a Data Engineer year, or a CRUD year into Staff. It also costs Omcoda operating time. That trade is not measured here.

---

## 8. Hard B→C chains

Rule: no match percentages. Two years of Plan B counts when the next employer is buying **the same responsibilities, at overlapping scale, with artifacts they know how to score**. Same tools, different object = conceptually similar. Hiring managers discount that.

Staff / Principal / Director / Google L5+ / bank senior-with-6–8-enterprise-years are **not reachable** from two years of independent work on any route. That is a floor, not a morale statement.

### 8.1 Route 1 — Cloud & Infrastructure

**Chain A (continuous).** Operate Tower as production: Terraform, CI, OIDC, secrets, observability, incident log, cost, IAM, backup restore. Maybe one client landing zone.

- **Titles:** Cloud / DevOps / Platform Engineer at GTA Series A–B SaaS — **mid**. First infra hire at a 10–40 person company — de facto senior in that room.
- **Degree:** small. Artifact > BA.
- **Does not reach:** Senior SRE (5+), EQ Bank Staff Cloud (8+ enterprise, Azure + Power Platform), Canada Life Senior (6+ enterprise), Google Staff SRE, Shopify Production Engineer at L5+, OSFI-facing cloud governance.

**Chain B (conceptually similar — the common fantasy).** AWS/Terraform freelance + certs → mid Cloud Engineer at RBC/TD/BMO.

- Same words (Terraform, Kubernetes, CI/CD). Different object: regulated estate, OpenShift, Entra, CAB, OSFI B-13/B-10.
- **Verdict:** a slogan, not a chain. Conversion mechanism for banks is **time inside the regulated envelope**, not school. A CS degree does not fix this.

**Chain C.** Productized landing zones + retainers, CRA-shaped independence.

- Continuous toward founding DevOps / MSP engineer. MSP is a TSO-risk (ticket gravity). Not a bridge to principal.

### 8.2 Route 2 — Software & Product

**Chain A — WordPress/Shopify/CMS.** Not continuous with Product Engineer. Reachable: Web Developer, junior frontend, agency “full stack.” Degree does not convert this chain.

**Chain B — Tower-class SaaS, built and operated.** Closest to continuous.

- **Titles:** Product Engineer, Full-Stack Engineer/Developer, Founding Engineer. Faire-like Product Engineer (2+ YOE, end-to-end) is the shape of a reachable seat. Linear Senior/Staff (5+ years at a high-quality software company) is not a 2-year default.
- **Level:** intermediate / early-senior IC at a startup. GitLab Intermediate-to-Senior, not Staff. A single SaaS is one deep project; Shopify Staff requires diversity of large-system work.
- **Gaps employers still probe:** someone else’s codebase, review culture, team testing, DSA.
- Bank full-stack experienced hire is conceptually similar (Java/.NET, compliance theatre), not continuous.

**Chain C — agency/Toptal contract full-stack.** Most continuous with employed Full-Stack as a *work week*. Weaker than Chain B as an *ownership story*. Level matches the work, not the invoice.

### 8.3 Route 3 — Data & Automation

**Chain A — Zapier/Make.** Continuous with Automation Specialist / RevOps / “business systems.” Not conceptually similar to Data Engineer (named anti-pattern: Zapier is not a pipeline). Not similar to Analytics Engineer unless there was secret dbt.

**Chain B — Python ETL + warehouse + dbt + tests.** The chain that makes “two years counts as real experience” **least metaphorical**.

- **Titles:** Analytics Engineer (mid) at SaaS on Snowflake/BQ+dbt; Data Engineer junior/mid on a managed ELT stack. Reverse-ETL-adjacent if CRM sync is owned.
- Bank DE is conceptually similar to the modern slice and not continuous with Hadoop/Netezza residue; mechanism 1 still likely blocks without a bachelor’s.

**Chain C — Tower internals.** Ingest status, valid-time eligibility state, rule versions, reactivation workflows, reconciliation, semantic definitions.

- Continuous with product-data DE/AE, integration-shaped DE, or workflow-leaning backend (often posted as Software Engineer).
- Still not Staff Data Platform (8–15 years, Spark/Iceberg/Kafka, multi-geo). A 10-firm managed product is not 400 million MLS updates.

### 8.4 Route 4 — Solutions & Implementation

The 80%+ figure hid that continuity is **sub-route-dependent**.

**Chain A — SMB glue.** After two years: more freelance; Implementation Consultant / Onboarding Specialist at small-to-mid SaaS (the default Plan C, ~CA$70–120k); maybe junior integration if the work included real API/error-handling.

- **Not reachable:** named-vendor mid SE (Prophix wants 3y presales; Consensus average is 11y), true FDE, product SWE, Google CE, enterprise SA, Integration Architect.

**Chain B — vendor-certified (Salesforce/HubSpot/Clio/Microsoft).** Continuous inside the ecosystem (Consultant → later SA). Partial into same-vendor SE. Not a 2-year SA/CTA. Exit to general SWE is a grind. High-income cage.

**Chain C — “I did FDE verbs.”** Independent glue does not pass DX Clouditive’s test (did the work change a *vendor product*?). Palantir/Anthropic will still give a coding interview. Accenture-class “FDE” at SI rates might take you; that is professional services with a worse title.

**Chain D — Tower as the product you implement (founder-FDE).** Closest continuity Route 4 has.

- Bloomberry n=100 FDE profiles: SWE 45%, SE/SA 22%, founder/early employee **8%**. FDEnest: early-stage startup engineers have already done the FDE job.
- **If Tower is real** (paying firms, uptime, integrations, you on-call): possible mid FDE at a small product company *if* the coding interview passes; mid SE at vertical SaaS; maybe junior/mid SWE. Google CE and enterprise SA still no.
- **If Tower is thin** (scripts around other people’s CRMs): this chain collapses to Chain A with extra storytelling.

### 8.5 Route 5 — Backend & Systems

**Chain A — Tower’s backend as production proof.** Strongest continuous chain on this route.

- **Titles:** Software Engineer, Backend Engineer, Software Developer (Wealthsimple-style Canadian product language).
- **Employer:** Canadian product companies with a real domain core (fintech, health, identity, vertical SaaS). Not FAANG new-grad, not bank campus.
- **Level:** mid / intermediate if the proof is real and the interview is passed. Honest FAANG mapping: L3/L4-equivalent, not L5. Smile “Intermediate Backend” asks 4+ years — you may still be under their number.
- Continuous with product-company backend. Conceptually similar, not continuous, with “Distributed Systems Engineer.” Not continuous with bank Java/Spring unless the stack or transfer is demonstrated.

**Chain B — freelance REST for SMBs.** Cash. Conceptually similar (API, Postgres, jobs). Not continuous with systems ownership. Junior to low-mid. Weak signal to Nue/Okta/Wealthsimple-class.

**Chain C — staff-aug on someone else’s product.** Continuous with FTE backend *at that company*, at the level they staffed you. Stronger collaboration signal than 1-person founder; weaker systems-ownership signal than Chain A unless you were given a bounded context.

**Not reachable:** Staff DS at FAANG; Principal; SRE-of-scale; “Platform Engineer” meaning Kubernetes platform; domain-senior seats that list 5+ years *in that domain* (e.g. Wealthsimple Cards).

### 8.6 Cross-route reachability after two years (implementation-shaped Plan B vs Tower-shaped Plan B)

| Plan C title | After generic indie glue / CMS / CRUD | After Tower (or equivalent) as a live system |
|---|---|---|
| Implementation Consultant | **Default yes** | Domain-continuous, product-not |
| Automation specialist (n8n/Zapier) | Continuous | Overkill / mis-aimed |
| Mid Cloud/DevOps at a product company | No / conceptual | **Yes, if you actually operated production** |
| Mid Cloud at a Canadian bank | No | Still conceptual (missing OSFI envelope) |
| Product / Full-Stack Engineer (startup, intermediate) | No from CMS; maybe from agency tickets | **Yes** (closest Route 2 fit) |
| Analytics Engineer / junior-mid DE | No from Zapier | **Yes if warehouse/state/tests exist** |
| Backend / Software Engineer (product, mid) | No from glue | **Yes if the core is real** |
| Pre-sales Solutions Engineer (named vendor) | Rare | Possible at a *vertical* SaaS if you deployed with customers |
| True FDE (Palantir / lab) | No | Maybe at a small company if coding interview passes; not Palantir-by-default |
| Staff / Principal / Director | No | No |
| Bank Lead / 6–10 year specialist | No | No |

**Retired claim.** “Plan B is 90% the Cloud job” / “80% the Solutions job” is false as a single number. Plan B is continuous with **mid IC product/cloud/backend/data seats outside banks** when the artifact is a live operated system. It is continuous with **Implementation Consultant** when the artifact is go-lives of other people’s software. It is conceptually similar, and usually insufficient, for regulated enterprise and for field-sales engineering. It is not a principal role in disguise.

---

## 9. Career optionality

The revision: *you are choosing a capability base from which the next decade branches.*

| Route | Branches that stay open if you own the *object* | What cages you | Requires leaving the route |
|---|---|---|---|
| **1** | SRE; platform-as-product; cloud/solutions architecture; cloud security/IAM; FinOps; principal production engineering; VP Infra (org track); MSP founder | TicketOps/MSP queue; YAML-only (RBC/Google SRE want a language); Kubernetes-as-religion; single-cloud ClickOps | Product engineering; client diagnosis as a primary craft (CNCF: platform value is *indirect*, users are internal developers) |
| **2** | Stay product engineer; frontend specialist; backend if the work went there; founding engineer; designer-engineer; later EM (a fork, not a ladder) | Agency CRUD; JS-framework fashion; CMS lock-in; founder-title inflation (“CTO of one”); PM drift (Route 6 was dropped for a reason) | Platform/SRE as mastery; bank leadership without the degree/org |
| **3** | Analytics engineering; data platform (later Spark/Kafka); durable workflow engines; reverse ETL / activation; backend if pipelines are services; founder of a data-shaped product | Zapier freelancer identity; vendor RPA; dashboard tinkerer; “automation engineer” as a marketing collision | ML Engineer / Data Scientist (different interview, worse degree mechanism); Staff data platform from glue |
| **4** | SE (real, mostly Plan C into a vendor); implementation (real, default); technical consulting (this *is* Plan B); SA/TA late and vendor-flavoured; SE Manager / Director of Solutions inside an org chart; founder/operator if productized | Salesforce / ServiceNow / Dynamics / MuleSoft cert pyramids (high income, high cage); HubSpot/Clio medium cage; “the tech is irrelevant” IC identity | Product engineering (SWE interview); platform/reliability (fantasy without a deliberate exit); Google CE (cloud years, not Zaps) |
| **5** | Staff backend / domain Architect; founding/small-company CTO; data platform if monitoring data is treated as a platform; later DS specialist at infra companies; bank/regulated backend *if* stack+domain filled | CRUD mill; language identity (“I am a Nest person”); interview-circuit specialist; premature distribution; taking a Linux “Systems Engineer” contract because the word matched | Client/org diagnosis as employed backend (Time Warp: almost no external client contact); Route 1 mastery |

**Optionality in language vs hiring practice.** Route 4 is the extreme case: the words (architect, engineer, solutions) attach to many jobs; the artifacts do not transfer without extra years or an interview the route did not train. Route 1 optionality is real and **conditional on escaping toil** (Google: you cannot make a career of grunge). Route 5 optionality is preserved by owning **invariants in a real domain**, not by collecting tools; the domain can change (immigration → money → identity) if the habit stays.

**Vendor-ecosystem question, answered.** Route 4 can narrow you into a vendor ecosystem; that is not hypothetical — it is the well-paid default. Route 1 single-cloud identity is recoverable if IaC + Linux + IAM ideas transferred; ClickOps is not. Route 3 Zapier/RPA is a cage. Route 2 CMS is a cage. Route 5 framework identity is a cage relative to GTA bank Java/Spring seats.

---

## 10. The Omcoda flywheel, route by route

Omcoda is not “I use AWS, therefore my infrastructure job helps the company.” The revision asked for a tighter test: does the independent loop and the company loop become the **same class of work**?

Omcoda’s constraints, restated from the site:

- Market gap, not client brief.
- Proprietary software, operated.
- Not for hire to build-to-spec.
- Immigration: eligibility monitoring + reactivation (Tower). Legal: pipeline visibility. Financial: connective tissue between compliance and engagement.
- Disciplines: solutions architecture, market development, managed operations.

| Route | Forward (craft → Omcoda) | Reverse (Omcoda → craft / Plan C) | Incentive compatibility |
|---|---|---|---|
| **1** | Uptime, deploys, IAM/tenant isolation, Canada-region residency, backups, cost. PIPEDA is a reason, not a vibe. | Legitimate evidence for product-company Cloud/DevOps (Chain A). Weak for banks. Strong for “founding infra hire.” 1-person ops is not an on-call rotation. | **Helpful dose, wrong as identity.** Premature EKS/service-mesh taxes the company and satisfies the route’s aesthetics. Platform work serves internal developers; Omcoda’s users are consultants and lawyers. |
| **2** | This is how Tower gets *made*: domain model, UX for professional users, tenancy, jobs (monitoring is time-based, not a CRUD form). | Operating Tower trains product-engineer interviews: “rules change; the system watches; here is the state machine; here is what broke at 2am.” | **Closest builder route, easiest betrayal.** The market wants the custom shop (Toronto project pricing). Brief → app → handoff is negative for Omcoda’s identity and weak for Product Engineer. |
| **3** | Tower *is* a monitoring + reactivation + pipeline product. Modeled eligibility state + durable activation is the object. CRM should be a destination, not the warehouse. | If internals are real: DE/AE/product-data artifacts (idempotency, backfill, reconciliation, schema evolution). If internals are Zaps: Plan C is wiped while the firm is funded. | **Real only if CRM is not treated as the system of record.** n8n can be the Act runtime; it should not be the Store or the Meaning. |
| **4** | Verbs match. Field time is how you see the gap (Palantir’s reason FDE exists). | Skills used by Omcoda; company shape anti-Omcoda if invoices are Clio/HubSpot/Zapier implementations. | **Steelman A (laboratory) vs B (trap).** Evidence leans **B for Plan B as the market currently pays; A only if Plan B is already founder-FDE of Tower.** Mixed books get pulled to custom because custom is easier to sell to a firm that already has a brief. Using Route 4 as a laboratory is a **discipline problem**, not a labour-market default. |
| **5** | A correct pathway data model *is* the product. Jobs are the clock. Reliability is the brand. Microservice premium is a cash cost in a 1-person firm. | The only realistic pre-degree way to own a **core** rather than a periphery. Longitudinal ownership is the missing piece of freelance APIs. | **Best studio for systems craft; over-engineering is the failure.** Modular monolith, relational source of truth, job runner. Interview translation of the restraint (“I chose not to distribute because X”) *is* systems judgement. |

**Flywheel diagram (causal, not motivational):**

```
diagnose a repeated gap across a class of firms
        → refuse the unique brief
        → encode the gap in a domain core (R5) with a product surface (R2)
        → keep eligibility state true and actionable (R3)
        → operate it with boring production excellence (R1)
        → deploy and learn in the field without becoming IT-for-hire (R4 as FDE-of-own-product)
        → artifacts that Plan C mid-IC seats can score
        ↛ bank Staff / Palantir-by-default / principal
        ↛ “we take briefs now, because cash”
```

**The tighter loop the revision hoped Route 4 might be** exists, but it is not “Solutions Engineer.” It is **founder-FDE of a vertical product**. That loop uses Route 4 skills and is destroyed by Route 4 incentives. Routes 2, 3, and 5 are the build/own side of the same loop. Route 1 keeps it trustworthy.

---

## 11. TSO fit and the question Route 4 had to survive

TSO = diagnose org bottlenecks, architect, write/integrate, automate, maintain live systems end-to-end.

**The full loop is a founder-operator week, not an employed route.** Every employed version amputates something:

| Employed shape | What it keeps | What it cuts |
|---|---|---|
| Platform / SRE (R1) | Live systems, architecture of infrastructure | Org/user diagnosis (users are internal developers) |
| Product engineer (R2) at Linear/PostHog-like | User loop, build, some support | If the company has separate SRE/CS, operations thins |
| Bank/product backend (R5) | Live core, diagnosis of *systems* | External client diagnosis (Time Warp: almost no paying-customer contact) |
| Pre-sales SE (R4) | Org conversation, architecture-as-narrative | Production ownership (disposable POCs; 56% sales) |
| Implementation consultant (R4) | Org conversation, go-live | Technical object stays the vendor; plateau is the base rate |
| True FDE (R4) | Both rooms, if it is Type-1 Builder | Thin in GTA; feeder is SWE first (45%); coding interview |
| Zapier/automation (R3/R4) | Org diagnosis, automate, some live care | Systems depth; Plan C engineering credit |

**The question the revision posed for Route 4:** *do you become a genuinely technical systems person who can operate with clients, or a client-facing implementation person whose technical depth plateaus?*

Evidence-shaped answer, still not a winner call: the labour market contains **both** attractors. **The base rate is the second.** True FDE and founder-operator-of-product are the first. Pre-sales SE is a third type (technical communicator). Two years is long enough to fall into the second and short enough that people will still *call* it the first.

Route 1’s symmetric tension, from the original table, also survives: independent-work proposition is strong because deliverables are concrete (CI/CD, migration, cost), and the centre of gravity is internal systems. That is a real tension with an architecture that cares about users, organizations, and value. Boring production excellence on Tower is the dose that does not require becoming a platform engineer at a bank.

---

## 12. Comparative architecture (not a scoreboard)

The revision asked to compare architectures, not intuitions, once the same evidence existed for all five.

### 12.1 What each route is *for*, if you take the object seriously

- **R1** is for owning how machines are allowed to change, fail, and cost. It multiplies other people’s shipping. It does not, by itself, decide what should exist.
- **R2** is for encoding a business in software people can use, and iterating while it is alive. Breadth is the advertised mastery; the real mastery is the domain model.
- **R3** is for making operational truth durable and actionable — not for drawing charts. Under one label sit a cash craft (low-code) and an engineering craft (warehouse/workflow). They do not share Plan C.
- **R4** is for making software real in someone else’s organization. That is either distribution for a product you own, or professional services. The market pays for the second.
- **R5** is for correctness of the core over years. It is the least package-shaped independent sale and the most employee-shaped deep work. For Omcoda, it is not optional: wrong eligibility state is not a UI bug.

### 12.2 Fit to the original TSO + Plan B + Plan C + Omcoda brief

This is an architecture map, not a ranking.

| Demand in the brief | Where it actually lives |
|---|---|
| Close clients before a degree | R4 glue, R3 workflows, R2 custom apps, R1 CI/landing-zone for *tech* buyers. Not R5 core-design as a package. Not bank cloud contracts. |
| Have that work count as engineering later | Only the Tower-shaped (or equivalent production) chains, plus agency/staff-aug that was already IC work. Glue/CMS/ClickOps count as *other* occupations. |
| Mastery as the asset | The objects in §4. Base-rate market objects fail this test on R4, R3-Zapier, R2-CMS, R1-TicketOps, R5-CRUD. |
| Omcoda as laboratory, not side quest | R2+R5+R3 build/own Tower. R1 keeps it saleable. R4 deploys it without taking briefs. Employed versions of any single route will pull hours *off* Tower unless the job *is* Tower. |
| B→C into Plan C roles at a real level | Mid product/cloud/backend/data IC outside banks, if artifacts are production. Implementation Consultant, if artifacts are go-lives. Not Staff. Not “I skip the degree and enter Principal.” |
| Decade optionality | Preserved by owning a portable object (control plane, domain core, eligibility state, product system). Destroyed by vendor identity, ticket identity, CMS identity, framework identity. |
| Not becoming a client-facing plateau | Requires production code you own, or true FDE. Route 4 employed default does not provide this. |

### 12.3 Contrasts that are now sharper than the Route 1 vs 4 table

The original table was: Cloud = stability/IaC/cost, internal, “optimize your pipeline”; Solutions = integration/business logic, high client contact, “automate your workflow”; risks = isolation vs non-technical AM.

Add:

- **Object:** control plane vs (usually) someone else’s vendor tenant. The Solutions object the revision hoped for — architecture of an organization’s workflows — is founder/FDE, not Implementation Consultant.
- **B→C:** Cloud Plan B is continuous to *product-company* mid cloud, conceptual to *banks*. Solutions Plan B is continuous to Implementation Consultant, conceptual to SE, not continuous to FDE/SWE unless the artifact is production software.
- **Omcoda:** Cloud helps as trust input and can steal years into internal-developer work. Solutions looks like the operator loop and is incentive-incompatible unless already productized.
- **Routes 2, 3, 5 are not spectators.** 2 is how the product exists. 5 is what the product *is*. 3 is whether eligibility is a modeled fact or a Zap. Dropping them from the first evidence gather made Route 4 look like the only operator-shaped craft. It isn’t.

### 12.4 A third architecture, now visible

Not “pick Route 4” or “pick Route 1.” A **TSO operating system** that uses the five routes as layers of one company:

1. **Choose the gap** (Omcoda market development — not a labour-market route).
2. **Own the core** (R5 object: invariants of eligibility/reactivation).
3. **Give it a product surface** (R2 object: domain model + UX for professional users).
4. **Keep operational truth** (R3 object: state, tests, activation).
5. **Keep it trustworthy to run on behalf of firms** (R1 object: IAM, restore, deploy, cost, residency).
6. **Put it in the field without selling uniqueness** (R4 object *restricted to* FDE-of-own-product).

Plan C is then a **translation of that laboratory**, not a separate identity. The translation is mid-IC in product companies, not a bank principal track, and not automatic.

This is still not a winner declaration among employment routes. It is the comparison of architectures the revision asked for.

---

## 13. Failure modes worth treating as design constraints

1. **Label collapse.** Calling yourself FDE, DevOps, Data Engineer, or Distributed Systems Engineer because the verbs overlap. Interviews and artifacts will not.
2. **Custom-shop gravity.** The fastest Plan B cash on Routes 2, 3, and 4 is the thing Omcoda refuses. Mixed invoices train clients to send briefs.
3. **Premature distribution / platform theatre.** Kafka, EKS, service mesh, “event backbone” as résumé lines in a 1-person firm. Fowler monolith-first and Shopify modular monolith are the counter-evidence. Hiring managers who can tell will treat it as a negative signal.
4. **Founder discount.** Recruiters code Omcoda as self-employed and under-count it versus a logo. Rewrite as engineering responsibilities, not as “CEO.” Hypothesis, but consistent with résumé-practice.
5. **TicketOps / implementation plateau / CRUD mill / Zapier identity.** Four names for the same trap: years pass, the object does not deepen, titles stay.
6. **Degree as magic.** It is a key at banks/gov/ATS and a DSA tutor. It does not create continuity where the object was wrong.
7. **GTA weather.** Very limited outlook. Pickiness goes up. “I automated workflows” is a crowded sentence.
8. **Ontario title law.** PEO restricts “Software Engineer.” Plan C titles that are quieter: Developer, Product Engineer, Backend Developer. Enforcement is uneven; banks and Big Tech still post Engineer.

---

## 14. What is not yet established

These are load-bearing for any later decision. They are not rhetorical.

1. **Tower’s current technical depth, tenant count, and whether it is already a live system or a prototype.** Chain D / Chain A on every route is theoretical until this is inspected. This pass did not read the codebase.
2. **Whether GTA immigration/legal firms will buy operated proprietary software** (Tower) rather than Clio + Zapier + a packaged implementation. Competitors exist (Lawmatics, SpaceLizit, Simplarity). Conversion, ACV, and sales-cycle length are not measured.
3. **Whether this subject can close enough independent work, pre-degree, to make contractor leverage real.** Rate cards exist; a personal pipeline does not.
4. **How Workday at RBC/TD actually treats an empty education field** for experienced hires in Canada. US skills-based-hiring studies are a proxy.
5. **Whether two years of 1-person production survives founder discount** in screening.
6. **GTA true-FDE hiring volume.** People exist in Toronto/Ottawa. A thick pipeline is not established. Remote US FDE is a work-authorization question, out of scope.
7. **Exact Tuesday mixes for this subject.** All percentage tables are composites.
8. **Longitudinal outcomes** of Zapier consultants who later became FDEs or DEs. Bloomberry’s feeder table does not list “no-code consultant.”
9. **Bank backend loops as “algorithm-medium, stack-hard.”** Widely asserted; no published rubric in the evidence files.
10. **“OS of the firm” as something employers hire.** It may only exist as founder language.
11. **Tax, IRAP, SR&ED, professional-corporation effects** on Plan B leverage in Ontario.
12. **The remaining comparison the protocol still owes:** a decision framework *after* Tower’s artifact is known. This pass compared architectures. It did not, and was told not to, pick a route.

---

## 15. What to do with this (research next, not a career pick)

The protocol’s original “next action” after locking the template was the first evidence gather (Routes 1 and 4). The revision’s next action was this pass.

What this pass unlocks, if the work continues:

1. **Inspect Tower as an artifact** against the 1-year tests in §4 (core, deploy, state, incident, users). That single inspection decides whether the continuous chains are available or still hypothetical.
2. **Keep a refusal log** on any client-facing work: invoice for operating Tower, or invoice for uniqueness? The flywheel is decided there, weekly.
3. **Rewrite Plan B as engineering evidence as it happens** (schema, incidents, SLOs, ADRs), not as a company narrative. Plan C will not do this translation for you.
4. **Treat interview theatre (DSA, system design) as a separate skill block** if Plan C includes product-company backend/SWE/FDE. Craft on Tower does not purchase that ticket.
5. **Do not use the 90/80 numbers again.** Replace them with the chain tables in §8.

---

## 16. Evidence index

Full sources, epistemic tags, and unabridged chains:

| File | Route |
|---|---|
| [evidence/route-1-cloud-infra.md](evidence/route-1-cloud-infra.md) | Cloud & Infrastructure |
| [evidence/route-2-software-product.md](evidence/route-2-software-product.md) | Software & Product Engineering |
| [evidence/route-3-data-automation.md](evidence/route-3-data-automation.md) | Data & Automation |
| [evidence/route-4-solutions-implementation.md](evidence/route-4-solutions-implementation.md) | Solutions & Implementation |
| [evidence/route-5-backend-systems.md](evidence/route-5-backend-systems.md) | Backend & Systems |

Primary context for the flywheel: [omcoda.com](https://www.omcoda.com/).

---

*End of deep pass. No route is eliminated. No route is selected.*
