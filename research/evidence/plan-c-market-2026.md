# Plan C job-market scan — Canada / GTA / remote-Canada (2026)

**Document type:** labour-market evidence file. Not a career decision.  
**Subject (given, not independently researched):** Wale Omotayo, Greater Toronto Area. CS degree is future access, not a current credential. ~2 years of independent operator work planned. Live domain system in view: immigration eligibility monitoring + client reactivation (Tower / Omcoda).  
**Researched:** 2026-09-22.  
**Method:** live web search + fetch of employer career pages (Ashby, Greenhouse, Lever, Workday), Job Bank, Ontario labour profiles, COPS, Indeed Hiring Lab. Secondary aggregators used only when a primary page 404'd, JS-rendered empty, or the Canadian sample was thin — flagged.

**Epistemic tags**

- **[Evidence]** — a posting, official labour series, or named scan that was fetched or whose text was extracted from the live page / official HTML. URL given.
- **[Inference]** — a conclusion from several pieces of evidence plus the subject context.
- **[Hypothesis]** — decision-relevant and not established by the sources in this file.

**Rules observed**

- No invented postings.
- If a URL 404'd or the ATS shell loaded without a job body, that is stated.
- Salary figures are as posted or as official LFS hourly wages. No invented conversions except the obvious `hourly × 2080` note, marked as arithmetic.
- “Posted / indexed date” is the date on the page or in the ATS metadata. Some Ashby boards are evergreen (“always hiring”).

---

## 0. How to read this file

Plan C destination families in this scan:

1. Product Engineer  
2. Software Engineer / Software Developer  
3. Backend Engineer / Backend Developer  
4. Full-Stack Engineer (only roles with meaningful backend/product ownership)  
5. Founding Engineer  
6. Forward-Deployed Engineer (true engineering-heavy vs relabeled Solutions Engineer)

Canadian product companies often put the **same job** under different titles. Wealthsimple’s “Senior Software Developer — Product Engineering” is a Product Engineer job with Canadian “Developer” language. Docebo’s “Senior Product Engineer I — Automation” is a backend/platform job with Product Engineer language. Treat the **verbs and object**, not the noun.

---

## 1. Official labour weather (Ontario / Job Bank / COPS)

### 1.1 NOC 21232 — Software developers and programmers

**[Evidence]** Job Bank Ontario outlook, updated 10 Dec 2025 (recent trends updated 28 Jul 2026): **Limited** for 2025–2027. Reasons: employment decline; few retirements. Toronto region: **Very limited**, and a **labour surplus** over 2023–2025. Ontario employment ~88,700; Toronto ~52,470. Sector mix in Toronto: professional/scientific/technical 60%, finance/insurance/real estate 14%, information 9%. Self-employed 11% vs 15% all occupations.

- Ontario outlook: https://www.jobbank.gc.ca/marketreport/outlook-occupation/22548/ON  
- Toronto outlook: https://www.jobbank.gc.ca/marketreport/outlook-occupation/22548/geo9219  
- Ontario labour profile (last updated 6 Feb 2026 on the services.labour.gov.on.ca page as indexed): https://services.labour.gov.on.ca/labourmarket-ui/jobProfile?nocCode=21232  

**[Evidence]** Education language, Job Bank requirements (Ontario):

> “A bachelor's degree in computer science or software engineering or in another discipline with a significant programming component or completion of a college program in computer science or related field is **usually required**.”

https://www.jobbank.gc.ca/marketreport/requirements/22548/ON

Job Bank also says this occupation is **not regulated** in Canada (no professional licence required to practise as a software developer). “Progression to software engineer is possible with experience.”

**[Evidence]** Educational attainment of *incumbents* in Ontario (Job Bank Ontario outlook page): bachelor’s 50%; above bachelor’s 27% → **77% university-level**. College-or-below-bachelor 11%. High school 11%.

**[Evidence]** Wages, LFS 2023–2024, updated 19 Nov 2025:

| Geography | Low | Median | High |
|---|---:|---:|---:|
| Toronto Region | $30.00/hr | $48.08/hr | $76.92/hr |
| Ontario | $30.29/hr | $48.08/hr | $77.40/hr |
| Canada | $30.00/hr | $48.08/hr | $76.92/hr |

https://www.jobbank.gc.ca/marketreport/wages-occupation/22548/22437  

Arithmetic only (not a posted salary): Toronto median $48.08 × 2080 ≈ **CA$100,000**; high $76.92 × 2080 ≈ **CA$160,000**. Product-SaaS and US-remote-Canada postings in this file sit well above that high.

**[Evidence]** COPS 2024–2033 national outlook for 21232: **BALANCE**. Employment 2023: 155,700. TEER 1 (“usually require a university degree”). Openings 76,300 vs seekers 98,900 over the decade (~7,630 openings/year vs ~9,890 seekers/year). School leavers are the main source of seekers, then immigrants. COPS notes 2023 vacancies “fell sharply” after the boom. Update notice on the page: 2026–2035 projections due starting fall 2026.

https://occupations.esdc.gc.ca/sppc-cops/occupationsummarydetail.jsp?lang=eng&tid=91

**[Inference]** Official Canada is not in a software-developer shortage. COPS’s “balance” still has **more projected seekers than openings**. Ontario/Toronto 3-year outlooks are worse than the national 10-year (Limited / Very limited + recent surplus). Plan C is entering a picky market.

### 1.2 Adjacent NOC 21231 — Software engineers and designers

**[Evidence]** Job Bank Ontario: **Very limited** 2025–2027. Same two reasons (decline + few retirements). Ontario employment ~72,950. Toronto ~43,880 (Ontario labour profile). Educational attainment Ontario: bachelor’s 52%; above bachelor’s 32% → **84% university**. Self-employed 9%. Median Ontario wage $56.73/hr; Canada $56.49/hr (Ontario labour profile as indexed).

- Ontario outlook: https://www.jobbank.gc.ca/marketreport/outlook-occupation/5482/ON  
- Toronto 21231: https://www.jobbank.gc.ca/marketreport/outlook-occupation/5485/geo9219  
- Ontario labour profile: https://services.labour.gov.on.ca/labourmarket-ui/jobProfile?nocCode=21231  

**[Evidence]** COPS 21231 2024–2033: **BALANCE**. Employment 2023: 113,100. Openings 46,900 vs seekers 60,400. New immigrants are the main source of seekers, then school leavers. TEER 1.

https://occupations.esdc.gc.ca/sppc-cops/occupationsummarydetail.jsp?lang=eng&tid=90

**[Inference]** 21231 is the “engineer/designer” bin (closer to Product Engineer / SWE at product companies and banks). The 3-year Ontario/Toronto weather is **harsher** than 21232. The degree density among incumbents is higher.

### 1.3 Adjacent NOC 21234 — Web developers and programmers

**[Evidence]** Job Bank Ontario: **Very limited** 2025–2027. Extra reason vs 21232: “several unemployed workers with recent experience.” Ontario employment ~11,450; Toronto ~6,450. Self-employed **21%**. Bachelor’s 43%; above bachelor’s 20%. Job Bank notes front-end is the common ask; full-stack “may be an asset.” Pace of growth “affected by the availability of advanced software which is simplifying the steps in web development.”

https://www.jobbank.gc.ca/marketreport/outlook-occupation/296888/ON

**[Inference]** 21234 is the cage next to Plan C if the artifact is CMS/theme/front-end. Official weather is worse, and Job Bank itself names AI/low-code as a demand drag.

### 1.4 Indeed Hiring Lab (Canada, 26 Aug 2025)

**[Evidence]** https://www.hiringlab.org/en-ca/2025/08/26/canadian-tech-hiring-freeze-continues/

- Canadian tech postings on Indeed, 15 Aug 2025: **19% below** Feb 2020.  
- Software engineer postings (most common tech title): **−51%** vs early 2020.  
- Web / .NET / front-end developer titles fell by even more.  
- Junior/standard tech titles: **−25%** vs early 2020. Senior/manager titles: **+5%**.  
- Tech employment in LFS “professional applied science (except engineering)” still **+35% vs 2019**, but **flat since mid-2022**. The freeze has hit *seekers and job-switchers* harder than employed headcount.

