# Reporting Template with Metrics

**Module 5 | Detailed SOPs: Reporting Template with Metrics**

## Why This Phase Matters
Retainers depend entirely on the client's perception of value. In the AI agency space, client churn occurs when business owners do not see how automated agents impact their operations. This template maps your system's performance metrics directly to business outcomes (hours saved, error reduction, financial efficiency).

---

## 1. Reporting Cycle & Cadence

* **Post-Launch (First 30 Days):** Send weekly summary updates to catch early edge cases and build client confidence.
* **Monthly Review:** Deliver the standard Monthly ROI Report accompanied by a 30-minute review call.
* **Quarterly Business Review (QBR):** Conduct a strategy call focusing on scaling opportunity backlogs and system expansions.

---

## 2. Monthly ROI Report Template

Copy the structure below to generate reports for your clients:

```markdown
# Monthly ROI & Performance Report: [Client Company Name]
**Reporting Period:** [Month, Year]  
**Overall System Health:** [Green / Yellow / Red]  
**Key Contact:** [Agency Account Manager]

---

## 1. Executive Summary
Provide a 3-5 sentence highlight of system value delivered this month.
- *Key Win:* [e.g., Deployed automated weather delay scheduler, preventing 32 dispatcher phone calls.]
- *Overall Impact:* [e.g., Saved 18.5 hours of GM administration, maintaining a 98.4% automated route accuracy rate.]

---

## 2. Quantitative Metrics Dashboard

| Metric | Previous Period | This Period | Cumulative Total | Notes / Target |
|:---|:---|:---|:---|:---|
| **System Executions** | [Number] | [Number] | [Number] | Total workflows processed |
| **Hours Saved (GM/Admin)**| [Hours] | [Hours] | [Hours] | Calculated from baseline |
| **Calculated Financial Return**| $[Amount] | $[Amount] | $[Amount] | Hours saved × burdened wage |
| **Automated Success Rate**| [X.X]% | [X.X]% | — | Executions without manual error |
| **Human Escalation Rate** | [X.X]% | [X.X]% | — | Target < 15% |
| **Average Token Cost / Run** | $[Amount] | $[Amount] | — | Budget limit: $[Limit] |
| **Client ROI Ratio** | [X.X]x | [X.X]x | [X.X]x | Financial return ÷ retainer fee |

---

## 3. Incident Log & Escalations
Summary of any errors or API outages occurred:
* **Date - Incident:** [e.g., 2026-08-12: Jobber API returned 502 error during dispatch run.]
* **Resolution:** [e.g., Fallback circuit-breaker held the queue. Workflow retried successfully 15 minutes later. No customer impact.]

---

## 4. Prioritized Optimization Backlog
Recommended updates for the next monthly sprint:
1. [e.g., Enable prompt caching for customer intake RAG ($120/mo projected token savings).]
2. [e.g., Integrate Google Calendar fallback sync for technician time-off tracking.]
```

---

## 3. Formulating ROI Calculations (Standard Guide)

Ensure you utilize conservative, defendable calculations in reports:

### recovered labor hours:
$$\text{Hours Saved} = \text{Executions} \times \frac{\text{Manual Process Minutes} - \text{Automated Process Minutes}}{60}$$

### financial savings value:
$$\text{Savings} = \text{Hours Saved} \times \text{Staff Fully Burdened Hourly Wage}$$

*Example (Trades Niche):*
If manual dispatching takes **15 minutes** per job, and the automated n8n routing requires **2 minutes** of manager review, you save **13 minutes** per execution.
At **120 jobs/month** and a burdened dispatch manager wage of **$45/hour**:
$$\text{Hours Saved} = 120 \times \frac{13}{60} = \mathbf{26\text{ hours/month}}$$
$$\text{Savings} = 26 \times \$45 = \mathbf{\$1,170\text{/month}}$$
Use this data during monthly reviews to justify your **$1,500/mo** operations retainer.
