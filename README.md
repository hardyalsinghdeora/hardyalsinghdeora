# Hardyal Singh

**Principal Software Engineer** · India · *open to new roles — anywhere in India · Remote*

I build the systems that turn a signed contract into an invoice, an activation and a live
subscription — and keep them auditable enough that finance trusts the numbers.

Fifteen years in backend and platform engineering, most of it on the commercial side: orders,
pricing, discounting, invoicing, subscriptions, and the identity and access model underneath
them. An order isn't finished when it's signed. It has to become a proposal, an approved
price, an invoice, an activation and a working account — across a dozen services and,
latterly, two generations of database that both had to keep serving.

That handoff is the work I'm known for.

---

### What I do

| | |
|---|---|
| **Commerce and billing** | Order and subscription data models, SKU catalogues, contract-term and proration derivations written to be finance-auditable, and a discount engine with a four-tier approval ladder running from self-approval to C-suite sign-off |
| **Migration under load** | Replacing a long-lived legacy estate with no maintenance window: a two-way bridge between legacy and current datastores, a one-time historical backfill kept strictly separate from the continuous reverse-sync, idempotency guards and drift detection |
| **Architecture** | Domain-decomposed services behind a single gateway, so auth, rate limiting, schema validation and caching get solved once at the edge instead of six times badly |
| **Access control** | Users → groups → organisations scoping across services, including multi-role users and ownership overrides |
| **Integrations** | CRM, finance and HR systems behind ports and adapters, so the vendor can be swapped without touching callers |

### How I work

Specification before implementation. Schema before endpoint. Reversible steps over big-bang
cutovers — every migration I've run could be turned around at any point, because the one
thing you cannot promise is that nothing will go wrong.

I design the schema before the endpoint, because the schema is what you live with. I write
the specification the team builds from, then review against it — code review is where the
standard actually gets set, not the style guide.

### Written up

**[Moving a live commerce platform between two databases without a maintenance window](https://github.com/hardyalsinghdeora/case-studies/blob/main/migration-live-commerce-platform.md)**
— a decision record: what we rejected and why, the two-flows separation, the reconciliation
lesson, and what it cost.

### Things I've built in the open

**Design interview prep, in TypeScript** — three repositories that work through the design rounds
of backend interviews end to end: requirements, diagrams, trade-offs and tested code.
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

**[claude-toolkit](https://github.com/hardyalsinghdeora/claude-toolkit)** — ten dependency-free
CLI tools that make AI-assisted coding sessions safer and cheaper: MCP server toggling with
restorable config, a macOS Keychain vault built so an agent can *use* a credential without ever
*seeing* it, database access that keeps passwords out of shell history, output compression, and
offline code/schema/session indexes, a zero-token daily work log, and an offline Jira/Confluence fetcher.

**[AI pull request reviewer for Bitbucket](https://github.com/hardyalsinghdeora/pr-review-extension)** *(in development)* — a Chrome extension that reviews
PRs against a configurable standard, with a provider abstraction over hosted and local models so
a team picks its own trade-off between cost, latency and privacy.

#### Reference builds

Small, tested sample projects for the backend patterns I rely on, each with decision records and CI.

| Project | What it shows |
|---|---|
| **[spring-boot-order-service](https://github.com/hardyalsinghdeora/spring-boot-order-service)** | Order-to-cash REST API in Java 21 / Spring Boot 3: idempotency keys, `ETag` + `If-Match` optimistic locking, an explicit state machine, RFC 9457 errors, Flyway |
| **[api-gateway-rate-limiter](https://github.com/hardyalsinghdeora/api-gateway-rate-limiter)** | TypeScript / Hono gateway: token-bucket and sliding-window rate limiting, circuit breaker, jittered retries for idempotent methods, Prometheus metrics |
| **[event-outbox-worker](https://github.com/hardyalsinghdeora/event-outbox-worker)** | Transactional outbox with an at-least-once relay, dead-letter handling and an idempotent consumer |
| **[db-migration-reconciler](https://github.com/hardyalsinghdeora/db-migration-reconciler)** | Python CLI to verify a live database migration: keyset checksums, drill-down diffs and a dry-run-first, resumable repair |

### Stack

`TypeScript` `Node.js` `Hono` `Express` `Python` `PHP` · learning: `Java` `Spring Boot`
`PostgreSQL` `MySQL` `Redis` `MongoDB` `Elasticsearch` `ClickHouse`
`RabbitMQ` `Grafana` `Sentry` `OAuth 2.0`
`Angular` `NgRx` `RxJS` `React` `Tailwind`
`AWS (S3, CloudFront, SQS, RDS)` `Azure` `Bitbucket Pipelines`

Certified SAFe 5 Agilist · Google Project Management · B.Tech, Electronics & Communication (RTU Kota)

### Reach me

[Email](mailto:hardyalsinghdeora@gmail.com) · [LinkedIn](https://www.linkedin.com/in/hardyalsinghdeora) · [Portfolio](https://hardyalsinghdeora.pages.dev/)
