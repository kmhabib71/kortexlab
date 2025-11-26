# BANFF ADVISORS OPERATIONS TRANSFORMATION

## Final Revised Slide Deck — Text Only

---

## SLIDE 1: TITLE

**OPERATIONS TRANSFORMATION**

# Building Your Washing Machine

6-Week Automation Roadmap for Banff Advisors

Kortex Lab • November 2024

---

## SLIDE 2: YOUR VISION, OUR MISSION

**David's Words That Guide Everything We Build:**

> "I fucking hate manual work. I hate dumb extra clicks."
> — David Bomzer

> "The business can grow and I can hire more mini-mes... the more we get the stuff out of my brain."
> — David Bomzer

> "All the insights, all the actions need to end up in the same washing machine."
> — David Bomzer

**What We Will Deliver:**

- One centralized data flow — emails, texts, calls, platform data
- Zero manual clicks for routine tasks
- Systems that enable mini-mes to operate like David
- Scale to 2026 goals without adding headcount
- Nothing depends on memory anymore

**2026 Goal:** Scale services business without throwing people at the problem

---

## SLIDE 3: THE OPPORTUNITY

**Key Metrics:**

| Metric                      | Value   |
| --------------------------- | ------- |
| Hours Saved Per Month       | 150-200 |
| Systems for Each New Client | 4       |
| Executive Clients to Serve  | 212     |
| Tools in Your Tech Stack    | 18      |

**Key Findings From Discovery:**

1. Exec-side sales pipeline is "a free for all" — zero deal tracking
2. Follow-ups are "all memory" — nothing automated
3. 10-20 hrs/week sorting emails and notes for tasks
4. Meeting notes dumped to Notion but not tagged to clients
5. Quarterly reports "riddled with bad data"
6. LinkedIn profiles go stale — B4B partners get mad
7. Liv has 200+ individual Slack channels for clients
8. Advisors each have different workflows (email vs Slack)
9. Tech connections break and nobody knows
10. Website inquiries go to Slack and die — "piss poor job mechanizing"
11. TSQ contract process has 24-hour delay
12. "I have no idea who Chris is" — lack of visibility across organization

_Based on discovery calls with David, Max, Kayla, Amanda, and Nathan_

---

## SLIDE 4: PAIN POINTS BY TEAM

### Client Ops (Max & Lily)

- P2P introductions: manual matching, no tracking
- Trending campaigns: 20-30 min each, filtering 300+ teams manually
- Client onboarding: 4 systems, 30-60 min per client
- Quarterly reports: "riddled with bad data," 5-10 min cross-referencing each
- Meeting note tagging: 5-6 hrs/week manually tagging to client profiles
- Compensation tracking: fully manual
- Narrative edits: multiple handoffs (advisor → client ops → client)
- Account plans in Contender: often "out of date," people don't look at them
- No notification when onboarding tasks complete

> "That would save me 5-6 hours a week" — Max Ravech

### B4B Operations (Kayla & Amanda)

- Pipeline filling: manual LinkedIn checks, duplicate hunting across systems
- Intro policing: manual follow-up tracking for all pending introductions
- Tier 3 network onboarding: no foolproof process after initial weeks
- Task extraction: buried in email and call notes
- LinkedIn freshness: "too many incidents" sending stale profiles
- Team setup: fully manual
- No system to remember to send executives to multiple pipelines over time
- No visibility on relationship warmth ("I don't know if we know Daryl")
- Auto-updater never puts "former" in job titles

> "The machine falls apart after the first few weeks" — Kayla Kanipe
> "We've had too many incidents where people update their LinkedIn and we send stale data" — Amanda Chi

### Advisors (David, Liv, Clare)

- No exec sales pipeline: "it's a free for all"
- Follow-ups: "That's nowhere. That's all memory."
- Fragmented communication: David uses email, Liv uses Slack (200+ channels per client)
- Inbound handling: "We do a piss poor job mechanizing"
- Website inquiries go to Slack with no follow-up system
- Different workflows per advisor — no standardization
- Client context not shared between advisors
- HubSpot used minimally (picked because "it was free")

> "It's lost, where we are with someone. Have we sent them follow-up information? Should we follow up with them? That's nowhere." — David Bomzer

### Cross-Team Issues (From Answers.md)

- Bad/missing data: wrong intro names, wrong company/client/search contact pulls
- Tier 3 database notes not tagged properly
- Tech connections break silently and nobody knows
- Deadline discrepancies between advisors and client ops
- Searches in the market: manual tracking

---

## SLIDE 5: 6-WEEK IMPLEMENTATION ROADMAP

### WEEK 1-2: FOUNDATION

