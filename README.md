# 📦 XYZ Fulfillment Hub
### Real-Time Warehouse Operations & Exception Management Dashboard

[![Live Demo](https://img.shields.io/badge/Demo-Live%20Artifact-blue?style=for-the-badge&logo=googlechrome&logoColor=white)](https://claude.ai/artifact/5kjYyazGcG16RewfsrVkNz)
[![Stack](https://img.shields.io/badge/Stack-Vanilla%20HTML%2FCSS%2FJS-orange?style=for-the-badge)](fulfillment-hub.html)
[![Setup](https://img.shields.io/badge/Dependencies-Zero-emerald?style=for-the-badge)](#-quick-start)

A lightweight operations dashboard built for warehouse floor teams to streamline order lifecycles, eliminate manual bottlenecks, and catch inventory shortages before picks fail.

---

## ⚡ Quick Start

### 🌐 Live Hosted Version
> **[Open Hosted Artifact Demo](https://claude.ai/artifact/5kjYyazGcG16RewfsrVkNz)**

### 💻 Run Locally
Zero dependencies, package managers, or build steps required.

1. **Direct Run:** Open `fulfillment-hub.html` directly in any web browser.
2. *(Optional)* Run via a local Python server:
   ```bash
   python3 -m http.server 8000

## 🎯 High-Priority Problems Addressed

Out of the eight operational bottlenecks identified, this iteration focuses on the four highest-impact visibility and exception gaps:

| # | Operational Pain Point | Solution Implemented |
| --- | --- | --- |
| **1** | **No at-a-glance order visibility** | **Interactive 6-Stage Kanban Board** spanning `Received` → `Processing` → `Picking` → `Packing` → `Staging` → `Shipped`. |
| **2** | **Priority orders missing dispatch cutoffs** | **Automated SLA Countdowns** with visual urgency alerts (4h target for priority orders, 24h for standard) that auto-flag breaches. |
| **3** | **Inventory phantom stock / stockouts** | **Preemptive Transfer Alerts** triggered when Warehouse 1 stock drops below open order demand and Warehouse 2 has reserve units. |
| **4** | **Informal, untracked issue logs** | **Centralized Issue Tracker** bound directly to Order IDs with clear open/resolved audit states. |

> **Out of Scope Note:** Carrier API integration and label printing generation were bypassed in this phase. Without a real carrier sandbox environment, these are standard vendor integrations. Engineering focus was prioritized toward core floor visibility, SLA defense, and stock integrity.

---

## 🛠️ Architecture & Key Features

* **Zero-Setup Single File:** Constructed with pure vanilla HTML, CSS, and modern JavaScript. Eliminates tooling friction for non-technical warehouse floor managers.
* **Persistent Local State:** Automatically seeds realistic baseline data (58 orders, 8 SKUs, 2 warehouses) into browser `localStorage`. Status shifts, inventory edits, and resolved issues persist through page reloads.
* **Core Views:**
* **📊 Dashboard:** High-level metric summary cards (Total Orders, SLA Breaches, Priority in Flight, Shipped, Open Issues) alongside the Kanban workflow.
* **📋 Orders:** Filterable table with rapid stage progression and inline issue flagging.
* **📦 Inventory:** Multi-warehouse stock tracking paired with predictive transfer-risk warnings.
* **⚠️ Issues:** Centralized exception handling desk for resolving warehouse floor blockers.



---

## 🚀 Next Steps & Roadmap

* [ ] **Carrier Webhook Integrations:** Automated tracking generation and real-time carrier status webhooks.
* [ ] **Multi-User State Sync:** WebSocket layer for concurrent multi-station floor updates and user action auditing.
* [ ] **Granular SLA Thresholds:** Rule engine supporting carrier-specific and destination-zone SLA rules.

---

## 📁 Repository Structure

```text
├── fulfillment-hub.html        # Complete standalone application
├── AI Usage Note - Fulfillment Hub Take-Home.docx # AI usage disclosure
└── README.md                   # Project documentation

```

```

```