**[Evidence]** Indeed 2026 Canadian Jobs & Hiring Trends (18 Dec 2025): software-development postings were among occupations remaining weak vs early 2020; 37% of software-development posts mentioned AI as of 30 Nov 2025. https://hiringlab.indeed.com/en-ca/2025/12/18/indeed-2026-canadian-jobs-hiring-trends-report/

**[Inference]** Official “Limited / Very limited” and Indeed’s freeze describe the same weather. Senior seats held up better than junior. A 2-year operator with no logo and no degree is applying into the **weak side** of a two-speed market.

### 1.5 Rate-card texture (not a posting)

**[Evidence]** Robert Half Canada 2026 “most in-demand” list still includes Software Engineer / Developer, Canada band **$86,250–$131,500**, with .NET, AI literacy, CI/CD, Azure/AWS named as posting tokens. https://www.roberthalf.com/ca/en/insights/research/most-in-demand-tech-jobs-in-canada  

Toronto Back End Developer RH bands: low $99,085 / mid $111,340 / high $142,891. https://www.roberthalf.com/ca/en/job-details/back-end-developer/toronto-on

Treat RH as a staffing-firm rate card, not LFS.

---

## 2. Is “Product Engineer” a real Canadian title?

**Short answer:** it is a **real title at Canadian and Canada-hiring product-SaaS companies**. It is **not** bank / Big-5 / most Canadian enterprise language. Those shops say Software Developer, Full Stack Developer, Application Developer. Shopify-class Canadian product companies historically say **Developer**, not Engineer (Ontario P.Eng. friction is one reason).

### 2.1 Where the title actually appears (this pass)

| Employer | HQ / listing | Title used | Source |
|---|---|---|---|
| Docebo (TSX/NASDAQ: DCBO) | Toronto hybrid | Staff / Senior Product Engineer | Ashby, live |
| Faire | Toronto + Kitchener-Waterloo | Product Engineer; Staff Product Engineer | Greenhouse, live |
| Ashby | Remote-Canada (lists Toronto among cities) | Senior / Staff Product Engineer | Ashby, live |
| Wealthsimple | Remote Canada / Toronto HQ | **Senior Software Developer — Product Engineering** (org name, not title) | Ashby, live |
| Linear | US + Europe remote; **not Canada** | Senior / Staff Product Engineer | Ashby, live (US comparator) |
| RBC / TD / BMO (this pass) | Toronto Workday | Software Developer / Full Stack Engineer **intern/co-op**; no “Product Engineer” FTE found | Workday |

**[Evidence]** Docebo, Faire, Ashby postings in §3. Wealthsimple: https://jobs.ashbyhq.com/wealthsimple/9f45d7bf-788e-456c-97d3-8fba8b88387d uses “Product Engineering” as the **department** and “Software Developer” as the **title**.

**[Evidence]** RBC Winter 2027 student posting (Toronto, posted 2026-08-17): titles offered are Full Stack / Android / iOS / API / Web / Hadoop / Automation **Developer**. Gate: “Currently enrolled at a Canadian post-secondary institution with a focus on computer science, engineering, or technology.” https://rbc.wd3.myworkdayjobs.com/en-US/rbcearlytalent1/job/TORONTO-Ontario-Canada/XMLNAME-2027-Winter-Student-Opportunities-Technology---Operations---Software-Developer--8-Months_R-0000184557-2

**[Evidence]** BMO Capital Markets Winter 2027 Full Stack Engineer intern (Toronto, posted 2026-08-26): enrollment + graduation 2027–2029 in CS/Math/Physics/Statistics/Engineering; Canadian work authorization without future sponsorship. https://bmo.wd3.myworkdayjobs.com/en-US/privileged/job/Toronto-ON-CAN/BMO-Capital-Markets-Winter-2027--Full-Stack-Engineer--Toronto_R260021769

**[Inference]** “Product Engineer” in 2026 Canada clusters at: (a) Canadian public SaaS that has absorbed US startup language (Docebo), (b) US product companies with Toronto/KW offices (Faire), (c) US remote-Canada startups (Ashby). The **job** exists more widely under Software Developer / Full-Stack Developer. Searching only “Product Engineer” in GTA will under-count seats and over-weight a small SaaS cluster.

**[Hypothesis]** An ATS at RBC/TD that sees “Product Engineer” on a résumé without a CS degree and without a bank stack (Java/.NET) will not auto-map it to their Developer reqs. Translation to “Software Developer — full stack, production systems” is the applicant’s job.

**[Evidence — title law, not a posting]** Ontario PEO treats unlicensed use of “Software Engineer” as restricted. Not re-fetched as HTML this pass; canonical FAQ: https://www.peo.on.ca/public-protection/complaints-and-illegal-practice/unlicensed-practice-enforcement-faq  
**[Inference]** That is one reason Shopify/Wealthsimple say Developer. Banks and US-owned ATS pages still post Engineer constantly. Enforcement is uneven.

---

## 3. Product Engineer

### 3.1 Postings / sources

#### P1 — Faire, Product Engineer (Brand) — Toronto / KW

- **URL:** https://boards.greenhouse.io/faire/jobs/8654106002?gh_jid=8654106002  
- **Employer:** Faire  
- **Location:** Kitchener-Waterloo, ON; Toronto, ON. Hybrid 3 days/week.  
- **Published:** 2026-07-28 (Greenhouse / search index). Live page fetched 2026-09-22.  
- **Salary:** Canada **$129,500–$178,000** + equity + benefits.  
- **Degree:** “A bachelor's degree in Computer Science/Software Engineering **or equivalent industry experience**.”  
- **YOE:** **2+ years**.  
- **Stack:** Kotlin, Java, Javascript; JUnit, Hibernate, Guice, Jersey; React, NextJS; HTTP/JSON/Protobuf; MySQL, CockroachDB; AWS. “Proficient in at least one of Java, Kotlin, or JavaScript.” Agentic coding tools.  
- **Responsibilities (quote):** “planning and building features end-to-end, working alongside product, design, and data”; “Build features across multiple stacks, potentially including Backend, Frontend, and Mobile”; “Experience driving product improvements end to end, including deciding what problems are worth solving and how to solve them.”  
- **Interview hints:** not specified on the JD.  
- **Object:** product + optional backend/frontend/mobile. Combined architecture is allowed; frontend-only is also allowed by the posting.

#### P2 — Faire, Staff Product Engineer (Brand) — Toronto / KW

- **URL:** https://boards.greenhouse.io/faire/jobs/8777008002?gh_jid=8777008002  
- **Employer:** Faire  
- **Location:** KW + Toronto.  
- **Published:** 2026-09-02. Live page fetched 2026-09-22.  
- **Salary:** Canada **$190,500–$262,000** + equity.  
- **Degree:** bachelor’s CS/SE **or equivalent industry experience**.  
- **YOE:** **5+ years**.  
- **Responsibilities (quote):** “helping teams execute on our hardest features, coaching engineers, and working alongside product, design, and data”; pillar-level, “supporting different teams from quarter to quarter.”  
- **Object:** staff-level product ownership + coaching. Not a 2-year seat.

#### P3 — Docebo, Senior Product Engineer I — PHP — Toronto

- **URL:** https://jobs.ashbyhq.com/docebo/71b7c563-ae1d-4840-b999-49d950e4c1e1  
- **Employer:** Docebo (TSX/NASDAQ: DCBO)  
- **Location:** Toronto, Ontario (hybrid Tue–Thu).  
- **Published:** 2026-06-18 (Ashby metadata). Live meta-description extracted 2026-09-22.  
- **Salary:** **CA$102,800–$137,000**.  
- **Degree:** “Bachelor’s degree in Computer Science or Software Engineering **(or have the equivalent ‘in-the-trenches’ experience)**.” Preferred/bonus, not a hard must in the Superpowers list.  
- **YOE:** **4+ years** Backend or Full Stack.  
- **Stack:** **PHP required** (“willing to work with PHP”); Java/Python/JS valued; bonus Docker/K8s/Terraform.  
- **Responsibilities (quote):** “Near Zero Handovers”; “design and deploy solutions”; “Monitor and troubleshoot live applications”; sprint planning / stand-ups.  
- **Interview hints:** not in the extracted body for this req (Staff PE below has a four-step loop).  
- **Object:** SaaS product engineering with a **PHP specialization gate**. Combined product+backend, but the language is a hard skill gate.