_Quick wins that build trust_

1. Client Onboarding Auto-Sync
2. AI Meeting Note Auto-Tagger
3. Smart Task Extraction Engine
4. Silent Failure Alerts

**Saves: ~50 hrs/month immediately**

---

### WEEK 3-4: SCALE

_Tackle the chaos zone_

5. P2P Introduction Tracker & Matcher
6. Pipeline Auto-Fill Assistant
7. LinkedIn Freshness Monitor
8. Data Quality Validator

**Saves: ~60 hrs/month on tracking**

---

### WEEK 5-6: OPTIMIZE

_Enable the mini-mes_

9. Executive Sales Pipeline Builder
10. Smart Quarterly Reports Generator
11. Trending Campaign AI Assistant
12. Advisor Workflow Standardizer

**Saves: ~40 hrs/month strategic enablement**

_Contender integrations via Retool • First automation live by end of Week 1_

---

## SLIDE 6: WEEK 1-2 PRIORITY AUTOMATIONS (FOUNDATION)

**Quick wins that deliver immediate ROI and build trust**

### Automation #1: Client Onboarding Auto-Sync

**Trigger:** TSQ sends signed contract PDF
**Flow:** Auto-create HubSpot contact → Trigger Whalesync to Notion → Create Contender profile via Retool → Generate Google Drive folder
**Time Saved:** 30-60 min → 5 min per client
**Tools:** HubSpot + Whalesync + Retool + Make.com

### Automation #2: AI Meeting Note Auto-Tagger

**Trigger:** Zoom transcript lands in Notion
**Flow:** AI extracts client name + call type → Auto-tags to client's Notion page → Updates Retool dashboard for accurate reporting
**Time Saved:** 5-6 hrs/week (Max specifically)
**Tools:** Zapier + OpenAI + Notion API

### Automation #3: Smart Task Extraction Engine

**Trigger:** Continuous scan of advisor communications
**Flow:** Scan David's emails + Liv's Slack channels → AI identifies action items → Auto-creates tasks in Notion → Assigns to correct team member with deadline
**Impact:** No more buried tasks in email/calls
**Tools:** Gmail API + Slack API + OpenAI + Notion

### Automation #4: Silent Failure Alerts (NEW)

**Trigger:** Scheduled health checks
**Flow:** Monitor Whalesync/Zapier connections → Alert team immediately when syncs fail → Weekly health check report
**Impact:** No more "tech breaking and we don't know about it"
**Tools:** Zapier + Slack alerts

> "That would save me 5-6 hours a week" — Max Ravech

---

## SLIDE 7: WEEK 3-4 SCALE AUTOMATIONS

**Tackle the "chaos zone" — tracking, matching, and follow-ups**

### Automation #5: P2P Introduction Tracker & Matcher

**Trigger:** New P2P request or client goal update
**Flow:** AI suggests peer matches based on goals/industry → Tracks intro status (sent/opened/meeting booked) → Auto-follow-up reminders at 3/7/14 days → Logs outcomes to Contender via Retool
**Impact:** End "intro policing" manual work
**Tools:** Retool + Notion + HubSpot sequences + OpenAI

### Automation #6: Pipeline Auto-Fill Assistant

**Trigger:** B4B pipeline request comes in
**Flow:** AI searches Contender for matching executives → Checks HubSpot for warm relationships ("do we know Daryl?") → Pre-populates candidate list with confidence scores → Amanda/Kayla reviews & approves
**Impact:** Reduces pipeline fill time by 70%
**Tools:** Retool + Contender data + HubSpot + OpenAI

### Automation #7: LinkedIn Freshness Monitor

**Trigger:** Weekly scheduled scan
**Flow:** Scan executive profiles in database → Detect role changes, missing "former" tags, company changes → Alert team before sending stale profiles → Auto-queue for manual review + sync
**Impact:** No more angry B4B partners from stale data
**Tools:** Retool + LinkedIn data provider + Slack alerts

### Automation #8: Data Quality Validator (NEW)

**Trigger:** Daily scan of recent records
**Flow:** Auto-detect wrong intro names → Flag company/client/search contact mismatches → Identify untagged Tier 3 records → Generate daily data quality report
**Impact:** Clean data, accurate reporting
**Tools:** Retool + cross-system validation

> "We've had too many incidents where people update their LinkedIn and we send stale data" — Amanda Chi

---

## SLIDE 8: WEEK 5-6 OPTIMIZE AUTOMATIONS

**Advanced intelligence that transforms how advisors work**

### Automation #9: Executive Sales Pipeline Builder

