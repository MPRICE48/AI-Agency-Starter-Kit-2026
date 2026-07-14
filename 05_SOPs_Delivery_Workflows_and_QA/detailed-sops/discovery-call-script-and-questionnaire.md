# Discovery Call Script and Questionnaire

**Module 5 | Detailed SOPs: Discovery Call Script and Questionnaire**

## Why This Phase Matters
Poor discovery is the primary cause of scope creep, underpriced projects, and failed AI implementations. A structured 30–45 minute conversation qualifies client opportunities, uncovers workflow blockers, and defines database constraints early, while ensuring data privacy boundaries are protected from day one.

---

## 1. Pre-Call Preparation (10 minutes)
- Research the prospect's company website, team size, and niche vertical.
- Review the intake channel source to identify context (e.g., did they view a specific case study?).
- Prepare a shared document or Notion page to capture notes.
- **Security Rule (Non-Negotiable):** Never ask for raw database passwords, production user logins, or administrative root access during a discovery call. Request only read-only test credentials, sandbox environments, or exported anonymized spreadsheets.

---

## 2. Discovery Call Agenda & Script

### Opening (2 minutes)
> "Hi [Prospect Name], thank you for scheduling this call. Today, my primary goal is to understand your day-to-day workflow processes, identify where your staff is spending the most time on manual tasks, and see if there is a clear ROI pathway for automating those steps. Everything we discuss is confidential. I will also walk through our data security protocols to ensure we protect your information from the very start. Does that sound good?"

### Discovery Questionnaire (30 minutes)

#### Section A: Current Process Mapping
1. "Could you walk me through a typical client journey from start to finish? For example, when a new lead requests an estimate, how does that get processed, scheduled, and billed?"
2. "Which steps in that sequence are handled manually by your team? Who is responsible for each step?"
3. "Which software tools do you currently use for this process (e.g., Jobber, ServiceTitan, Clio, HubSpot, QuickBooks)?"
4. "Where does the workflow slow down or break, especially during peak seasons?"

#### Section B: Quantifiable Pain Points
1. "How many hours per week does your staff spend on manual data entry, scheduling adjustments, or customer follow-ups?"
2. "What are the common errors that happen in this process (e.g., scheduling double-bookings, manual typos in invoicing, lost lead details)?"
3. "What is the financial cost or operational delay caused by these errors?"

#### Section C: Systems & Access Feasibility
1. "Which databases or software hold the primary customer information?"
2. "Do these systems offer API access, webhook configurations, or import/export settings?"
3. "For design and validation phases, can your team provide a staging or sandbox sandbox environment with fake data, or an exported sheet of historical test records?"

#### Section D: Niche-Specific Triggers
* **[CUSTOMIZE FOR YOUR NICHE - Landscaping & Home Services]**
  - "How are technicians notified of schedule updates or emergency route adjustments?"
  - "What happens to the job queue when weather delays occur?"
  - "How do you collect reviews or follow up on unpaid invoices?"

---

## 3. Qualification Scorecard

Rate the opportunity from 1 (low) to 5 (high) on these parameters to qualify the project:

| Parameter | Score (1-5) | Qualification Standard |
|:---|:---|:---|
| **Process Clarity** | | Clear, logical rules exist. If a human cannot explain the process rules on paper, it cannot be automated with AI. |
| **Data Access Willingness** | | Client agrees to provide sandbox/test environments or read-only API credentials. |
| **ROI Potential** | | High time savings (e.g., >10 hours/week) or significant error reduction value. |
| **System Compatibility** | | Target systems have modern API integrations or Webhook support (e.g., n8n has native nodes or HTTP options). |
| **Budget Alignment** | | Target budget aligns with our Productized Service Catalog pricing floors. |

*Action:* If total score is **$\ge 18$**, proceed to the **Scoping Phase**. If below, politely route the prospect to your email nurture list or self-serve audit templates.

---

## 4. Post-Call Actions
- Send a summary email to the prospect within 24 hours outlining identified pain points, estimated hours saved (hypothesized ROI), and next steps.
- Create an entry in your CRM logging system.
- If qualified, schedule the **Scoping Workshop** and request staging API access parameters.