#### P4 — Docebo, Senior Product Engineer I — Automation — Toronto

- **URL:** https://jobs.ashbyhq.com/docebo/f98c67f0-3ee3-4f3e-aaec-9b10c15d9f9d  
- **Employer:** Docebo  
- **Location:** Toronto hybrid; “Based in Canada” as timezone anchor vs Italy.  
- **Salary:** **CA$102,800–$137,000** + bonus (Ashby compensation field).  
- **Degree:** not listed in Superpowers.  
- **YOE:** **4–8 years**, “deep expertise in Go” + PHP working knowledge.  
- **Stack:** Go, PHP, AWS, Kubernetes, DynamoDB, PostgreSQL, MySQL; Datadog; SLOs.  
- **Responsibilities (quote):** “architect, build, and scale business-critical **backend systems** in Go and PHP”; “establish SLOs”; “Tier-1 customer escalations”; “domain-driven architectures at enterprise scale.”  
- **Interview:** Talent 30m → HM + senior SWE 60m → “Technical Deep Dive & System Design” with Product Engineering → Engineering Leadership.  
- **Object:** this title says Product Engineer and the work is **backend/automation/platform**. Specialization toward K8s + distributed services.

#### P5 — Docebo, Staff Product Engineer — Toronto

- **URL:** https://jobs.ashbyhq.com/docebo/1492f67d-1b4e-4f6b-af70-bb1a2bcdf73d  
- **Employer:** Docebo  
- **Location:** Toronto.  
- **Published:** 2026-08-12.  
- **Salary:** **CA$148,100–$197,500**.  
- **Degree:** Staff loop text (extracted) refers to “equivalent practical experience” on the interview/education line.  
- **YOE:** **10–12+ years** full-stack SaaS, shipped end-to-end.  
- **Stack:** PHP, Node.js, Golang, Angular, React, serverless, AWS, Kubernetes, observability; PostHog/Amplitude.  
- **Responsibilities (quote):** “define product direction”; “full-stack architecture”; “Engage directly with internal stakeholders and customers”; “Institutionalize AI-assisted development.”  
- **Interview:** Talent 30m → HM 60m → “technical and architectural assessment” (system design, AI leverage) → panel on collaboration / product strategy / leadership.  
- **Object:** staff product+architecture. Not a 2-year seat.

#### P6 — Ashby, Senior Product Engineer — Remote Canada

- **URL:** https://jobs.ashbyhq.com/Ashby/272bc3f4-5af6-4c14-b797-a424b62d306c  
- **Employer:** Ashby (US company; Canada payroll).  
- **Location:** Remote — Canada (lists Waterloo, Montreal, Calgary, Vancouver, Toronto, Edmonton).  
- **Compensation field:** **CA$195,000–$248,000 + equity**.  
- **Degree:** **absent**. “I studied computer science to solve problems, not tickets” is founder colour, not a requirement.  
- **YOE:** no number. Explicit anti-junior: “More than 90% of the team would be considered Senior or above… mentorship opportunities are very limited.” “You haven’t led or taken ownership of projects before” is a do-not-apply.  
- **Stack:** TypeScript, React, GraphQL, Node.js, Postgres, Redis. Prior stack not required.  
- **Responsibilities (quote):** “own projects end-to-end (wearing hats traditionally worn by product and design)”; “research competitors, write product specs, make wireframes”; examples include interview-scheduling constraint solver and “declarative filter architecture… compile it to SQL.”  
- **Interview (quote):** “There are no leetcode or whiteboard exercises.” Loop: HM 15–30m → 1h pair in **their actual codebase** → 3h15 product thinking / technical design / infrastructure.  
- **Object:** combined product + backend architecture. The filter→SQL example is the domain-core analog of an eligibility compiler.

#### P7 — Ashby, Staff Product Engineer — Remote Canada

- **URL:** https://jobs.ashbyhq.com/ashby/448baa35-cd72-468a-bcab-51dd55b7a275  
- **Published:** 2026-04-30.  
- **Compensation:** **CA$256,000–$380,000 + equity**.  
- Same JD body as Senior; Staff is a level/comp band, not a different job description.  
- **Object:** same combined architecture; years/scope implied by Staff pay.

#### P8 — Linear, Senior / Staff Product Engineer — US/Europe remote (US comparator)

- **URL:** https://jobs.ashbyhq.com/linear/12f8f208-0b9c-4569-bb3d-41c8a197029e  
- **Employer:** Linear  
- **Location:** “open to candidates based in the **US and Europe**.” Not Canada. Published 2026-03-04.  
- **Salary:** “Competitive salary and equity.” No CAD band.  
- **Degree:** **absent**.  
- **YOE:** **5+ years** “building customer-facing products at a **high-quality software company**.”  
- **Stack:** React, TypeScript, Node, GraphQL, PostgreSQL, MobX, Temporal, Redis, GCP/k8s.  
- **Responsibilities (quote):** “Work closely with founders and design”; “driving complex, end-to-end features (not just incremental improvements and refactors)”; “Comfortable working without heavy PM overhead.”  
- **Interview hints:** Linear publishes work-trial process: https://linear.app/now/how-we-hire-at-linear and https://linear.app/blog/why-and-how-we-do-work-trials-at-linear  
- **Object:** combined product+full-stack. The “high-quality software company” phrase is a **logo/bar gate**.

### 3.2 Stated vs preferred vs likely hard gates

| Gate | Stated | Preferred | Likely hard (inference) |
|---|---|---|---|
| Degree | Faire: BA or equivalent. Docebo PHP: BA or “in-the-trenches.” Ashby/Linear: absent. | CS tokens help ATS. | **Equivalent clause is real at Faire/Docebo.** Ashby/Linear will not ATS-reject on empty education. Banks (not in this family) will. |
| Years | Faire IC 2+; Docebo Senior 4+ / Staff 10–12+; Linear 5+; Ashby unlabeled but anti-junior. | “Shipped SaaS end-to-end.” | **2 years only clears Faire-shaped IC**, not Docebo Senior / Ashby Senior / Linear. |
| Stack | Docebo PHP or Go; Faire Java/Kotlin/JS; Ashby/Linear TS+React+Postgres. | Agentic AI tools now **stated** at Faire, Docebo, Ashby. | Language match is a hard screen at Docebo PHP. Ashby says they retrain from Swift/Kotlin. |
| Ownership | End-to-end, specs, users. | Mentorship at Staff. | **Ticket-only / CMS / agency** fails the “deciding what problems are worth solving” line. |
| Interview | Ashby: no LeetCode, pair-in-repo + product/design. Docebo Staff: system design. Linear: work trial. | — | Production walkthrough of Tower is in-family for Ashby/Faire. DSA still appears at Big Tech / some banks (not sampled as live FTE this pass). |

### 3.3 Junior / intermediate / senior split

**[Evidence]** Faire is the only Canada Product Engineer IC in this file that posts **2+ years**. Docebo’s “Senior I” starts at 4+. Ashby’s Canada PE roles are a senior-weighted team by their own writing. Linear starts at 5+ at a “high-quality software company.”

**[Inference]**

| Level | What the 2026 Canada/US-remote sample is actually hiring | 2-year operator fit |
|---|---|---|
| Junior | Almost absent in Product Engineer title. Indeed: junior tech titles −25%. | Not this title. Adjacent: junior Software Developer / web (21234 cage). |
| Intermediate | Faire 2+ “or equivalent industry experience.” | **The reachable Product Engineer seat** if Tower is a real product. |
| Senior | Docebo 4–8, Wealthsimple-class 5+, Ashby unlabeled senior, Linear 5+. | Under the number unless they count founder ownership as compressed seniority. |
| Staff | Faire 5+ and $190k+; Docebo 10–12+; Ashby Staff $256k+. | No. |

### 3.4 Combined vs specialized

**[Inference]** True Product Engineer (Faire Brand, Ashby, Linear) preserves **product + full-stack ownership**. The same title at Docebo Automation is already a **backend/K8s specialization**. Faire’s posting *permits* frontend-only. Filter: if the JD never mentions schema, jobs, or API contracts, it is a frontend Product Engineer.

### 3.5 How a 1-person founder (eligibility monitoring + reactivation) is read

