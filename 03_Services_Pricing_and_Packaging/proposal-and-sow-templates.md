# Proposal and SOW Templates

**Module 3: Services, Pricing, and Packaging**

> **Why this exists**  
> Clear, professional proposals and Statements of Work (SOWs) are the foundation of trust, scope control, and profitability in an AI Automation / Agent Agency. In 2026, with agentic multi-agent systems, RAG, and non-deterministic LLM outputs, ambiguity is dangerous. Vague scopes lead to scope creep, unrealistic expectations about “perfect” AI results, and disputes over IP or liability when models change or hallucinations occur.  
> This file provides ready-to-customize outlines and placeholder language so you can move quickly from discovery to signed agreement while protecting your agency. These are **educational templates only** — never use them verbatim with clients without qualified legal review.

## How to Use This File
1. Start with the **Proposal Outline** for early-stage conversations (sales asset).
2. Move to the full **SOW Template** once the client is ready to commit (use after pricing is agreed via the Pricing Strategy Guide and Service Catalog).
3. Replace every `[PLACEHOLDER]` with real details.
4. Customize scopes and deliverables directly from the **Productized Service Catalog** (the four tiers).
5. Add or adjust IP, liability, and payment language using guidance from `contract-structures-and-key-clauses.md`.
6. Always run the final document by a qualified attorney in your jurisdiction before sending.
7. Keep a signed PDF + editable source version in your project management system.

**Immediate next step:** Copy the SOW outline below into your preferred document tool (Notion, Google Docs, or Word). Fill it for one of your current prospects using the scopes from the Productized Service Catalog.

## How It Connects to Other Sections of the Kit
- **Directly uses** pricing, scopes, timelines, exclusions, and IP guidance from `productized-service-catalog.md` and `pricing-strategy-guide-and-calculator.md`.
- **Feeds into** the sales process (`sales-frameworks-objection-handling.md` and `lead-generation-playbook.md` in Module 6) and delivery workflows (`end-to-end-client-journey-map.md` and `detailed-sops/` in Module 5).
- **Complements** the higher-level contract framework in `contract-structures-and-key-clauses.md` (MSA + DPA).
- Supports clean handoff to delivery teams and retainers.

---

## ⚠️ CRITICAL LEGAL DISCLAIMER — READ BEFORE USING ANY TEMPLATE

**These are educational templates only.**  
The outlines, sample language, and structures in this file are provided strictly for educational and illustrative purposes as part of the AI Agency Starter Kit 2026. They have **not** been reviewed or approved by a licensed attorney for your jurisdiction, business model, client types, or specific use cases.

**AI-specific risks you must address:**
- LLM outputs are **non-deterministic** and can contain hallucinations, inaccuracies, or biases.
- LLM providers (OpenAI, Anthropic, Google, etc.) can change models, capabilities, pricing, or availability with little or no notice.
- Token consumption and performance can vary significantly.
- Self-hosted or third-party tools introduce additional variables.

**You must:**
- Have a qualified attorney review, customize, and approve **every** proposal, SOW, MSA, and related document before use with real clients.
- Explicitly limit your liability for AI outputs, model changes, hallucinations, indirect/consequential damages, and data issues.
- Include clear disclaimers, warranties limitations, and indemnification language appropriate to your jurisdiction.

**Results vary. Always validate with real clients and legal counsel.**  
Using these templates without proper legal review can expose your agency to significant legal, financial, and reputational risk. The authors and maintainers of the AI Agency Starter Kit 2026 assume no liability for any consequences arising from the use of these materials.

---

## Proposal Outline (Sales / Pre-SOW Document)

Use this as a 1–3 page professional document to summarize the opportunity and recommended solution. It builds excitement and leads naturally into the detailed SOW.

### Recommended Structure

**1. Cover / Header**  
[YOUR_BRAND] Proposal  
Prepared for: [CLIENT NAME]  
Date: [DATE]  
Project: [PROJECT / ENGAGEMENT NAME]  
Prepared by: [YOUR NAME], [YOUR TITLE]

**2. Executive Summary** (3–5 sentences)  
Brief restatement of the client’s primary pain point or goal + the high-level outcome you will deliver (reference the specific tier from the Productized Service Catalog).

**3. Understanding of Your Needs**  
- Summary of discovery findings (or what you learned in initial conversations)
- Key workflows/processes discussed
- Quantified pain or opportunity where possible (hours, errors, revenue impact)
- **[CUSTOMIZE FOR YOUR NICHE]** Example language for landscaping contractors, law firms, medical practices, etc.

**4. Recommended Solution**  
- Which package(s) from the **Productized Service Catalog** you recommend (Discovery, Implementation, Retainer, or Hybrid)
- High-level description of what will be built (multi-agent orchestration, RAG where relevant, integrations, self-hosted n8n where appropriate)
- Expected outcomes and sample ROI metrics (pull from your case studies or the ROI proof template)
- Why this approach (agentic systems with human oversight, process-first, ongoing optimization via retainer)

