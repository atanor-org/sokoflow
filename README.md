# SokoFlow

**The tax-compliant, offline-first commerce suite for African retail, wholesale, distribution, and hospitality businesses.**

Governments across Africa (Rwanda EBM, Kenya eTIMS, Uganda EFRIS, Ghana E-VAT, Nigeria NRS) now require every business to issue tax-authority-verified invoices in real time. The free government tools only print receipts. Global ERPs can't certify and won't work offline.

SokoFlow is a single product that runs **sales, stock, and customer billing** — and automatically issues the **verified tax invoices** your country legally demands, **even when the internet is down**.

- **Deploy anywhere:** Docker image / Docker Compose, single-tenant, on-prem, private cloud, or local server
- **Sovereign data:** customer data stays in the customer's infrastructure
- **Fiscal-engine ready:** certified adapters for RRA EBM (Rwanda), KRA eTIMS (Kenya), URA EFRIS (Uganda) — more on the roadmap
- **Offline-first:** transactions queue locally and resync when connectivity returns
- **Zero AI:** deterministic, auditable, workflow-driven, boring-by-design financial-grade software

---

## Why SokoFlow exists

Real demand, written into law:

| Country | Mandate | Status |
|---------|---------|--------|
| Rwanda | EBM / EIS (VSDC / OSDC) | Mandatory for all taxable sales |
| Kenya | eTIMS (VSCU / OSCU) | Mandatory for all businesses since Sep 2023 |
| Uganda | EFRIS | Mandatory; 12 sectors since Jul 2025 |
| Ghana | E-VAT | All VAT-registered businesses by end-2024 |
| Nigeria | NRS Merchant Buyer Solution | Large taxpayers Nov 2025; phased rollout |

Non-compliance means fines, blocked VAT deductions, and exclusion from public tenders. **This is not nice-to-have. It is survival.**

## Project status

> **Early stage.** This repository currently contains the project scaffold (positioning, licensing, governance). The MVP is being built — see [docs/ROADMAP.md](docs/ROADMAP.md).

## Roadmap (high-level)

1. **MVP (M0–M3):** commerce core (items, stock, sales, invoices, receipts, POS, AR), offline queue, **RRA EBM adapter + certification**, Docker installer, licensing
2. **Reach (M4–M6):** Kenya eTIMS adapter, pharmacy/hospitality verticals
3. **Scale (M7–M12):** Uganda EFRIS, Tanzania/Ghana, channel-partner program

## Contributing

We welcome contributions from developers, founders, and operators across Africa. Start with [CONTRIBUTING.md](CONTRIBUTING.md).

## Security

Report security issues privately — see [SECURITY.md](SECURITY.md). This software handles fiscal documents; security is not optional.

## License

[MIT](LICENSE) © Atanor

---

Made in Kigali, Rwanda · [Atanor](https://github.com/atanor-org)