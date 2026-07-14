# Project Management Templates for AI Agency Delivery

**Module 5 | SOPs, Delivery Workflows, and QA**  
*Ready-to-implement Notion (and ClickUp) structures for client portals and internal delivery boards that align with the end-to-end client journey and detailed SOPs.*

---

## Why This Exists

Delivery in an AI automation agency is complex: multiple concurrent stages, non-deterministic AI outputs that require rigorous QA, variable token costs, client expectations around transparency, and the need to transition smoothly into retainers. 

A well-designed project management system does three critical things in 2026:
- Gives clients **visibility and confidence** without exposing internal agency operations or sensitive credentials
- Gives the agency **control, traceability, and scalability** so founder time is not consumed by status chasing
- Directly supports **retainer value demonstration** by feeding clean metrics into monthly reports

Without structured templates, agencies suffer from scattered information, missed QA gates, scope creep, and clients who feel “in the dark” even when progress is being made. These templates turn the high-level journey map and SOP checklists into living, visual systems that both parties can trust.

**Core 2026 principles**: Agentic workflows need tracking of AI-specific signals (hallucination rates, fallback triggers, cost per execution). Retainers require ongoing optimization visibility. Self-hosted tools (n8n) and data governance demand strict separation of internal vs client-visible information.

---

## How to Use It

1. **Choose your primary tool** — Notion is recommended for most agencies (flexible databases + beautiful client-facing pages). ClickUp is excellent if you need heavier task automation and native time tracking.
2. **Build the two-layer system**:
   - **Internal Delivery Workspace** (full access for agency team only)
   - **Client Portal** (filtered, read-mostly or comment-only views shared with the client)
3. **Recreate using the tables below** — Copy the property lists and view structures directly into Notion or ClickUp.
4. **Link everything** — Use relations between the journey stages, SOP checklists, and reporting metrics.
5. **Automate where possible** — Use native automations or connect via n8n/Make to update status when QA gates pass or costs are logged.
6. **Review monthly** — During retainer reviews, the client portal becomes the single source of truth for progress and ROI.

**Pro tip**: Start with one pilot client. Build the boards, run the full journey once, then refine before templatizing for all clients.

---

## How It Connects to Other Sections

- **Direct implementation of** `end-to-end-client-journey-map.md` — Every stage in the Mermaid flowchart becomes a status or view in these boards.
- **Uses checklists from** `detailed-sops/` (discovery-call-script-and-questionnaire.md, build-checklist-and-qa-protocol.md, etc.) — Embed or relate the checklists as subtasks or linked pages.
- **Feeds** `reporting-template-with-metrics.md` — Pull live numbers from board properties (hours saved estimates, cost to date, success rates) into monthly reports.
- **Supports sales process** — A clean, professional client portal in proposals demonstrates operational maturity and reduces objections about “how will I know what’s happening?”
- **Enforces security** from Module 7 — Client portal never contains credentials, internal notes, API keys, or agency financials.
- **Enables scaling** in Module 8 — Clear ownership fields, relations, and views make it easy to hand off projects to contractors or internal AI agents.

This file is the visual operating system that makes the rest of Module 5 usable at scale.

---

## Recommended Tool Choice (2026)

**Primary recommendation: Notion**  
Reasons:
- Excellent balance of structured databases + beautiful, client-friendly pages
- Powerful relations and rollups (perfect for linking journey stages to metrics)
- Easy to create filtered views and permission layers
- Native AI features (Notion AI) can summarize updates or draft client reports
- Simple to embed Mermaid diagrams, SOP checklists, and reporting dashboards

**Strong alternative: ClickUp**  
Use if you need heavier automation, native time tracking, or prefer a more traditional task-focused interface. Many agencies run hybrid setups (Notion for client portal + ClickUp for internal execution).

**Avoid for client portals**: Pure task tools (Linear, Jira) that feel too technical for non-technical clients, or spreadsheets that lack relations and rich views.

---

## Client Portal Layout (Shared with Client)

This is the **filtered, client-safe view**. It shows progress, documents, and value — nothing internal.

### Recommended Structure (Notion Pages + Linked Database)

**Top-level pages in the shared workspace**:
- **Dashboard** (home page the client lands on)
- **Project Journey** (visual timeline + current stage)
- **Deliverables & Documents**
- **Metrics & ROI**
- **Communication & Feedback**

