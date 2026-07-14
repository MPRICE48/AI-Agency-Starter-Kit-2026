# Module 4: Tech Stack Build Guides and Examples

Welcome to the technical delivery layer of the **AI-Agency-Starter-Kit-2026**. This module outlines our recommended core tool stack, secure self-hosting deployments, four practical workflow blueprints, and operational optimization standards.

## Folder Purpose

The purpose of this folder is to transition your agency from abstract planning to reliable technical execution. In the AI agency space, long-term retention relies on delivering production-grade systems that run securely, cost-efficiently, and comply with data residency rules. We prioritize n8n self-hosting alongside structured data layers to maximize margins and data sovereignty.

## File Navigation & Reading Order

We recommend reading and completing these files in the following order:

1. **[`tech-stack-comparison.md`](tech-stack-comparison.md)**  
   *A core analysis comparing n8n, Make.com, Zapier, Voiceflow, database systems, and vector tools.* Use this to align your tool choices with client budgets and security requirements.
2. **[`setup-guides-and-links.md`](setup-guides-and-links.md)**  
   *Step-by-step production setup guides using Docker Compose + Traefik and Nginx + Let's Encrypt reverse proxies.* Follow this to build a hardened production server.
3. **[`llm-rag-prompting-best-practices-cost-monitoring-testing.md`](llm-rag-prompting-best-practices-cost-monitoring-testing.md)**  
   *Technical guidelines for XML prompt structures, recursive character chunking rules, LiteLLM token monitoring, and regression evaluations.*
4. **[`example-workflows/`](example-workflows/) (Subfolder)**  
   *Production-ready automation blueprints detailing n8n configurations and node structures:*
   * **[`lead-qualification-agent.md`](example-workflows/lead-qualification-agent.md)** — Webhook intake, data enrichment, ICP scoring, and CRM routing.
   * **[`client-onboarding-multi-agent-flow.md`](example-workflows/client-onboarding-multi-agent-flow.md)** — Multi-agent setup triggered by a won deal to create Google Drive folders, Airtable portals, and welcome drafts with human sign-off.
   * **[`support-triage-with-rag.md`](example-workflows/support-triage-with-rag.md)** — Semantic search on Pinecone context, automated replies, and Zendesk escalation logic.
   * **[`internal-agency-automation-examples.md`](example-workflows/internal-agency-automation-examples.md)** — Auditing report generator and weekly client billing efficiency reporting.

## How It Connects to Other Modules

* **Productized Packages (`03_Services_Pricing_and_Packaging/`)**  
  The workflows detailed here directly implement the Discovery, Implementation, and Retainer packages defined in Module 3.
* **Delivery SOPs (`05_SOPs_Delivery_Workflows_and_QA/`)**  
  The build checklists and QA protocols directly govern how you customize, load-test, and stabilize the n8n templates created in this module.
* **Compliance Checks (`07_Legal_Compliance_Operations/`)**  
  The Docker deployment options, reverse proxies, and encryption variables documented in the setup guide support your GDPR and HIPAA compliance assertions.

---

> **[CUSTOMIZE FOR YOUR NICHE]**  
> Swap out the default CRM nodes (Jobber, ServiceTitan) or vector databases for the exact integrations required by your target niche. Ensure all production credentials are stored securely via the n8n credential vault and never hardcoded in workspace templates.
