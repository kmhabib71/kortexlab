# Banff Advisors - Technical Discovery & Automation Roadmap

Hey Matthew,

Finished the deep dive with Banff yesterday. This is going to be a fun one - they've got all the classic symptoms of a company that grew too fast on duct tape and prayers. Good news is they know it, have budget, and their team is technical enough to actually use what we build.

---

## TL;DR

**The Damage:** 89 hrs/month wasted on manual work across fragmented systems
**The Fix:** 12-week automation buildout (3 phases)
**The ROI:** $4,450/month saved, 3-4 month payback
**The Blocker:** Their proprietary platform has no API (we'll need to build one)

---

## What They Actually Do

Banff is a boutique exec advisory firm - basically a "career family office" for C-suite people. Two-sided marketplace:
- **Exec clients** (CEOs, CPOs) pay for career guidance + job placement
- **Enterprise clients** (PE/VC firms) pay for access to exec talent

Currently at 8-10 new exec clients/month, want to hit 20+ without hiring. The ops team (2 people handling 212 active clients) is completely buried.

**Tech Stack:**
- HubSpot (CRM - barely used)
- Notion (actual ops hub)
- **Contender** (proprietary platform - **NO API** ⚠️)
- Google Drive, Gmail, Slack, Zoom, DocuSign, Retool

Classic fragmentation problem. Data lives everywhere, nothing talks to anything.

---

## Current State Workflows (The Disasters)

### 1. Client Onboarding: 60 Minutes of Copy-Paste Hell

When a client signs, this happens:

```
Contract signed (DocuSign)
→ Manual email to TSQ (24hr delay)
→ TSQ sends contract, client signs
→ PDF emailed to ops team
→ First person to respond = client owner (weird system but ok)

Then the owner manually enters data into 4 systems:

HUBSPOT (10 min):
• Find/create contact
• Add LinkedIn URL (often have to hunt for this)
• Set client type, advisor, pathway, contract date, billing terms
• Mark as Tier 1

NOTION (5 min):
• Whale Sync auto-creates page when HubSpot tier changes ✓
• Manually add HubSpot link
• Manually add Contender link (doesn't exist yet, chicken/egg problem)

CONTENDER (15-20 min): ← THE PAIN
• Check if profile exists (might be Tier 3 from prior outreach)
• If new: Download LinkedIn PDF, upload to Contender, parse
• Manually download + upload profile photo
• Change tier 3→1
• Assign advisor
• Manually tag: functional expertise, industry expertise,
  target functions, target industries (all dropdown hell)

GOOGLE DRIVE (5 min):
• Create folder structure: /Clients/{Name}/Narratives/Resumes/LinkedIns/Bios
• Set sharing permissions

SEND WELCOME EMAIL (5 min):
• HubSpot template (semi-automated)
• Kickoff scheduler link + form
```

**Total: 40-60 min × 10 clients/month = 8-10 hrs/month**

**Why it's stupid:** Same data entered 4 times. High error rate. Contender has no API so it's all manual UI clicking.

---

### 2. Task Extraction: The 10-20 Hr/Week Black Hole

This is where most time disappears. Their communication is completely fragmented:

**How tasks arrive:**
- David (advisor): Emails client ops with tasks
- Liv (advisor): Slack messages
- Claire (advisor): Email + Slack + sometimes verbal + sometimes forgets
- All advisors: Zoom calls that dump transcripts to Notion (unread)

**Current process:**
1. Client ops starts day checking email, Slack, Notion transcripts
2. Manually extracts tasks from each source
3. Tries to prioritize (no system, just "who's loudest")
4. Updates Retool dashboard manually (often forgotten)

**What gets missed:**
- Tasks buried in long emails
- Action items mentioned in 60-min Zoom calls
- Follow-ups without explicit deadlines
- Basically anything that requires reading comprehension

**Time cost:** 2-3 hrs/day per ops person = **20-30 hrs/week team-wide**

---

### 3. P2P Introductions: Completely Invisible

"P2P" = introduce one exec client to another for networking. Good for retention, build goodwill, etc.

**Current workflow:**
```
Advisor: "Introduce Client A to Client B, both in healthcare"
↓
Ops manually drafts intro email
↓
Looks up both profiles in Contender/Notion for context
↓
Sends double opt-in intro
↓
...nothing else happens
```

**Tracking:** ZERO. No record of:
- Who was introduced to whom
- When
- Whether they actually connected
- Any outcome or value

It's like the introduction never happened. Can't measure value, can't avoid duplicate intros, can't follow up.

---

### 4. Sales Follow-Up: Pure Hope-Based Marketing

**Exec side:** Advisors have sales calls, keep notes in Notion, hope they remember to follow up. No deal pipeline, no reminders, nothing.

**Enterprise side:** Monthly manual review meeting where Amanda goes through spreadsheet asking "what happened with this lead?" One person tracking everything in her head.

They're definitely losing deals from lack of follow-up. How many? Unknown, because they're not tracking it.

---

### 5. Trending Campaigns: 10-15 Hours of Manual Labor + Profile Staleness Risk

"Trending" = send exec profile to PE/VC firms over 2-month campaign to generate opportunities.

**Current process:**
```
Week 1:
• Review client profile in Contender for accuracy
• Manually check if LinkedIn has updated (open both tabs, compare)
• Update Contender if stale (all manual entry)

Week 2-8:
• Manually select B4B partners to receive profile
• Send "whisper" batches weekly via Contender UI
• Manually track which partners got which profiles (spreadsheet? email folder?)
• Manually follow up at week 4
• Manually follow up at week 8
• Manually write summary report for client

Time: 10-15 hours per campaign
```

**The horror story:** Executives update their LinkedIn (new job, new role), but Contender profile is stale because no one manually updated it. Then they send outdated info to partners. Team's words: "we look like idiots."

---

### 6. Activity Tracking Dashboard: Broken By Design

They built a nice Retool dashboard to track all client activities:
- Kickoff calls
- Check-in calls
- Narrative edits
- Interview prep
- P2P introductions
- Trending campaigns

**The theory:**
```
Zoom call happens
→ Transcript dumps to Notion (via Zapier) ✓
→ Advisor tags call type in Notion
→ Retool reads Notion data
→ Dashboard shows activity counts
→ Alerts trigger if client inactive >45 days
```

**The reality:**
```
Zoom call happens ✓
→ Transcript dumps to Notion ✓
→ Advisor forgets to tag call type ✗
→ Retool shows ZERO activity
→ Dashboard is wrong
→ Team stops trusting it
→ Dashboard becomes useless
```

Human error rate on tagging is probably 40-50%. Dashboard is fiction.

---

## Root Cause Analysis

All these problems trace back to 4 root causes:

### 1. Contender Isolation
Their proprietary platform is an island. No API, no webhooks, no automation. Everything is manual UI clicking. This blocks:
- Automated onboarding
- Profile freshness monitoring
- Trending campaign automation
- Any integration with the rest of their stack

**Fix required:** Build API (their devs can do it, 3-4 weeks)

### 2. Communication Channel Fragmentation
Client updates arrive via: Email, Slack, text, Zoom, phone calls, smoke signals. No single source of truth.

**Fix required:** AI extraction layer that reads all channels and funnels to Notion

### 3. Human-Dependent Data Quality
Everything relies on humans remembering to tag, categorize, and log things correctly. Humans are bad at this.

**Fix required:** AI auto-tagging with validation, not manual entry

### 4. Zero Follow-Up Automation
Everything is one-and-done. Send email → hope for response. Make intro → hope they connect. No automated nudges.

**Fix required:** Smart reminder engine based on activity type

---

## The Technical Plan

### Architecture Overview

```
┌─────────────────────────────────────────────┐
│         AI INTELLIGENCE LAYER               │
│  (OpenAI GPT-4)                            │
│  • Task extraction from email/Zoom/Slack   │
│  • Call type auto-detection                │
│  • Profile change monitoring               │
│  • Smart follow-up triggers                │
└─────────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────────┐
│      ORCHESTRATION LAYER                    │
│  (Make.com)                                │
│  • Client onboarding workflow              │
│  • P2P introduction workflow               │
│  • Trending campaign engine                │
│  • Task routing & assignment               │
└─────────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────────┐
│         DATA LAYER                          │
│  HubSpot ↔ Notion ↔ Contender ↔ Gmail     │
│           ↕                                 │
│      Google Drive                           │
└─────────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────────┐
│    PRESENTATION LAYER                       │
│  Retool dashboards (ops, advisor, exec)    │
└─────────────────────────────────────────────┘
```

### Phase 1: Quick Wins (Weeks 1-4)

**Project 1.1: AI Task Extraction**

Stop the 10-20 hr/week task hunting madness.

```
Gmail + Zoom + Slack
↓
Make.com watches for:
• Emails from advisors
• Messages mentioning client names
• New Zoom transcripts in Notion
↓
OpenAI GPT-4 extracts:
• Client name(s)
• Action items (list each separately)
• Urgency (urgent/normal/low)
• Any deadlines mentioned
↓
Notion: Create tasks
• Auto-assign to client ops owner (lookup from client record)
• Set due date based on urgency
• Tag source (email/zoom/slack)
• Link to original content
↓
Slack notification to assigned person
```

**Tech Stack:** Make.com + OpenAI API + Gmail/Slack/Notion APIs

**Time to build:** 1-2 weeks

**Impact:** 90%+ task capture rate, zero email sorting time

---

**Project 1.2: Sales Follow-Up Automation**

Make it impossible to lose deals from lack of follow-up.

**The stupidly simple approach:** Create email address `sales@banffadvisors.com`. Advisor forwards sales call notes.

```
Email arrives at sales@banffadvisors.com
↓
AI parses:
• Prospect name, company, role
• Interest level (hot/warm/cold from language analysis)
• Next step mentioned
• Timeline
↓
HubSpot: Create deal record
↓
Schedule follow-up based on interest:
• Hot: 2 days
• Warm: 1 week
• Cold: 2 weeks
↓
Reminder sent to advisor via Slack:
"Follow up with {Name} - discussed {topic} on {date}
[Click to send template email]"
↓
Track: If no response after 2 follow-ups → Move to nurture
```

**Why this works:** Even "tech dinosaurs" can forward an email. No behavior change required.

**Time to build:** 2 weeks

**Impact:** 100% sales call capture, +10-15% conversion from better follow-up

---

**Project 1.3: Instant Contract Generation**

Cut the 24-48hr contract delay to zero.

**Current:** Advisor emails TSQ → 24hr wait → TSQ sends DocuSign → client signs → 24-48hr total

**New:**
```
Retool form (5 fields):
• Client name
• Email
• Contract type (dropdown)
• Terms
• Custom? (Y/N checkbox)

Submit →
If standard (80% of cases):
  → DocuSign API sends immediately (0 min delay)
If custom (20% of cases):
  → Email TSQ for review (flag as non-standard)

Contract signed (DocuSign webhook) →
Trigger onboarding automation (Phase 2)
```

**Time to build:** 1-2 weeks

**Impact:** Standard contracts instant (0min vs 24hr), better client experience

---

### Phase 2: Foundation (Weeks 5-8)

**Project 2.1: Automated Client Onboarding**

The big one. Kill the 60-min manual setup.

**CRITICAL PATH:** Build Contender API first (their dev team, 3-4 weeks)

**Required endpoints:**
```
POST   /api/executives/create
PATCH  /api/executives/{id}
POST   /api/executives/{id}/photo
GET    /api/executives/{id}
```

**Once API exists, workflow is:**

```
DocuSign: Contract signed (webhook)
↓
Make.com Scenario "New Client Onboarding":

1. Parse contract PDF
   Extract: Name, Email, Terms, Price, Type

2. RocketReach API
   Enrich: LinkedIn URL, Photo, Current role

3. HubSpot API
   POST /contacts/v1/contact
   Set: Tier=1, Type=Exec Client, all contract data

4. Notion (auto-creates via Whale Sync when HubSpot tier changes)
   Add: HubSpot link, Contender link, Drive link

5. Contender API
   POST /api/executives/create
   Upload photo, Set tier=1, Assign advisor, Tag expertise

6. Google Drive API
   Create folder: /Clients/{Name}/Narratives/Resumes/LinkedIns/Bios
   Set permissions

7. Round-robin assignment
   Max ↔ Lily (alternate each client)
   Update HubSpot, Notion, Contender with owner

8. Send welcome email
   HubSpot template + kickoff scheduler

9. Slack notification
   "#new-clients: {Name} onboarded - Owner: {Max}"

Total elapsed time: ~2-3 minutes
```

**Error handling:** Each step has 3 retries. Failures Slack to #ops-alerts with details.

**Time to build:** 3-4 weeks (includes Contender API dev)

**Impact:** 60min → 10min (83% reduction), zero data entry errors

---

**Project 2.2: P2P Introduction Tracking**

Make P2Ps visible and measurable.

**Notion database:**
```
P2P Introductions
├─ Client A (relation)
├─ Client B (relation)
├─ Requested By (advisor)
├─ Topic/Purpose (text)
├─ Status (Requested|Sent|Connected|Follow-up 1|Follow-up 2|Closed)
├─ Dates (requested, sent, last follow-up)
├─ Outcome (text)
└─ Impact Rating (1-5)
```

**Workflow:**
```
Advisor fills Retool form:
• Client A (dropdown)
• Client B (dropdown)
• Why? (text)
↓
Make.com:
• Fetch both profiles (Contender + Notion)
• Generate intro email via GPT-4:
  "Hi {A} and {B}, wanted to introduce you because {purpose}..."
• Create draft in advisor's Gmail
↓
Slack advisor: "P2P draft ready - review and send"
↓
After sent:
• Week 1: Check for reply (Gmail API)
  No reply? → Slack: "P2P no response, follow up?"
• Week 2: Second reminder
• Month 1: Ask advisor to rate impact (1-5)
```

**Retool dashboard:**
- Kanban view (Requested | Sent | Connected | Closed)
- Metrics: Total P2Ps, avg time to intro, avg impact, top connectors

**Time to build:** 2-3 weeks

**Impact:** 100% P2P visibility (from 0%), measurable value

---

**Project 2.3: AI Activity Auto-Tagging**

Fix the broken dashboard by removing human error.

**Current problem:** Advisors forget to tag call type → dashboard shows wrong data

**Solution:**
```
Zoom transcript dumps to Notion (already happening via Zapier)
↓
Make.com trigger: New transcript
↓
OpenAI analysis:
"Analyze this call and identify:
1. Call type: Kickoff|Check-in|Narrative Edit|Interview Prep|Branding|P2P|Other
2. Client name(s)
3. Action items
4. Sentiment (positive/neutral/negative)"
↓
Notion: Auto-update record
• Set call type
• Tag to client(s)
• Create tasks from action items
↓
Slack advisor: "{Type} call auto-tagged for {Client} - correct? ✅❌"
↓
If wrong: Advisor clicks ❌ → override → select correct type
Override tracked for model improvement
```

**Data quality monitoring:**
- Weekly report: % auto-tagged, % overridden, common mistakes
- Use data to retrain prompts

**Time to build:** 2-3 weeks

**Impact:** 90%+ tagging accuracy, dashboard actually useful

---

### Phase 3: Advanced (Weeks 9-12)

**Project 3.1: Trending Campaign Automation + Profile Freshness**

**Part 1: Profile Staleness Prevention**

The "don't look like idiots" problem.

```
Weekly cron (Monday 9am):
↓
For each Tier 1 client:
  Get LinkedIn URL from Contender
  ↓
  RocketReach API: Fetch current LinkedIn data
  ↓
  Compare: Contender role vs. Current role
  ↓
  If mismatch:
    Create Notion task:
    "URGENT: Profile Update - {Client}
     LinkedIn shows: {new role}
     Contender shows: {old role}
     Update before next trending campaign"
    Assign to client ops owner
```

**Freshness score:**
- <30 days: Green (good to use)
- 30-90 days: Yellow (review before use)
- >90 days: Red (DO NOT USE in trending)

Block trending campaigns for Red profiles.

---

**Part 2: Trending Campaign Builder**

**Retool interface:**
```
1. Select client (dropdown - only Green/Yellow profiles)
   ↓ Shows profile preview + freshness score

2. Select targeting:
   • Target industries (checkboxes)
   • Target roles (checkboxes)
   ↓ Auto-generates B4B partner list (filters by match)

3. Review partners (e.g., "50 PE firms matched")

4. Configure schedule:
   • Start date
   • Batch size (default: 10 partners/week)
   • Duration (default: 8 weeks)

5. Launch campaign
```

**Execution:**
```
Make.com workflow runs weekly:
↓
Week 1-8:
  Select next batch (10 partners)
  ↓
  Contender: Send profile "whisper" to batch
  ↓
  Log in Notion: Date sent, partners contacted
  ↓
  Week 4: Auto-email partners
  "Is {Client} relevant for any roles?"
  ↓
  Week 8: Generate report
  • Partners contacted
  • Engagement metrics
  • Any inquiries
  Email to advisor + client
```

**Time to build:** 3-4 weeks

**Impact:** 15hr campaign → 30min setup, zero stale profiles

---

**Project 3.2: Client Health Monitoring**

Shift from reactive to proactive servicing.

**Health Score Algorithm:**
```python
health_score = 100
health_score -= days_since_last_activity × 0.5
health_score += activities_last_90_days × 5
health_score += avg_sentiment_last_3_calls × 10
health_score += 20 if trending_active

Risk Level:
• >60 days no contact: HIGH risk
• 30-60 days: MEDIUM risk
• <30 days: LOW risk

Churn Prediction (if contract_age > 6 months):
• health_score < 40: HIGH churn risk
```

**Automated interventions:**
```
Daily Make.com run:
Calculate health scores
↓
If score < 50:
  Create Notion task: "Client needs attention: {Name}"
  Suggest actions:
  • Schedule check-in
  • Send market update
  • Propose P2P intro
↓
If risk = HIGH:
  Slack advisor: "URGENT: No contact with {Name} in {days} days"
↓
If churn_risk = HIGH:
  Slack leadership: "Churn alert: {Name}"
```

**Retool dashboard:**
- Traffic light view (Green/Yellow/Red)
- Sort by: Health score, days since contact, churn risk
- Individual client: Health trend over time, recommended actions

**Time to build:** 3-4 weeks

**Impact:** Proactive engagement, churn prediction, no clients >60 days inactive

---

## The Critical Path: Contender API

This is our biggest risk. Multiple projects depend on it:
- Client onboarding automation (Phase 2)
- Profile freshness monitoring (Phase 3)
- Trending campaign automation (Phase 3)

**What we need:**

Minimal viable API:
```
Executives:
├─ POST   /api/v1/executives (create profile)
├─ PATCH  /api/v1/executives/{id} (update)
├─ POST   /api/v1/executives/{id}/photo (upload)
└─ GET    /api/v1/executives/{id} (read)

Campaigns:
├─ POST   /api/v1/campaigns/trending (create)
└─ GET    /api/v1/campaigns/{id} (status)

Partners:
└─ GET    /api/v1/partners?industry={}&role={} (filter)

Webhooks:
└─ POST   /api/v1/webhooks/register
   Events: profile.updated, tier_changed, campaign.completed
```

**Auth:** API key-based, rate limit 100 req/min

**Dev estimate:** 3-4 weeks (their backend team)

**Mitigation if delayed:** Prioritize Phase 1 + Phase 3 projects that don't need API. Phase 2 can slide if necessary.

---

## Tech Stack & Costs

| Component | Tool | Cost |
|-----------|------|------|
| **Orchestration** | Make.com | $29-99/mo (depends on ops volume) |
| **AI** | OpenAI GPT-4 | ~$40-60/mo (1.75M tokens/mo estimate) |
| **CRM** | HubSpot | (already have) |
| **Ops Hub** | Notion | (already have) |
| **Profiles** | Contender | (already have, need API) |
| **Dashboards** | Retool | (already have) |
| **Enrichment** | RocketReach | (already have license) |
| **Contracts** | DocuSign | (already have, need API access) |

**New recurring costs:** ~$100-150/month

**One-time implementation:** $15-20K (our time)

---

## The Numbers

**Time Savings:**

| Process | Current | Future | Saved/Month |
|---------|---------|--------|-------------|
| Client onboarding | 60min | 10min | 8.3 hrs |
| Task extraction | 40 hrs | 4 hrs | **36 hrs** |
| Sales follow-up | 5 hrs | 0.5 hrs | 4.5 hrs |
| P2P tracking | 5 hrs | 1 hr | 4 hrs |
| Trending campaigns | 30 hrs | 4 hrs | 26 hrs |
| Activity tagging | 12 hrs | 2 hrs | 10 hrs |
| **TOTAL** | | | **~89 hrs/month** |

**Distribution:**
- Client Ops (Max, Lily): 30-40 hrs/month each
- Advisors (David, Liv, Claire): 10-15 hrs/month each

**ROI:**
- 89 hrs/month × $50/hr average = $4,450/month value
- Cost: $100-150/month recurring + $15-20K implementation
- **Payback: 3-4 months**
- **Year 1 ROI: ~300%**

**Business impact:**
- Scale capacity: 8-10 clients/month → 20+ (no new hires)
- Sales conversion: +10-15% from better follow-up
- Client satisfaction: Faster response, proactive engagement

---

## Risks & Mitigation

### Technical Risks

**Contender API delayed**
- Likelihood: Medium
- Impact: High (blocks 3 major projects)
- Mitigation: Start Phase 1 + Phase 3 work while API is in dev, Phase 2 can slide

**AI accuracy <80%**
- Likelihood: Low
- Impact: Medium
- Mitigation: Extensive testing, human-in-loop validation, prompt tuning

**API rate limits**
- Likelihood: Low
- Impact: Low
- Mitigation: Batch operations, retry logic, upgrade plans

### Organizational Risks

**Advisor resistance ("tech dinosaurs")**
- Likelihood: Medium
- Impact: Medium
- Mitigation: Keep UIs stupid-simple, pilot with 1 advisor first, show quick wins

**Data quality degradation**
- Likelihood: Medium
- Impact: High
- Mitigation: Auto-validation, weekly audits, accountability metrics

**Scope creep**
- Likelihood: Medium
- Impact: Low
- Mitigation: Strict phase gates, change request process

---

## Implementation Timeline

**Week 1:**
- API credential gathering
- Make.com + OpenAI setup
- Start Project 1.1 (Task Extraction)

**Week 2:**
- Finish 1.1, pilot test
- Start Project 1.2 (Sales Follow-up)

**Week 3:**
- Finish 1.2
- Start Project 1.3 (Contracts)

**Week 4:**
- Finish 1.3
- **Phase 1 Review** - Show quick wins

**Week 5:**
- Contender API dev kickoff (critical!)
- Start Project 2.1 setup (everything except Contender)
- Start Project 2.2 (P2P)

**Week 6-7:**
- Finish 2.2
- Start Project 2.3 (Auto-tagging)
- Wait for Contender API

**Week 8:**
- Finish 2.1 (once API ready)
- Finish 2.3
- **Phase 2 Review**

**Week 9-10:**
- Project 3.1 (Trending automation)

**Week 11-12:**
- Project 3.2 (Health monitoring)
- **Final review + handoff**

---

## Why This Works

1. **They're already 70% there** - Modern stack (Notion, Retool, HubSpot), just need glue
2. **Clear pain points** - Not selling them on fuzzy "efficiency," pointing to specific hour-sucks
3. **Quick wins in Phase 1** - Prove value before asking for big Contender API investment
4. **Reasonable scope** - 12 weeks aggressive but doable if Contender API delivers
5. **Expansion potential** - This is Phase 1 of multi-year relationship

**The only real risk:** Contender API timing. But even if it delays, we deliver massive value in Phases 1 & 3.

---

## Next Steps

If you're good to move forward:

1. **Kickoff meeting:** Monday Nov 25 (already scheduled with Amanda, Kayla, Max)
2. **Resource needs:**
   - Me (Make.com + orchestration)
   - Someone for Retool work (5 hrs/week)
3. **Budget:** $15-20K for 12 weeks

Once approved, I'll:
- Gather API creds from their team
- Set up Make.com + OpenAI accounts
- Build detailed project board with milestones
- Coordinate with their dev team on Contender API specs

Let me know if you want to talk through any of this. Ready to roll.