**Trigger:** Detect sales-related call in David's Notion notes
**Flow:** Auto-create HubSpot deal → Set follow-up reminders at 7/14/30 days → Track progression stages → Surface deals at risk of "lost to neglect"
**Impact:** Finally: exec-side deal tracking exists!
**Tools:** Notion + HubSpot + Zapier

### Automation #10: Smart Quarterly Reports Generator

**Trigger:** Quarterly report request or scheduled
**Flow:** Pull verified data from all sources (Notion + Contender + HubSpot) → Cross-reference for accuracy → Generate draft report → Flag data gaps before sending to client
**Impact:** 5-10 min per report → 30 seconds
**Tools:** Retool + Multi-source aggregation + OpenAI

### Automation #11: Trending Campaign AI Assistant

**Trigger:** New trending campaign request
**Flow:** Analyze client goals + past campaign performance → AI recommends top 15-20 B4B teams (not all 300+) → Auto-generate personalized email draft → Pre-schedule 8-week whisper cadence
**Impact:** 20-30 min → 5 min per campaign
**Tools:** Retool + Contender + OpenAI + HubSpot sequences

### Automation #12: Advisor Workflow Standardizer (NEW)

**Trigger:** Any advisor communication
**Flow:** Unified task routing: David email + Liv Slack + Clare → Single Notion task queue → Auto-attach client context → Standard follow-up cadence regardless of advisor
**Impact:** Same workflow for all advisors, client context shared
**Tools:** Gmail + Slack + Notion + Make.com

> "Quarterly reports are riddled with bad data — I spend 5-10 min each cross-referencing" — Max Ravech

---

## SLIDE 9: INTEGRATION ARCHITECTURE

**Building on your existing stack — no platform migrations needed**

### Your Current 18 Tools:

HubSpot, Notion, Contender, Retool, Zapier, Whalesync, Gmail, Slack, Zoom, Google Drive, Google Sheets, Google Calendar, Typeform, Juicebox, Rocketreach, LinkedIn, Quickbooks, Pave

### Key Constraint: CONTENDER = NO API

All Contender automations must route through Retool as the integration layer. Nathan's team already built this pattern — we extend it, not reinvent it.

### Keep & Enhance:

- **HubSpot:** Finance/billing relies on it — keep as CRM backbone
- **Notion:** Team loves it — enhance with auto-tagging, not replace

### The Washing Machine Architecture:

```
INPUT SOURCES
├── Gmail (David's emails)
├── Slack (Liv's 200+ channels)
├── Zoom (transcripts)
├── Website (inquiry form)
└── HubSpot (inbound tracking)
           │
           ▼
    ┌─────────────────────────────────┐
    │      AUTOMATION HUB             │
    │  Make.com + Zapier + Retool     │
    │         + OpenAI                │
    └─────────────────────────────────┘
           │
           ▼
OUTPUT SYSTEMS
├── Notion (client pages, tasks)
├── Contender* (via Retool)
├── HubSpot (deals, sequences)
├── Google Drive (folders)
└── Slack (alerts, notifications)

*Contender updates via Retool workflows
```

### Access Needed:

- HubSpot API token
- Notion API + workspace access
- Retool admin access
- Zapier account access
- Whalesync credentials
- Google Workspace admin
- Contender data structure docs (from Nathan)

---

## SLIDE 10: EXPECTED IMPACT

### Big Numbers

| Metric                            | Value                    |
| --------------------------------- | ------------------------ |
| Hours Saved Monthly               | 150+ (~1 FTE equivalent) |
| Reduction in Manual Data Entry    | 85%                      |
| Buried Tasks or Missed Follow-ups | 0                        |

### Scale Without Adding Headcount

Support 8-10 new clients/month with current team. Systems work for you, not the other way around. Ready for 2026 growth goals.

---

### Team-Specific Wins

**Max & Lily (Client Ops):**

- Onboarding: 60 min → 5 min per client
- Meeting tagging: completely eliminated (saves 5-6 hrs/week)
- Quarterly reports: verified data, no cross-referencing
- Trending campaigns: AI recommends teams, not manual filtering

**Kayla & Amanda (B4B):**

- Pipeline filling: AI-assisted matching with warm relationship check
- Intro policing: automated tracking and follow-up reminders
- LinkedIn: proactive alerts before sending stale profiles
- Tier 3 onboarding: foolproof process that doesn't "fall apart"

**David, Liv, Clare (Advisors):**

- Sales pipeline: finally exists on exec side
- Follow-ups: automated, nothing depends on memory
- Mini-me enablement: data out of David's brain, into system
- Unified workflow: same process whether email or Slack

> "The business can grow and I can hire more mini-mes if we get the data out of my brain" — David Bomzer