**5. Timeline & Investment**  
- High-level timeline (reference the timelines in the Service Catalog)
- Investment summary (use numbers from your Pricing Strategy Guide + Service Catalog)
  - One-time fees
  - Monthly retainer (if applicable)
  - Any API/infrastructure estimates with security margin noted
- Payment terms overview (50% on signing for implementation, monthly in advance for retainers, etc.)

**6. Why [YOUR_BRAND]**  
- Relevant experience, niche focus, approach to risk management (AI disclaimers, monitoring, cost control)
- Commitment to transparent scoping and change management

**7. Next Steps**  
- Proposed timeline for SOW review and signing
- Any additional discovery needed
- Call to action / signature block or “Ready to proceed?” question

**8. Appendix (optional)**  
- High-level architecture diagram (Mermaid or image)
- Sample deliverables from similar work (anonymized)
- Link to or excerpt from the Productized Service Catalog

---

## Statement of Work (SOW) Template

This becomes the detailed, signed agreement for the specific engagement. It should reference or attach the MSA if you have one.

### Header
**Statement of Work (SOW)**  
SOW Number: [SOW-YYYY-XXX]  
Effective Date: [DATE]  
Between: [YOUR_BRAND] (“Agency”) and [CLIENT LEGAL NAME] (“Client”)  
Project / Engagement: [NAME]  
Package: [Discovery & Audit / Implementation / Operations Retainer / Hybrid] as defined in the Productized Service Catalog

### 1. Scope of Work
Describe what is included at a high level, then drill into specifics.

**This SOW covers the [Tier Name] package** as detailed in the Agency’s Productized Service Catalog (attached or referenced).

**In-scope activities include:**
- [Bullet list drawn directly from the Service Catalog for the chosen tier]
- Specific workflows/agents to be built or audited: [LIST]
- Integrations: [LIST]
- Technology stack: Primarily self-hosted n8n (or Client’s preferred environment), with LLM providers [LIST], RAG/vector capabilities where scoped, and human-in-the-loop oversight.
- **[CUSTOMIZE FOR YOUR NICHE]** Add vertical-specific details (e.g., “Automated job scheduling, technician dispatching, invoicing follow-up, and customer review request sequences for a landscaping contractor”).

**Out-of-scope / Exclusions** (critical — list explicitly):
- Anything not listed above
- Major custom development outside the agreed low-code/no-code patterns
- Data migration or cleansing beyond agreed scope
- Ongoing monitoring and optimization (unless Retainer tier is selected)
- Performance guarantees beyond tested scenarios
- 24/7 real-time support (unless explicitly scoped)

### 2. Deliverables
Use a table for clarity.

| Deliverable | Description | Format | Due / Milestone |
|:---|:---|:---|:---|
| [e.g., Audit Report] | Comprehensive findings, prioritized opportunities, ROI projections, recommended roadmap | PDF + editable source | End of Discovery phase |
| [e.g., Deployed Workflows] | Fully functional agents/workflows in production environment | n8n instance + exports + documentation | Implementation completion |
| User Guide & Runbook | Step-by-step operational instructions | PDF + recorded walkthrough | Handoff |
| Monthly Performance Reports (Retainer) | Metrics, optimizations performed, recommendations | Dashboard + PDF summary | Monthly |
| Quarterly Business Review | ROI tracking, strategy discussion | Presentation + call | Quarterly |

**Additional deliverables** as scoped in the attached Service Catalog tier description.

### 3. Timeline & Milestones
High-level phases with dates or week numbers.

**Example for Implementation tier (customize per project):**
- Week 1–2: Detailed scoping workshop & final requirements sign-off
- Week 3–6: Build, integration, internal testing & QA (including hallucination/edge-case testing)
- Week 7–8: Client UAT, training, and deployment
- Week 9–10: 30-day stabilization window
- Ongoing (if Retainer): Monthly optimization + reporting

**Milestone acceptance criteria** and sign-off process will be defined in the detailed project plan.

### 4. Intellectual Property (IP) Ownership
**Agency retains all rights** to its pre-existing frameworks, templates, prompt libraries, multi-agent orchestration patterns, generalized workflow designs, evaluation methods, and any improvements that can be productized or reused with other clients (anonymized, without Client data).

**Client owns**:
- All Client-specific data, credentials, and outputs generated by the system in normal operation.
- Custom workflows/agents built exclusively for Client’s unique processes and explicitly scoped as bespoke in this SOW.
- Client data models and proprietary business logic documented during the engagement.

A more detailed IP clause is included in the Master Services Agreement (or will be added here if no MSA exists). See also the IP section in the Productized Service Catalog.

