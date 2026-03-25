# Rural Smart City Dashboard

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-brightgreen?style=for-the-badge)](https://qwsbtd.github.io/Rural-Smart-City-Dashboard/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)
[![No Dependencies](https://img.shields.io/badge/Dependencies-Zero-orange?style=for-the-badge)](#technical-overview)

> An animated, real-time AI infrastructure dashboard simulating grid optimization, precision agriculture, community services, and federated learning — built for Ogden, AR as part of a nonprofit-led rural revitalization initiative. Zero dependencies. Runs entirely in the browser.

---

<!-- Add a screenshot or screen recording here once the dashboard is live -->
<!-- ![Dashboard Preview](assets/dashboard-preview.gif) -->

---

## The Problem

Rural communities are systematically excluded from AI-driven infrastructure improvements. **Ogden, AR** is one of thousands of small communities facing:

- **Aging grid infrastructure** with limited visibility into efficiency or failure prediction
- **No access to precision agriculture tools** that larger operations take for granted
- **Disconnected community services** with no unified monitoring or coordination layer
- **Deep and justified distrust** of centralized data systems — a legacy of extractive relationships between technology institutions and rural communities

AI can address these problems. But only if it is designed with trust, privacy, and equity at the center — not as afterthoughts.

---

## Dashboard Features

The dashboard simulates five live panels, each representing a real infrastructure domain targeted by the initiative:

| Panel | Description |
| --- | --- |
| **Grid Efficiency Chart** | Animated time-series chart tracking power grid performance — models optimization scenarios across distributed rural infrastructure |
| **Crop Yield Table** | Live-updating table displaying simulated agricultural output by crop type — supports precision farming decision support |
| **Service Node Monitor** | Real-time status grid for community service nodes (health, connectivity, water, emergency) — surfaces failures and degraded states |
| **Federated Learning Status** | Live panel showing model training rounds, participating nodes, and privacy metrics — visualizes the distributed AI layer without exposing raw data |
| **Live Clock** | System clock anchoring all panels to a shared time reference — signals the intent for real-time sensor integration |

---

## AI & Ethics Design Decisions

These are not compliance checkboxes. Each decision reflects a principled tradeoff chosen to make AI deployment viable in a community that has reason to be skeptical of technology promises.

### Federated Learning — Data Stays Local

Rather than centralizing community data in a cloud system, the architecture uses **federated learning**: AI models train on-device at each node, and only model updates (not raw data) are shared. This is a deliberate tradeoff — it is slower and more complex to implement than centralized training, but it gives residents and local institutions genuine data sovereignty.

### Explainability as a Core Requirement

Every AI subsystem is designed to produce **auditable, human-readable outputs**. In communities with historical reasons to distrust centralized systems, a black-box recommendation is worse than no recommendation. Explainability is required at the architectural level, not bolted on later.

### Privacy-Preserving Data Collaboratives

The roadmap includes cross-community learning — sharing insights across rural nodes without sharing identifying data. Techniques like differential privacy and secure aggregation allow collective intelligence without collective exposure. This lets a small community benefit from patterns observed across many communities while keeping its own data local.

### Zero External Dependencies

The dashboard runs with no external libraries, no CDN calls, no telemetry. This was a deliberate choice: in low-bandwidth rural environments, every external dependency is a potential failure point and a potential data leak. The constraint also demonstrates that a sophisticated, animated, real-time interface does not require a bloated dependency chain.

---

## Technical Overview

### Stack

- **HTML5 / CSS3 / Vanilla JavaScript** — zero build tools, zero frameworks, zero dependencies
- **Canvas API** — animated grid efficiency chart
- **CSS Grid & Flexbox** — responsive dashboard layout
- **`setInterval` / `requestAnimationFrame`** — live data simulation and animation loop

### Architecture

```text
index.html
├── <style>          — Embedded CSS (single-file deployment)
└── <script>
    ├── GridChart     — Canvas-based animated efficiency chart
    ├── CropTable     — Interval-driven yield data simulation
    ├── NodeMonitor   — Service node status with randomized fault injection
    ├── FedPanel      — Federated learning round/metric simulation
    └── Clock         — Live time display
```

No server required. No API keys. No accounts. Open `index.html` and it runs.

### Deployment

Hosted on **GitHub Pages** — the static file is served directly from the `main` branch, making it instantly accessible and auditable by anyone.

---

## Getting Started

```bash
# Clone the repository
git clone https://github.com/qwsbtd/Rural-Smart-City-Dashboard.git

# Open the dashboard — no build step required
cd Rural-Smart-City-Dashboard
open index.html   # macOS
# or: start index.html (Windows) / xdg-open index.html (Linux)
```

The live version is deployed at:
`https://qwsbtd.github.io/Rural-Smart-City-Dashboard/`

---

## Roadmap

### Phase 1 — Simulated Dashboard (Current)

- [x] Animated grid efficiency chart
- [x] Live crop yield table simulation
- [x] Service node status monitor
- [x] Federated learning status panel
- [x] Zero-dependency, single-file deployment
- [x] GitHub Pages hosting

### Phase 2 — Real Sensor Integration

- [ ] IoT sensor API connectors (grid, weather, soil)
- [ ] WebSocket-based live data feed
- [ ] Threshold alerting and anomaly detection
- [ ] Local-first data storage (IndexedDB)

### Phase 3 — Federated Learning Infrastructure

- [ ] On-device model training prototype (TensorFlow.js)
- [ ] Secure aggregation protocol implementation
- [ ] Cross-node model versioning and rollback
- [ ] Differential privacy integration
- [ ] Multi-community pilot with partner nodes

---

## About the Initiative

**The Rural Smart City Initiative** is a nonprofit project applying AI-enabled infrastructure to real community needs in Ogden, AR — a small rural community facing the same infrastructure challenges as thousands of other under-resourced towns across the country.

**The mission is simple:** build AI systems that work *for* the communities they serve — where data sovereignty, explainability, and equity are design requirements, not aspirations.

| | |
| --- | --- |
| **Role** | Founder, Nonprofit Leadership |
| **Scope** | Ogden, AR community revitalization |
| **Focus Areas** | Grid optimization, precision agriculture, community services, privacy-preserving AI |
| **Approach** | Mission-driven, long-horizon delivery — community trust before feature velocity |

### Why This Matters for Employers

This project demonstrates:

- **Leadership under ambiguity** — forming technical opinions and architectural decisions with incomplete information across a long-horizon, multi-stakeholder initiative
- **Applied AI ethics** — designing for explainability, privacy, and equitable outcomes as *primary requirements*, not compliance exercises
- **Technical depth without complexity theater** — a sophisticated, animated, real-time dashboard built with zero dependencies, because constraints sharpen design
- **Stakeholder communication** — translating complex AI systems into accessible language for non-technical community partners, funders, and local government

---

## Contributing

This project represents a real community initiative. If you are interested in contributing — whether as an engineer, a researcher, a data privacy expert, or a rural community advocate — open an issue or reach out directly.

Ideas especially welcome in:

- Federated learning architecture
- Privacy-preserving data techniques
- Rural IoT sensor integration
- Accessibility and low-bandwidth optimization

---

## License

[MIT License](LICENSE) — open source by design. If this work is useful to other rural communities or nonprofits, take it.