**[Inference]** Continuous **if** the story is: domain model of eligibility states, jobs that must not double-fire, a product surface consultants use, incidents at 2am, iteration from field failures. That is Faire’s “end-to-end” and Ashby’s “filter architecture compiles to SQL.”

**[Inference]** Conceptually similar if Tower is a thin UI over someone else’s CRM with Zapier-class automation. Same words (workflows, customers), different object.

**[Inference]** Discounted if the résumé lead is “Founder/CEO, Omcoda” without engineering artifacts; if there is no second engineer to evidence review culture; if the stack is PHP/Go/Java and the applicant is TS/Python-only (Docebo PHP is a hard example). Ashby’s interview (pair in *their* repo + product spec) is the friendliest translation mechanism in this family. Linear’s “high-quality software company” is a logo discount against a 1-person firm.

---

## 4. Software Engineer / Software Developer

### 4.1 Postings / sources

#### S1 — Wealthsimple, Future Opportunities: Senior Software Developer — Product Engineering

- **URL:** https://jobs.ashbyhq.com/wealthsimple/9f45d7bf-788e-456c-97d3-8fba8b88387d  
- **Employer:** Wealthsimple  
- **Location:** Remote (Canada). Hybrid company, Toronto HQ.  
- **Published:** 2026-07-06. Talent-pool posting (not a single open req).  
- **Salary:** **CA$151,200–$189,000 + equity**.  
- **Degree:** **absent**.  
- **YOE:** **5+ years** “shipping production systems that real users or businesses depend on”; “operated as a senior contributor on a team.”  
- **Stack:** React / React Native; Ruby on Rails; Kotlin/Java nice-to-have; other languages accepted if willing to ramp. AI-agentic workflow is a stated bring.  
- **Responsibilities (quote):** “own meaningful slices of the product end-to-end”; “build Ruby services that handle core business logic and integrations, while also shipping React and React Native”; “regulatory and compliance requirements, complex data structures… reconciliation.”  
- **Interview hints:** AI may screen applications; humans make final decisions. No loop published.  
- **Object:** combined product+backend in a regulated domain. Canadian title = Developer.

#### S2 — Wealthsimple, Senior Software Developer — Cards

- **URL:** https://jobs.ashbyhq.com/wealthsimple/062a74c6-65e3-4210-bfb3-e0f1af9fe732  
- **Employer:** Wealthsimple  
- **Location:** Toronto Headquarters; workplace Remote (Ashby fields).  
- **Salary (Ashby field):** **CA$151,200–$189,000 + equity**.  
- **Degree:** not in the short extracted description.  
- **YOE / domain:** “Experience building and owning backend systems in a payments, card, or financial services environment” — **domain years**, not generic YOE.  
- **Stack:** Ruby on Rails or comparable; React/RN a plus.  
- **Responsibilities (quote):** “own meaningful slices of the card stack end to end — from card issuance and authorization through transaction processing, disputes, rewards, and card lifecycle management. This is not a features-on-top-of-a-BaaS role.”  
- **Object:** backend/domain specialization (cards). Combined product ownership of that slice.  
- **Note:** full JD body was only 228 characters in the meta description; treat quotes as the live excerpt, not a complete posting.

#### S3 — Harvey, Staff Software Engineer, Full Stack — Toronto

- **URL:** https://jobs.ashbyhq.com/harvey/01f31ece-f3fe-4991-b6fb-b59f21faa8e9  
- **Employer:** Harvey (US legal-AI; Toronto office).  
- **Location:** Toronto hybrid, 3+ days. Relocation assistance. Canadian work rights; **no visa sponsorship**.  
- **Published:** 2026-02-11. Live description extracted 2026-09-22.  
- **Salary:** **CA$196,800–$295,200** + possible bonus + equity.  
- **Degree:** “5+ YoE **(post-BS/MS)**” — degree is **assumed in the years formula**, not listed as a separate required document.  
- **YOE:** 5+ post-degree in “product focused full-stack.”  
- **Stack:** React, TypeScript, Tailwind, Python.  
- **Responsibilities (quote):** “shaping the foundation of our product platform while directly building user-facing features”; notifications, permissions, feature flags; “enterprise-grade collaboration product experiences for law firms.”  
- **Object:** full-stack **and** platform. Combined, with a platform tilt.

#### S4 — RBC, 2027 Winter Student — Software Developer, 8 Months — Toronto

- **URL:** https://rbc.wd3.myworkdayjobs.com/en-US/rbcearlytalent1/job/TORONTO-Ontario-Canada/XMLNAME-2027-Winter-Student-Opportunities-Technology---Operations---Software-Developer--8-Months_R-0000184557-2  
- **Employer:** RBC  
- **Location:** Toronto (RBC Centre).  
- **Posted:** 2026-08-17. Deadline 2026-09-21.  
- **Salary:** not posted (student/co-op).  
- **Degree:** **enrollment-gated** — “Currently enrolled at a Canadian post-secondary institution with a focus on computer science, engineering, or technology.” Transcript required.  
- **YOE:** student.  
- **Stack:** generic SDLC / languages / databases.  
- **Responsibilities:** pipeline into Full Stack, Android, iOS, API, Web, Hadoop, Automation Developer.  
- **Object:** bank Developer, not Product Engineer.  
- **Why it is in the file:** this is the **visible RBC Software Developer language** in September 2026. A dedicated experienced-hire FTE Developer req was **not successfully fetched** this pass (searches returned campus posts). Do not infer FTE degree language from this intern post alone.

#### S5 — BMO, Junior Software Developer, Winter 2027 Co-op — Toronto

- **URL:** https://bmo.wd3.myworkdayjobs.com/en-US/privileged/job/Toronto-ON-CAN/Junior-Software-Developer--Winter-2027--Co-op-Internship----4-Months_R260024650  
- **Posted:** 2026-08-20. Deadline 2026-09-20.  
- **Salary field:** $50,100–$93,000 (Workday band; intern reality is the low end).  
- **Degree:** “Only students currently enrolled… returning to their studies.” Graduates redirected to new-grad page.  
- **YOE colour:** “As a full-time employee, we would require **3–5 years** of experience, however as part of the BMO campus program…”  
- **Object:** campus door. Useful as a stated FTE years hint (3–5) from the same JD.

#### S6 — Job Bank / COPS / Ontario labour (occupation, not a vacancy)

See §1. Primary URLs already listed. This is the official “Software Developer” occupation the banks and product companies both map into.

#### S7 — Indeed Hiring Lab + Robert Half 2026 (market, not a vacancy)

See §1.4–1.5.

### 4.2 Stated vs preferred vs likely hard gates

| Gate | Stated | Preferred | Likely hard |
|---|---|---|---|
| Degree | Job Bank “usually required.” Harvey years counted “post-BS/MS.” Wealthsimple absent. RBC/BMO campus: **enrollment**. | CS for bank ATS. | **Campus doors are closed without enrollment.** Wealthsimple-class FTE is equivalent-friendly. Bank FTE education box was **not directly observed** this pass. |
| Years | Wealthsimple Senior 5+; Harvey Staff 5+; BMO colour 3–5 FTE. | “Senior contributor on a **team**.” | Wealthsimple’s “on a team” is a **collaboration gate** against 1-person founder. |
| Domain | Cards: payments/card rails. Harvey: legal/enterprise SaaS. | Regulated-systems comfort. | Cards is a **domain-years** seat. Generic Tower ≠ card authorization. |
| Stack | Rails/React at WS; Python/TS at Harvey; Java/.NET folklore at banks (RH 2026 still cites .NET). | AI-agentic workflow now stated at WS. | Stack mismatch is a screen. Domain core (eligibility) **is** transferable as a *systems* story, not as a *cards* story. |

### 4.3 Junior / intermediate / senior split

**[Evidence]** The live product-company Developer seats in this file are **Senior** (5+) or Staff. The live bank seats are **co-op**. Indeed: junior titles are the ones that collapsed.

**[Inference]** After ~2 years Plan B:

