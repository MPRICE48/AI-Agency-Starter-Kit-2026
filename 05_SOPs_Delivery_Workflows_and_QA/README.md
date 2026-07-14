# Module 5: SOPs, Delivery Workflows, and QA

Welcome to the operational execution layer of the **AI-Agency-Starter-Kit-2026**. This module outlines the step-by-step processes required to discover customer problems, scope architectures, build and QA non-deterministic agents, hand off deployments, and automate your own agency's workflows.

## Folder Purpose

The purpose of this folder is to transition your agency from abstract planning to repeatable delivery operations. AI agents, multi-agent loops, and RAG pipelines introduce unique operational risks (hallucinations, token cost spikes, API changes). These SOPs establish mandatory stage gates and QA protocols to protect your margins and build long-term client retainer trust.

## File Navigation & Reading Order

We recommend reading and completing these files in the following order:

1. **[`end-to-end-client-journey-map.md`](end-to-end-client-journey-map.md)**  
   *The master stage-gate map outlining all project phases from Discovery through to Retainer Optimization.*
2. **[`project-management-templates.md`](project-management-templates.md)**  
   *Notion and ClickUp project database structures separating internal delivery views from client portals.*
3. **[`detailed-sops/`](detailed-sops/) (Subfolder)**  
   *Step-by-step execution scripts and protocols:*
   * **[`discovery-call-script-and-questionnaire.md`](detailed-sops/discovery-call-script-and-questionnaire.md)** — Pain mapping, stack auditing, and client qualification scorecards.
   * **[`scoping-process.md`](detailed-sops/scoping-process.md)** — Technical feasibility checks, process mapping guidelines, and proposal boundaries.
   * **[`build-checklist-and-qa-protocol.md`](detailed-sops/build-checklist-and-qa-protocol.md)** — Development safety rules, edge case tests, and hallucination evaluations.
   * **[`reporting-template-with-metrics.md`](detailed-sops/reporting-template-with-metrics.md)** — Copy-paste monthly ROI dashboards and recovered labor hour formulas.
4. **[`internal-agency-ops-prompts-and-sops.md`](internal-agency-ops-prompts-and-sops.md)**  
   *Structured system instructions to deploy internal AI agents (summarizers, researchers, proposal drafts, and code review).*

## How It Connects to Other Modules

* **Productized Catalog (`03_Services_Pricing_and_Packaging/`)**  
  The scoping and SOW templates directly enforce the pricing floors and service boundaries defined in Module 3.
* **Tech Stack Builds (`04_Tech_Stack_Build_Guides_and_Examples/`)**  
  The build checklist and QA parameters govern how you write prompts, index vectors, and setup environments inside your n8n instances.
* **Legal Agreements (`07_Legal_Compliance_Operations/`)**  
  The data governance rules applied during the Handoff phase ensure compliance with client-signed Master Services Agreements (MSA) and DPAs.

---

> **[CUSTOMIZE FOR YOUR NICHE]**  
> Tailor the discovery questionnaire scripts and monthly ROI dashboard formulas to align with the specific tools and business vocabularies of your target client vertical.