---

## SLIDE 11: QUESTIONS YOU MIGHT HAVE

### Strategic Questions (David)

**Q: How does this help me hire more mini-mes?**
A: Every automation moves data from your brain into systems. Max can operate like you because he has access to the same insights, relationships, and follow-up cadences — automatically.

**Q: What's the ROI? How fast do we see results?**
A: Week 1: First client auto-onboarded. Week 2: Meeting auto-tagging live (5-6 hrs/week saved for Max). By Week 6: 150+ hours/month saved across team.

**Q: Will this actually stick? We've tried things before.**
A: We start small, prove value in Week 1, then scale. You see working automation before we add complexity. Plus Silent Failure Alerts mean you know immediately if something breaks.

**Q: Why these priorities vs. others?**
A: Prioritized by: (1) immediate time savings, (2) David's stated pain points, (3) technical feasibility with Contender constraint. Happy to adjust based on your feedback.

---

### Technical Questions (Nathan/Amanda)

**Q: How do you handle Contender having no API?**
A: Retool becomes our bridge layer. Nathan's team already uses this pattern for data pulls and workflows. We extend it for writes and updates. No new architecture needed.

**Q: What happens when something breaks?**
A: Automation #4 (Silent Failure Alerts) — monitors all Whalesync/Zapier connections and alerts team immediately. Weekly health check report. No more "tech breaking and we don't know about it."

**Q: What about Nathan being on paternity leave?**
A: He offered to hop on calls occasionally for technical questions. We document everything. Amanda is primary contact. We work with existing Retool patterns, not inventing new ones.

**Q: Can you show me the data flow architecture?**
A: Yes — see Slide 9. Happy to walk through any specific flow in detail.

---

### Operational Questions (Max/Kayla/Amanda)

**Q: How exactly will the auto-tagging work?**
A: Zoom transcript lands in Notion → AI reads transcript → Extracts client name + call type (check-in, sales, intro) → Matches to client page → Auto-tags. Low-confidence matches go to review queue.

**Q: What if the AI tags something wrong?**
A: Confidence scoring on every tag. Below threshold → human review queue. You approve before it goes live. System learns from corrections.