- Junior Software Developer at a non-product shop / agency: possible, and a 21234-adjacent cage.  
- Intermediate Developer at a Canadian product company: possible **if** production artifacts + interview. Wealthsimple Senior is above that.  
- Senior Developer at WS/Harvey: under the posted years unless founder-scope is credited.  
- Bank new-grad: enrollment-gated now; later, a completed CS degree opens the door. Bank experienced-hire: years + Java/.NET + regulated-envelope; conceptually similar, not continuous.

### 4.4 Combined vs specialized

**[Inference]** Wealthsimple Product Engineering preserves combined ownership. Wealthsimple Cards specializes to payments backend. Harvey Staff FS is combined with platform. RBC’s posting is a **bucket of specialized Developer types**. The family name “Software Engineer/Developer” does not preserve product+backend by itself.

### 4.5 Founder-read

**[Inference]** Continuous with Wealthsimple-style Product Engineering if Tower is a live regulated-adjacent domain (eligibility rules change; reconciliation; jobs). Conceptually similar to Cards (money movement vs eligibility state). Discounted by: no team, no Rails, “CEO” coding, missing 5 years. Harvey’s “post-BS/MS” years formula **under-counts** a founder who has no degree.

---

## 5. Backend Engineer / Backend Developer

### 5.1 Postings / sources

#### B1 — Harvey, Senior Software Engineer, Backend — Toronto

- **URL:** https://jobs.ashbyhq.com/harvey/18454695-e72d-40a5-a6c1-99677ef516ad  
- **Employer:** Harvey  
- **Location:** Toronto hybrid 3+/2. Canadian work rights; **no sponsorship**.  
- **Published:** 2026-06-11 (search index). Live description extracted 2026-09-22.  
- **Salary:** **CA$164,000–$225,000** (extracted live). Search snippets also showed $164k–$246k; **use the live extracted $164k–$225k**.  
- **Degree:** “4+ years **(post-BS/MS)**” — degree assumed in the years count.  
- **YOE:** 4+ backend-focused on platform and/or product teams.  
- **Stack:** distributed systems, REST/gRPC, databases, scalable services; RBAC / feature flags / integrations as plus. Language not pinned in the extracted body.  
- **Responsibilities (quote):** “Design and build foundational backend infrastructure including authentication, permissions, feature flagging, notifications, and document management integrations”; “Build and evolve Harvey’s internal **product platform**”; “security, privacy, and system reliability… sensitive legal data.”  
- **Object:** backend **platform** that enables products — not frontend, not sales-SE, not data-only. Slight specialization toward platform/K8s-ish infrastructure (auth, flags) vs domain core.

#### B2 — Docebo, Senior Product Engineer I — Automation — Toronto

See P4. Title is Product Engineer; work is **backend systems in Go/PHP** with K8s/AWS. Include here as the GTA backend seat that does not say “Backend Engineer.”

#### B3 — Wealthsimple, Senior Software Developer — Cards

See S2. Backend/domain (issuance, authorization, lifecycle). Hard domain gate.

#### B4 — Faire Product Engineer (Brand) — backend option

See P1. Explicitly “Fullstack, Backend or Frontend.” Backend path: Java/Kotlin, Hibernate, Jersey, MySQL/Cockroach, AWS. Combined *or* specialized — candidate chooses.

#### B5 — Job Bank partner posting, “back-end developer,” Toronto (weak / possibly fake)

- **URL:** https://www.jobbank.gc.ca/jobsearch/jobposting/50248948  
- **Employer listed:** “Bluth Company” via CareerBeacon. Posted 8 Sep 2026. Advertised until 9 Oct 2026.  
- **Salary:** $70,000–$120,000. Hybrid.  
- **Degree:** “Bachelor’s degree in Computer Science or similar.”  
- **Stack:** Python, Java, Node.js, or Ruby; SQL/NoSQL.  
- **Note [Evidence]:** Job Bank disclaimer: “provided by a partner site. Job Bank is not responsible.” **“Bluth Company” is a sitcom firm (Arrested Development).** Do **not** treat this as a real employer. Kept only to show (a) Job Bank maps backend developer to **NOC 21234** in the sidebar (median $39.42/hr — the *web* wage), and (b) partner-feed quality is poor.

#### B6 — Robert Half Toronto Back End Developer 2026 bands

https://www.roberthalf.com/ca/en/job-details/back-end-developer/toronto-on — $99,085 / $111,340 / $142,891. Not a vacancy.

#### B7 — Smile.io, Senior Software Engineer — APIs (Canada remote) — **404**

- **URL attempted:** https://jobs.lever.co/Smile.io/360f0c21-af05-41e8-b3c8-5bbb2f238ed8  
- **Status:** **404 Not Found** on fetch 2026-09-22.  
- Search index still held a Canada-remote Rails/API JD (5 years Rails, JSON APIs, JWT/OAuth, Postgres, Kafka). **Do not treat as live.** If needed later, start from https://jobs.lever.co/Smile.io (board root not fetched).

### 5.2 Stated vs preferred vs likely hard gates

| Gate | Stated | Preferred | Likely hard |
|---|---|---|---|
| Degree | Harvey post-BS/MS years. Job Bank 21232 “usually.” | CS knowledge (Harvey: “general Computer Science knowledge”). | Harvey’s formula **discounts non-degree years**. |
| Years | Harvey Senior 4+; Docebo Automation 4–8; WS Cards = domain experience. | “Operated” systems, not just written APIs. | 2 generic freelance CRUD years will not clear 4+. |
| Stack | Go+PHP+K8s at Docebo Automation; Rails/cards at WS; Java/Kotlin at Faire backend. | gRPC, RBAC, Datadog/SLOs. | **Language + “distributed systems” theatre.** A modular-monolith Tower is the right object and the wrong résumé slogan if the JD says microservices/K8s. |
| Interview | Docebo: system design. Harvey: not published. | Production debugging stories. | System design + coding. Live eligibility state machine is in-family; “I used Nest and Postgres” is not. |

### 5.3 Junior / intermediate / senior split

**[Evidence]** No junior Backend Engineer title was fetched in the Canadian product-company sample. Seniors start at 4+.

**[Inference]** Intermediate backend at a small Canadian product company is the reachable Plan C, usually **posted as Software Developer / Software Engineer**, not “Backend Engineer.” “Backend Engineer” in GTA 2026, in this sample, is a **senior/platform** label (Harvey, Docebo Automation).

### 5.4 Combined vs specialized

**[Inference]** Harvey Senior Backend still “ship user-facing features” — combined-leaning platform. Docebo Automation specializes to backend+K8s. Cards specializes to payments. A 1-person founder who needs Plan C to stay on **domain core + product** should avoid JDs whose first six bullets are Kubernetes, DynamoDB, and SLOs unless they actually operated that control plane.

### 5.5 Founder-read

**[Inference]** Continuous if Tower’s backend is the product: schema of pathways, idempotent jobs, API contracts, failed-job stories, tenancy. Conceptually similar if the work was integrations/CRUD for SMBs. Discounted if: no tests, no observability, résumé says “distributed microservices” for a single deployable (hiring managers who can tell will score that negative), or the years formula is post-BS/MS.

---

## 6. Full-Stack Engineer (backend/product ownership only)

Filter applied: excluded frontend-only, CMS, and “full stack” that is theme+WordPress. Included only JDs that own APIs/schema/jobs **and** a user surface.

### 6.1 Postings / sources

#### F1 — Wealthsimple Senior Software Developer — Product Engineering

See S1. Quote: “Whether you lean frontend or backend, you'll be expected to contribute meaningfully across the stack.”

#### F2 — Faire Product Engineer (Brand)

See P1. “Build features across multiple stacks, potentially including Backend, Frontend, and Mobile.”

#### F3 — Harvey Staff Software Engineer, Full Stack — Toronto

See S3. Platform + user-facing. 5+ post-BS/MS.

#### F4 — Ashby Senior Product Engineer — Remote Canada

See P6. “You’re not afraid to tackle any part of a technology stack.”

#### F5 — Dimely, Founding Engineer, Full-Stack — Toronto (also a Founding seat)

