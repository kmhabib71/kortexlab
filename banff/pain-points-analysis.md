# Banff Advisors - Pain Points Analysis (From Meeting Transcript)

## Business Overview

**What They Do:**
- Executive search and advisory firm with two business lines:
  1. **Executive (Exec) Side:** Individual executive clients (positioners, private advisors)
  2. **Enterprise (B4B - Banff for Business):** Corporate clients (PE firms, VCs, companies)

**Core Service:** Connect executives with opportunities through their proprietary network

**Team Structure:**
- Advisors: David, Liv, Claire (client-facing, sales)
- Client Ops: Max, Lily (service delivery)
- B4B Operations: Kayla, Amanda (enterprise servicing)
- Data/Reporting: Nathan (on paternity leave)

---

## Critical Pain Points (Ranked by Impact)

### 🔴 PAIN POINT 1: Introduction Tracking - Completely Manual
**What They Said:**
> "Manual back tracking of introductions... there's a lot of manual work around follow-ups... we forget to follow up"

**The Problem:**
- After calls, they manually open Contender and type notes
- Track who was introduced to whom manually
- No automated follow-up system
- If they don't tag properly, data is lost
- Takes 5-10 minutes per call × dozens per week

**Impact:**
- 10-15 hours/week wasted on manual data entry
- Missed follow-ups = lost revenue
- Clients fall through cracks

**Quote:**
> "We're not remembering to follow up whatsoever. We're just kind of throwing things out in the world and moving on to the next."

---

### 🔴 PAIN POINT 2: Client Setup - "Annoying Amount of Time"
**What They Said:**
> "Client setup takes an annoying amount of time"

**The Problem:**
- Manual setup across 4 systems: HubSpot → Notion → Contender → Google Drive
- Takes 30-45 minutes per client
- Copy-paste contract details from PDF email
- Manually create profiles, add LinkedIn, tag fields
- Sometimes have to backtrack to find "who is this client?"

