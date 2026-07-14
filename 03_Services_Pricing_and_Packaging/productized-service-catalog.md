# Productized Service Catalog

**Module 3: Services, Pricing, and Packaging**

> **Why this exists**  
> In 2026, successful AI Automation / Agent Agencies have largely moved away from unpredictable one-off freelance projects. The winning model is **productized tiers** that combine clear scope, measurable outcomes, and recurring revenue through retainers. This catalog gives you ready-to-customize packages built around **niche specialization**, **agentic orchestration** (multi-agent systems with human oversight), **process-first discovery**, and **ongoing optimization**.  
> These tiers are grounded in real 2025–2026 practitioner patterns: discovery as a low-risk entry point, implementation scoped for no/low-code delivery (especially n8n self-hosted), and retainers as the profit and relationship engine because LLMs drift, costs fluctuate, new capabilities emerge, and clients need continuous ROI protection.  
> Productization reduces scope creep, improves delivery consistency, enables leverage, and turns your expertise into scalable assets while protecting margins.

## How to Use This File
1. Read the full catalog end-to-end.
2. Customize every **[CUSTOMIZE FOR YOUR NICHE]** section with your vertical (e.g., landscaping contractors, law firms, medical practices, home services).
3. Align pricing with your actual costs using the `financial-model-template.md` (Module 2).
4. Use the tables and scopes directly in proposals (see `proposal-and-sow-templates.md`).
5. Reference during discovery calls and sales conversations (Module 6).
6. Update quarterly as your capabilities, tool costs, and client results evolve.
7. Pair with `pricing-strategy-guide-and-calculator.md` for value-based adjustments and margin math.

**Immediate next step:** Duplicate this file, replace all placeholders, and run it by 3–5 ideal clients for feedback before publishing on your site or in proposals.

## How It Connects to the Rest of the Kit
- **Feeds forward into:** `proposal-and-sow-templates.md` (scopes & IP language), `case-study-roi-proof-template.md`, `detailed-sops/scoping-process.md` and `build-checklist-and-qa-protocol.md` (Module 5), and all sales assets (Module 6).
- **Receives input from:** Niche validation and ICP work (`niche-selection-icp-validation-framework.md`, Module 2), your tech stack decisions (`tech-stack-comparison.md` — n8n is the default recommendation for most productized builds), and financial modeling.
- **Supports:** Retainer-heavy operations, internal agency automation, and scaling decisions (Modules 7–8).
- This is the **commercial heart** of your agency. Everything else exists to help you sell, deliver, and retain these packages profitably.

---

## 4-Tier Productized Service Catalog — Quick Overview

| Tier | Price Range | Typical Timeline | Primary Focus | Recurring Revenue Potential | Best For |
|:---|:---|:---|:---|:---|:---|
| **1. Discovery & Audit** | $1,500 – $3,000 (one-time) | 1.5 – 3 weeks | Opportunity identification + roadmap | Low (entry point) | Qualifying buyers, building trust |
| **2. Implementation** | $5,000 – $15,000+ (one-time)| 4 – 10 weeks | Build, integrate, deploy, handoff | Medium (leads to retainer) | Core delivery |
| **3. Operations Retainer** | $1,000 – $3,000 / month | Ongoing (min. 3 months) | Monitoring, optimization, scaling, ROI reporting | **High** | Long-term partnership & profit |
| **4. Hybrid / Licensing** | Setup $5k–$12k + $500–$2,000/mo license or hybrid retainer | Varies | Productized templates + managed service | Very High | Scaling vertical solutions |

**Pricing philosophy (2026 reality):** Anchor in effort + risk + market rates, then layer value-based elements where you can prove ROI. Retainers are non-negotiable for sustainability — pure one-offs often destroy margins through maintenance burden and client expectation mismatches. Always validate your numbers against your `financial-model-template.md`.

---

## Tier 1: Discovery & Audit Package

**Investment:** $1,500 – $3,000 (one-time)  
**Goal:** Give the client clarity and a prioritized roadmap while qualifying serious buyers and reducing later scope risk.

### Scope
- Stakeholder interviews and current-state workflow mapping (manual processes, tools, pain points, data flows)
- AI/automation opportunity scan with scoring (impact × feasibility × strategic fit)
- High-level agentic architecture recommendations (when multi-agent orchestration + RAG + human-in-the-loop adds value)
- Technology recommendations with emphasis on self-hostable, cost-predictable options (n8n as default where appropriate)
- Rough ROI model and 90-day implementation roadmap
- Risk & change-management assessment (data access, integration complexity, team readiness)
- **[CUSTOMIZE FOR YOUR NICHE]** — Example for landscaping contractors: Focus on job scheduling, invoicing, lead follow-up, technician dispatching, and customer communication loops. For law firms: Intake, document review routing, deadline tracking, client communication.

