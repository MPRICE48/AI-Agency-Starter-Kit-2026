# Scoping Process SOP

**Module 5 | Detailed SOPs: Scoping Process**

## Why This Phase Matters
Effective scoping translates discovery insights into a precise, value-anchored project proposal. It establishes boundaries on integrations, defines what is out of scope, outlines the agentic architecture, and prevents 90% of future delivery disputes or scope-creep margin leaks.

---

## 1. Step-by-Step Scoping Protocol

### Step 1: Process Mapping (Days 1-3)
- Construct a visual workflow flowchart (using Mermaid syntax or whiteboard tools) detailing the client's current manual steps.
- Highlight the decision gates, data transfer points, and human validation checks.
- Group operations into logical blocks (e.g., Lead Intake, Qualification, Route Optimization, CRM Sync).

### Step 2: Tech Selection & Design (Days 2-4)
- Select the orchestrator engine (self-hosted n8n is the primary default).
- Identify external API integrations, webhooks, and database dependencies.
- Map the data flow security rules: Ensure all credentials reside in Docker environment variables or secure credential managers rather than within the workflow nodes.
- Determine RAG requirements: Estimate vector database scale, indexing pipelines, and document ingestion models if semantic search is required.

### Step 3: Proposal Drafting (Days 4-6)
Draft a formal Statement of Work (SOW) utilizing the template in `proposal-and-sow-templates.md`. Ensure you include:
1. **Current State Process Chart**
2. **Proposed Automation Flow**
3. **In-Scope Deliverables:** Explicitly define the number of n8n workflows, agents, and target databases.
4. **Out-of-Scope Exclusions:** Clearly state what is NOT included (e.g., custom mobile app dev, database migrations, cleanups).
5. **Acceptance Criteria:** Set the metric thresholds for milestone completion (e.g., "UAT session passes with $\ge 95\%$ functional accuracy on 30 test records").

---

## 2. Technical Feasibility Check

Before finalizing the SOW, verify the following checklist:

- [ ] **API Availability:** Confirm the client's tools (e.g., CRM, accounting software) have accessible endpoints and authorization permissions.
- [ ] **Data Quality Validation:** Verify the test dataset contains structured, clean records. If raw data is chaotic, require the client to clean it before development starts.
- [ ] **Latency Tolerances:** Ensure the client understands that multi-agent prompts can take 5–15 seconds to execute. If immediate response is required, design fast caching routers.
- [ ] **Rate Limits:** Check API call limits for all integrated services. If volume is high, build n8n delay nodes to batch executions.

---

## 3. Client Alignment Review
- Conduct a 30-minute alignment call with the client's project lead.
- Walk through the visual process map and get verbal sign-off on the transition from manual steps to automated steps.
- Confirm payment terms (e.g., 50% upfront, 50% upon UAT sign-off).
- Sign SOW, Master Services Agreement (MSA), and Data Processing Agreement (DPA) before writing any workflow code.