### 5. Payment Terms
**Total Investment** (reference exact numbers from your pricing):
- One-time Implementation / Discovery fee: $[AMOUNT]
- Monthly Operations Retainer: $[AMOUNT]/month (minimum [X] months)
- Estimated API & Infrastructure fee (with security margin): $[AMOUNT]/month or as reconciled quarterly

**Payment Schedule**:
- 50% of one-time fees due upon signing of this SOW
- Remaining 50% due upon [milestone, e.g., deployment or acceptance]
- Retainers billed monthly in advance
- Net [15/30] days unless otherwise agreed
- Late payments may pause work

All pricing includes the security margins for variable API token consumption as outlined in the Pricing Strategy Guide.

### 6. Liability, Disclaimers & Warranties (Critical AI Section)
**THE AGENCY MAKES NO WARRANTIES**, express or implied, regarding the accuracy, completeness, reliability, or fitness for a particular purpose of any AI-generated outputs, recommendations, or automated workflows. AI systems are inherently non-deterministic.

**Client acknowledges and agrees that**:
- LLM outputs may contain hallucinations, errors, biases, or outdated information.
- LLM providers may change models, capabilities, availability, or pricing with limited notice, which can affect system behavior and cost.
- The Agency will implement reasonable monitoring, fallback mechanisms, and human oversight where scoped, but cannot guarantee zero errors or perfect performance.
- Client is responsible for reviewing all AI outputs before relying on them for business, legal, financial, or safety-critical decisions.
- The Agency’s total liability under this SOW shall be limited to the fees paid by Client in the [3/6/12] months preceding any claim. In no event shall the Agency be liable for indirect, incidental, consequential, special, or punitive damages, including lost profits or business interruption.

**Indemnification**: Client agrees to indemnify and hold harmless the Agency from claims arising from Client’s use of the deliverables or Client-supplied data.

Additional liability limitations appear in the Master Services Agreement.

### 7. Change Management
Any work outside the defined Scope requires a written Change Order signed by both parties. Change Orders will describe the additional scope, impact on timeline, and adjusted fees. The Agency will not perform out-of-scope work without approved Change Order.

### 8. Term & Termination
- Implementation / Discovery projects: Effective until deliverables are accepted or as otherwise agreed.
- Retainers: Month-to-month after initial term, terminable by either party with [30/60] days written notice.
- Either party may terminate for material breach with [15/30] days cure period.
- Upon termination, Client receives deliverables completed to date (subject to payment) and Agency retains its reusable IP.

### 9. Data Security & Confidentiality
Agency will handle Client data in accordance with the Data Processing Agreement (if applicable) and industry-standard practices. Client is responsible for providing accurate, authorized data and for its own compliance obligations (GDPR, CCPA, HIPAA, etc.).

### 10. Signatures
**Agency**  
Signature: _______________________________  
Name / Title: ____________________________  
Date: __________________________________

**Client**  
Signature: _______________________________  
Name / Title: ____________________________  
Date: __________________________________

---

## Sample Language — Implementation Tier for [Niche Example]

**Scope excerpt (customize)**:  
Design and deployment of a multi-agent lead qualification + enrichment + CRM sync system for [landscaping contractor / law firm / medical practice]. Includes n8n self-hosted orchestration, RAG over approved knowledge base (if scoped), cost monitoring with security buffer, hallucination testing protocol, documentation, and 30-day stabilization.

**Liability excerpt (always include)**:  
Client understands that the automated qualification agent may occasionally route or score leads incorrectly. The Agency has implemented fallback logic and monitoring, but final review of all AI-influenced decisions remains the Client’s responsibility.

---

## Customization & Quality Checklist (Before Sending Any Document)

- [ ] All `[PLACEHOLDERS]` replaced with real information
- [ ] Scopes, deliverables, timelines, and pricing exactly match the agreed tier from the Productized Service Catalog
- [ ] IP Ownership section is clear and balanced (Client owns their data/outputs; Agency retains reusable IP)
- [ ] Strong AI liability and non-deterministic disclaimers are present and prominent
- [ ] Payment terms, change management, and termination clauses are included
- [ ] Exclusions are explicit
- [ ] Document has been reviewed by qualified legal counsel for your jurisdiction
- [ ] Version controlled and stored with project files
- [ ] Client has received a copy of (or link to) the relevant tier description from the Service Catalog

---

## Next Steps After Using This Template

1. **Customize:** Adapt the text to fit the exact parameters of your project.
2. **Review:** Cross-reference all pricing, scopes, and exclusions with your `pricing-strategy-guide-and-calculator.md` outputs.
3. **Legal Check:** Bring the customized template to a licensed attorney to convert it into a formal legal agreement for your jurisdiction.
4. **Execute:** Sign and archive the completed SOW before starting development.
