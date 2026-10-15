# Hi, I'm Huynh Nhat Khanh 👋

**Backend Engineer, Golang.** I build event-driven services for multi-tenant SaaS: async job workers, queues, object storage, and the APIs around them. I also ship React/TypeScript frontends alongside the backend.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/khanhhuynhnhat/)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:khanhhuynh28082000@gmail.com)
[![AWS SAA-C03](https://img.shields.io/badge/AWS-Solutions_Architect_Associate-FF9900?style=flat&logo=amazonwebservices&logoColor=white)](https://cp.certmetrics.com/amazon/en/public/verify/credential/ecc6c4e55a20485aa01fd4be0f6876ed)
[![AWS CLF-C02](https://img.shields.io/badge/AWS-Cloud_Practitioner-FF9900?style=flat&logo=amazonwebservices&logoColor=white)](https://cp.certmetrics.com/amazon/en/public/verify/credential/53d7da8e3d9c468aaf06fdf88fc99cba)
![Profile views](https://komarev.com/ghpvc/?username=HuynhNhatKhanh&style=flat&color=0e75b6&label=Profile+views)

---

## 📦 Projects

### [vnsalary](https://github.com/HuynhNhatKhanh/vnsalary) — Vietnam gross ↔ net salary & income tax library
[![Go Reference](https://pkg.go.dev/badge/github.com/HuynhNhatKhanh/vnsalary.svg)](https://pkg.go.dev/github.com/HuynhNhatKhanh/vnsalary)
A Go library and CLI that computes Vietnamese net pay, compulsory insurance and personal income tax under the law in force on the payment date, exact to 1 VND. Released as v0.1.0–v0.3.0 on pkg.go.dev.
- Every statutory number cites its decree or law article, including the 2026 PIT law (overtime, meal allowance, the tax a bonus adds)
- Integer money, no floats; net → gross inverse proven to return the smallest gross
- 36 golden cases from an independent reference implementation, 12 matched to the VND against TopCV; fuzzing; CI on three Go versions with the race detector; every change through a pull request

### [MEVLens](https://github.com/HuynhNhatKhanh/mevlens) — Arbitrum arbitrage observatory
A Go service that reads every Arbitrum One block, detects atomic arbitrage on Uniswap v2/v3/v4-style pools, and records profit, gas and priority-fee bids before and after the switch to Priority Gas Auctions. Read-only research tool.
- Concurrent block fetching with a **single-writer deterministic core** (ports & adapters, enforced by a lint rule and an architecture test)
- Minimal Arbitrum-aware JSON-RPC client: batching, per-endpoint rate limits, failover across free endpoints
- **ClickHouse** with idempotent batches and reorg rewind; **Prometheus + Grafana** dashboards and alerts
- Design decisions written as ADRs

### [auth-jwt](https://github.com/HuynhNhatKhanh/auth-jwt) — authentication service
Go + Fiber, Clean Architecture: ES256 access/refresh tokens, OTP 2FA, account lockout, rate limiting, Redis token blacklist, Docker Compose, GitHub Actions CI, golangci-lint.

### [grpc-user-service](https://github.com/HuynhNhatKhanh/grpc-user-service)
Clean Architecture service exposing the same use cases over gRPC, gRPC-Gateway REST and Gin.

---

## 💼 At work (private code)

**Hanbiro Vietnam, 01/2024 – 08/2026** — nCRM v4, a multi-tenant SaaS CRM (10+ Go microservices).
- **Primary owner of 2 Go services:**
  - **File & media pipeline:** RabbitMQ workers for virus scanning (ClamAV) and thumbnails (libvips/pdfium/ffmpeg), TTL retry queues, chunked bulk delete; Nginx serves thumbnails straight from disk, bypassing Go and the DB.
  - **Tenant provisioning:** DNS, mail domain + DKIM and storage for each new tenant, automated from 30–60 min of manual work to about 1 minute.
- Contributed to the team's Event Sourcing/CQRS framework, GraphQL gateway resolvers, and the orchestration layer of a RAG chatbot.
- React/TypeScript alongside backend since 05/2024: analytics dashboards (ECharts), rule configuration screens, chatbot UI.

---

## 🛠️ Stack

**Main:** Go · gRPC/Protobuf · GraphQL · REST · RabbitMQ · PostgreSQL (Citus) · Ceph S3 · Docker · Nginx · Linux  
**Also used:** React · TypeScript · MUI · ECharts · MySQL · ClickHouse · Prometheus/Grafana (MEVLens) · C# .NET 6 · PHP/Laravel  
**Tools:** Claude Code for daily work, with tests and code review as the gate

## 🌱 Open source
Go best-practice guides for gRPC and Temporal, merged into [agentic-awesome-skills](https://github.com/sickn33/agentic-awesome-skills).