### Deliverables
- Professional Audit Report (PDF + editable source)
- Prioritized Opportunity Backlog (table with effort/impact scores and estimated time/cost savings)
- Visual 90-day roadmap (Mermaid or exportable diagram)
- 60-minute debrief presentation + Q&A
- Recorded walkthrough for internal client sharing

### Timeline & Process
1. Kickoff call (45–60 min)
2. Data collection & interviews (1 week)
3. Analysis & report drafting (3–7 days)
4. Draft review call (optional)
5. Final presentation & handoff

**Total:** 1.5–3 weeks

### Exclusions
- No custom development, deployment, or integration work
- No production system access beyond agreed read-only or test environments
- No guarantees of exact future ROI (projections are estimates based on assumptions you will validate together)
- No ongoing support or monitoring (see Retainer tier)

### Sample ROI Language You Can Use
“Similar engagements in [your niche] have surfaced 15–40 hours per week of manual work and identified pathways to 25–60% time reduction in targeted workflows after implementation.”

---

## Tier 2: Implementation Package

**Investment:** $5,000 – $15,000+ (one-time, scoped by number of workflows/agents, integrations, and data complexity)  
**Goal:** Deliver a production-ready, documented system that creates measurable operational leverage.

### Scope
- Detailed scoping workshop (builds on Discovery output or standalone)
- Design and build of productized AI agents and orchestrated workflows (multi-agent patterns where beneficial — e.g., lead qualification → enrichment → routing → CRM sync)
- Secure integrations with client tools (CRM, email, calendars, databases, accounting, etc.) via APIs, webhooks, or native connectors
- RAG/knowledge retrieval setup when internal documents or data improve accuracy (self-hosted vector approaches recommended for data control)
- Comprehensive QA protocol: hallucination testing, edge-case handling, fallback mechanisms, cost monitoring, regression tests
- Deployment (strong preference for self-hosted n8n instance on client or agency-managed VPS for cost control, data residency, and long-term ownership)
- Documentation, runbooks, and client team training (1–2 live sessions + recorded)
- 30-day post-launch stabilization window (in-scope bug fixes and minor tweaks)
- Basic performance dashboard / reporting foundation

### Deliverables
- Fully functional, deployed automation/agent system in production
- Architecture diagram + data flow map
- Complete user guide + operational runbook
- Handoff training session(s) + recorded video
- Source files / workflow exports (with environment variable guidance — never hardcoded secrets)
- 30-day stabilization support log

### Timeline
4–10 weeks typical (simple single-workflow: 4 weeks; multi-agent + several integrations + RAG: 8–10+ weeks). Fixed timeline with change-request process for anything outside agreed scope.

### Exclusions
- Ongoing monitoring, optimization, model updates, or scaling (Retainer tier)
- Major custom code or fine-tuning of base LLMs (productized n8n + approved nodes only)
- Large-scale data migration or cleansing beyond agreed scope
- Performance SLAs beyond tested scenarios
- 24/7 support

**[CUSTOMIZE FOR YOUR NICHE]** — Add specific workflow examples relevant to your vertical (e.g., “Automated job completion + invoicing + review request sequence for landscaping companies” or “Client intake → conflict check → document assembly → matter opening for law firms”).

**IP Note:** See dedicated IP section below. Implementation always includes clear language on reusable vs. client-specific components.

---

## Tier 3: Operations & Optimization Retainer

**Investment:** $1,000 – $3,000 per month (billed monthly in advance)  
**Goal:** Protect and compound the value of the implemented system while creating predictable, high-margin recurring revenue.

### Why Retainers Are Essential in 2026
LLMs evolve constantly. Token costs shift. New agentic capabilities appear. Client processes change. Without ongoing human + agentic oversight, systems degrade, costs balloon, or opportunities are missed. Retainers convert one-time projects into long-term partnerships and turn your agency into a true “digital operations partner.”

### Scope (Typical Allocation: 10–20 delivery hours/month + monitoring overhead)
- Proactive monitoring of all workflows/agents (performance, errors, cost anomalies, drift)
- Monthly optimization sprints (prompt tuning, model evaluation, routing/caching improvements, cost reduction)
- Minor enhancements and small new automations (within retainer capacity)
- Quarterly Business Review (QBR) with hard ROI reporting (hours saved, error reduction, cycle-time improvement, revenue impact where measurable)
- Priority support with defined SLA
- Model updates, security patches, and compliance adjustments
- Scaling support (adding volume or new workflows)
- Coordination of human-in-the-loop review where required