- **URL:** https://zerogtalent.com/ai-jobs/dimely/founding-engineer-full-stack-remote-hybrid-san-francisco-77291  
- **Employer:** Dimely (YC S24). **This is an aggregator reprint**, not Dimely’s own ATS. Dates on the page: listed Mar 24, 2026 / Aug 12, 2026; page said “Posted 6 months ago” on fetch. **Primary Dimely career URL was not found this pass.**  
- **Location:** Toronto, on-site / in person.  
- **Salary:** **C$100,000–$120,000** + “meaningful equity.”  
- **Degree:** **absent**.  
- **YOE:** aggregator tag “3+ yrs Mid.” Body: fourth hire; own product areas end-to-end.  
- **Stack:** TypeScript, Next.js, React; Postgres implied; NetSuite/Salesforce/QuickBooks/Stripe integrations.  
- **Responsibilities (quote):** “You will own product areas end to end: talk to the customer, understand the problem, decide what to build, make the architectural call, ship it, and confirm it works in production.” “Infrastructure for workflows that may span multiple systems and require retries, idempotency, and failure recovery.”  
- **Object:** **combined product + backend + field.** Closest commercial analog to Tower (unstructured rules → validated state → activation in other systems).

#### F6 — Element Fleet, Full Stack Developer — Toronto — **Workday posting unavailable on fetch**

- **URL:** https://elementfleet.wd3.myworkdayjobs.com/en-US/external_career_site/job/Toronto/Full-Stack-Developer_R105901  
- **Fetch 2026-09-22:** Workday shell loaded with **`postingAvailable: false`**. Search index (published 2026-09-01) had held: Toronto, 1 Adelaide St. E; **bachelor’s CS/IT or equivalent practical experience**; **minimum 5 years** API/back-end; APIs/microservices; **base $62,600–$86,000**.  
- **Do not treat as a confirmed-live vacancy.** If the index was accurate, it is an enterprise GTA full-stack with a **low cash band** and a real backend bar — the opposite of Harvey/Ashby.

#### F7 — BMO CM Full Stack Engineer intern — Toronto

See S5 sibling: https://bmo.wd3.myworkdayjobs.com/en-US/privileged/job/Toronto-ON-CAN/BMO-Capital-Markets-Winter-2027--Full-Stack-Engineer--Toronto_R260021769  
Enrollment-gated. Useful as bank **title** (they will say Engineer on a campus req) not as a Plan C FTE.

### 6.2 Stated vs preferred vs likely hard gates

Same table as Product Engineer + Software Developer, with two extras:

- **[Inference]** “Full stack” at Element-class enterprise (if that JD was real) can mean API + a UI in a Java/.NET estate, PM-heavy, low pay. Combined in name, specialized in practice.  
- **[Inference]** AI-assisted coding is now a **stated** requirement (Faire, Wealthsimple, Docebo, Dimely), not a nice-to-have.

### 6.3 Junior / intermediate / senior split

**[Evidence]** Live full-stack *product* seats in this file start at Faire 2+ or Dimely founding (unlabeled, ~3+ on the aggregator). Employed senior full-stack at WS/Harvey/Ashby is 5+ or “already senior.”

**[Inference]** The junior full-stack market is the 21234/agency market Job Bank calls Very limited. Do not use “Full-Stack Engineer” as a junior Plan C target title.

### 6.4 Combined vs specialized

**[Inference]** This family’s inclusion filter *is* the combined test. Failures: frontend-only Faire option; Harvey platform-only if the candidate never ships user features; Docebo Automation (backend title-inflation of Product Engineer).

### 6.5 Founder-read

**[Inference]** Continuous with Faire IC, Dimely founding, Ashby PE, WS Product Engineering **when Tower is a product**: users, domain model, jobs, integrations, operation. Dimely’s “unstructured contract terms → validated billing state → sync to finance systems” is the closest **posted** analog to “unstructured immigration facts → eligibility state → reactivation.” Discounted at Harvey/Ashby Senior on years and (Harvey) degree-years. Discounted at banks on stack and enrollment.

---

## 7. Founding Engineer

### 7.1 Postings / sources

#### FE1 — Publicus, Founding Builder — Toronto

- **URL:** https://hire.publicus.ai/  
- **Employer:** Publicus (gov procurement intelligence).  
- **Location:** Toronto.  
- **Stage (stated):** **Seed + Innovative Solutions Canada**. “80% month-over-month growth” is a company claim, not verified here.  
- **Salary / equity:** **CA$100k–$150k** + **0.5%–2%** equity.  
- **Degree:** **absent**.  
- **YOE:** **2–6 years**, “ideally at startups building software products.”  
- **Stack:** not pinned. AI-assisted development expected; “You manage agents to write code.”  
- **Responsibilities (quote):** “Traditionally, this would be called a founding engineer role.” “Not customer-facing — you're building the systems, agents, and infrastructure.” “One week: automated outbound pipeline. Next: a procurement data enrichment system.”  
- **Interview:** “A demo of the coolest thing you've built… No AI slop.”  
- **Object:** internal GTM/data systems as much as product. Combined builder, **not** field-FDE (they say not customer-facing).

#### FE2 — Uniflow Labs, Founding Engineer — AI/ML — Toronto

- **URL:** https://uniflow.tech/careers/founding-engineer-ai-ml/  
- **Employer:** Uniflow Labs.  
- **Location:** Toronto hybrid 2–3 days. Reports to CTO.  
- **Stage (stated):** **seed-stage**, “working execution substrate… pilot studies.”  
- **Salary / equity:** “Competitive, based on experience” + “Meaningful founding-team equity.” **No cash number.**  
- **Degree:** **absent**. Papers/projects requested.  
- **YOE:** **5+ years in ML/AI with production deployment.**  
- **Stack:** Python, PyTorch/JAX, RAG, LLMs, structured generation.  
- **Responsibilities (quote):** research-agent pipeline; RAG with provenance; claim validation.  
- **Object:** **ML specialization**, not product+backend generalist. Wrong family if the craft is Tower’s domain core.

#### FE3 — Dimely, Founding Engineer, Full-Stack — Toronto

See F5. YC S24, fourth hire, **C$100–120k + meaningful equity**, degree absent, customer-facing, TypeScript/Next. Aggregator, not primary ATS.

#### FE4 — Keplar, Founding Engineer — Toronto

- **URL:** https://jobs.ashbyhq.com/keplar/3a7fa25f-ce10-4a59-ab8b-072c62b5ac13  
- **Published (search index):** 2025-09-16 — **older than the rest of this scan.**  
- **Fetch 2026-09-22:** Ashby title resolved (“Founding Engineer @ Keplar”); **full JD body did not extract** (JS shell).  
- Search index had held: Toronto; Kleiner Perkins / SV Angel–backed (founded 2022); “competitive salary and meaningful early-stage equity”; voice interfaces / agents.  
- **Treat as a thin, possibly stale listing.** Do not quote index text as live.

### 7.2 Typical company stage, equity vs cash, degree posture

**[Evidence]** In the Canadian sample that actually loaded:

| Company | Stage | Cash | Equity | Degree | Years |
|---|---|---|---|---|---|
| Publicus | Seed + ISC | $100–150k | **0.5–2%** (rare public %) | Absent | 2–6 |
| Dimely | YC S24, 4th hire, “years of runway” | $100–120k | “Meaningful” | Absent | ~3+ (aggregator) |
| Uniflow | Seed, pilots | Unstated | “Meaningful founding-team” | Absent | 5+ ML |

**[Inference]** Founding Engineer in Toronto 2026 is a **seed / first-10-engineers** title. Cash is **below** Wealthsimple/Docebo/Faire Senior and **near** Job Bank median-to-high. The bet is equity. Publicus is the only one willing to print a percentage; 0.5–2% at seed is founder-adjacent, not employee-token.

**[Inference]** Degree posture: **absent** on every founding JD that loaded. The screen is a **demo of shipped systems**, not a PDF. This is the friendliest degree mechanism of the six families.

**[Hypothesis]** Many “Founding Engineer” posts are evergreen or recruiter-amplified (Keplar date; Dimely on a third-party board). Volume is thin versus Software Developer. The title is real and rare.

### 7.3 Stated vs preferred vs likely hard gates

| Gate | Stated | Preferred | Likely hard |
|---|---|---|---|
| Degree | Absent. | CS helps Uniflow ML. | **Demo / shipped product.** |
| Years | Publicus 2–6; Uniflow 5+ ML; Dimely unlabeled. | Startup, not agency. | Uniflow 5+ ML is a specialist gate. Publicus 2–6 is the open window. |
| Location | Toronto in-person/hybrid. | — | Remote-Canada founding seats were **not** in this sample. |
| Customer | Dimely yes; Publicus **no**; Uniflow research users. | High agency. | A founder who only wants field work will bounce off Publicus’s “not customer-facing.” |

