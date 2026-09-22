# Route 2 — Software & Product Engineering (Full-Stack / App Building)

**Document type:** labour-market and craft evidence file.  
**Not:** a LifeWriting document, route ranking, or recommendation.  
**Subject (given, not independently researched):** Wale Omotayo, Greater Toronto Area, Canada. Building toward a Technical Systems Operator (TSO) archetype: diagnose org bottlenecks, architect technical solutions, write/integrate software, automate, maintain live systems end-to-end. Plan B is independent contractor/operator work that can close clients before a CS degree. Plan C is later full-time engineering where ~2 years of Plan B should count as real experience. CS degree is in play. Omcoda (omcoda.com) is a managed solutions provider for professional-services firms, not a custom software shop. Current product: Tower. Route 6 (Technical Product / Product Management) was dropped; this route is kept as **engineering (building products)**, not PM.

**Researched:** 2026-09-22.  
**Scope:** building complete end-to-end applications — frontend interfaces plus backend systems — as user-facing products. Stacks sampled: Next.js / React / TypeScript product engineering; Rails (37signals, Shopify, Toronto Rails shops); Django/Python SaaS backends. Markets sampled: GTA/Canadian hiring, Canadian banks/government, Big Tech, startups, Upwork/Toptal/agency freelance.

---

## Epistemic protocol

Every substantive claim is tagged:

- **[Evidence]** — stated by a primary or named secondary source; URL given.
- **[Inference]** — a conclusion that follows from cited evidence but is not itself measured.
- **[Hypothesis]** — plausible, decision-relevant, and not established by the sources in this file.

Secondary labour-market aggregators (rate cards, ATS-seo blogs, recruiter content mills) are used only as market *texture* and are flagged as weak. Vendor blogs selling development services are not treated as wage surveys.

**This file does not declare a winner among routes.**

---

## Route characterization (what this is / is not)

**[Inference]** This route is the craft of shipping a working application that a user can log into, use, and depend on: data model, API, UI, auth, deployment, and iteration. It is distinct from:

- **frontend-only / design-engineer** (UI system without owning persistence and operations);
- **backend-only / platform** (services without owning the user-facing product loop);
- **product management** (deciding the roadmap without writing the system);
- **custom software shop / agency delivery** (building to a client brief and handing off);
- **SRE / TSO-as-operator** (running live systems as the primary job, even if this route *touches* operations).

