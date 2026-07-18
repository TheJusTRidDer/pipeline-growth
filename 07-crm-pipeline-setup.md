# CRM Pipeline Setup Guide — HubSpot (Free)

## Why HubSpot Free

| Feature | Free Tier | Why You Need It |
|---|---|---|
| Contact management | Unlimited | Store all prospects and clients |
| Deal pipeline | 1 pipeline, multiple stages | Track prospects from lead to close |
| Task management | Unlimited | Never drop a follow-up |
| Email integration | 1 connected mailbox | Log all emails automatically |
| Meeting scheduler | Yes | Share booking link in emails |
| Dashboard | Basic | See pipeline value at a glance |

**Setup time:** 1.5 hours

---

## Step 1: Create Your Pipeline Stages

Go to Settings → CRM → Pipelines → Deals.

Create a single pipeline named **"Growth Sales"** with these stages:

| Stage | Description | Exit Criteria |
|---|---|---|
| **1. Prospect** | Identified but not yet contacted | Added to sequence |
| **2. Contacted** | First outreach sent (email/LinkedIn) | Any reply received |
| **3. Responded** | Prospect replied to outreach | Discovery call booked |
| **4. Discovery Call** | 30-min call completed | Audit offered or proposal requested |
| **5. Audit in Progress** | $497 Growth Audit delivered | Audit report delivered |
| **6. Proposal Sent** | Formal proposal delivered | Follow-up scheduled |
| **7. Negotiation** | Discussing terms, pricing, scope | Verbal agreement |
| **8. Closed Won** | Contract signed, onboarding | First payment received |
| **9. Closed Lost** | Prospect declined | Reason logged |
| **10. Nurture** | Not now but potential future | 90-day re-engagement |

---

## Step 2: Custom Properties to Track

Create these custom contact/deal properties:

| Property Name | Type | Values | Purpose |
|---|---|---|---|
| `Client Tier` | Dropdown | Audit, Growth Engine, Growth Partner | Track service tier |
| `Lead Source` | Dropdown | Referral, LinkedIn, Cold Email, Partner, Website, Other | Channel attribution |
| `Priority Score` | Number (0-100) | 0-100 | Lead scoring |
| `Pipeline Value (Annual)` | Currency | $0-$500k | ARR tracking |
| `Last Contact Date` | Date | Auto | Recency tracking |
| `Referral Source` | Text | Name of referrer | Referral tracking |
| `Pain Point` | Multi-checkbox | Pipeline inconsistency, Low close rate, No outbound, Poor positioning, Other | Personalization |
| `Decision Maker Role` | Dropdown | CEO, Managing Partner, Head of BD, CMO, Founder, Other | Role-based messaging |
| `Budget Signal` | Dropdown | High, Medium, Low, Unknown | Prioritization |
| `Follow-up Scheduled` | Date | Auto | Never drop a ball |

---

## Step 3: Import Your Existing Clients

Create a CSV with these columns and import into Contacts:

```csv
First Name,Last Name,Email,Phone,Company,Website,Industry,Client Tier,Monthly Retainer,Start Date,Last Contact Date
[Name],[Name],[email],[phone],[Company],[url],[Industry],[Engine/Partner],[$],[Date],[Date]
```

**Import path:** Contacts → Import → Select CSV → Map fields

---

## Step 4: Set Up Email Integration

| Action | Steps |
|---|---|
| Connect your email | Settings → Integrations → Email → Connect |
| Enable logging | Toggle "Log emails automatically" |
| Create email templates | Settings → Conversations → Templates |
| Set up meeting link | CRM → Meetings → Create booking link |

**Email templates to create (from `03-cold-email-sequence.md`):**
- Template 1: Initial outreach (Direct Ask)
- Template 2: Insight Hook (Referral Math)
- Template 3: Case Study
- Template 4: Growth Audit offer
- Template 5: Breakup

---

## Step 5: Create Contact Lists (Segments)

| List Name | Criteria | Use |
|---|---|---|
| **Active Pipeline** | Deal stage = 1-7 | Weekly review |
| **Warm Leads** | Priority Score > 60 | Prioritize outreach |
| **Needs Follow-up** | Last Contact Date > 7 days + stage 1-2 | Never miss a touch |
| **Referral Sources** | Lead Source = Referral | Send thank-yous |
| **Nurture** | Stage = 10, last contact > 90 days | Quarterly re-engagement |
| **Top 20 Prospects** | Manual list | High-touch personal outreach |

---

## Step 6: Set Up Daily CRM Workflow

**Every morning (15 minutes):**

| Time | Action |
|---|---|
| 08:00 | Check dashboard: pipeline value, deals stuck > 7 days |
| 08:05 | Review tasks: any follow-ups due today |
| 08:08 | Check "Active Pipeline" list: move deals forward |
| 08:12 | Add new prospects from LinkedIn/Apollo from yesterday |
| 08:15 | Log any calls/emails from previous day |

**Weekly review (30 minutes every Friday):**

| Metric | Track | Target |
|---|---|---|
| New prospects added | Count | 50+ |
| Emails sent | Count | 200+ |
| Replies received | Count | 5+ |
| Discovery calls booked | Count | 2+ | 
| Proposals sent | Count | 1+ |
| Deals closed | Count + $ | 1 every 2 weeks |
| Pipeline value | $ | $50k+ |

---

## Step 7: Dashboard Setup

Create a simple dashboard with these tiles:

| Tile | Data | Chart Type |
|---|---|---|
| Pipeline by Stage | Deal count + value per stage | Funnel |
| Monthly New Deals | New deals created this month | Bar |
| Lead Source Breakdown | Deals by Lead Source | Pie |
| Close Rate | Won vs Lost this quarter | Gauge (50%+ = green) |
| Monthly Revenue | Won deal values by month | Line |
| Upcoming Tasks | Tasks due in next 7 days | List |

---

## Step 8: Follow-up Automation Rules (Manual SOP)

| Rule | Action |
|---|---|
| Prospect unresponsive after 5 emails | Move to Nurture stage, schedule 90-day re-engage |
| Discovery call completed | Create task: "Send proposal within 24 hours" |
| Proposal sent with no reply in 5 days | Create task: "Follow-up call/email" |
| Deal stays in Negotiation > 14 days | Create task: "Check-in — what's blocking?" |
| Closed Won | Create task: "Send welcome email + schedule onboarding" |
| Closed Lost | Create task: "Log reason + schedule 6-month check-in" |

---

## Tools to Complement HubSpot Free

| Tool | Purpose | Cost | Integration |
|---|---|---|---|
| **Apollo.io** | Prospect lists + email finder | $99/mo | Native HubSpot sync |
| **HubSpot Sales Hub (Paid)** | Sequences, automation, reporting | $50/mo/user | Native |
| **Mixmax** | Email tracking, templates, sequences | $24/mo | Chrome extension |
| **Calendly** | Advanced meeting scheduling | Free | Native |
| **Notion** | SOPs, templates, client deliverables | Free | Manual |
| **Slack** | Async client communication | Free | Native |

**Minimum viable stack:** HubSpot Free + Apollo.io ($99) + Calendly (Free)

---

## Step 9: First 7 Days — CRM Setup Checklist

| Day | Action | Done? |
|---|---|---|
| 1 | Create pipeline stages + custom properties | ☐ |
| 2 | Import existing client data (10+ clients) | ☐ |
| 3 | Connect email + upload templates from sequence | ☐ |
| 4 | Create 5 contact lists | ☐ |
| 5 | Set up meeting booking link | ☐ |
| 6 | Build dashboard | ☐ |
| 7 | Add first 20 new prospects from lead list | ☐ |
