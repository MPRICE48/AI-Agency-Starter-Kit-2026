# Case Study & ROI Proof Template

**Module 3: Services, Pricing, and Packaging**

> **Why this exists**  
> In 2026, clients do not buy "AI features" or "cool agents"—they buy business outcomes. They want to know how much time they will save, how much their error rates will decrease, and how it will impact their bottom line. A structured Case Study is your most powerful sales asset.  
> This file provides a **standardized case study template** along with **three realistic, practitioner-grade vertical examples** (landscaping crew optimization, law firm intake, and HVAC booking automation). Use these examples to understand how to quantify value and construct stories that prove ROI before you have your own customer data.

---

## Part 1: Case Study Template

Copy this outline to write your own client case studies as you deliver successful implementations.

```markdown
# Case Study: How [CLIENT_NAME] Achieved [PRIMARY_METRIC, e.g., 55% Admin Time Reduction]

**Client Profile:** [Niche, company size, location, e.g., Mid-sized Residential Landscaping Contractor with 12 crews, Austin, TX]  
**Technology Used:** [e.g., n8n (self-hosted), Google Maps API, Jobber CRM, Anthropic Claude 3.5 Sonnet]  
**Timeline:** [e.g., 6 weeks implementation + 30-day stabilization]

## Executive Summary
A 3-5 sentence summary of the project. Detail the baseline situation, the automated agentic solution deployed, and the concrete metrics achieved.

## The Challenge
*What was holding the client back? What were their manual bottlenecks?*
- Detail the manual process before automation (e.g., "The owner spent 3 hours every evening manually mapping routes and texting crew leaders...").
- Quantify the cost of the problem (hours wasted, missed jobs, lead response latency, error rates).
- Explain system or data constraints (e.g., "Field notes were recorded on paper and re-typed into QuickBooks weekly, creating transcription errors").

## The Solution: Agentic Operations
*What did you build? How did you apply the agentic orchestration model?*
- **Workflow Orchestration:** Describe the n8n logic and tool connectors.
- **Agent Roles:** List the specific agent roles and their responsibilities (e.g., "Orchestrator Agent, Route Optimizer, Customer Text Dispatcher").
- **Knowledge & RAG:** Detail what data sources the agents accessed (e.g., historical pricing databases, company policy sheets).
- **Human-in-the-Loop (HITL) Gate:** Explain where human oversight was placed for safety (e.g., "Any estimate over $2,500 required manager review before sending").

## Quantifiable ROI & Business Impact
Provide concrete metrics comparing the baseline against the post-automation results:
* **Time Saved:** [e.g., 22 hours per week reclaimed by the General Manager]
* **Speed/Latency:** [e.g., Average quote response time decreased from 24 hours to 8 minutes]
* **Accuracy:** [e.g., Data entry discrepancies between Jobber and QuickBooks fell by 95%]
* **Financial Impact:** [e.g., Estimated $45,000/year in administrative overhead saved]

## Key Lessons & Optimization
What challenges arose during development or production, and how were they solved under the retainer model? (e.g., context compression to reduce token costs, prompt adjustments to handle non-standard address inputs).
```

---

## Part 2: Realistic Niche Examples (2026)

### Example 1: Landscaping Crew & Route Optimization

**Client Profile:** GreenScape Maintenance (15 seasonal crews, residential and commercial maintenance, Atlanta, GA)  
**Technology Deployed:** self-hosted n8n, OpenAI GPT-4o-mini (classification/extraction), Google Maps Distance Matrix API, Jobber API.  
**Engagement Model:** $3,000 Discovery + $12,500 Implementation + $2,000/mo Retainer.

#### The Challenge
GreenScape’s Operations Manager spent 3–4 hours every evening manually building crew schedules and routing paths for the next day. Rain delays or equipment breakdowns required manual rescheduling, causing dispatch errors and customer complaints about missed appointments. The manual scheduling process cost the company approximately 18 hours/week in manager overhead.

#### The Solution: The "Daily Dispatcher" Agent
1. **Intelligent Routing Agent:** An n8n workflow triggered at 5:00 PM that pulls active jobs from Jobber, groups them by geographic zones, queries the Google Maps API for optimal route ordering, and assigns crews based on historical crew speed and equipment loads.
2. **Weather-Aware Fallback Agent:** A scheduler node that monitors local weather forecasts. If precipitation exceeds 40%, the agent automatically holds outdoor maintenance jobs and schedules rain-date fallbacks based on open calendar slots.
3. **HITL Gate:** The optimized routes and schedules are presented to the Operations Manager in a simple n8n web form at 6:00 PM. The manager reviews, adjusts (if necessary), and clicks "Approve."
4. **Automated Notification Agent:** Upon manager approval, the system sends automated SMS updates to technicians detailing their route and SMS confirmations to homeowners with estimated arrival times.