**Key Database: “Client Projects” (filtered view only)**

**Recommended Properties (Client-safe)**:

| Property Name | Type | Purpose | Example Values | Client Visibility |
|:---|:---|:---|:---|:---|
| Project Name | Title | Main identifier | “Acme Landscaping – Lead Qualification” | Yes |
| Current Stage | Select | Maps to end-to-end journey | Discovery, Scoping, Development, Internal QA, Client UAT, Deployment, Handoff, Retainer Review | Yes |
| Overall Status | Select | High-level health | On Track, At Risk, Blocked, Complete | Yes |
| Next Milestone | Date | What’s coming up | 2026-08-15 – Client UAT session | Yes |
| Progress % | Number (rollup or formula) | Visual completion | 65% | Yes |
| Key Wins This Period | Text | Highlights for client | “Reduced lead response time from 4h to <15min” | Yes |
| Estimated Hours Saved /mo | Number | Feeds ROI reporting | 47 | Yes |
| Documents | Relation / Files & Media | Links to shared files | Proposal, Architecture Diagram, Runbook | Yes |
| Last Updated | Last edited time | Transparency | — | Yes |

**Recommended Views for Client Portal**:
- **Kanban by Stage** (simple board showing movement through the journey)
- **Timeline / Calendar** (milestones and retainer review dates)
- **Table – Current Projects** (sorted by stage or next milestone)
- **Dashboard Gallery** (cards with key metrics and status)

**Security Rule (Critical)**: This database and all pages use **filtered views only**. The client never sees the full internal database or any properties marked “Internal Only”.

---

## Internal Delivery Board Layout (Agency Only)

This is the **full-power workspace** used by the agency team and internal agents.

**Main Database: “Delivery Projects” (full access, private workspace)**

**Complete Recommended Properties**:

| Property Name | Type | Purpose / Notes | Example | Visibility |
|:---|:---|:---|:---|:---|
| Project Name | Title | — | — | Internal + Client (filtered) |
| Client | Relation | Link to Clients database | Acme Landscaping | Internal |
| Current Journey Stage | Select | Exact match to end-to-end map | Development → Internal QA | Internal + Client |
| Sub-Status | Select | Granular tracking | Hallucination Testing, Awaiting Client Feedback | Internal |
| Owner (Agency) | Person / Select | Who is responsible | Founder / Contractor / AI Agent | Internal |
| Priority | Select | — | High / Medium / Low | Internal |
| Due Date | Date | Next hard deadline | — | Internal |
| SOP Checklist Status | Relation or Checkbox | Link to detailed-sops checklists | Build Checklist 87% complete | Internal |
| Hallucination Test Pass Rate | Number (formula) | From QA protocol | 96% | Internal |
| Token / API Cost to Date | Number (rollup) | Tracked via n8n or manual entry | $187.40 | Internal |
| Fallback Triggers (This Period) | Number | How often human escalation was needed | 3 | Internal |
| Estimated Hours Saved / Month | Number | For client reporting | 47 | Internal + Client |
| Client Satisfaction (Internal) | Select | Internal pulse check | Green / Yellow / Red | Internal |
| Next Action | Text | Clear next step | “Complete regression suite” | Internal |
| Internal Notes / Risks | Text | Never shared with client | “Prompt version 3.2 still drifting on edge case X” | Internal |
| Credentials / API Keys | **Never add here** | Store in n8n env vars or encrypted vault only | — | Never |

**Recommended Internal Views**:
- **Kanban – Full Journey** (all stages visible)
- **My Active Projects** (filtered by Owner)
- **At Risk / Blocked** (filtered)
- **Retainer Clients – Monthly Review** (filtered by stage = Retainer Review)
- **Cost & QA Dashboard** (table or board with rollups for token spend and test pass rates)
- **Calendar** (by Due Date + Retainer Review dates)

---

## Security Best Practices (Non-Negotiable)

- **Never store credentials, API keys, or production access details** in the project management tool. Use environment variables in n8n and a separate secure vault (Doppler, Infisical, 1Password, etc.).
- **Client portal must be a filtered view or a separate shared workspace** in Notion. Double-check permission settings so clients cannot access the raw parent databases or internal notes.
- **Educate your team** on the "Data Governance Boundaries at Handoff" (see `end-to-end-client-journey-map.md`). Downgrade credentials and remove developer access logs during the Handoff phase.
