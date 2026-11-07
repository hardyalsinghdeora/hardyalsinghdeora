# Hardyal Singh

**Agentic AI Architect · Principal Software Engineer** · Ahmedabad, India · *open to new roles: remote, hybrid, or on-site in Pune, Bengaluru or Hyderabad*

I build LLM agents that are safe to leave running: grounded in retrieved evidence, bounded in
steps and cost, least-privilege by default, and auditable. Underneath that is fifteen years of
production backend engineering, most of it on the commercial side, where a duplicate write is a
duplicate invoice.

That backend discipline (idempotency, audit trails, rollback plans, cost budgets) is the part
most agent projects are missing, and it's what I bring to them.

**[Ask my portfolio agent anything about my work →](https://hardyalsinghdeora.pages.dev/)**
It answers from my career profile and shows the sources it used.

---

### AI agents and tooling

| | |
|---|---|
| **[Portfolio agent with hybrid RAG](https://github.com/hardyalsinghdeora/portfolio)** | A bounded Gemini function-calling loop on Cloudflare Workers. BM25 and embeddings fused by reciprocal rank fusion, cited sources, a prompt-injection guard, provider fallback to Claude, and a retrieval eval set run on every build |
| **Unattended PR-review agent** *(in daily use at work)* | TypeScript, Node.js and MCP. Reviews every open pull request on a 30-minute cadence, reads the linked ticket first, and posts severity-gated findings with file and line |
| **[AI pull request reviewer](https://github.com/hardyalsinghdeora/pr-review-extension)** *(built, not yet launched)* | Chrome extension with one structured-output review interface over Anthropic Claude, Google Gemini and local Ollama models, so a team picks its own cost, latency and privacy trade-off |
| **[claude-toolkit](https://github.com/hardyalsinghdeora/claude-toolkit)** | Ten dependency-free CLI tools that keep AI coding agents safe and cheap: a Keychain vault so an agent can *use* a credential without *seeing* it, read-only-by-default database access, output compression, offline indexes |
| **[Ops Copilot](https://github.com/hardyalsinghdeora/ops-copilot)** *(learning project)* | LangGraph supervisor with specialist agents over two MCP servers, hybrid retrieval, an LLM-as-judge reviewer and human approval before any ticket is filed |
| **[nanobanana-mcp](https://github.com/hardyalsinghdeora/nanobanana-mcp)** | MCP server that gives Claude image generation and editing through Gemini's image model |

### Backend and platform

Fifteen years in backend and platform engineering: orders, pricing, discounting, invoicing,
subscriptions, and the identity and access model underneath them, across 12+ domain services
behind one API gateway.

| | |
|---|---|
| **Commerce and billing** | Order and subscription data models, finance-auditable contract terms and proration, and a discount engine with a four-tier approval ladder from self-approval to C-suite sign-off |
| **Migration under load** | A MySQL to PostgreSQL migration across six product lines with no maintenance window: a re-runnable historical backfill kept separate from a continuous reverse-sync, with idempotency guards and drift detection. Partly live, the rest in pilot |
| **Architecture** | Domain-decomposed services behind a single gateway, so auth, rate limiting, schema validation and caching are solved once at the edge |
| **Access control and integrations** | Users → groups → organisations scoping across services; CRM, finance and HR systems behind ports and adapters |

**Written up:** [Moving a live commerce platform between two databases without a maintenance window](https://github.com/hardyalsinghdeora/case-studies/blob/main/migration-live-commerce-platform.md),
a decision record of what we rejected and why, the two-flows separation, the reconciliation
lesson, and what it cost.

#### Reference builds

Small, tested sample projects for the backend patterns I rely on, each with decision records and CI.

| Project | What it shows |
|---|---|
| **[spring-boot-order-service](https://github.com/hardyalsinghdeora/spring-boot-order-service)** | Order-to-cash REST API in Java 21 / Spring Boot 3: idempotency keys, `ETag` + `If-Match` optimistic locking, an explicit state machine, RFC 9457 errors, Flyway |
| **[api-gateway-rate-limiter](https://github.com/hardyalsinghdeora/api-gateway-rate-limiter)** | TypeScript / Hono gateway: token-bucket and sliding-window rate limiting, circuit breaker, jittered retries for idempotent methods, Prometheus metrics |
| **[event-outbox-worker](https://github.com/hardyalsinghdeora/event-outbox-worker)** | Transactional outbox with an at-least-once relay, dead-letter handling and an idempotent consumer |
| **[db-migration-reconciler](https://github.com/hardyalsinghdeora/db-migration-reconciler)** | Python CLI to verify a live database migration: keyset checksums, drill-down diffs and a dry-run-first, resumable repair |

#### Design interview prep, in TypeScript

Three repositories that work through the design rounds of backend interviews end to end:
requirements, diagrams, trade-offs and tested code.
- **[low-level-design](https://github.com/hardyalsinghdeora/low-level-design)**: 40 object-oriented
  design problems, from a parking lot to Splitwise, a stock brokerage and subscription billing, each
  with class and sequence diagrams and a tested solution (476 tests).
- **[system-design](https://github.com/hardyalsinghdeora/system-design)**: 32 classic system design
  problems, 30 concept notes, and 16 runnable building blocks such as rate limiters, an LSM-tree and
  fencing-token leases.
- **[design-patterns](https://github.com/hardyalsinghdeora/design-patterns)**: the 23 GoF patterns
  plus 14 modern backend ones, including circuit breaker, outbox, saga, CQRS and event sourcing, with
  payments and orders as the examples.

Closest to my day job: [subscription billing](https://github.com/hardyalsinghdeora/low-level-design/blob/main/problems/subscription-billing.md),
a [double-entry wallet](https://github.com/hardyalsinghdeora/low-level-design/blob/main/problems/digital-wallet.md),
a [subscription billing platform](https://github.com/hardyalsinghdeora/system-design/blob/main/problems/subscription-billing-platform.md)
and a [payment system](https://github.com/hardyalsinghdeora/system-design/blob/main/problems/payment-system.md).

### How I work

Specification before implementation, schema before endpoint, reversible steps over big-bang
cutovers. Every migration I've run could be turned around at any point, because the one thing
you cannot promise is that nothing will go wrong. I write the specification the team builds
from, then review against it: code review is where the standard actually gets set.

I treat an agent like any other production system that touches real data: structured output
over prose, retrieval before answering, a hard cap on model and tool calls, a fallback when a
provider fails, and secrets the model never sees.

### Stack

- **AI:** `MCP` `Anthropic Claude` `Google Gemini` `Ollama` `RAG` `Embeddings` `Function calling` `Structured output`
- **Backend:** `TypeScript` `Node.js` `Hono` `Express` `Python` `PHP` · learning: `Java` `Spring Boot`
- **Data:** `PostgreSQL` `MySQL` `Redis` `MongoDB` `Elasticsearch` `ClickHouse` `RabbitMQ`
- **Cloud and delivery:** `AWS (EC2, Lambda, S3, CloudFront, SQS, RDS)` `Cloudflare Workers` `Azure` `Docker` `CI/CD`
- **Front end:** `Angular` `NgRx` `RxJS` `React` `Tailwind`

Certified SAFe 5 Agilist · Google Project Management · B.Tech, Electronics & Communication (RTU Kota)

### Reach me

Notice period 30 days. Email is fastest.

[Email](mailto:hardyalsinghdeora@gmail.com) · [LinkedIn](https://www.linkedin.com/in/hardyalsinghdeora) · [Portfolio](https://hardyalsinghdeora.pages.dev/) · [Résumé](https://hardyalsinghdeora.pages.dev/resume-agentic-ai.html) · [Substack](https://substack.com/@hardyalsingh)