**[Evidence]** Product-company definitions treat this as “full-stack code + user outcome,” not “tickets in one layer.” PostHog: a product engineer “builds products for real users, writes full stack code,” talks to users, owns product decisions, and does support. (https://posthog.com/product-engineer/what-is-a-product-engineer) Linear’s Senior/Staff Product Engineer posting asks for 5+ years building customer-facing products, React/TypeScript plus Node/GraphQL/PostgreSQL, “end-to-end features (not just incremental improvements),” and comfort “working without heavy PM overhead.” (https://linear.app/careers/12f8f208-0b9c-4569-bb3d-41c8a197029e) Gergely Orosz’s “product-minded engineer” is an engineer who stays an engineer: “someone who would likely make a good product manager if they ever decide to give up the joy of engineering.” (https://blog.pragmaticengineer.com/the-product-minded-engineer/)

**[Inference]** The labour market uses overlapping titles for this craft: Full-Stack Engineer/Developer, Product Engineer, Software Engineer (product team), Founding Engineer. Those titles are **not** interchangeable at screening time. “Product Engineer” clusters at product startups (Linear, PostHog, Faire, Notion-style postings). Canadian banks still post “Full Stack Developer / Software Engineer” with Java/.NET stacks. Shopify’s IC title is “Developer,” not “Engineer.” (https://shopify.engineering/what-being-a-staff-developer-means-at-shopify)

---

## 1. Actual work composition

### 1.1 What a Tuesday is made of (employee product/full-stack)

There is **no** high-quality time-use study of “full-stack product engineers” as a distinct occupation. The ranges below are **synthesized** from calendar studies of software engineers, self-report of maintenance vs new work, and role definitions at product companies. They are **not** a time-and-motion study of this craft.

**Clockwise calendar data (ICs, mixed software engineering, 2021–2022):** **[Evidence]** 80,000 developers / 5,000 companies / 1.5 million meetings. Average IC software engineer: **10.9 hours/week in meetings** (~27% of a 40-hour week); **19.6 hours of “focus” time** (blocks of ≥2 hours); **6.3 hours fragmented**. Large-company ICs: 12.2 meeting hours and 16.9 focus hours; small-company ICs: 9.7 meeting hours and 22.5 focus hours. Tuesdays have the least focus time: **80% of standups are scheduled Tuesday**. Engineering managers: 17.9 meeting hours, 10.4 focus hours. (https://www.computerworld.com/article/1612747/for-developers-too-many-meetings-too-little-focus-time.html)

**Stripe / Harris Poll “Developer Coefficient” (2018, 1,000+ developers + 1,000+ executives, 5 countries):** **[Evidence]** Mean work week 41.1 hours. Developers spend **17.3 hours/week** on maintenance issues (debugging, refactoring, modifying, “bad code”) — about **42%** of the week — of which ~13.5 hours is framed as technical debt and ~3.8 hours as fixing bad code. About **13.5 hours** remain for new feature development in Stripe’s accounting. (https://stripe.com/files/reports/the-developer-coefficient.pdf; summary: https://adtmag.com/articles/2018/09/10/developer-survey.aspx)

**Caveats on those two studies:** **[Inference]** Clockwise measures *calendar shape*, not task type — “focus time” is coding + debugging + design + reading. Stripe is self-report, 2018, enterprise-skewed, and treats maintenance as “lost” productivity, which product companies would partly call “operating the product.” Neither study isolates full-stack product work from backend platform work.

**Stack Overflow 2024 professional-developer module:** **[Evidence]** 61% of respondents spend **more than 30 minutes/day searching for answers**; people managers spend more time *answering* questions (61% >30 min/day). (https://survey.stackoverflow.co/2024/professional-developers/) **[Evidence]** 2025 survey: 45% say debugging AI-generated code is more time-consuming; 66% cite “AI solutions that are almost right” as a top frustration. (https://survey.stackoverflow.co/2025/) This is interrupt cost, not a Tuesday split.

**Product-engineer role texts imply a different mix than “ticket full-stack.”** **[Evidence]** PostHog product engineers “talk to users… decide what to build… own pricing, revenue, and user experience… support customers directly.” (https://posthog.com/product-engineer/what-is-a-product-engineer) Orosz: they consider work done only after user-behaviour and business metrics, not at merge. (https://blog.pragmaticengineer.com/the-product-minded-engineer/) Linear: shape the problem, not just implement. (https://linear.app/careers/12f8f208-0b9c-4569-bb3d-41c8a197029e) Faire Toronto Product Engineer: “planning and building features end-to-end, working alongside product, design, and data”; “deciding what problems are worth solving.” 2+ years; bachelor’s in CS/SE **or equivalent industry experience**. (https://jobera.com/job/faire-product-engineer-brand-fullstack-backend-or-frontend-e808b1c4/)

**37signals / Basecamp as the small-product extreme:** **[Evidence]** “teams of two, one designer, one programmer; and we ship projects in 6 weeks or less. Working full stack… is crucial.” (https://dev.37signals.com/building-basecamp-project-stacks-with-hotwire/) A Principal Programmer describes 18 years on product, with the Basecamp domain model (`Recording` / delegated types) as the architectural object. (https://dev.37signals.com/the-rails-delegated-type-pattern/) **[Inference]** In that culture, “docs/PM” is mostly writing and shaping, not Jira administration; “client/user interaction” is support and use of their own products; meeting load is structurally lower than Clockwise’s large-company mean.

#### Tuesday % ranges — employed full-stack / product engineer

These are **[Inference]** ranges for a *typical Tuesday at a product company*, combining Clockwise (meetings/focus), Stripe (maintenance vs new), and product-engineer role definitions. They are **not** measured. Two sub-modes:

| Activity (employee) | Small product co. / startup IC | Large co. / bank product team | Notes |
|---|---:|---:|---|
| **Code / build (new behaviour)** | 30–45% | 20–35% | Stripe ~13.5h/41.1h ≈ 33% “new”; Clockwise focus time is the envelope. |
| **Architecture / design** | 8–15% | 5–12% | Higher at senior+; juniors inherit. 37signals: domain modelling *is* the work. |
| **Debugging / maintenance / incidents** | 20–35% | 25–40% | Stripe 42% maintenance is an upper bound if you count all non-new work. |
| **Client / user interaction** | 8–20% | 3–10% | Product-engineer cultures (PostHog support, user research) vs bank teams behind a BA/PM. |
| **Docs / PM / meetings / Slack** | 15–30% | 25–40% | Clockwise 27% meetings at IC mean; 30% at large cos; Tuesday is the worst day. |

**[Hypothesis]** A “Product Engineer” at Linear/PostHog/Faire spends more Tuesday time on user/metrics/design tradeoffs than a “Full Stack Developer” on a bank squad, even if both write React + an API. Title is a weak predictor; **team shape** (PM-heavy vs engineer-shaped) is the stronger one.

**What it feels like (employee):** **[Inference]** Long stretches of incomplete work. A feature is not done at PR merge (Orosz). Production is a character in the story (Stripe maintenance hours). At large firms the day is chopped; Clockwise’s “fragmented time” is the felt experience of never quite starting. At small product firms the day is closer to maker’s hours, but the engineer is also the PM, the support queue, and the designer’s pair (PostHog, 37signals, Linear).

### 1.2 Freelance / independent app builder

**[Evidence]** Practitioner accounts consistently describe freelancing as a **multi-role job**, not “the same coding job without a boss.” DEV Community (2025): freelancer is developer + salesperson + negotiator + project manager + support engineer + accountant; stress is income uncertainty, not sprint deadlines. (https://dev.to/raajaryan/freelancing-vs-job-vs-startup-my-honest-developer-perspective-35f8) What’s My Pivot (2026): freelancing requires positioning, sales, and turning vague business problems into scoped work. (https://whatsmypivot.com/blog/software-engineer-to-freelance-developer-transition-guide-2026)

**[Evidence]** Toptal’s own funnel is a **multi-week professional screen**, not a portfolio upload: language/personality → skill review → live screen → 1–3 week test project → continued excellence; **typically fewer than 3% accepted**; stage pass rates published as 26.4% → 7.4% → 3.6% → 3.2% → 3%. Full process 3–8 weeks. (https://www.toptal.com/top-3-percent) **[Inference]** Getting onto Toptal is itself a job, with interview-like labour, before any client Tuesday exists.

**[Evidence]** Canadian freelance full-stack *rate cards* (weak, aggregator): Freel.ca 2026 — junior CA$45–70/hr, mid CA$70–125, senior CA$125–195. (https://freel.ca/rates/full-stack-developer-freelance-rates-canada) Index.dev 2026 — Canada average US$85–100/hr; platform vs direct-hire gap **20–30%**. (https://www.index.dev/blog/freelance-developer-rates) Toronto custom-shop vs freelancer tables (vendor blogs, treat as texture not measurement): junior freelancer ~CA$45–70; senior ~CA$125–190; boutique agency ~CA$160–275. (https://www.essentialdesigns.net/news/custom-software-agency-vs-freelancers-toronto) Project bands for a complete app: vendor blogs cluster MVP ~CA$30k–80k, production ~CA$80k–300k. (https://byteager.ca/blog/how-much-custom-software-development-cost-toronto-2026)

**[Inference]** Rate cards do not describe Tuesday composition. A freelancer at 50% utilisation doing sales and revisions has a different day than a Toptal contractor embedded 40 hours on one product team.

#### Tuesday % ranges — freelance app builder

**[Hypothesis]** No calendar study of freelance full-stack exists in this file. The following is a reasoned range for a **solo GTA freelancer who must both sell and deliver**, early-to-mid Plan B, not a fully booked Toptal contractor.

| Activity (freelance app builder) | Lean pipeline / hunting | Fully booked (Toptal/agency-style) |
|---|---:|---:|
| **Code / build** | 20–40% | 45–65% |
| **Architecture** | 5–15% | 8–15% |
| **Debugging / revisions / “can you just…”** | 15–25% | 15–25% |
| **Client / user interaction (calls, WhatsApp, scope)** | 15–30% | 10–20% |
| **Docs / PM / proposals / invoices / sales** | 20–40% | 8–15% |

**What it feels like (freelance):** **[Inference]** The product is rarely *your* product. The client is in the room. Scope is the adversary. The emotional texture is “close the next invoice” rather than “ship the next experiment.” WordPress/Shopify gigs feel like configuration and theme surgery; custom-app gigs feel like compressed product engineering without the afterlife of operations (unless a retainer exists).

**[Evidence]** Agency vs product contrast is widely attested, quality mixed: agency weeks jump stacks and clients; product weeks marry one codebase. (Representative: https://theremotespot.com/remote-web-development-jobs-agency-vs-product/ ; https://richbray.medium.com/should-you-work-at-a-product-company-or-an-agency-as-a-developer-92cc3ee51e90) **[Inference]** A Toronto agency full-stack contractor’s Tuesday is closer to the **employee** table (standups, tickets, code review) than to the solo-hunter freelance table — but the *object* of work resets every client.

### 1.3 Independent operator-founder (Omcoda / Tower-shaped)

**[Inference]** A 1-person company that both **builds** and **operates** a product (Omcoda’s stated model) has a Tuesday that is not “full-stack job + side hustle.” It is product engineering *plus* sales, onboarding, monitoring, and iteration for live firms. No empirical time-use study of this specific shape was found.

**[Hypothesis]** For a ~1-person managed-solutions operator with one live product:

| Activity | Range | Why |
|---|---:|---|
| Code / build | 20–40% | New surfaces on Tower; integrations. |
| Architecture / domain modelling | 10–20% | The product *is* a model of immigration/legal workflow. |
| Debugging / live-system care | 15–30% | Operator, not hand-off. |
| Client / user interaction | 15–30% | Firms are customers; managed ops is the offer. |
| Docs / PM / GTM / admin | 15–30% | Market development is an explicit Omcoda discipline. |

This is the Tuesday closest to **TSO + product engineering superimposed**, and the furthest from “Upwork WordPress Tuesday.”

### 1.4 Labour-market weather around the job (not composition, but it changes how the job feels)

**[Evidence]** Ontario / Toronto Job Bank outlook **2025–2027** for software engineers and designers (NOC 21231): **Very limited** — employment decline plus few retirements. Toronto region ~43,880 people in the occupation; 61% in professional/scientific/technical services, 12% in finance/insurance/real estate. Median Toronto wage **$56.49/hour** (LFS 2023–2024). Educational attainment in Ontario: **52% bachelor’s, 32% above bachelor’s** (84% university-level). Self-employed: **9%** vs 15% all occupations. (https://services.labour.gov.on.ca/labourmarket-ui/jobProfile?nocCode=21231 ; wages: https://www.jobbank.gc.ca/wagereport/occupation/5485)

**[Evidence]** Same Toronto outlook table: software developers and programmers (NOC 21232) **Very limited**; web developers and programmers (NOC 21234) **Very limited**; web designers (21233) **Limited**. Computer systems developers and programmers (21230) **Moderate**. (https://www.jobbank.gc.ca/outlookreport/location/geo9219)

**[Inference]** Plan C full-time product/full-stack hiring in the GTA is not a shortage market in 2025–2027 official outlook. That does not freeze Plan B (self-employment and contracting sit partly outside vacancy stats), but it **raises the bar** on what “2 years of Plan B counts as experience” must look like, because employers can be picky.

**[Evidence]** Google GTA SWE median TC (Levels.fyi, updated 2026-08-30): L3 CA$169,754; L4 CA$248,096; L5 (Senior) CA$325,043; L6 CA$392,817; L7 CA$607,655. (https://www.levels.fyi/companies/google/salaries/software-engineer/locations/greater-toronto-area) Faire Toronto Staff Product Engineer base **CA$190,500–$262,000** plus equity (Sept 2026 posting). (https://jobera.com/job/faire-staff-product-engineer-brand-db98c1ed/) Flexgen GTA Senior Full-Stack (Next.js/React/TS/Prisma/Mongo): **CA$125k–$155k**, 10+ years asked. (https://flexgen.zya.me/job/senior-full-stack-engineer-31)

---

## 2. Independence → organizational leverage

Three vehicles, not one career.

### 2.1 Employee

**[Evidence]** Ladders exist and fork after Senior. GitLab: Intern → Associate → Intermediate → Senior → Staff → Senior Staff, with **Fullstack / Frontend / Backend** families; Senior is explicitly a **destination role**; Staff or EM requires **company need**, not tenure. Staff IC and EM are equivalent in base compensation and prestige. Principal Engineer is the IC equivalent of a Senior Engineering Manager, operating across several teams / a sub-department. (https://handbook.gitlab.com/handbook/engineering/careers/ ; https://handbook.gitlab.com/job-description-library/engineering/engineering-management/) Shopify: Staff is “an entirely new role,” not a more-senior Senior; leadership via technical excellence, manager partnership, business alignment, mentorship; years-in-seat without diverse projects does not produce Staff. (https://shopify.engineering/what-being-a-staff-developer-means-at-shopify) Will Larson’s Staff-plus archetypes: Tech Lead, Architect, Solver, Right Hand. (https://staffeng.com/guides/staff-archetypes/)

**[Inference]** Organizational leverage as an employee is **scope of system + people influenced**, not hours billed. The product engineer who stays on one squad writing features can plateau at Senior forever (GitLab says this is fine and intended). Leverage beyond that is architectural and organizational, which is a *different job* (Shopify, Larson).

**[Evidence]** Ontario title law is a real friction. PEO: software developers “are not permitted to use the title ‘Software Engineer’”; PEO treats unlicensed use as misleading. (https://www.peo.on.ca/public-protection/complaints-and-illegal-practice/unlicensed-practice-enforcement-faq) Engineers Canada: in most provinces the title “engineer” is restricted; Alberta created a 2023 exception for “software engineer.” (https://engineerscanada.ca/become-an-engineer/use-of-professional-title-and-designations) **[Inference]** GTA employers still post “Software Engineer” constantly; enforcement is uneven. Shopify’s “Developer” language is one corporate adaptation. For Plan C, “Full-Stack Developer / Product Engineer / Software Developer” are the legally quieter titles in Ontario; “Software Engineer” is the Big Tech/bank import.

### 2.2 Contractor

**[Evidence]** Toptal/Upwork/agency markets will **sell you as a complete-app builder**. Toptal: scoped senior work, US$60–200+/hr, most senior full-stack ~US$90–150. (https://www.toptal.com/top-3-percent ; market commentary https://cadence.withremote.ai/blog/toptal-vs-upwork) Upwork: open marketplace, wide band US$15–150+, Project Catalog packages common deliverables (logo, Shopify theme, landing page) at fixed prices. (same) Toronto agencies sell **complete custom applications** as projects in the CA$30k–300k+ bands. (https://byteager.ca/blog/how-much-custom-software-development-cost-toronto-2026)

**[Inference]** Yes, you can sell complete apps as projects. That is the **default commercial expression** of this route in Plan B. It is also the model Omcoda’s website refuses.

**[Evidence]** Founding-engineer vs contractor is a documented distinction on the buy side: contractor optimizes task completion and hours; founding engineer owns the whole problem (DB Monday, API Tuesday, UI Wednesday, CI Thursday, customer Friday) with equity alignment. (https://hypernestlabs.com/insights/founding-engineer-vs-contractor) **[Inference]** Plan B contractor work trains **delivery under a brief**. Plan B founding-engineer / operator work trains **ownership of a live product**. Employers later can tell the difference if they look; many recruiters will not look past the word “freelance.”

### 2.3 Independent operator-founder

**[Evidence]** Omcoda’s public position (primary): “We are not a custom software shop. We do not take briefs, build to spec, and hand off.” “We are a managed solutions provider. We identify gaps… build proprietary software… and operate that software on behalf of the firms that need it.” Disciplines named: solutions architecture, market development, managed operations. “We are not for hire — we bring the solution. If you need something built to your spec, we are not the right fit.” (https://omcoda.com)

**[Inference]** The independent-operator vehicle for *this route* is: own the codebase, own the runtime, sell **access to an operated product**, not a project. Leverage is **one system × N firms**, not **one engineer × N briefs**.

**Tension (custom app shop vs proprietary product):**

| | Custom app shop / freelance projects | Proprietary operated product (Omcoda) |
|---|---|---|
| Unit of sale | A build | An outcome + a running system |
| Who owns the software | Usually the client | The operator |
| After launch | Handoff, maybe a retainer | Managed operations |
| What compounds | Reputation, maybe a component library | Domain model, data, playbooks, the product |
| Plan B cash | Faster to first invoice | Slower; needs a real gap and a live system |
| Plan C résumé read | “I built many apps for clients” | “I built and ran a SaaS in X domain” |

**[Inference]** This route *can* fund Plan B either way. Only the right-hand column is compatible with Omcoda’s stated identity. The left-hand column is the path of least resistance in Upwork/agency markets and is the **gravity well** of Route 2.

**[Hypothesis]** A 1-person founder can sell a few custom apps to pay rent without becoming “a custom shop” as a *company identity* if those apps are treated as research for the proprietary product — but clients will not experience the difference, and the Tuesday mix will drift toward briefs. The flywheel (Section 7) is the test.

---

## 3. Degree mechanisms (three, separately)

CS/SE degree is not one thing. Split:

1. **Formal eligibility** — can you apply / be appointed.
2. **ATS / screening advantage** — do you get seen.
3. **Organizational progression** — does it matter for Senior → Staff/Principal → Director.

Across four employer types.

### 3.1 Formal eligibility

#### Startups / product companies

**[Evidence]** Faire Toronto Product Engineer (and Staff PE): “A bachelor's degree in Computer Science/Software Engineering **or equivalent industry experience**.” 2+ years (mid) / 5+ years (staff). (https://jobera.com/job/faire-product-engineer-brand-fullstack-backend-or-frontend-e808b1c4/ ; https://jobera.com/job/faire-staff-product-engineer-brand-db98c1ed/) Linear Senior/Staff PE: **5+ years** building customer-facing products; **no degree line** in the posting fetched. (https://linear.app/careers/12f8f208-0b9c-4569-bb3d-41c8a197029e) PostHog handbook: you can “wake up tomorrow and decide to be” a product engineer; no credential gate in the definition. (https://posthog.com/product-engineer/what-is-a-product-engineer)

**[Inference]** For this route at product startups, a CS degree is **rarely a hard eligibility bar** once 2+ years of shipped product exist. It is often written as “or equivalent.” Early-career (0–2 years, no production) is different: startups still hire without degrees, but they hire on **proof of shipped work**, which is exactly Plan B’s job.

#### Big Tech

**[Evidence]** Google “Software Engineer, Early Career, Campus” minimum qualifications: “Bachelor's degree in Computer Science, a similar technical field of study, **or equivalent practical experience**.” Preferred: Master’s in CS. The role is campus-shaped (data structures/algorithms via coursework/projects/internships). (https://www.google.com/about/careers/applications/jobs/results/78703249065943750-software-engineer-early-career-campus) **[Evidence]** Burning Glass / news summary of Sergey Brin (2025–26): Google job postings requiring a college degree fell from **93% (2017) to 77% (2022)**; Brin: Google has “hired tons of people who don’t have bachelor’s degrees.” (https://timesofindia.indiatimes.com/education/careers/news/google-has-hired-tons-of-people-without-college-degrees-says-sergey-brin-heres-why/articleshow/126505460.cms)

**[Inference]** Formal eligibility at Google-class SWE is **degree OR equivalent practical experience**. Campus *programs* still behave like degree pipelines. Equivalent experience is real but must survive a DS&A interview loop, which a CS degree cheaply prepares for and a WordPress freelance year does not.

**[Hypothesis]** Two years of Plan B building Tower would more easily satisfy “equivalent practical experience” for a **product-adjacent / full-stack** posting than for a Google early-career campus posting, which is still algorithmically gated.

#### Canadian banks / large financials

**[Evidence]** Student/co-op path is **enrollment-gated**. RBC Borealis Software Developer co-op: “Currently enrolled at a Canadian post-secondary institution with a focus on computer science, engineering, or technology”; transcripts required; roles include Full Stack / Back End / Front End. (https://rbc.wd3.myworkdayjobs.com/en-US/RBCEARLYTALENT1/job/RBC-WATERPARK-PLACE-88-QUEENS-QUAY-WTORONTO/XMLNAME-2027-Winter-Student-Opportunities-RBC-Borealis---Software-Developer--4-8-Months_R-0000184501-1) TD Software Engineer Co-op/Intern Winter 2027: “Must be enrolled in an undergraduate/graduate degree (requirement of all co-op/intern positions).” (https://www.themuse.com/jobs/tdbank/software-engineer-coop-intern-winter-2027) Scotiabank GBM Trade Floor Technology Consultant (Full Stack Developer) internship: student internship frame. (https://jobsca.org/finance_toronto-c117072/2026-09-scotiabank_i4202901367)

**[Evidence]** Experienced-hire examples are mixed and often **degree-as-usual rather than degree-as-law**. Scotiabank Fullstack Software Engineer Specialist (ScotiaTech Bogotá, supporting Canada): “University or College degree in Computer Science, Engineering or related tech field” plus 3+ years; Java/Spring/microservices/DB2. (https://jobs.scotiabank.com/job/Bogota-Fullstack-software-engineer-specialist-DC/601320817/) RBC Lead Full Stack Developer (Toronto, posted 2026-08-27): **10+ years** C#/.NET/Azure; the fetched posting emphasizes experience and Azure certs, not a degree sentence in the snippet. (https://rbc.wd3.myworkdayjobs.com/en-US/RBCGLOBAL1/job/TORONTO-Ontario-Canada/Lead-Full-Stack-Developer_R-0000163643-1)

**[Evidence]** Official occupational description (NOC 21231, Ontario): “A bachelor's degree, usually in computer science, computer systems engineering, software engineering or mathematics **or completion of a college program in computer science is usually required**.” P.Eng. licensing is required to *practise as a Professional Engineer* and to stamp drawings — not to write bank Java. Experience as a computer programmer is “usually required.” (https://services.labour.gov.on.ca/labourmarket-ui/jobProfile?nocCode=21231) NOC 21232 (developers/programmers): bachelor’s **or college program**; “Progression to software engineer is possible with experience.” Occupation “not regulated in Canada” per Job Bank. (https://www.jobbank.gc.ca/marketreport/requirements/22532/ca)

**[Inference]** Banks’ **co-op/new-grad** doors are formally closed without enrollment. Experienced-hire doors are formally “usually a degree” (NOC + many postings) with a live practice of hiring degree-holders. A hard “no degree, no apply” rule is **not proven** for all experienced TD/RBC full-stack seats; it is **proven** for their student programs.

#### Canadian government

**[Evidence]** Treasury Board qualification standard for the **IT group** (core public administration): minimum is **graduation from a two-year program** of study from a recognized post-secondary institution with specialization in CS, IT, IM, or another specialty relevant to the position — **not** necessarily a bachelor’s. Managers **may** accept “an acceptable combination of education, training and/or experience” as an alternative, but **are not obliged to**, and when they do it applies **to that position only**. (https://www.canada.ca/en/treasury-board-secretariat/services/staffing/qualification-standards/core.html ; FAQ: https://www.canada.ca/en/treasury-board-secretariat/services/staffing/qualification-standards/frequently-asked-questions-qualification-standards.html) Live posting example: IT Analyst, Software Solutions (Programmer) repeats that standard plus 2 years programming in named languages; school classes do not count as the experience. (https://emploisfp-psjobs.cfp-psc.gc.ca/psrs-srfp/applicant/page1800?poster=1862552)

**[Inference]** Federal IT eligibility is a **two-year credential by default**, with a discretionary experience alternative that must be *written into that competition*. A CS bachelor’s exceeds the minimum. Zero post-secondary + 2 years of GitHub is **not** reliably eligible unless a manager explicitly opens the alternative — and that alternative does not port to the next posting.

#### Freelance / Toptal / agencies

**[Evidence]** Toptal screens language, skill, live exercises, test project — not degrees. (https://www.toptal.com/top-3-percent) Upwork is open registration. **[Inference]** Formal eligibility for Plan B selling is **none**. Clients buy risk reduction (Toptal badge, reviews, a live demo), not a diploma.

### 3.2 ATS / screening advantage

**[Evidence]** Rejectless analysis of 1,000 SWE postings (claimed 2025): “BS/MS in CS or related field” appears in **62%** of postings; **89% of those** include “or equivalent experience.” Authors claim only **4%** explicitly require a CS degree with no alternative, and that 73% of sampled companies’ recruiters said they don’t hard-filter on it. **Treat as directional, not a census** — methodology is a commercial blog. (https://www.rejectless.app/guides/parsed-1000-swe-job-postings-what-ats-actually-looks-for)

**[Evidence]** Classet: a degree is an easy binary for ATS knockout filters; “skills-based hiring” on the job post often does not change resume screening. (https://www.classet.ai/blog/skills-based-hiring-screening) ATS research notes (Workday/Taleo-style): qualification match scores include **minimum education level** as a knockout alongside years and required skills. (https://github.com/sunnypatell/ats-screener/blob/main/research/ats-parsing-scoring-research.md)

**[Evidence]** Blind thread (anecdotal, experienced non-degree SWE): after ~2 YOE, “industry experience is all that matters” except companies that set degree as a hard Workday question that auto-rejects; some Microsoft roles asked “do you have a bachelor’s degree” as a minimum with no equivalent. (https://www.teamblind.com/post/entering-software-engineer-job-market-with-no-degree-dyc3kx5t)

**[Inference] by employer type:**

| Employer type | Screening effect of a CS/SE bachelor’s |
|---|---|
| **Startups (Greenhouse/Ashby, small volume)** | Weak. Humans read. Shipped product and a trial (Linear work trial; Notion paid trial) dominate. Degree is a nice-to-have keyword. |
| **Big Tech** | Medium for **campus/L3**. Recruiter search and university targeting still happen even when the posting says “or equivalent.” Medium-low after a credible 2–4 years + interview performance. High if the candidate cannot pass DS&A — the degree’s hidden value is **interview prep**, not the PDF. |
| **Canadian banks / insurers** | **High.** Workday, transcripts culture (even for co-ops), regulated-employer HR. “Bachelor’s in CS” is a cheap filter when 200 applicants exist. “Equivalent experience” is often *policy language*, not *search practice*. |
| **Federal / provincial IT** | **High as eligibility**, then screening on the essential education box. If the poster did not include the experience-alternative note, the degree/diploma **is** the screen. |
| **Freelance** | Near zero. Toptal is a skill gauntlet. Upwork is reviews and proposals. |

**[Inference]** For Wale, a CS degree’s screening value is **front-loaded on Plan C banks/gov/Big Tech new-grad-ish funnels** and **weak on Plan B**. After 2 years of *ambiguous* freelance, the degree may still be the thing that gets a Workday résumé past a knockout. After 2 years of a **named, live, domain-specific SaaS with users**, the degree’s screening value falls at startups and remains at banks.

**[Hypothesis]** GTA bank ATS configs for experienced “Full Stack Developer” still use education as a soft filter even when not a knockout. This file does not have an internal Workday screenshot; do not treat as fact.

### 3.3 Organizational progression (Senior → Principal / Director)

**[Evidence]** GitLab: progression **beyond Senior is gated on availability and need**. Staff/Principal are leadership jobs (org-level technical strategy), not “more code.” (https://handbook.gitlab.com/handbook/engineering/careers/) Shopify Staff: quality and diversity of projects, not years; “you could work 10 years supporting the same product, making the same changes, and be no closer.” (https://shopify.engineering/what-being-a-staff-developer-means-at-shopify) Larson: Staff-plus is archetype × organizational recognition. (https://staffeng.com/guides/staff-archetypes/) LeadDev: Principal is organization-wide technical direction; Distinguished ≈ director-level IC. (https://leaddev.com/career-development/who-are-staff-principal-and-distinguished-engineers)

**[Evidence]** Ontario educational attainment in NOC 21231: **84% bachelor’s or above** (52% + 32%). (https://services.labour.gov.on.ca/labourmarket-ui/jobProfile?nocCode=21231) **[Inference]** That is not a promotion rule; it is the **population** from which Principal/Director seats are drawn. HR cultures that already used degree as entry signal rarely drop it at Director.

**[Inference] by employer type:**

| Employer type | Degree effect on Senior → Principal/Director |
|---|---|
| **Startups** | **Low for IC Staff/Principal** if the person has been the technical spine of a shipped product. **Medium for Director/VP** at the point investors/boards want a “proper exec” — still more about scale of org than diploma. A 1-person founder does not automatically become Principal upon joining; scope must map (GitLab/Shopify). |
| **Big Tech** | **Low-medium.** Promo packets are impact, level guidelines, and calibration. Degree is almost invisible by L5+. **Exception:** some research/Principal tracks still prefer advanced degrees; that is not this route’s centre. |
| **Canadian banks / gov** | **Medium-high for Director+.** Large-org leadership jobs inherit corporate credential norms, bilingual/security profiles, and “executive potential” language. A missing bachelor’s is a *discussable exception* at IC Senior; it is a *committee problem* at Director. Gov EX-equivalent and bank people-leader roles are not known for celebrating self-taught founders. |
| **Freelance** | N/A. There is no Principal. Toptal “senior” is a rate, not a ladder. |

**[Inference]** The degree’s **progression** value is therefore the opposite shape of its **Plan B** value: nearly useless for closing freelance clients; most useful if Plan C is **bank/gov leadership over a 15-year horizon**; least useful if Plan C is **Staff Product Engineer at a product company** on the back of a real system.

**[Hypothesis]** A part-time Canadian CS degree earned *while* operating Tower would maximize mechanism (2) for banks without delaying mechanism-free Plan B. That trade against Omcoda operating time is not measured here.

---

## 4. Deepest technical object owned

Core question: what does this route eventually let you **own**, as mastery rather than as a slide title?

### 4.1 Surface vs mastery

| Horizon | Surface object (what you point at) | Mastery object (what you actually hold) |
|---|---|---|
| **1 year** | “An app.” Repo, UI, deploy. | A **thin vertical slice**: one user journey that persists data, authenticates, and stays up. You own **glue**, not a domain. |
| **3 years** | “The product” / “the codebase.” | A **domain model** that survives feature churn — entities, invariants, permissions, state machines — plus a **UX grammar** consistent enough that new screens are instances, not inventions. 37signals’ `Recording` is the canonical example of this depth. (https://dev.37signals.com/vanilla-rails-is-plenty/) |
| **5 years** | “The platform our product runs on.” | A **product-system**: multi-tenant boundaries, observability, failure modes, data integrity, performance budget, and the operational loop that keeps the product true. You own **how the business is encoded in software**. |
| **Principal / Staff-plus** | “Technical strategy.” | **A durable product architecture that other engineers can extend without you in every PR**, plus the political skill to keep it aligned with the business (Shopify Staff “alignment with business objectives”; Larson Architect archetype). The object is no longer screens. It is **the constraint system**. |

**[Evidence]** 37signals: they do not split “application” vs “domain” layers; they have domain models (Active Records and POROs) invoked from controllers/jobs. Basecamp 4 on a ~9-year-old Basecamp 3 codebase: ~400 controllers, ~500 models, millions of users. Delegated types (`Recording` / recordables) are “the architecture on which it’s built.” (https://dev.37signals.com/vanilla-rails-is-plenty/ ; https://dev.37signals.com/the-rails-delegated-type-pattern/) **[Inference]** The deepest object in mature product engineering is **the domain model of the product**, not React, not “the UX system,” and not “the codebase” as a pile of files.

**[Evidence]** Linear’s stack list is a reveal of what they consider the real objects: realtime sync framework, GraphQL API, Temporal agentic workloads, Postgres, k8s — *and* “beautiful and scalable UI components.” (https://linear.app/careers/12f8f208-0b9c-4569-bb3d-41c8a197029e) **[Inference]** Even a famously design-forward product company locates mastery in **sync, data, and lifecycle**, with UI as the expression.

**[Evidence]** Lee Robinson via PostHog: product engineers “have a broad understanding of the available tools and **deep experience applying those tools to build products**” — not deep expertise in every layer. (https://posthog.com/product-engineer/what-is-a-product-engineer) **[Inference]** This is a warning: Route 2’s advertised mastery (“full-stack”) is **application of tools to a product**, which can stall at *breadth*. The deeper object still has to be chosen. For Omcoda/Tower that object is the **eligibility-and-reactivation domain**, not Next.js.

### 4.2 Candidate mastery objects — ranked by depth, not prestige

1. **Domain model of a live business workflow** (eligibility states, file stages, compliance clocks, client-reactivation predicates). This is the object that compounds with Omcoda. **[Inference]**
2. **Multi-tenant operated runtime** (isolation, config-per-firm, monitoring, backup, identity). This is the TSO-adjacent object. **[Inference]**
3. **Application architecture** (modular monolith vs services, job systems, event history — Basecamp chassis). **[Evidence]** 37signals chassis discussion. (https://dev.37signals.com/the-rails-delegated-type-pattern/)
4. **UX system / design language implemented in code** (component library, interaction rules). Real, but it is **downstream** of the domain; designer-engineers can own this without owning the business. **[Inference]**
5. **The particular codebase** (repo mastery). Necessary, perishable, not the destination. Shopify Staff: ten years of the same changes ≠ Staff. (https://shopify.engineering/what-being-a-staff-developer-means-at-shopify)
6. **“The product” as a market object** (positioning, pricing). PostHog includes this in the *role*; it is **not a technical object**. Owning it as a founder is business ownership, not engineering mastery. **[Inference]**

**[Hypothesis]** If this route is practised as agency CRUD or JS-framework fashion, the object owned at year 5 is still (5) or a shallow (4). If practised as Tower-class product, year 5 can hold (1)+(2). Principal in a large org usually requires (3) at company scale, which a 1-person SaaS does not automatically provide.

---

## 5. HARD B→C CHAIN

Most important section. No match percentages. Distinguish **continuous** (same job, new employer) from **conceptually similar** (related craft, employers will still make you prove it).

Three Plan B shapes, because they do not lead to the same Plan C.

### 5.1 Chain A — Freelance WordPress / Shopify / “website apps”

| Link | Content |
|---|---|
| **Independent Plan B work** | Theme customization, plugin/app config, landing pages, stores, small JavaScript, hosting. Marketplace Project Catalog work. (Upwork Project Catalog explicitly packages Shopify themes and landing pages: https://cadence.withremote.ai/blog/toptal-vs-upwork) |
| **Actual responsibilities** | Implement a brief; pixel-match a design; wrangle plugins; fight hosting; client revisions. Little original data modelling. Rare production incident ownership beyond “the site is down.” |
| **Evidence artifacts** | Portfolio of sites, testimonials, before/after screenshots, maybe a GitHub of themes. **Not** architecture docs, SLOs, or domain models. |
| **Exact Plan C job title (reachable)** | Web Developer, WordPress/Shopify Developer, Junior/Intermediate Frontend Developer, “Full Stack” at a small agency (often meaning PHP/Liquid + JS). |
| **Employer type** | Digital agencies, SMB in-house, e-commerce retainers. Occasionally a product company’s **marketing-site** team. |
| **Expected level after ~2 years** | Junior to low-intermediate. Hiring-manager anecdote: weak freelance on a bootcamp résumé read as **internship-ready, not SDE2**. (https://www.reddit.com/r/cscareerquestions/comments/xauqp9/will-freelance-software-development-count-towards/) |
| **Degree effect** | Does not convert this chain into Product Engineer. May open bank/gov **new-grad/co-op** if enrolled, which is a **different chain**, not a promotion of WordPress work. |

**Titles not reachable on this chain after 2 years:** Staff/Senior Product Engineer; Backend Engineer on services; Google L4+; bank Lead Full Stack (10+ years .NET/Azure in the RBC example); Founding Engineer at a high-bar startup (Linear asks 5+ years of *customer-facing products at a high-quality software company*).

**Continuous vs conceptually similar:** **[Inference]** Conceptually similar to “I build things on the web.” **Not continuous** with product engineering. The objects (CMS, theme, plugin) do not transfer to domain models and production backends. Shopify *platform* engineering at Shopify-the-company is a different occupation from Shopify-theme freelance (reddit practitioners distinguish theme work vs headless/app work: https://www.reddit.com/r/webdev/comments/15gonfv/is_shopify_development_a_good_career_pathway/).

### 5.2 Chain B — Building and operating a real SaaS (Tower-class)

| Link | Content |
|---|---|
| **Independent Plan B work** | Identify a market gap; design a system; implement full stack; put real firms on it; operate it (Omcoda’s three disciplines). (https://omcoda.com) |
| **Actual responsibilities** | Domain modelling (eligibility, reactivation); auth and tenancy; data integrity; UI for professional users; monitoring; on-call-by-default; talking to users; saying no to custom briefs. This is **founding product engineering plus managed operations**. |
| **Evidence artifacts** | Live URL; architecture write-up; data model; incident notes; before/after operational metrics for a firm; case study with permission; repo (if shareable); demo of the actual workflow, not a landing page. GitHub without a live system is weaker than a live system without GitHub. |
| **Exact Plan C job title (reachable)** | **Product Engineer**, **Full-Stack Engineer/Developer**, **Founding Engineer**, possibly **Frontend Engineer** or **Backend Engineer** if the candidate can pass a specialized loop. Startup **Senior** is possible *if* the work demonstrates end-to-end features with visible product impact (Linear’s language) — not automatic from “I was CEO.” |
| **Employer type** | Product startups and scale-ups (Faire, Wealthsimple-like, vertical SaaS). Small product companies that run work trials. **Not** primarily FAANG campus. **Not** primarily bank new-grad. |
| **Expected level after ~2 years** | **Intermediate / early-Senior IC at a startup**, mapped to “can own a slice end-to-end without a PM writing tickets.” GitLab would likely call this Intermediate-to-Senior Fullstack, **not** Staff. Shopify Staff requires diversity of large-system experience explicitly denied to “one year out of bootcamp” and to “10 years of the same changes.” A single SaaS is **one deep project**. |
| **Degree effect** | **Eligibility:** unused at most startups. **Screening:** still helps banks/gov if Plan C pivots there; “founder” can *hurt* bank ATS (nonstandard title) unless rewritten as “Software Developer, Omcoda — built and operated X.” **Progression:** irrelevant at year 2; at year 10 in a bank, the degree may matter more than Tower did. |

**Titles not reachable on this chain after 2 years:** Staff / Senior Staff / Principal at Shopify, Linear, GitLab, Google L5+; Engineering Manager (no people-management evidence); Director; specialized Backend (distributed systems) or specialized Frontend (design systems at depth) *unless the SaaS actually went there*; Canadian bank “Lead Full Stack” of the 10-year Azure flavour.

**Continuous vs conceptually similar:** **[Inference]** **Closest to continuous** with Product Engineer / Founding Engineer. Same object: a user-facing system owned end-to-end. Gaps employers will still probe: working in *someone else’s* codebase, code review culture, testing at team scale, CS fundamentals interviews. Those are **real gaps**, not moral failures.

**[Evidence]** Faire mid Product Engineer: 2+ years, end-to-end product judgment, React/Next, Java/Kotlin/JS — this is the **shape** of a reachable Plan C title. (https://jobera.com/job/faire-product-engineer-brand-fullstack-backend-or-frontend-e808b1c4/) Linear Senior/Staff: 5+ years at a high-quality software company — **not** a 2-year founder default. (https://linear.app/careers/12f8f208-0b9c-4569-bb3d-41c8a197029e)

**[Hypothesis]** A well-documented Tower (multi-tenant, real clients, uptime, domain depth) plus a strong interview can enter **Faire-like Product Engineer at the 2-year bar**, not Linear Senior/Staff. Bank full-stack experienced hire is **conceptually similar but not continuous**: different stack (Java/.NET), different SDLC, different compliance theatre; degree/ATS become the gating mechanisms again.

### 5.3 Chain C — Contract full-stack at an agency / product team

| Link | Content |
|---|---|
| **Independent Plan B work** | Toptal/agency/contract: embed on client teams or deliver projects inside a shop. (https://www.toptal.com/top-3-percent) |
| **Actual responsibilities** | Tickets, PRs, standups, someone else’s architecture, estimated hours, QA, maybe client calls. Closer to employed IC than Chain A. Context-switch across clients (agency) or one product (embedded contractor). |
| **Evidence artifacts** | Named clients if allowed; tech stack list; references; GitHub if public; “delivered X in Y months.” Confidentiality often **strips the best artifacts**. |
| **Exact Plan C job title (reachable)** | Full-Stack Engineer/Developer, Software Developer, Frontend or Backend depending on what the contracts actually were. Some startups will title this Product Engineer if the contractor owned features. |
| **Employer type** | Product companies and banks that already hire contractors-to-perm; agencies-to-product is a known (not guaranteed) jump. (Agency-vs-product literature: https://richbray.medium.com/should-you-work-at-a-product-company-or-an-agency-as-a-developer-92cc3ee51e90) |
| **Expected level after ~2 years** | **Matches the level of the work, not the invoice.** Two years of supervised mid-level tickets → mid-level FTE. Two years as the senior on small client apps → maybe Senior at a **small** company, still not Staff. Toptal’s screen is a positive signal but is not a level mapping. |
| **Degree effect** | Weak at product firms if references exist; still material at banks. Contractor history can look like “job hopping” in corporate ATS unless grouped as one practice (resume-structure advice: https://blog.corecv.ai/how-to-put-freelance-or-contract-work-on-a-tech-resume/). |

**Titles not reachable:** Principal; Director; FAANG Senior without passing their loop; specialized platform/SRE titles unless the contracts were that.

**Continuous vs conceptually similar:** **[Inference]** **Most continuous with employed Full-Stack Engineer** as a *work week* (same rituals). **Less continuous than Chain B** as an *ownership story*. Employers who fear contractors (“mercenary, no product sense”) will discount it; employers who fear founders (“can’t work on a team”) will prefer it.

### 5.4 Plan C titles — reachable vs not, after ~2 years Plan B

Keep this as a matrix, not a score.

| Plan C title | After 2y Chain A (CMS freelance) | After 2y Chain B (Tower-class SaaS) | After 2y Chain C (agency/contract FS) |
|---|---|---|---|
| **Full-Stack Engineer/Developer (startup, intermediate)** | Conceptually similar at best; usually no | **Reachable** if artifacts show backend+frontend+prod | **Reachable** (most continuous) |
| **Product Engineer (Faire-like, 2+ YOE bar)** | Not reachable | **Reachable**, closest fit | Reachable if feature ownership was real, not ticket-only |
| **Frontend Engineer (product)** | Possible at junior/web-dev level | Reachable, but may be seen as generalist | Reachable if UI-heavy contracts |
| **Backend Engineer (services)** | Not reachable | Reachable only if the SaaS has real backend depth (jobs, tenancy, data), and interview passes | Reachable if contracts were backend |
| **Founding Engineer** | Not reachable | **Conceptually almost identical** — hiring is taste and risk | Possible if contractor acted as de-facto founding |
| **Senior Product Engineer (Linear 5+ YOE bar)** | Not reachable | **Not reachable on years**; maybe interview-exception at a smaller firm | Not reachable on years |
| **Staff / Principal** | Not reachable | Not reachable | Not reachable |
| **Eng Manager / Director** | Not reachable | Not reachable (no team) | Not reachable |
| **Bank Full Stack (experienced)** | Unlikely; ATS+stack | Possible as rewrite-to-developer; degree and Java/.NET still bind | Possible with stack match |
| **Bank/gov new-grad/co-op** | Only via **enrollment**, not via the freelance | Same | Same |
| **Google L3 campus** | Unlikely without DS&A + degree/equivalent story | Unlikely without DS&A; “equivalent experience” is the legal door | Same |
| **Designer-engineer / UX engineer** | Possible if the work was visual | Possible if UI craft is excellent | Possible |

**[Inference]** “2 years of Plan B should count as real experience” is **true only for Chain B and Chain C**, and only for **IC product/full-stack titles around intermediate**. It is **false** for Staff+, for bank leadership, and for Chain A as a product-engineer story. Founder years are **real** but **nonstandard**; they count when rewritten as engineering responsibilities, not as “CEO, Omcoda.”

**[Evidence]** Stack Overflow hiring-manager resume advice: once you have work experience, **education becomes less relevant**; personal projects matter less; standout shipped work still helps. (https://stackoverflow.blog/2020/11/25/how-to-write-an-effective-developer-resume-advice-from-a-hiring-manager/) **[Inference]** Tower must be formatted as **work experience**, not as a project under Education.

---

## 6. Career optionality

### 6.1 Branches this route can open

**[Inference]** From a genuine product-engineering base (Chain B or good Chain C):

- **Product engineer (stay)** — Linear/PostHog/Faire-shaped. Deepens domain + full-stack + user loop. Closest to this route’s centre.
- **Frontend specialist** — if taste and performance work dominate (Parallelz Toronto Senior PE is already frontend-heavy Next.js: https://echojobs.io/job/parallelz-senior-product-engineer-un06w).
- **Backend / platform** — if the work goes into data, jobs, isolation, reliability. Not automatic from “I also wrote an API.”
- **Founding engineer** — Chain B *is* this; later, doing it for someone else’s zero-to-one.
- **Engineering manager** — GitLab: try management before committing; Staff and EM are a fork, not a ladder. Requires people work this route does not automatically produce. (https://handbook.gitlab.com/handbook/engineering/careers/)
- **Designer-engineer** — 37signals designer+programmer pairs; possible if visual craft is real. Different hiring loops.
- **Platform / infra** — only if the product’s runtime becomes the interest (k8s, observability). Adjacent to TSO; not the default full-stack path.
- **Vertical solutions architect / operator** — Omcoda’s own “solutions architecture + managed operations.” This is **off the employee ladder** and onto the operator archetype.

### 6.2 Narrowing traps

- **Agency CRUD.** Many apps, none owned. Résumé looks busy; mastery object stays “tickets.” Service-vs-product literature (mixed quality) repeats context-switch and lower ceiling. (https://thelinuxcode.com/product-based-vs-service-based-companies-a-practical-guide-from-a-2026-engineering-lens/)
- **JS-framework fashion.** Next.js / RSC / whatever-2026. **[Evidence]** Linear still cares about React+TS+Postgres; they do not hire “Next.js people.” (https://linear.app/careers/12f8f208-0b9c-4569-bb3d-41c8a197029e) **[Inference]** Framework identity expires; domain model and data integrity do not. A CS degree does not save a candidate whose GitHub is tutorial clones of the current meta-framework.
- **CMS lock-in.** WordPress/Shopify theme expertise is a market (Codeable exists as a WP-specific vetted network: https://www.codeable.io/blog/upwork-vs-toptal/) and a **cul-de-sac** relative to Product Engineer titles.
- **Founder-title inflation.** “CTO of a 1-person company” reads as uncalibrated in Staff packets (Shopify: Staff is not a Senior with a louder title).
- **PM drift.** Orosz notes product-minded engineers *could* become PMs. Route 6 was dropped. **[Inference]** Using this route as a back door into PM throws away the mastery object (the system) for a coordination job.

**[Evidence]** Job Bank: web developers (21234) and software developers (21232) both **Very limited** in Toronto 2025–2027. (https://www.jobbank.gc.ca/outlookreport/location/geo9219) **[Inference]** Optionality is not “the market is hungry so any branch works.” Optionality is **skill transfer**. Breadth without a mastery object is a crowded, cooling market.

---

## 7. Omcoda flywheel

Omcoda is not a custom shop. Tower is immigration eligibility monitoring + client reactivation, operated for firms. (https://omcoda.com)

This route is the **closest of the engineering routes to BUILDING Tower-class products**. It is also the route most able to **betray** Omcoda by becoming a shop.

### 7.1 Forward flywheel (craft → Omcoda)

```
domain insight (how immigration files actually move)
        → product engineering (model it in software)
                → live system (Tower in production)
                        → managed operations (run it for firms)
                                → new gaps observed in operation
                                        → next proprietary module
```

**[Inference]** Product engineering supplies: data model, UX for professional users, integrations, tenancy, auth, background jobs (monitoring eligibility is a **time-based system**, not a CRUD form), observability. Without this route, Omcoda cannot *make* Tower; it can only slide-deck it.

**[Evidence]** Omcoda names “solutions architecture,” “market development,” and “managed operations” as the three disciplines; “every solution starts with a market gap, not a client brief.” (https://omcoda.com) **[Inference]** Forward flywheel requires the engineering object to stay **generic to a class of firms** (vertical specialization), not snapshot-custom to the loudest client.

### 7.2 Reverse flywheel (Omcoda → craft)

```
operating Tower for firms
        → real constraints (compliance, messy data, adoption, support)
                → better product engineering taste
                        → artifacts that Plan C Product Engineer interviews actually probe
                                → choice: stay operator-founder  OR  enter product/full-stack IC
```

**[Inference]** Reverse is how Plan B becomes **Plan C-readable** without doing WordPress. The case study is not “I used React.” It is “eligibility rules change; the system watches; the firm reactivates; here is the state machine; here is what broke at 2am.”

**[Inference]** Reverse also trains TSO behaviours (diagnose bottleneck, maintain live system) that pure product-engineering employment may *untrain* if the company has a separate SRE/support org (PostHog deliberately does not: engineers do support).

### 7.3 The custom-shop failure of the flywheel

**[Evidence]** The commercial market *wants* the shop: Toronto businesses are quoted custom software as projects; agencies bill CA$100–250/hr to take briefs. (https://www.naveck.com/blog/web-development-companies-cost-canada/ ; https://byteager.ca/blog/how-much-custom-software-development-cost-toronto-2026)

**[Inference]** If Route 2 Plan B is “I will close clients by building whatever they ask,” the flywheel becomes:

```
client brief → custom app → handoff → next brief
```

That is **negative** for Omcoda’s identity (explicitly refused) and **weak** for Plan C Product Engineer (no owned product, confidentiality, CMS-shaped work). It is **positive** for short-term cash and for Chain C (agency) résumés.

**Precision rule:** **[Inference]** Selling implementation labour on Tower (configuring *the* product for a firm) is managed operations — allowed. Selling a **different app** for a firm’s unique workflow is a custom shop — refused. Selling a **module that becomes part of Tower** because several firms share the gap is product engineering — allowed. The test is whether the artefact remains Omcoda’s and is reusable.

**[Hypothesis]** The highest-integrity Plan B offer on this route is not “full-stack freelancer” and not “agency.” It is **vertical product operator who can also write the product**. That is a harder sale than websites. It is the only sale that does not fight the website.

---

## 8. Mastery horizon and primitives

### 8.1 Primitives (3–5) — the things this route is *made of*

Not frameworks. Frameworks rotate.

1. **Domain modelling** — entities, invariants, state machines, permissions. Rails/Django/Next-all-alike live or die here. (37signals `Recording`; Tower eligibility states.)
2. **Request/data lifecycle** — HTTP, authn/authz, persistence, jobs/queues, consistency. The “full stack” actually means this loop, not “React + Node.”
3. **User-facing interaction design in code** — information hierarchy, forms, empty/error/permission states, professional-user density (immigration consultants are not consumer-app users).
4. **Production operation of an application** — deploy, migrate, logs, backups, multi-tenant blast radius. This is the TSO overlap.
5. **Product feedback loop** — instrument, talk to users, cut scope, kill features (PostHog/Orosz). Without (5), (1)–(4) produce elegant unused systems.

**[Inference]** Next.js, Rails, and Django are **vehicles for (1)–(4)**. Choosing one is a Plan B speed decision, not a mastery identity. Rails still has a documented path to a 9-year product chassis at small team size (37signals). Next.js/React is what Toronto product postings currently name (Faire, Parallelz, Flexgen, NationGraph). Django remains a common SaaS backend paired with a JS frontend (architecture-guide literature; weaker as a *craft culture* source than 37signals).

### 8.2 Observable benchmarks (not credentials)

**Year 1 — a slice exists.**

- A real user (not the builder) can complete a core workflow.
- Data persists; auth exists; deploys are repeatable.
- You can draw the domain on one page (boxes and states), and the code roughly matches the drawing.
- **[Evidence-shaped bar]** Linear/Faire both treat “end-to-end feature” as the unit, not screens. (https://linear.app/careers/12f8f208-0b9c-4569-bb3d-41c8a197029e)

**Year 3 — a product-system exists.**

- Multi-step workflow with permissions and audit-ish history (professional services require this; Basecamp’s recordings/history are the analog).
- Background work (eligibility monitoring is not a button).
- You have broken production and repaired it; you can tell the story.
- At least one module was rewritten because the domain was wrong, not because the framework was unfashionable. (Shopify Staff: mistakes as growth. https://shopify.engineering/what-being-a-staff-developer-means-at-shopify)
- Artifacts a hiring manager can touch: live system, schema, one incident, one metric that moved.

**Year 5 — others can extend it; you own constraints.**

- A second engineer (hire, contractor, or future teammate) can add a feature without destroying tenancy or the state machine.
- You can say **no** to a lucrative custom brief because it would break the product object (Omcoda identity test).
- You can explain build-vs-buy and modular-monolith-vs-services for *this* domain, not in interview abstractions.
- **Still not Principal at a large org** unless you have also done cross-team technical leadership (GitLab/Shopify). Year-5 mastery of *your* product ≠ Staff-plus.

**Principal-shaped (long horizon, not a 2-year Plan C target).**

- Larson Architect or Tech Lead: the constraint system of a **company-scale** product area. (https://staffeng.com/guides/staff-archetypes/)
- Or: Omcoda-scale principal as **operator-architect** of a vertical system run across many firms — a different institution, no ladder.

---

## 9. Failure modes / tension with TSO

TSO (given): diagnose org bottlenecks, architect technical solutions, write/integrate software, automate, **maintain live systems end-to-end**.

Route 2 overlap: write/integrate software, architect solutions.  
Route 2 miss: **operate as the job**, unless deliberately practised as Chain B.

### 9.1 Product-building vs operator of live systems

**[Inference]** Employed product engineers at companies with separate SRE/support **hand off** runtime pain. Stripe’s 42% maintenance figure shows the pain still exists, but it is framed as a tax on feature work, not as the craft. TSO treats live-system care as the centre.

**[Evidence]** PostHog’s product-engineer definition *includes* support. 37signals programmers ship and live with what they shipped. (https://posthog.com/product-engineer/what-is-a-product-engineer ; https://dev.37signals.com/building-basecamp-project-stacks-with-hotwire/) **[Inference]** Those cultures are TSO-compatible. Bank squad + BA + separate ops is not.

**Failure mode:** become a **feature factory IC** whose production is “someone else’s problem.” Plan C at a large org can **undo** TSO formation.

**Failure mode (opposite):** become a **hero operator** who never raises the abstraction (no domain model, only firefighting). That is TSO without product engineering; Tower stays a pile of scripts.

### 9.2 Frontend fashion vs systems depth

**[Evidence]** Toronto postings in this research wave name Next.js/React/TypeScript repeatedly (Faire, Parallelz, Flexgen, NationGraph). Linear names React/TS but locates hard systems in sync/Temporal/Postgres. 37signals names vanilla Rails and delegated types, explicitly *against* paradigm fashion. (URLs above.)

**[Inference]** The GTA hiring surface will pull a Plan B builder toward **Next.js identity**. The mastery object will pull toward **domain + data + time**. Chasing the posting language is rational for Plan C screens and can starve (1) and (2) in Section 8.

### 9.3 Custom-shop gravity vs TSO/Omcoda

Already stated; it is the commercial failure mode. TSO cannot form if the system is handed off. Omcoda cannot form if the system is the client’s.

### 9.4 Interview vs reality gap

**[Evidence]** Google early-career still wants DS&A experience. (https://www.google.com/about/careers/applications/jobs/results/78703249065943750-software-engineer-early-career-campus) Bank co-ops want transcripts. Linear wants 5+ years at a high-quality software company plus a work-trial culture. **[Inference]** Chain B produces the *job* of product engineering faster than it produces the *signals* of Big Tech/bank hiring. Failure mode: excellent operator-founder who cannot pass a whiteboard, or excellent LeetCode student who cannot operate Tuesday.

### 9.5 Degree-as-delay

**[Inference]** A full-time CS degree can starve Tower’s live-system years — the exact years that make Plan B count. A degree that *enables* co-op at RBC/TD is a **different strategy** (student path), not an add-on to operator path. Doing both concurrently is a load problem, not a philosophy problem. Not measured.

### 9.6 Title / PEO / “engineer” identity

**[Evidence]** PEO restriction on “Software Engineer” in Ontario. (https://www.peo.on.ca/public-protection/complaints-and-illegal-practice/unlicensed-practice-enforcement-faq) **[Inference]** Building an identity as “I am a Software Engineer” is legally noisy in the GTA and technically imprecise for this route. “Product engineer / software developer / systems operator” are cleaner. This is a small failure mode (ego and LinkedIn) that can become a real one if PEO-enforcement cycles heat up.

---

## 10. What is NOT yet established

1. **Wale’s current depth** on primitives (1)–(5). This file is occupational, not a skills audit.
2. **Whether Tower, as it exists today, is a Chain-B artefact or a prototype.** Live firms, tenancy, monitoring, uptime — not verified here (Omcoda was read as positioning, not as a product inspection).
3. **How GTA hiring managers actually score “Founder, Omcoda (1 person)” vs “Full-Stack Contractor, Agency X” vs “BSc CS + intern.”** We have role texts and anecdotes, not a local audit.
4. **Bank/Workday knockout settings** for experienced full-stack roles (degree required vs preferred). Co-op gates are clear; experienced-hire gates are not.
5. **Time-use of freelance app builders and 1-person SaaS operators.** Tuesday % tables for those modes are hypotheses.
6. **Conversion cases:** how many Canadian indie-SaaS founders entered Faire/Shopify/Wealthsimple Product Engineer seats at the 2-year mark, at what level, with/without degrees. Not found.
7. **Whether “Product Engineer” is a stable GTA title outside a handful of startups.** Banks still say Full Stack Developer. Title optionality may be coastal.
8. **Stack choice for Tower** (Next vs Rails vs Django) as a Plan C signal. Postings currently lean React/Next in Toronto product land; Rails remains culturally elite at 37signals/Shopify. No evidence that the *framework* is the deciding artefact.
9. **Toptal acceptance probability** for this subject. Published 3% is a company funnel statistic, not a personal base rate.
10. **Official 2025–2027 “Very limited” outlook vs actual vacancy quality.** Job Bank counts and posting quality can diverge; we did not census LinkedIn/Indeed.
11. **PEO enforcement frequency** against GTA “Software Engineer” job titles in tech. Policy is clear; practice is visibly noncompliant.
12. **CS degree part-time feasibility** at GTA universities while operating Omcoda — academic, not labour-market, and not researched.
13. **Client-closing rates** for a managed-solutions offer vs custom-app offer in immigration/legal/financial verticals. Omcoda asserts a model; market conversion is unknown.
14. **How much “AI writes the CRUD now” compresses this route’s junior rung.** PostHog claims one engineer + LLM ships what teams used to; SO 2025 shows distrust and debugging tax. Net effect on Plan B pricing and Plan C junior hiring is **not established**.

---

## 11. Source list

Primary and named sources actually used. Vendor rate blogs included because they shape the *quoted* freelance market; they are weak as measurement.

### Role definitions and craft

- PostHog, “What is a product engineer?” — https://posthog.com/product-engineer/what-is-a-product-engineer
- Gergely Orosz, “The Product-Minded Software Engineer” — https://blog.pragmaticengineer.com/the-product-minded-engineer/
- Linear, Senior/Staff Product Engineer — https://linear.app/careers/12f8f208-0b9c-4569-bb3d-41c8a197029e
- Faire, Product Engineer (Brand) Toronto — https://jobera.com/job/faire-product-engineer-brand-fullstack-backend-or-frontend-e808b1c4/
- Faire, Staff Product Engineer (Brand) — https://jobera.com/job/faire-staff-product-engineer-brand-db98c1ed/
- Notion, Product Engineer (secondary listing) — https://www.notion.so/Product-Engineer-2a98b80b88dd80e1b4d0c508ddb98dab
- Stripe, Full Stack Engineer, Growth — https://stripe.com/careers/listing/full-stack-engineer-growth/7964956
- Parallelz, Senior Product Engineer, Toronto — https://echojobs.io/job/parallelz-senior-product-engineer-un06w
- NationGraph, Software Engineer, Product, Toronto — https://echojobs.io/job/nationgraph-software-engineer-product-dlwea
- Flexgen, Senior Full Stack Engineer, GTA — https://flexgen.zya.me/job/senior-full-stack-engineer-31
- Stem Health, Full Stack Developer, Toronto (Rails) — https://www.jobs.ca/stem-health/jobs/full-stack-developer-toronto-on-f52f1d341e61
- product.engineer, role template — https://www.product.engineer/jobs/product-engineer

### Career ladders / Staff-plus

- GitLab Engineering Career Development — https://handbook.gitlab.com/handbook/engineering/careers/
- GitLab Engineering Leadership / Principal Engineer — https://handbook.gitlab.com/job-description-library/engineering/engineering-management/
- GitLab Staff / Principal infrastructure matrix — https://handbook.gitlab.com/handbook/engineering/careers/matrix/staff/ ; https://handbook.gitlab.com/handbook/engineering/careers/matrix/infrastructure/principal/
- Shopify, “What Being a Staff Developer Means” — https://shopify.engineering/what-being-a-staff-developer-means-at-shopify
- Shopify, ~Mastery — https://www.shopify.com/news/mastery
- Shopify, Senior Staff Software Engineer posting — https://www.shopify.com/careers/senior-staff-software-engineer-optimization_2e2f43f4-f4a5-4163-acbc-6448cf1557f3
- Will Larson, Staff archetypes — https://staffeng.com/guides/staff-archetypes/
- LeadDev, Staff / Principal / Distinguished — https://leaddev.com/career-development/who-are-staff-principal-and-distinguished-engineers
- Pragmatic Engineer, Shopify leveling (secondary) — https://newsletter.pragmaticengineer.com/p/inside-shopifys-leveling-split

### Domain-model / Rails product craft

- 37signals, “Vanilla Rails is plenty” — https://dev.37signals.com/vanilla-rails-is-plenty/
- 37signals, delegated types / Recordings — https://dev.37signals.com/the-rails-delegated-type-pattern/
- 37signals, Hotwire project stacks / teams of two — https://dev.37signals.com/building-basecamp-project-stacks-with-hotwire/
- Rails Foundation, 37signals profile — https://rubyonrails.org/foundation/37signals

### Time use / DX

- Computerworld on Clockwise meeting/focus study — https://www.computerworld.com/article/1612747/for-developers-too-many-meetings-too-little-focus-time.html
- Stripe, The Developer Coefficient (PDF) — https://stripe.com/files/reports/the-developer-coefficient.pdf
- ADTmag summary of Developer Coefficient — https://adtmag.com/articles/2018/09/10/developer-survey.aspx
- Stack Overflow Developer Survey 2024 Professional Developers — https://survey.stackoverflow.co/2024/professional-developers/
- Stack Overflow Developer Survey 2025 — https://survey.stackoverflow.co/2025/
- Stack Overflow blog, tasks developers spend time on (2025) — https://stackoverflow.blog/2025/12/10/tell-us-what-you-really-really-do-not-want-to-spend-time-working-on/
- Atlassian State of Teams 2024 — https://www.atlassian.com/blog/state-of-teams-2024

### Canadian / GTA labour market, degrees, titles

- Ontario labour market, NOC 21231 — https://services.labour.gov.on.ca/labourmarket-ui/jobProfile?nocCode=21231
- Job Bank wages, software engineers — https://www.jobbank.gc.ca/wagereport/occupation/5485
- Job Bank Toronto outlooks — https://www.jobbank.gc.ca/outlookreport/location/geo9219
- Job Bank requirements, NOC 21232 — https://www.jobbank.gc.ca/marketreport/requirements/22532/ca
- NOC 21232 profile — https://noc.esdc.gc.ca/Structure/NOCProfile?GocTemplateCulture=en-CA&code=21232&version=2021.0
- Treasury Board, qualification standards (IT group) — https://www.canada.ca/en/treasury-board-secretariat/services/staffing/qualification-standards/core.html
- Treasury Board, qualification standards FAQ — https://www.canada.ca/en/treasury-board-secretariat/services/staffing/qualification-standards/frequently-asked-questions-qualification-standards.html
- PSC posting, IT Analyst Software Solutions — https://emploisfp-psjobs.cfp-psc.gc.ca/psrs-srfp/applicant/page1800?poster=1862552
- RBC Borealis Software Developer co-op — https://rbc.wd3.myworkdayjobs.com/en-US/RBCEARLYTALENT1/job/RBC-WATERPARK-PLACE-88-QUEENS-QUAY-WTORONTO/XMLNAME-2027-Winter-Student-Opportunities-RBC-Borealis---Software-Developer--4-8-Months_R-0000184501-1
- RBC T&O Software Developer co-op — https://rbc.wd3.myworkdayjobs.com/en-US/RBCEARLYTALENT1/job/TORONTO-Ontario-Canada/XMLNAME-2027-Winter-Student-Opportunities-Technology---Operations---Software-Developer--4-Months_R-0000184555-1
- RBC Lead Full Stack Developer, Toronto — https://rbc.wd3.myworkdayjobs.com/en-US/RBCGLOBAL1/job/TORONTO-Ontario-Canada/Lead-Full-Stack-Developer_R-0000163643-1
- TD Software Engineer Co-op/Intern Winter 2027 — https://www.themuse.com/jobs/tdbank/software-engineer-coop-intern-winter-2027
- Scotiabank Fullstack Software Engineer Specialist — https://jobs.scotiabank.com/job/Bogota-Fullstack-software-engineer-specialist-DC/601320817/
- Scotiabank GBM full-stack internship (agg.) — https://jobsca.org/finance_toronto-c117072/2026-09-scotiabank_i4202901367
- PEO unlicensed practice FAQ — https://www.peo.on.ca/public-protection/complaints-and-illegal-practice/unlicensed-practice-enforcement-faq
- Engineers Canada, title use — https://engineerscanada.ca/become-an-engineer/use-of-professional-title-and-designations
- Google SWE Early Career Campus — https://www.google.com/about/careers/applications/jobs/results/78703249065943750-software-engineer-early-career-campus
- Levels.fyi, Google SWE GTA — https://www.levels.fyi/companies/google/salaries/software-engineer/locations/greater-toronto-area
- Times of India / Brin on Google degrees — https://timesofindia.indiatimes.com/education/careers/news/google-has-hired-tons-of-people-without-college-degrees-says-sergey-brin-heres-why/articleshow/126505460.cms

### Freelance / agency markets

- Toptal, “Why 3%” screening process — https://www.toptal.com/top-3-percent
- Cadence, Toptal vs Upwork 2026 — https://cadence.withremote.ai/blog/toptal-vs-upwork
- Second Talent, Toptal vs Upwork — https://www.secondtalent.com/alternatives/toptal-vs-upwork/
- Index.dev, freelance rates by country 2026 — https://www.index.dev/blog/freelance-developer-rates
- Freel.ca, Canada full-stack freelance rates — https://freel.ca/rates/full-stack-developer-freelance-rates-canada
- Codeable, Upwork vs Toptal for WordPress — https://www.codeable.io/blog/upwork-vs-toptal/
- Essential Designs, agency vs freelancer Toronto (vendor) — https://www.essentialdesigns.net/news/custom-software-agency-vs-freelancers-toronto
- Byteager, custom software cost Toronto 2026 (vendor) — https://byteager.ca/blog/how-much-custom-software-development-cost-toronto-2026
- Naveck, web development companies cost Canada (vendor) — https://www.naveck.com/blog/web-development-companies-cost-canada/
- Modall, custom software Canada 2026 (vendor) — https://modall.ca/blog/custom-software-development-canada
- HyperNest, founding engineer vs contractor — https://hypernestlabs.com/insights/founding-engineer-vs-contractor
- DEV, freelancing vs job vs startup — https://dev.to/raajaryan/freelancing-vs-job-vs-startup-my-honest-developer-perspective-35f8
- What’s My Pivot, SWE to freelance — https://whatsmypivot.com/blog/software-engineer-to-freelance-developer-transition-guide-2026
- JobStera, freelance vs full-time 2026 — https://jobstera.com/articles/en/freelance-vs-full-time-tech-2026
- CoreCV, freelance on a tech resume — https://blog.corecv.ai/how-to-put-freelance-or-contract-work-on-a-tech-resume/
- Stack Overflow, hiring-manager resume advice — https://stackoverflow.blog/2020/11/25/how-to-write-an-effective-developer-resume-advice-from-a-hiring-manager/
- r/cscareerquestions, does freelance count — https://www.reddit.com/r/cscareerquestions/comments/xauqp9/will-freelance-software-development-count-towards/
- r/webdev, Shopify career pathway — https://www.reddit.com/r/webdev/comments/15gonfv/is_shopify_development_a_good_career_pathway/

### Screening / ATS (weak-to-moderate)

- Rejectless, 1,000 SWE postings — https://www.rejectless.app/guides/parsed-1000-swe-job-postings-what-ats-actually-looks-for
- Classet, skills-based hiring vs screening — https://www.classet.ai/blog/skills-based-hiring-screening
- ATS parsing research notes — https://github.com/sunnypatell/ats-screener/blob/main/research/ats-parsing-scoring-research.md
- TeamBlind, no-degree SWE — https://www.teamblind.com/post/entering-software-engineer-job-market-with-no-degree-dyc3kx5t

### Agency vs product (mixed quality, used as texture)

- theremotespot, agency vs product — https://theremotespot.com/remote-web-development-jobs-agency-vs-product/
- Richard Oliver Bray, product company vs agency — https://richbray.medium.com/should-you-work-at-a-product-company-or-an-agency-as-a-developer-92cc3ee51e90
- TheLinuxCode, product-based vs service-based 2026 — https://thelinuxcode.com/product-based-vs-service-based-companies-a-practical-guide-from-a-2026-engineering-lens/

### Subject venture (primary, given)

- Omcoda — https://omcoda.com

---

*End of evidence file. No route ranking is implied.*