**Current Flow (All Manual):**
1. Receive signed contract via email from TSQ billing
2. Find client in HubSpot (sometimes don't know who they are)
3. Update 10+ fields in HubSpot
4. Wait for Whalesync to create Notion page (but still manual work after)
5. Manually add HubSpot + Contender links to Notion
6. Create Contender profile from scratch (upload LinkedIn PDF, photo, all fields)
7. Manually create Google Drive folder structure
8. Send welcome email (template exists, but manual send)

**Impact:**
- 2-3 clients/week × 45 min = 2-3 hours/week
- Target: 8-10 clients/month = 6-7.5 hours/month just on setup
- Prone to errors (wrong info, missing steps)

---

### 🔴 PAIN POINT 3: Follow-Up System Non-Existent (Exec Side)
**What They Said:**
> "On the exec side, there's zero follow-up. We're not tracking any of this stuff because it's just like 8 clicks and I got 14 meetings a day."

**The Problem:**
- No deal pipeline on executive side
- Sales notes in Notion, but no reminders
- "It's all memory" - David
- Advisors are "tech dinosaurs" who won't use systems
- Probably losing clients due to lack of follow-up

**Impact:**
- Lost deals (can't quantify, but acknowledged as real problem)
- Manual monthly reviews on enterprise side (4-5 hours/month)
- Arrogance: "We let them come to us" - admitted not smart

**Quote:**
> "I imagine there's quite a few clients that we miss at some point just cause we don't follow up with them."

---

### 🔴 PAIN POINT 4: Zoom Notes Dumping, Not Utilized
**What They Said:**
> "It kind of just dumps into Notion. We don't necessarily utilize it... the steps beyond it going into Notion, we haven't done yet."

**The Problem:**
- Zoom transcripts auto-dump into Notion via Zapier
- Not tagged to client automatically
- Not parsed for action items
- Have to manually:
  - Tag transcript to client profile
  - Tag call type (kickoff, check-in, branding, etc.)
  - Extract action items

**Current Manual Process:**
- 30 min to 1 hour filtering Zoom transcripts when multiple calls happen simultaneously
- If advisor doesn't tag call type → doesn't count in reporting dashboard

**Impact:**
- 3-5 hours/week on manual transcript tagging
- Missed action items buried in transcripts
- Reporting dashboard inaccurate if tags missed

---

### 🔴 PAIN POINT 5: Alerting System Broken by Human Error
**What They Said:**
> "If you don't tag this as the right kind of meeting... our reporting and our alerting system is all out of whack. So that's sort of the human error."

**The Problem:**
- Built Retool dashboard to alert when clients need attention
- Relies on manual tagging in Notion
- If call type not tagged correctly → client doesn't show up as "needs follow-up"
- At-risk clients slip through

**Impact:**
- Clients churn without warning
- Manual workaround: monthly reviews to catch what was missed
- System exists but defeated by manual dependency

---

### 🔴 PAIN POINT 6: Tasks Buried in Email + Slack + Text
**What They Said:**
> "Tasks getting buried in email... a lot of client info and update is flowing through different channels, and it doesn't all end up in the same place."

**The Problem:**
- Client updates come via: Email, Zoom, Slack, text messages, phone calls
- No central task management
- Advisors use different workflows:
  - David uses email for client updates
  - Liv uses Slack
  - Claire (new) figuring out her own system

**Current Workaround:**
- Monthly sales catch-up calls
- Amanda manually takes notes in Notion
- Sends follow-up email with action items
- "We chat about it, we put it here, we write it in an email, we send it out"

**Impact:**
- Missed deadlines
- Duplicate work
- Manual reconciliation between systems

---

### 🔴 PAIN POINT 7: Data Quality Issues - "Wrong Info Pulled"
**What They Said:**
> "Wrong intro facilitated name... wrong company, client, search contact pulls through. Need to find the email and validate it."

**The Problem:**
- Use RocketReach and other databases to pull contact info
- Often wrong or outdated
- Have to manually validate via email/LinkedIn
- Then manually fix in system
- Sometimes still wrong after fix

**Impact:**
- 2x-3x work for every search
- Client-facing errors ("we look like idiots")
- Ongoing data hygiene problem

---

### 🔴 PAIN POINT 8: Manual Profile Updates (LinkedIn)
**What They Said:**
> "If they update their LinkedIn and we haven't talked to them in 2 years... we have to manually make sure, oh fuck, did we update their LinkedIn? Because what we're going to send is not live."

**The Problem:**
- Contender stores "fake LinkedIn" (parsed PDF)
- If person updates real LinkedIn → Contender profile outdated
- They share these profiles with clients/PE firms
- Manual job to check and update

**Impact:**
- Risk of sharing outdated info to clients
- Manual labor checking LinkedIn updates
- Professional reputation risk

---

### 🔴 PAIN POINT 9: Contract Handoff Delay (24-36 Hour Gap)
**What They Said:**
> "I send an email to TSQ... they have a 24 hour turnaround... it's kind of silly that we had such a big gap in these crossovers."

**The Problem:**
- When client says "yes" → David emails TSQ billing
- TSQ has 24-hour SLA to send DocuSign
- Another delay waiting for signature
- Then manual handoff to Client Ops

**Impact:**
- 24-48 hour delay to close deal
- Client could change mind
- Extra friction in sales process

---

### 🔴 PAIN POINT 10: Google Drive Manual Folder Creation
**What They Said:**
> "When a new client signs, they get one of these folders."

**The Problem:**
- Every new client needs Google Drive folder for narratives, resumes, bios
- Created manually
- Not part of automated flow

**Impact:**
- Part of the "45 minute client setup" time
- Sometimes forgotten

---

### 🔴 PAIN POINT 11: No Pipeline Visibility = Surprise Onboarding
**What They Said:**
> "Knowing who's at the door and about to sign would be helpful."

**The Problem:**
- Client Ops doesn't know when deals are about to close
- Can't prepare in advance
- Suddenly get 2-3 new clients in one week

**Impact:**
- Reactive scrambling
- Can't plan workload

---

### 🔴 PAIN POINT 12: Contender Doesn't Communicate Well
**What They Said:**
> "Contender doesn't enjoy communicating with other tools very well... it's our own in-house software product, so we can change it, but right now it's not been developed with that in mind."

**The Problem:**
- Proprietary platform, no API
- Can't automate data in/out
- Retool pulls data read-only
- Manual entry still required

**Impact:**
- Limits automation possibilities
- Requires engineering work to fix

---

### 🟡 PAIN POINT 13: Day-to-Day Servicing Not Standardized
**What They Said:**
> "Day to day servicing is challenging... in reality, it's just different for each client... where things go a little haywire is after that 2-month onboarding."

**The Problem:**
- First 2 months standardized (kickoff, narratives, trending)
- After that: ad-hoc requests from advisors
- Build task list manually
- Hard to predict workload

**Impact:**
- Reactive vs. proactive
- Can't scale without adding headcount

---

### 🟡 PAIN POINT 14: Manual Compensation Tracking
**What They Said:**
> (From notes document) "Compensation tracking" listed as manual work

**The Problem:**
- Using Pave for comp data
- Still manual tracking/entry

**Impact:**
- Unknown (need to explore in follow-up)

---

### 🟡 PAIN POINT 15: Website Inquiries Go to Slack, Poorly Managed
**What They Said:**
> "We do a piss poor job... We do a poor job like mechanizing the like make sure someone gets back to them."

**The Problem:**
- Website inquiries → Slack channel
- No workflow to ensure response
- Probably losing inbound leads

**Impact:**
- Lost business
- Unprofessional

---

## Tech Stack (Current State)

| Tool | Purpose | Issues |
|------|---------|--------|
| **HubSpot** | CRM, email tracking, enterprise deal pipeline | Not used for exec pipeline, manual deal entry |
| **Notion** | Notes, client pages, task tracking | Manual tagging required, notes buried |
| **Contender** | Proprietary platform - exec profiles, intros | No API, manual profile creation, manual updates |
| **Whalesync** | HubSpot → Notion sync | Works but limited (only creates page, still manual work after) |
| **Zapier** | Zoom → Notion transcript dump | Not utilized beyond dump, no parsing/tagging |
| **Retool** | Dashboards, alerting, reporting | Good for visualization, but relies on manual data tagging |
| **Google Drive** | Client files (narratives, resumes) | Manual folder creation |
| **Gmail** | Client communication | Tasks buried in threads |
| **Zoom** | Calls | Transcripts not parsed for action items |
| **RocketReach** | Contact data | Data quality issues |
| **TypeForm** | Forms/surveys | Unknown integration |
| **QuickBooks** | Accounting/billing | Handled by TSQ (external) |
| **Pave** | Compensation data | Manual tracking |
| **DocuSign** | Contracts | Handled by TSQ with 24hr delay |

---

## Opportunities (What's Working)

✅ **Whalesync:** HubSpot → Notion client page creation works
✅ **Zoom → Notion:** Transcripts auto-dump (just not utilized)
✅ **Retool:** Good centralization point for dashboards
✅ **Welcome Email Templates:** Exist in HubSpot
✅ **Team Mindset:** "Systems thinking" team, open to automation

---

## Key Quotes (Client Sentiment)

**On Manual Work:**
> "I fucking hate manual work. I hate dumb extra clicks." - David

**On Data:**
> "How does all that end up in the same washing machine?" - David

**On Scaling:**
> "The more we give them the stuff out of my brain and the data of the company... I can hire more mini-mes." - David

**On Adoption:**
> "We're too busy manually tracking things to save time for raising kids." - Kayla (joking but real)

**On Excitement:**
> "We're excited for you enabling us to spend time on more fun, strategic things that we enjoy doing." - Kayla

---

## Business Context

- **Current Scale:** 212 executive clients
- **Growth Target:** 8-10 new exec clients/month
- **Client LTV:** 1-4 years (average probably 2 years)
- **Team Size:** Small (6-8 people mentioned)
- **2026 Push:** Scale services without adding headcount

---

## What They Expect from You

**Week 1 Deliverable:**
- System map showing how departments connect
- Automation priorities

**Access Needed:**
- HubSpot API
- Notion API
- Retool developer access
- Google Workspace API
- Contender (TBD - might need engineering support)

**Follow-Up Meetings:**
- Monday 1:30 PM PST: Deep dive with Kayla (B4B servicing)
- Tuesday 1:30 PM PST: Deep dive with Amanda (exec servicing details)

---

## Top 6 Automation Priorities (Your Recommendation)

### Priority 1: Introduction Tracking Automation ⭐⭐⭐
**Impact:** 10-15 hrs/week saved
**Build:** Zoom/Gmail → AI summarization → Contender auto-entry

### Priority 2: Client Setup Automation ⭐⭐⭐
**Impact:** 6-7.5 hrs/month saved
**Build:** Contract signed → auto-create in all 4 systems + Drive folder

### Priority 3: Follow-Up System (Exec Side) ⭐⭐
**Impact:** Prevent lost deals
**Build:** Notion notes → auto-create reminders/tasks

### Priority 4: Zoom Transcript Parsing ⭐⭐
**Impact:** 3-5 hrs/week saved
**Build:** AI parse transcripts → extract action items → auto-tag

### Priority 5: Unified Task Management ⭐⭐
**Impact:** Reduce missed deadlines 80%
**Build:** Email/Slack → Notion task auto-capture

### Priority 6: Pipeline Visibility Dashboard ⭐
**Impact:** Better workload planning
**Build:** HubSpot deals → alert Client Ops of upcoming clients

---

## Red Flags

⚠️ **Contender API:** Proprietary, no API - might need engineering help
⚠️ **Advisor Adoption:** "Tech dinosaurs" - need simple, zero-click solutions
⚠️ **Different Workflows:** Each advisor does their own thing - need to standardize
⚠️ **Nathan on Leave:** Data/reporting person gone for months

---

## Next Steps for You

1. ✅ Watch Loom videos from Kayla/Amanda
2. ✅ Prepare questions for Monday/Tuesday deep dives
3. ✅ Draft system map showing current vs. future state
4. ✅ Create automation roadmap with before/after metrics
5. ✅ Wait for API access credentials
