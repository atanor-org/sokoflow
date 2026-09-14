# Roadmap

**Status: early stage.** The MVP is not built yet. This is the plan, based on
verified regulatory demand across East Africa.

## Mission

Make every African business tax-compliant without a second thought — with a
product that runs on their own server, works offline, and requires almost no
support.

## Why this roadmap

Rwanda RRA, Kenya KRA, Uganda URA, Ghana GRA, and Nigeria NRS have all made
real-time electronic invoicing mandatory. Free government tools only print
receipts. This is the open, productized alternative.

## Phases

### Phase 0 — Foundations (M0)
- [ ] Finalize product scope and data model
- [ ] Begin RRA EBM (VSDC/OSDC) certification documentation
- [ ] Recruit 5 design partners in Rwanda

### Phase 1 — MVP (M1–M3)
- [ ] Commerce core: items, stock, sales orders/invoices/receipts, POS, AR
- [ ] Purchasing / AP (simplified)
- [ ] Offline queue + resync engine
- [ ] RRA EBM adapter (certificate signing, transmission, compliance storage)
- [ ] RBAC + immutable audit trail
- [ ] Docker deployment: single-command installer, backup/restore, health checks
- [ ] Licensing: machine-locked keys, trial/expiry, update channel
- [ ] Live pilots issuing certified EBM invoices

### Phase 2 — Regional reach (M4–M6)
- [ ] Kenya eTIMS adapter (VSCU / OSCU) + KRA integrator approval
- [ ] Pharmacy vertical module
- [ ] Hospitality vertical module

### Phase 3 — Scale (M7–M12)
- [ ] Uganda EFRIS adapter
- [ ] Tanzania TRA EFDMS adapter
- [ ] Ghana E-VAT adapter (as demand justifies)
- [ ] Channel-partner program (accountants, IT resellers)

## Non-goals for the MVP

- No payroll (governments provide free filing platforms; we integrate, not compete)
- No full double-entry GL in month one
- No AI of any kind, ever
- No per-customer custom development

## Contributing

Check [CONTRIBUTING.md](../CONTRIBUTING.md). Pick an item, fork, build, PR.