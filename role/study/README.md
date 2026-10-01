# Role Study — Craft & Design Reading

**Document type:** LifeWriting Role execution (not research).  
**Status:** Active study shelf. Role Architecture research is complete; see [`../foundations/README.md`](../foundations/README.md) and [`../../research/combined-role-architecture.md`](../../research/combined-role-architecture.md).

This directory holds **books and long-form craft material** for the Technical Systems Operator identity: maintainable object-oriented design, patterns, dependency injection, legacy change, and code quality. These sit alongside the **40-hour foundations laboratory** (Travis, TypeScript primitives) and **C# coursework**—they deepen **combinatorial / design** mastery (Layer 2 in the foundations model), not the evidence dossiers in [`research/`](../../research/).

**Running record of study work:** [`../register/STUDY-LOG.md`](../register/STUDY-LOG.md)  
**Study Partner protocol:** [`../seats/STUDY-PARTNER.md`](../seats/STUDY-PARTNER.md)

---

## Materials on shelf (`materials/`)

| File | Focus | Tie to role spine |
|------|--------|-------------------|
| `clean-code.pdf` | Naming, functions, boundaries, error handling, tests | Product surfaces and backend code that stay diagnosable under production pressure |
| `Head First Design Patterns - … (2020).pdf` | OO patterns, extensibility | Modeling domain invariants without entangling UI, persistence, and policy |
| `Dependency Injection Principles.pdf` | Composition, testability, lifetimes | Aligns with C# / .NET and formal modular boundaries in systems work |
| `working-effectively-with-legacy-code.pdf` | Seams, characterization tests, incremental change | Operating existing codebases (Plan A/B, enterprise) without unbounded rewrites |

PDFs live under [`materials/`](materials/) so the repo root and `research/` stay text-first.

---

## How this relates to other Role paths

| Path | Role |
|------|------|
| [`foundations/`](../foundations/) | Conclusion, 40-hour plan, language anchors (TS / C# / Go), benchmark repos |
| [`study/`](.) | **This shelf** — assigned craft reading |
| [`register/STUDY-LOG.md`](../register/STUDY-LOG.md) | Append-only inquiries and breakthroughs from study (any source) |
| [`seats/STUDY-PARTNER.md`](../seats/STUDY-PARTNER.md) | Agent protocol for working through material |

When a book chapter produces a durable invariant or primitive insight, log it in **STUDY-LOG** with the book and chapter cited—not in `research/`.
