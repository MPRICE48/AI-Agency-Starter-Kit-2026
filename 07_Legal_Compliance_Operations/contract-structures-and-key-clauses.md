# Contract Structures and Key Clauses

**⚠️ CRITICAL LEGAL DISCLAIMER — READ BEFORE PROCEEDING ⚠️**

THIS DOCUMENT IS FOR EDUCATIONAL AND INFORMATIONAL PURPOSES ONLY. IT IS NOT LEGAL ADVICE AND DOES NOT CREATE AN ATTORNEY-CLIENT RELATIONSHIP. The structures, sections, and illustrative example clauses below are synthesized from common 2025–2026 industry practices for AI automation and agentic service providers. They are not lawyer-reviewed templates. Laws governing AI outputs, data processing, liability, IP, and contracts vary significantly by jurisdiction, industry vertical, and specific use case.

YOU MUST HAVE EVERY AGREEMENT REVIEWED, CUSTOMIZED, AND APPROVED BY A QUALIFIED ATTORNEY LICENSED IN THE RELEVANT JURISDICTION(S) BEFORE USE WITH ANY CLIENT OR PROSPECT.

---

## Why This Exists

In the 2026 AI Automation / Agent Agency model, you deliver productized, retainer-heavy services built on multi-agent orchestration, RAG pipelines, tool-calling workflows, and ongoing optimization. These engagements involve deep integration with client data and systems, probabilistic (non-deterministic) outputs, and reusable intellectual property that enables scalability across clients in your niche.

Standard freelance or one-off project agreements are insufficient and create material risk. This file gives you the structural understanding to:
- Clearly allocate IP so you retain rights to generalized agent templates, prompt libraries, orchestration patterns, and frameworks.
- Manage expectations around the inherent variability of LLM-powered agents (hallucinations, context drift, model updates).
- Define scopes, acceptance criteria, payment, data handling, and exit/transition paths.
- Address data protection obligations when agents access, reason over, store, or act on client information.

---

## How It Connects to Other Sections of the Kit

- **Module 3 (Services, Pricing, Packaging):** MSA/SOW structures and the key disclaimers are incorporated into proposals and statements of work.
- **Module 5 (SOPs & QA):** Termination/data return procedures align with handover and offboarding SOPs.
- **Module 4 (Tech Stack):** DPA must accurately list your actual sub-processors (LLM APIs, n8n hosting, vector DBs) and reflect self-hosted vs. cloud data residency choices.

---

## Master Services Agreement (MSA) Structure

The MSA establishes the high-level, long-term framework governing the overall relationship. Multiple SOWs live under one MSA.

### Core Sections
1. Parties, Effective Date, Definitions
2. Engagement Structure & Scope (reference SOWs)
3. Term, Renewal, and Termination (with transition assistance)
4. Fees, Payment Terms, and Invoicing
5. Confidentiality / Non-Disclosure
6. Intellectual Property Rights (critical background IP carve-outs)
7. Data Protection & Security (reference DPA)
8. Representations, Warranties & AI-Specific Disclaimers
9. Limitation of Liability & Indemnification
10. Governing Law & Dispute Resolution

---

## Illustrative Clauses (Discussion Drafts for Counsel)

### 1. Non-Deterministic Outputs & Hallucination Disclaimer
> **Non-Deterministic Nature of AI Technologies and Outputs.** Client acknowledges that the Services utilize artificial intelligence, large large models, retrieval-augmented generation (RAG), multi-agent orchestration, tool-calling, and related probabilistic technologies (collectively, “AI Technologies”). These systems are inherently non-deterministic. Outputs, decisions, and automated actions may vary, contain inaccuracies or “hallucinations,” reflect biases present in training data or prompts, or fail to perform as expected under edge cases, novel inputs, or after upstream model changes by third-party providers.  
>   
> [YOUR_BRAND] will implement commercially reasonable design, testing, monitoring, logging, fallback mechanisms, and human-in-the-loop oversight as described in the applicable SOW. Except as expressly and specifically guaranteed in a particular SOW, [YOUR_BRAND] provides no warranty, express or implied, that any AI-generated output, agent decision, or automated workflow will be accurate, complete, reliable, uninterrupted, or fit for any particular purpose. Client is solely responsible for reviewing and validating all outputs and automated actions before any business, legal, financial, medical, or other material reliance. [YOUR_BRAND] shall have no liability for losses arising from Client’s failure to conduct such review or to maintain appropriate human oversight gates.

### 2. Intellectual Property Ownership (Agency Source vs. Client Output/Data)
> **Intellectual Property Rights.**  
> **a. Agency Retained Background IP.** [YOUR_BRAND] retains all right, title, and interest in and to its pre-existing and independently developed intellectual property, including without limitation prompt libraries, agent architectures and templates, workflow orchestration patterns, generalized RAG configurations, code libraries, methodologies, know-how, and any improvements or generalizations thereof created during the engagement that are not specific to Client’s proprietary data or processes (“Agency Background IP”).  
>   
> **b. Client Ownership of Specific Deliverables.** Upon full payment of all applicable fees, Client owns all right, title, and interest in the specific custom-configured workflows, agent instances, integrations, vector stores/embeddings populated exclusively with Client’s data, reports, and other deliverables created solely for Client under an SOW (“Client Deliverables”). This expressly includes Client’s raw and processed data and Client-specific outputs.  
>   
> **c. License Grant.** [YOUR_BRAND] grants Client a limited, non-exclusive, non-transferable, royalty-free license to use Agency Background IP solely as embedded in the Client Deliverables for Client’s internal business purposes during the term of the applicable SOW and any active retainer. This license ends upon termination of the relevant engagement unless otherwise agreed in writing.

### 3. Termination & Transition Assistance
> **Termination and Transition.**  
> **a. For Convenience.** Either party may terminate this Agreement or any SOW upon [30/60] days’ prior written notice.  
>   
> **b. Effect of Termination.** Upon termination or expiration:  
> - Client pays all undisputed amounts due for Services performed through the effective date.  
> - [YOUR_BRAND] shall, upon Client’s written request and at Client’s expense, provide reasonable transition assistance for up to [30] days, including export of workflow configurations, documentation, and credential handoff procedures (without disclosing [YOUR_BRAND]’s internal credentials or Agency Background IP).  
> - [YOUR_BRAND] shall return or securely destroy all Client Confidential Information, Client data, Client-specific vector embeddings, and logs containing Client information.

---

## Data Processing Agreement (DPA) Essentials

A DPA is required whenever your workflows process Personal Data on behalf of the Client. Ensure it covers:
- **Roles:** Client = Controller; Agency = Processor.
- **Scope:** Describe agent workflows, RAG on client documents, logging for QA/debugging.
- **Sub-processors:** Living list of LLM providers, hosting VPS, vector DBs, and monitoring tools.
- **Data Subject Rights:** Assistance flows to support requests (access, deletion, correction).
- **Prohibition on training:** Outlaw the use of client personal data or outputs to train or fine-tune public foundation models (flowed down from provider terms).
