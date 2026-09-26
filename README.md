# XYZ Fulfillment Hub — Take-Home Submission

**Live hosted version:** https://claude.ai/artifact/5kjYyazGcG16RewfsrVkNz
**Run locally:** open `fulfillment-hub.html` directly in any browser — no build step, no server, no dependencies. (Optional: `python3 -m http.server` in this folder, then visit `localhost:8000/fulfillment-hub.html`.)

## Problems addressed (and why these four)

Of the eight pain points in the brief, this app targets:

1. **No at-a-glance order status** → a Kanban board across all six fulfillment stages (Received → Processing → Picking → Packing → Staging → Shipped).
2. **Priority orders missing deadlines** → a per-order SLA countdown (4h for priority orders, 24h for standard), color-coded and auto-flagged when overdue.
3. **Stock shown as available but not findable** → an inventory view that flags a SKU for transfer *before* a pick fails: when Warehouse 1 stock is below the number of un-shipped orders for that SKU, and Warehouse 2 has cover stock.
4. **Problems handled informally and forgotten** → a persistent issue log tied to order IDs, with open/resolved status.

Deliberately out of scope for this iteration: courier API integration and label generation. The brief has no real courier system to test against, and these are solved problems with existing vendor APIs — the effort was better spent on the visibility and exception-tracking gaps the brief explicitly called out.

## How it works

- Single-file HTML/CSS/JS — no framework, no install. Chosen because the warehouse team is described as "experienced but not comfortable with technology," so the deployment story needs to be "open a link."
- Sample data (58 orders, 8 SKUs, 2 warehouses) is generated on first load and persisted in the browser (localStorage) so demo actions — advancing an order's stage, resolving an issue — survive a page refresh.
- Four views: **Dashboard** (KPIs + Kanban), **Orders** (filterable table with stage-advance and flag-issue actions), **Inventory** (stock + transfer-risk flags), **Issues** (exception log).

## What I'd build next with more time

- Real courier API hooks (label generation, pickup confirmation webhooks) instead of a manual courier field
- Multi-user concurrency and an audit trail on stage changes
- Configurable SLA thresholds per channel/courier rather than hardcoded priority/standard tiers

## Files in this submission

- `fulfillment-hub.html` — the application
- `AI_usage_note.pdf` — AI usage disclosure (per submission requirements)
- `README.md` — this file
