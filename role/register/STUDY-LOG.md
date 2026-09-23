# Study Log — Running Inquiries & Primitive Breakdowns

**Purpose:** Living, append-only record of technical inquiries, first-principles deconstructions, primitive discoveries, and architectural mental models generated during the 40-hour foundations study.  
**Seat Responsible:** [`role/seats/STUDY-PARTNER.md`](../seats/STUDY-PARTNER.md)  
**Foundation Blueprint:** [`role/foundations/README.md`](../foundations/README.md)  

**Current (read first, then the newest stamp at the bottom):** 2026-09-23 17:00 UTC — Initialized. Foundational inquiry logged: *"Where is GitHub's code physically stored?"* and the deconstruction of *Language Primitives vs. Combinatorial Creativity*.

---

## 2026-09-23 16:50 UTC — Entry Posture & Language Primitives vs. Combinations

**Kind:** Founder Breakthrough / Mental Model.

**Founder Statement:**
> "I start to see why each thing exists... it’s just design. I'm going to put this here to be this thing for this other thing—like a class, an operation. But then after that, it's just math, logic, and rules... In Tower, I created my own DAG system with primitive elements. But what is fundamentally happening down to the grain? Is a Get node pulling, or is it an illusion? If you have an insufficient understanding of the primitives, things befuddle you. But once you know the primitives deeply, the other part is combinatorial creativity—using known primitives in non-canonical ways."

**Mechanical Reality:**
- **Layer 1 (The Primitives / Physics Engine):** A finite set of computational and runtime rules. In any language runtime, this is memory layout (stack vs. heap), execution pointers (call stack, event loop microtasks/macrotasks), type boundaries, and synchronous vs. asynchronous control flow. Primitives are bounded, observable, and masterable (90%+ comprehension achievable within a focused 40-hour block).
- **Layer 2 (The Combinatorial Space):** The infinite arrangement of those primitives to solve real-world problems. Experienced developers who claim a language still "befuddles" them after 20 years are either confusing the language's ongoing feature bloat with its core physics, or mistaking the infinite combinatorial space of software design for a failure of primitive mastery.

**Distilled Invariant:**
> Master the finite physics of the primitives down to the grain; enjoy the infinite combinatorial creativity of the architecture.

---

## 2026-09-23 17:00 UTC — Inquiry: "Where is GitHub's code physically stored?"

**Kind:** Inquiry / First Principles & System Mechanics.

**Founder Question:**
> "Where is GitHub's code even stored?"

**Mechanical Reality:**

When you type `git push origin main`, where do those bytes actually land on Earth?

1. **The Ingestion Boundary (The Edge & SSH/HTTPS Terminus):**
   - The push command opens a secure TLS or SSH connection hitting a GitHub proxy (running HAProxy or custom load balancers on GitHub IP space, primarily hosted in Microsoft Azure data centers alongside GitHub’s own enterprise data centers in North America—such as Ashburn, Virginia).
   - The connection authenticates your token or SSH key against GitHub’s auth service (`token-service` / GitHub Identity).

2. **The Git Storage Tier (Spokes & DGit):**
   - GitHub does **not** store your repository in an ordinary SQL database. Git is a content-addressable filesystem made of **blobs, trees, and commits** identified by SHA hashes.
   - GitHub built a proprietary distributed storage architecture originally called **Spokes** (and later enhanced into **DGit**). 
   - Spokes routes your push to a cluster of dedicated Linux storage servers running custom file services. A single repository does not live on one server; it is synchronously replicated across **three physical disk storage servers** in different fault domains.
   - On the storage server's Linux ext4/XFS filesystem, your repo lives as a **bare Git repository** (specifically stored in Git packfiles under `/data/repositories/...`).

3. **The Metadata Tier (MySQL / Vitess):**
   - While the raw code and commit history live on the Spokes disk servers, the relational metadata—pull requests, issue comments, user permissions, webhooks, repo settings, star counts—is stored in a massive **MySQL cluster horizontally sharded using Vitess** (an open-source database clustering system).
   - When you view a file on `github.com`, the Ruby on Rails web server queries MySQL/Vitess to check your read permissions, then queries the Spokes storage server via RPC to extract the Git blob from the packfile, syntax-highlights it, and sends the HTML to your browser.

4. **The Cold Backup & Durability Tier:**
   - Snapshots of raw repository packfiles and database backups are continuously mirrored into **Azure Blob Storage** (geo-replicated across multiple geographic regions) and cold storage archives to guarantee that physical hardware failure in any single data center cannot destroy code history.

**Distilled Invariant:**
> A GitHub repo is physically stored as bare Git packfiles on a 3x-replicated Linux storage cluster (Spokes/DGit), while its social and operational metadata is sharded across a massive MySQL/Vitess relational fleet, backed by geo-replicated object storage.