**Q: Will this mess up our existing Whalesync/Zapier setups?**
A: No. We build alongside, not replace. We monitor existing connections (Automation #4) and only extend them. Nothing breaks what's working.

**Q: How do we handle exceptions/edge cases?**
A: Configurable rules per client type. Exception handling built in — unusual cases get flagged for human review, not auto-processed.

**Q: What about clients who aren't in the system yet?**
A: Auto-create client stub when detected in meeting/email → Queue for enrichment → Human verifies before full activation.

---

### Skeptical Questions

**Q: We've built things ourselves that didn't work — why is this different?**
A: Three reasons: (1) We mapped YOUR exact workflows from discovery calls, not generic templates. (2) We start with one automation, prove it works, then scale. (3) We build monitoring from Day 1 so you know when things break.

**Q: What's the catch? What WON'T you be able to automate?**
A: Relationship-building calls, strategic decisions, narrative writing quality, high-judgment client interactions. AI assists, humans decide. We automate the administrative burden, not the human touch that makes Banff special.

**Q: How do you handle the fact that every client is different?**
A: Configurable rules per client type/tier. Standard process with exception handling built in. Edge cases get flagged, not forced through.

**Q: What's your experience with companies like ours?**
A: [Insert Kortex Lab credentials/case studies here]

---

## SLIDE 12: NEXT STEPS

### Immediate Actions

**1. Grant API Access** (This Week)

- HubSpot API token
- Notion API + workspace access
- Retool admin access
- Zapier account access
- Whalesync credentials
- Google Workspace admin
- _Amanda coordinating with Interlaced_

**2. Kickoff Week 1 Build** (Next Week)

- Begin client onboarding auto-sync
- Begin AI meeting note tagger
- _Target: First automation live by end of Week 1_

**3. Weekly Check-ins** (Ongoing)

- 30-min sync each week
- Demo progress, gather feedback, adjust priorities
- _Max or Amanda as primary contacts_

---

### What We Need From You

- [ ] API tokens and admin access (Amanda)
- [ ] One test client for onboarding pilot
- [ ] Access to 3-5 sample Zoom transcripts to train tagger
- [ ] Contender data structure docs (Nathan's team)
- [ ] 30 min/week for feedback and iteration calls
- [ ] Decision: Who is primary contact? (Recommend Amanda or Max)

---

### Success Metrics We'll Track

| Week   | Milestone                                     |
| ------ | --------------------------------------------- |
| Week 1 | First client auto-onboarded end-to-end        |
| Week 2 | Meeting auto-tagger live, Max validates       |
| Week 3 | P2P tracker handling real introductions       |
| Week 4 | Pipeline auto-fill in production              |
| Week 5 | Exec sales pipeline tracking live             |
| Week 6 | Full system operational, 150+ hrs/month saved |

---

## READY TO BUILD YOUR WASHING MACHINE

**First quick win delivered in Week 1**

All the insights, all the actions, in the same place.
No more manual work. No more dumb extra clicks.
Systems that enable mini-mes to scale the business.

---

**Kortex Lab**
info@kortexlab.ai

---

## APPENDIX: PRIORITY AUTOMATION MATRIX

| Priority | #   | Automation                    | Time Saved         | Week | Primary Owner   |
| -------- | --- | ----------------------------- | ------------------ | ---- | --------------- |
| 🔴 P1    | 1   | Client Onboarding Sync        | 30-60 min/client   | 1-2  | Max/Lily        |
| 🔴 P1    | 2   | AI Meeting Note Tagger        | 5-6 hrs/week       | 1-2  | Max             |
| 🔴 P1    | 3   | Task Extraction Engine        | 10-20 hrs/week     | 1-2  | All advisors    |
| 🔴 P1    | 4   | Silent Failure Alerts         | Prevents disasters | 1-2  | Amanda          |
| 🟡 P2    | 5   | P2P Introduction Tracker      | 3-4 hrs/week       | 3-4  | Kayla           |
| 🟡 P2    | 6   | Pipeline Auto-Fill            | 70% faster         | 3-4  | Amanda          |
| 🟡 P2    | 7   | LinkedIn Freshness Monitor    | Prevents errors    | 3-4  | Amanda          |
| 🟡 P2    | 8   | Data Quality Validator        | Clean data         | 3-4  | Nathan (remote) |
| 🟢 P3    | 9   | Exec Sales Pipeline           | New capability     | 5-6  | David           |
| 🟢 P3    | 10  | Smart Quarterly Reports       | 5-10 min→30 sec    | 5-6  | Max             |
| 🟢 P3    | 11  | Trending Campaign AI          | 75% faster         | 5-6  | Max             |
| 🟢 P3    | 12  | Advisor Workflow Standardizer | Unified process    | 5-6  | All advisors    |

---

## APPENDIX: KEY QUOTES TO REFERENCE IN PITCH

Use these to show you listened and understood:

| Quote                                                                          | Speaker | Use When Discussing        |
| ------------------------------------------------------------------------------ | ------- | -------------------------- |
| "I fucking hate manual work. I hate dumb extra clicks."                        | David   | Any automation benefit     |
| "The business can grow and I can hire more mini-mes"                           | David   | Scale, ROI                 |
| "All the insights, all the actions need to end up in the same washing machine" | David   | Integration architecture   |
| "It's a free for all... that's all memory"                                     | David   | Exec sales pipeline        |
| "We do a piss poor job mechanizing"                                            | David   | Inbound handling           |
| "That would save me 5-6 hours a week"                                          | Max     | Meeting auto-tagger        |
| "Quarterly reports are riddled with bad data"                                  | Max     | Smart reports              |
| "The machine falls apart after the first few weeks"                            | Kayla   | Tier 3 onboarding          |
| "Too many incidents where people update their LinkedIn"                        | Amanda  | LinkedIn freshness         |
| "I have no idea who Chris is"                                                  | Max     | Visibility/context sharing |
| "Huge push going into 2026 to scale and grow"                                  | Amanda  | 2026 goals                 |
| "Not trying to throw people at the problem"                                    | Amanda  | Automation ROI             |

---

## APPENDIX: TOOLS INVENTORY (All 18)

**Currently Using:**

1. HubSpot (CRM, email tracking, deals - enterprise side)
2. Notion (client pages, meeting notes, tasks)
3. Contender (proprietary platform - NO API)
4. Retool (dashboards, data bridge to Contender)
5. Zapier (automations)
6. Whalesync (HubSpot ↔ Notion sync)
7. Gmail (advisor emails)
8. Slack (team comms, Liv's client channels)
9. Zoom (calls, transcripts)
10. Google Drive (client folders)
11. Google Sheets (misc tracking)
12. Google Calendar (scheduling)
13. Typeform (intake forms)
14. Juicebox (people data)
15. Rocketreach (contact finding)
16. LinkedIn (profile data, outreach)
17. Quickbooks (finance)
18. Pave (compensation data)

**Will Add:**

- Make.com (complex automations)
- OpenAI API (AI processing)
- LinkedIn data provider (freshness monitoring)

---

_End of Slide Deck_