### Deliverables
- Monthly performance report + optimization log + recommendations
- Continuously improved & updated production system
- Quarterly strategy + ROI presentation
- Access to support/ticketing channel
- Annual system health & architecture review (included)

### Timeline
Ongoing monthly engagement. Minimum 3-month commitment recommended to realize full value and allow proper optimization cycles.

### Exclusions
- Major new implementations or large-scope projects (use Implementation tier or scoped add-on)
- 24/7 real-time monitoring or emergency response beyond agreed SLA
- Client hosting/infrastructure costs (pass-through or client responsibility; self-hosted n8n keeps this predictable and controllable)
- Extensive custom development

---

## Tier 4: Hybrid & Licensing Models

These combine elements of the above for flexibility and scalability.

**Common Structures**
- **Setup + License:** $5,000–$12,000 implementation/setup fee + $500–$2,000/month license fee for access to your pre-built, maintained vertical agent templates or workflow suites (white-labeled or co-branded).
- **Full Hybrid Retainer:** Higher implementation or discovery fee + comprehensive operations retainer that includes infrastructure management.
- **Usage-Based Overlay:** Base retainer + transparent overage pricing for high-volume tasks or token consumption (with buffers and alerts).

**When to Offer Hybrid/Licensing**
- You have (or are building) reusable vertical solutions.
- Client wants lower upfront commitment or prefers “rent vs. build.”
- You want to productize and sell the same high-quality patterns to multiple similar clients while still offering customization.

---

## Intellectual Property (IP) Ownership — Critical Terms

Clear IP language protects your ability to productize, prevents disputes, and builds professional trust.

### Standard Framework (Include verbatim or adapted language in every SOW)

**Client Owns:**
- All client-specific data, credentials, configurations, and outputs generated during normal operation of the delivered system.
- Any custom workflows, agents, or integrations built exclusively for the client’s unique processes and explicitly scoped as bespoke in the SOW.
- Client data models and proprietary business logic documented during discovery.

**Agency Retains Ownership / Reusable Rights:**
- All pre-existing frameworks, templates, prompt libraries, multi-agent orchestration patterns, evaluation harnesses, cost-monitoring tools, and generalized workflow designs developed or owned by the agency prior to or independent of the engagement.
- Anonymized improvements, patterns, and learnings that can be productized or applied to other clients (without any client data or confidential information).
- Core n8n workflow structures, node configurations, integration patterns, and agent templates that form your productized catalog.
- Any enhancements to your internal methodologies, tools, or reusable components.

**Work Product Created During Engagement:**
- Clearly documented in the SOW on a per-deliverable basis.
- Default: Client receives a perpetual, non-exclusive license to use the delivered system for their internal business. Agency retains rights to reuse generalized components.

**Why This Structure Works in 2026**
It enables true productization (build once, leverage many times) while giving clients full ownership of their data and specific operational outcomes. Vague language is a common source of later conflict — be explicit.

---

## Pricing Strategy, Customization & Safeguards

- **Entry point strategy:** Discovery tier lowers risk for both sides and filters tire-kickers.
- **Retainer math:** Price to cover monitoring/optimization time + API cost buffer + profit. Review actuals monthly for first 3–6 clients.
- **Value-based elements:** Include projected ROI in Discovery reports. Consider success or shared-savings components only after you have reliable baseline data.
- **Niche customization checklist:**
  - [ ] Replace all example workflows with your vertical’s highest-pain, highest-ROI processes.
  - [ ] Adjust timelines and pricing bands based on typical client size and complexity in your niche.
  - [ ] Add 1–2 niche-specific ROI metrics or case study hooks.
  - [ ] Update exclusions to match common integration realities in your market.
- **Add-ons** (price separately): Advanced RAG corpus building, voice agents, premium SLAs, executive training workshops, white-glove onboarding.
- **Payment terms (recommended):** 50% on signing for Implementation; monthly in advance for Retainers. Use your MSA + SOW.

**Results vary.** Actual outcomes depend on data quality, client adoption, integration complexity, and ongoing execution. These ranges reflect 2025–2026 productized AI automation agency benchmarks for SMB-focused work. Always validate pricing and scopes with real client conversations and your own cost structure. This document is for educational and internal planning purposes. Consult qualified legal and financial professionals before using in client agreements.
