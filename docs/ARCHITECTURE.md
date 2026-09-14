# Architecture (high-level)

> ⚠️ This is a living design note. The MVP does not exist yet — nothing below
> is code.

## Design principles

1. **Boring and deterministic.** No AI, no ML, no prediction. Every operation
   is a transaction: structured, validated, and fully auditable.
2. **Single-tenant by default.** One Docker deployment per customer. Data
   stays in the customer's control (data sovereignty is a legal requirement
   in Rwanda and a selling point everywhere).
3. **Offline-first.** Transactions (especially fiscal invoices) queue locally
   and sync to the tax authority in the correct order when connectivity
   returns.
4. **The fiscal adapter is the moat.** The commerce core is identical in every
   country; the country's tax integrator (EBM/eTIMS/EFRIS/…) is a swappable,
   certified layer.

## Proposed stack

| Layer | Choice | Why |
|---|---|---|
| Backend | TypeScript/Node or Go | Boring, fast to build, great for two founders |
| Frontend | React | Huge talent pool; forms, tables, dashboards |
| Database | PostgreSQL | Restorable, battle-tested, fits audit requirements |
| Cache/queue | Redis | Offline queue, jobs, locks |
| Caching/objects | MinIO (optional) | Local object storage for receipts/attachments |
| Deployment | Docker Compose (+ optional K8s) | Single-tenant, reproducible |

## Deployment topology (per customer)

```
┌─ GNU/Linux or Windows host ────────────────┐
│  nginx ─→ web ─→ postgres                  │
│            │                               │
│            └→ worker ─→ redis              │
│  fiscal adapter (EBM / eTIMS / EFRIS)      │
└────────────────────────────────────────────┘
         │ (HTTPS / encrypted queue)
         ▼
   Tax authority (RRA / KRA / URA / …)
```

`./install.sh` preflight-checks, pulls images, initializes the DB, provisions
TLS, and prints a health URL. `./atanor backup` / `./atanor restore` handle
encrypted, versioned backups.

## Fiscal adapter interface (target)

- Accepts an invoice → validates → signs with customer certificate → encrypts
  → transmits → stores the returned compliance certificate
- Supports ordered offline queues with configurable retention windows
- Exposes daily fiscal reconciliation reports
- Handles void/credit-note/refund flows per authority rules

## See also

- [ROADMAP.md](ROADMAP.md) — phased build plan
- [SECURITY.md](../SECURITY.md) — security expectations