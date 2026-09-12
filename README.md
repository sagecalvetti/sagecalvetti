Staff software engineer focused on platform reliability and API design.

## Zelma Grimes

I build and operate distributed systems that move data between services without losing it. I own the ingestion pipeline, the queue consumer workers, and the RPC boundaries that keep teams independent. My operational priority is reducing mean time to recovery through better traces and runbooks, and I accept the occasional schema migration cost to avoid long-lived feature branches. I've shipped APIs, backfill workers, and internal tooling that cut deployment friction.

### 🛠 Tech & Infrastructure

**Core** `TypeScript` `Node.js` `PostgreSQL` `Redis`

**Data** `Kafka` `Debezium` `Flyway`

**Infra** `Docker` `GitHub Actions` `Grafana` `Prometheus`

**Tooling** `ESLint` `Prettier` `tsx`

### ⚙️ Engineering Areas

- Designing idempotent ingestion APIs with at-least-once delivery and deduplication keys.
- Building queue consumer workers with retry policies and dead-letter queues for malformed payloads.
- Managing database migrations and backfills with zero-downtime release strategies.
- Instrumenting services with structured logs, metrics, and distributed traces to debug cross-service failures.

### 🔭 Current Focus

- Reducing tail latency on the ingestion path without adding a second cache layer.
- Migrating the monolith's order service to a separate schema without breaking existing RPCs.
- Tuning Kafka consumer group rebalancing to handle bursty traffic without dropping messages.
- Standardizing error codes across internal APIs so clients can handle failures without string matching.

### 📌 Engineering Notes

- Tests that hit the real database catch migration bugs; mocks hide them.
- Prefer additive schema changes; destructive changes go through a deprecation window.
- Retry only idempotent operations; for everything else, fail fast and let the queue handle it.
- Deploy small, monitor the error rate, and roll back before investigating if the trace shows a regression.

### 🧭 How I Work

- Design APIs with explicit contracts and versioning from day one.
- Optimize for operational simplicity: fewer moving parts beats clever abstractions.
- Write documentation for the on-call engineer who inherits the system.

*Reliability is a feature, not a patch.*