### 7.4 Junior / intermediate / senior split

**[Inference]** Founding Engineer is **not leveled**. Publicus 2–6 years is intermediate-shaped. Uniflow 5+ is senior-shaped specialist. There is no junior founding engineer in this sample (early-stage companies cannot afford a trainee as hire #4).

### 7.5 Combined vs specialized

**[Inference]** Dimely = combined product+backend+customer (continuous with TSO). Publicus = builder of internal systems (can slide to GTM-eng / Type-3 FDE). Uniflow = ML specialist.

### 7.6 Founder-read

**[Inference]** This is the family that **most literally** reads a 1-person operator as in-distribution — *if* the demo is a live domain system. Publicus’s interview *is* “show us the thing.” Dimely’s problem (rules in messy documents → state → activation) is Tower-shaped.

**[Inference]** Discount risks: (1) they want a **#2 engineer in the room**, not another solo founder; (2) equity-for-cash only works if the subject wants employee-founder, not Omcoda; (3) “Founder” on a résumé without a product demo is discounted harder here than “Software Developer,” because the whole screen is the demo.

---

## 8. Forward-Deployed Engineer

### 8.1 Title-inflation numbers (re-found)

**[Evidence]** Bloomberry / Revealera, published 18 Nov 2025, **last updated 25 Jan 2026**, n≈1,000 FDE postings + n=100 LinkedIn profiles:

https://bloomberry.com/blog/i-analyzed-1000-forward-deployed-engineer-jobs-what-i-learned/

- Demand Jan–Oct 2025 vs 2024: **+1,165%** YoY.  
- Internal types: **Type 1 Builder ~60%**; **Type 2 Sales Engineer+ ~30%**; **Type 3 internal GTM/RevOps ~10%**.  
- Median disclosed salary **USD $173,816**. Equity in 70%; OTE in 8%; **quota in 0%** of the corpus they coded as FDE.  
- Years (among postings that specify): 0–2 **12%**; 3–5 **60%**; 6–8 **20%**; 9+ **8%**.  
- Org: dedicated FDE team 45%; engineering 38%; GTM/sales 14%; CS 7%; solutions/PS 7%.  
- Skills: Python 66%, TypeScript 35%, AWS 32%, GCP 22%, Azure 18%, K8s 14%, Docker 12%.  
- Responsibilities: customers 55%; build/deploy AI/ML 37%; integrate APIs 32%.  
- Company size: **58% at 11–200 employees**.  
- Feeder roles (n=100): **SWE 45%**; SE/SA 22%; DE/DS 15%; technical consultant 10%; **founder / early employee 8%**.

Type 1 markers (author synthesis): 70–90% coding, 30–50% travel, $140–250k. Type 2: 30–40% coding, <20% travel, $120–200k + commission.

**[Evidence]** Tandem, article dated 2026-08-10, modified 2026-09-07:

https://usetandem.ai/blog/fde-vs-implementation-engineer-vs-solutions-engineer

> “Titles are unreliable (**FDE postings grew 800%+ in 2025**, much of it relabeling), so use the **output test**, not the job title.”

Output test: (1) does work end at signature? → SE; (2) configure what exists vs build what doesn’t? → IE vs continue; (3) do custom builds feed the product roadmap? → real FDE, else services.

Practitioner split from nine interviews: day “splits roughly in half” customer / building. Scoping washes people out.

**[Inference]** Bloomberry’s 1,165% and Tandem’s 800%+ are the same phenomenon, different windows/corpora. Both warn that **the title is inflated**. Use output, reporting line, quota, and whether production code ships.

### 8.2 Postings / sources

#### FD1 — Salesforce, Forward Deployed Engineer (Mid/Senior) — Toronto

- **URL:** https://salesforce.wd12.myworkdayjobs.com/en-US/external_career_site/job/Canada---Toronto/Forward-Deployed-Engineer--FDE---Mid-Senior-Level-_JR356746  
- **Employer:** Salesforce  
- **Location:** Canada — Toronto.  
- **Published (search index):** 2026-08-27.  
- **Fetch 2026-09-22:** Workday page **rendered empty** (no job body). Quotes below are from the search index snapshot of that same URL, not from a successful HTML extract. **Treat as indexed, not re-verified.**  
- **Salary (indexed):** Ontario base **CAD $95,130–$145,130** (same band as Salesforce Canada SE in prior research).  
- **Degree:** not in the indexed snippet.  
- **YOE (indexed):** “**3+ years** (6–10 years for Senior levels) of software engineering or technical delivery… at least one production system you’d be proud to walk us through.”  
- **Stack (indexed):** agentic AI; Salesforce platform certs preferred (Admin, Platform Developer I, Agentforce); LangChain/LlamaIndex; Snowflake/Databricks/BigQuery.  
- **Responsibilities (indexed quote):** “experienced **Technical Builders** who design, build, and deploy agentic AI solutions directly inside enterprise customer environments”; “partnering closely with a Deployment Strategist”; “real code, real environments”; travel **~25%**.  
- **Object test:** production deployment + Salesforce platform. **Could be Type 1 or Type 2** depending on whether the work is Apex/config vs net-new product code. The Ontario cash band matching **SE**, plus Salesforce-cert preference, is a Type-2 risk. The “Technical Builder / production from day one” copy is Type-1 language.

#### FD2 — Palantir, Forward Deployed Software Engineer — New York (US comparator; original title)

- **URL:** https://jobs.lever.co/palantir/dab396d4-2f14-4796-aac0-0d82883dccf0  
- **Employer:** Palantir  
- **Location:** New York, NY (live Lever page fetched 2026-09-22).  
- **Salary:** **USD $135,000–$200,000** + RSUs / incentives.  
- **Degree:** “Strong engineering background, **preferred** in CS / Mathematics / Software Engineering / Physics / Data Science.” Not required.  
- **YOE:** **1+ years relevant, post-college work experience.**  
- **Stack:** Python, Java, C++, TypeScript/JavaScript.  
- **Responsibilities (quote):** “You’ll work in small, agile teams and own the end-to-end execution”; “Wrangling massive-scale data and using AI”; “Developing custom applications tailored to customer needs”; “Engaging directly with customer stakeholders, from technical teams to executives.” Travel up to 25%.  
- **Object:** Type 1 by definition (they coined it).  
- **Canada note:** Talentify index of a **Toronto** Palantir FDSE (https://www.talentify.io/job/forward-deployed-software-engineer-toronto-ontario-palantir-technologies-6088c126-3129-4dc6-93b7-a35f0cfa8789) said **“This job is now closed.”** No live Palantir Toronto FDSE was fetched on Palantir’s Lever board this pass.

#### FD3 — Palantir FDSE — other live Lever URLs (same JD family)

Fetched/indexed as live in search, not all opened:

- https://jobs.lever.co/palantir/8148182c-6127-4689-b615-7815a94173bb (Dubai)  
- https://jobs.lever.co/palantir/13f99633-43b5-4459-8e84-25073f257c18 (NY Warp Speed; US Person)  
- https://jobs.lever.co/palantir/d83fac1c-353e-4b77-a586-3276b1090b6e (US Government; clearance; $135–200k)

Same 1+ post-college, preferred STEM, strong-coder bar.

#### FD4 — Ethicrithm, Forward Deployed Engineer — Canada remote

- **URL:** https://jobgether.com/offer/6a805c0a490731f1e1a5561f-forward-deployed-engineer---canada  
- Experienced twin: https://jobgether.com/offer/6a960ebd0875ca77c4b49046-forward-deployed-engineer---experienced---canada  
- **Employer:** Ethicrithm Inc. (Palantir partner / delivery). Jobgether is an aggregator; datePosted in page JSON: **2026-08-15**.  
- **Location:** Remote Canada; travel ~5% Canada/US; no visa processing.  
- **Salary:** not posted.  
- **Degree:** not posted.  
- **YOE:** “experienced FDEs with real-life, recent **Palantir Foundry**” on the Experienced req.  
- **Stack:** Python and/or TypeScript; Palantir Foundry / AIP.  
- **Responsibilities (quote):** “deploying the Palantir platform”; “implementing data pipelines and building workflows and tools.”  
- **Object:** **partner/SI delivery of Palantir**, not Palantir core FDE. Type 1-ish coding possible; economic role is professional services. Closer to implementation of someone else’s platform than to founder-FDE of Tower.

#### FD5 — Bloomberry + Tandem (labour sources, not vacancies)

See §8.1.

### 8.3 Stated vs preferred vs likely hard gates

| Gate | Stated | Preferred | Likely hard |
|---|---|---|---|
| Coding | Palantir “strong coder.” Bloomberry: “If you can’t code, you can’t be an FDE.” | Python + TS. | **Coding interview.** Glue/SE without production code fails Type 1. |
| Degree | Palantir preferred STEM. | — | Not the gate. Coding + decomposition are. |
| Years | Palantir 1+ post-college; Salesforce indexed 3+ / 6–10; Bloomberry mode 3–5. | Production system you can walk through. | Canadian “FDE” at SI/partner: **platform tenure** (Foundry) can replace SWE years. |
| Quota / OTE | Bloomberry corpus: 0% quota. | — | If the live JD has OTE/quota → Type 2, whatever the title. Salesforce’s Ontario band matching SE is a smell; the indexed JD did not mention quota. |
| Travel | Palantir 25%; Salesforce ~25%; Ethicrithm ~5%. | — | GTA true-FDE volume is thin; US labs are work-authorization. |
| Feeder | Bloomberry: SWE 45%, founder 8%. | — | Founder is a **real but small** feeder. Independent Zapier is not in the table. |

### 8.4 Junior / intermediate / senior split

**[Evidence]** Bloomberry: junior 12%, mid 60%, senior 20%, staff 8%. Palantir’s 1+ is the exception (they run a new-grad-adjacent FDSE machine). Salesforce Toronto indexed as mid/senior.

**[Inference]** After 2 years, a Type-1 FTE FDE at a small product company is the optimistic continuous case **if the coding interview passes**. Palantir/Anthropic-class is not a 2-year default. Partner “FDE” (Ethicrithm) is more available and is **services**.

### 8.5 Combined vs specialized (true FDE vs relabeled SE)

Use Tandem’s output test + Bloomberry types:

| Signal | Type 1 Builder FDE | Type 2 relabeled SE | Type 3 internal |
|---|---|---|---|
| Output | Production code in customer env; feeds product | Demos/POC; handoff | Internal GTM tools |
| Comp | Base + equity | Base + OTE | Base |
| Reporting | Eng or FDE org | Sales | GTM/RevOps |
| This file | Palantir FDSE | Salesforce Toronto **at risk** (SE pay band + certs) | Publicus “Founding Builder” is internally facing — adjacent, not FDE |

**[Inference]** A GTA search for “Forward Deployed Engineer” will mix Palantir-partner delivery, Salesforce Agentforce builders, and leftover SE. The title alone does not preserve engineering.

### 8.6 Founder-read

**[Evidence]** Bloomberry feeder: founder/early employee **8%**. FDEs “have already learned to scope ambiguous problems, build with limited resources, and talk to customers.”

**[Inference]** Continuous **as founder-FDE of your own product** (Tower in the field, production code, on-call). Conceptually similar to Ethicrithm/Palantir-partner (deploy a platform in firms) if the applicant actually wrote Foundry/Python in production — which a Tower founder probably did not. Discounted at Palantir on: coding interview, “post-college,” no logo, GTA req closed. Discounted at Salesforce if they want Agentforce certs and 3–10 years “technical delivery.”

**[Hypothesis]** GTA true-FDE hiring volume is still thin. People exist; a pipeline is not established. This pass found **one** Canada-titled vendor FDE (Salesforce, body not re-fetched) and **one** partner FDE (Ethicrithm), plus closed Palantir Toronto.

---

## 9. Cross-family: how the 1-person Tower operator is read

Assume ~2 years, no CS degree yet, GTA, live eligibility-monitoring + reactivation system.

| Family | If Tower is a real operated product | If Tower is thin (CRM + scripts) |
|---|---|---|
| Product Engineer | **Continuous** with Faire-shaped IC (2+, or-equivalent). Under years for Docebo Senior / Ashby Senior / Linear. | Discounted to frontend/agency / 21234. |
| Software Developer | **Continuous** with Canadian product-company Developer (WS-class is 5+ — you will be mid, not Senior). Bank campus closed; bank FTE conceptual. | Junior Developer / web. |
| Backend | **Continuous** with domain-backend if schema/jobs/APIs are real. Harvey 4+ post-BS/MS under-counts. Docebo Automation is K8s-specialized. | CRUD freelancer; not Nue/Harvey-class. |
| Full-stack (real) | **Continuous** with Faire / Dimely / WS PE. | Agency full-stack. |
| Founding Engineer | **Most literally in-distribution** (Publicus 2–6, demo interview; Dimely analog). Cash $100–150k. | They will see no demo. Fatal. |
| True FDE | **Conceptually similar → maybe continuous** at a small product company if coding interview passes. Founder is an 8% feeder, not the mode. Palantir-by-default: no. | Relabeled SE/implementation. |

**[Inference]** The market does not pay a premium for “I was a founder.” It pays for **responsibilities it knows how to score**: production systems, users, incidents, schemas, end-to-end features. Recruiters will still code “Omcoda / CEO” as self-employed and under-count. Rewrite as engineering.

**[Inference]** Combined product+backend is preserved at Faire, Ashby, Linear, Wealthsimple Product Engineering, Dimely, Palantir FDSE. It is **not** preserved at Docebo Automation (backend/K8s), Wealthsimple Cards (payments), Publicus (internal tools), Ethicrithm (vendor platform), RBC Developer bucket, or 21234 web.

---

## 10. Fetch failures, 404s, and thin spots (do not invent around these)

| URL | What happened |
|---|---|
| https://jobs.lever.co/Smile.io/360f0c21-af05-41e8-b3c8-5bbb2f238ed8 | **404** |
| https://salesforce.wd12.myworkdayjobs.com/en-US/external_career_site/job/Canada---Toronto/Forward-Deployed-Engineer--FDE---Mid-Senior-Level-_JR356746 | Shell loaded, **empty body** |
| https://elementfleet.wd3.myworkdayjobs.com/en-US/external_career_site/job/Toronto/Full-Stack-Developer_R105901 | Workday **`postingAvailable: false`** |
| https://jobs.ashbyhq.com/keplar/3a7fa25f-ce10-4a59-ab8b-072c62b5ac13 | Title only; JD body not extractable; index date **2025-09-16** |
| https://jobera.com/job/greenhouse-senior-software-engineer-i-can-2026-4fbc51f5/ | Fetch **timed out**. Search had held Greenhouse Canada Senior FS $117.5–176.3k, 5+ years, Ruby/React/OpenSearch — **not used as a confirmed posting** |
| Palantir Toronto FDSE on Talentify | Marked **closed** |
| RBC/TD/BMO experienced-hire FTE Developer | **Not successfully fetched** this pass (campus posts only) |
| Shopify live Developer req | **Not fetched** this pass |
| https://www.jobbank.gc.ca/jobsearch/jobposting/50248948 | Live, but employer name **Bluth Company** is not credible |

Ashby pages are JS apps; several JDs were recovered from `<meta name="description">`, which matched the visible posting text on the boards that WebFetch also rendered (Faire Greenhouse was full HTML).

---

## 11. What is still not established

1. How Workday at RBC/TD treats an **empty education field** on an experienced-hire Developer req in Canada. Campus posts are enrollment-gated; that does not prove FTE.  
2. Live Shopify / Clio / KOHO / Thinkific / Wave FTE JDs this week.  
3. Whether Salesforce Toronto FDE is Type 1 or Type 2 — body not re-fetched.  
4. GTA true-FDE vacancy count as a time series.  
5. Whether two years of 1-person production **survives founder discount** in screening. Bloomberry’s 8% says it *can*; it does not say it *usually does*.  
6. Tower’s actual technical depth (out of scope; not inspected). Every “continuous” row above is conditional on that artifact.

---

*End of scan. 2026-09-22. No family is selected or eliminated.*