#### Quantifiable ROI & Business Impact
* **Manager Time Saved:** Reclaimed 14 hours/week for the Operations Manager (78% reduction in scheduling admin).
* **Crew Utilization:** Billable hours per crew increased by 11% due to optimized route transit times (equivalent to adding 1.5 extra jobs per crew per week).
* **No-Shows/Cancellations:** Reduced missed appointments by 85% through automated customer SMS confirmations.
* **Financial Return:** The client realized approximately $52,000 in saved administrative time and increased crew billing in the first 6 months.

---

### Example 2: Client Intake & Conflict Checking for a Law Firm

**Client Profile:** Beacon Family Law (5 attorneys, boutique practice, Seattle, WA)  
**Technology Deployed:** self-hosted n8n, Clio API, Anthropic Claude 3.5 Sonnet (for extraction and logical checking), Pinecone Vector DB (for RAG conflict searches).  
**Engagement Model:** $2,500 Discovery + $15,000 Implementation + $1,800/mo Retainer.

#### The Challenge
Incoming web and phone inquiries were manually reviewed by a legal assistant. The intake process required checking Clio database records for conflicts of interest (e.g., past representation of opposing parties) and routing qualified leads to attorneys. The average lead-to-call response latency was 28 hours, resulting in a 35% drop-off rate as prospects hired competitors who responded faster.

#### The Solution: The "Intake & Conflict Check" Agent Loop
1. **Inquiry Parsing Agent:** A webhook processes new inquiries from web forms, emails, or call-service transcripts. Claude extracts names of the prospect, spouse, opposing parties, and case summaries.
2. **RAG Conflict Checker:** The extracted names are queried against Beacon’s historical client database in Clio and a vectorized index of past opposing parties in Pinecone. The agent flags potential matches.
3. **HITL Intake Gate:** If a conflict check is clean, the agent drafts a client profile and schedules a consultation call link. If a conflict is flagged, it locks the file and alerts the Managing Partner.
4. **Automated Handoff:** The legal assistant receives an alert in Slack with the pre-drafted client profile, conflict check certificate, and scheduling status. They review and sign off with a single click.

#### Quantifiable ROI & Business Impact
* **Response Latency:** Decreased average response time from 28 hours to 9 minutes for qualified, conflict-free leads.
* **Lead Conversion:** Initial consultation booking rate increased by 42%.
* **Admin Time Saved:** Reclaimed 12 hours/week of administrative work for the legal assistant.
* **Risk Mitigation:** Eliminated human error in manual conflict checking, reducing malpractice risk.

---

### Example 3: Customer Booking Agent for an HVAC Service Contractor

**Client Profile:** Apex Comfort Systems (8 residential service trucks, Dallas, TX)  
**Technology Deployed:** self-hosted n8n, Vapi (for voice synthesis), OpenAI GPT-4o-mini (classification), ServiceTitan API.  
**Engagement Model:** $3,000 Discovery + $18,000 Implementation + $2,500/mo Retainer.

#### The Challenge
Apex missed approximately 30% of incoming customer calls after hours and during summer dispatch spikes. Answering services were expensive ($1.50/minute) and could only record messages without checking real-time technician availability or booking jobs, resulting in lost emergency service calls to competitors.

#### The Solution: The "Apex Voice Assistant"
1. **Interactive Voice Agent:** Built a Vapi voice connection integrated with an n8n scheduling workflow. The agent answers calls, identifies the service request (e.g., AC not cooling), and queries ServiceTitan for real-time technician availability.
2. **RAG Knowledge Base:** The voice agent queries a company knowledge base (RAG) to answer common customer questions regarding diagnostic fees, operating hours, and service guarantees.
3. **Intelligent Booking Loop:** The agent offers available appointment slots, captures the customer's contact details, and logs the booking directly in ServiceTitan.
4. **Emergency Escalation Gate:** If the customer reports a critical hazard (e.g., gas smell or system fire), the agent immediately terminates the AI loop and routes the call to the on-call manager's phone.

#### Quantifiable ROI & Business Impact
* **Lead Capture:** Captured and booked 45 additional after-hours service calls per month that would have previously been missed.
* **Booking Latency:** Reduced appointment booking time to under 3 minutes without human staff intervention.
* **Answering Service Costs:** Cut third-party call center costs by $1,800/month.
* **Revenue Lift:** Generated an additional $11,500/month in gross billing through automated after-hours bookings.

---

## Actionable Next Steps

1. Use the **Case Study Template** to document pilot projects.
2. Adapt these vertical examples to pitch similar prospects in your validated niche.
3. Use the metric baselines in these examples to justify implementation and retainer fees during sales conversations.
