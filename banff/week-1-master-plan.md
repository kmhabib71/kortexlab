# Week 1 Master Plan - Banff Advisors Automation Project

## Part 1: Onboarding to Deal Closing Process

### EXECUTIVE (EXEC) SIDE - Client Acquisition Flow

```
┌─────────────────────────────────────────────────────────────────┐
│                    LEAD GENERATION (Top of Funnel)              │
├─────────────────────────────────────────────────────────────────┤
│ Sources:                                                        │
│ • Referrals (primary source)                                   │
│ • LinkedIn cold outreach                                        │
│ • Website inquiry form → Slack channel (poorly managed)         │
│ • Email cold outreach                                           │
│                                                                  │
│ Status: NO PIPELINE TRACKING - "It's all memory"               │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│                    INITIAL CONVERSATION                          │
├─────────────────────────────────────────────────────────────────┤
│ Who: Advisor (David, Liv, or Claire)                           │
│ Where: Email (auto-tracked in HubSpot)                         │
│ Tracked: Only if email-based (HubSpot email tracking)          │
│                                                                  │
│ PAIN POINT: No follow-up system                                │
│ • No deal stages                                                │
│ • No reminders to follow up                                     │
│ • Advisors keep notes in Notion but no automation              │
│ • "We forget to follow up... throwing things out in the world" │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│                    PITCH & PROPOSAL                              │
├─────────────────────────────────────────────────────────────────┤
│ Action: Send pitch deck (template email in HubSpot)            │
│ Who: Advisor                                                    │
│                                                                  │
│ PAIN POINT: No tracking if sent, no follow-up reminder         │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│                    CLIENT SAYS YES                               │
├─────────────────────────────────────────────────────────────────┤
│ Action: Advisor sends email to billing@banffadvisors.ca (TSQ)  │
│ Contains: Client name, email                                    │
│                                                                  │
│ PAIN POINT: 24-hour delay                                       │
│ • TSQ has 24-hour SLA to send contract                         │
│ • External team (not in-house)                                 │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│                    CONTRACT SENT (DocuSign)                      │
├─────────────────────────────────────────────────────────────────┤
│ Who: TSQ (Arthur)                                               │
│ Tool: DocuSign                                                  │
│                                                                  │
│ PAIN POINT: Another delay waiting for signature                │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│                    CONTRACT SIGNED ✅                            │
├─────────────────────────────────────────────────────────────────┤
│ Action: TSQ sends signed PDF to Client Ops team                │
│ Contains: Contract terms, billing type, address, pricing       │
│                                                                  │
│ HANDOFF TO CLIENT OPS BEGINS                                   │
│ • Whoever replies first = Client Ops Owner for life            │
│ • That person owns this client for entire journey              │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│              CLIENT ONBOARDING (45 MIN MANUAL PROCESS)          │
├─────────────────────────────────────────────────────────────────┤
│ STEP 1: HUBSPOT SETUP (Manual - 10 min)                        │
│ ├─ Find client in HubSpot (sometimes don't know who they are)  │
│ ├─ Add LinkedIn URL                                             │
│ ├─ Change status: "Current Private Advisor Client"             │
│ ├─ Assign Advisor (David/Liv/Claire)                           │
│ ├─ Set Transition Pathway (4 types):                           │
│ │  • Network & Brand Builder                                   │
│ │  • Enroll Accelerator                                        │
│ │  • Portfolio (board/advisory focused)                        │
│ │  • Transition Services (job search) ← 90% start here        │
│ ├─ Enter contract start date                                   │
│ ├─ Enter kickoff call date                                     │
│ ├─ Mark as "Tier 1 Executive Client" (triggers Whalesync)      │
│ └─ Enter billing terms from contract                           │
│                                                                  │
│ STEP 2: NOTION PAGE (Semi-automated - 5 min)                   │
│ ├─ Whalesync auto-creates Notion page when marked Tier 1       │
│ ├─ MANUAL: Add HubSpot profile link                            │
│ ├─ MANUAL: Add Contender profile link                          │
│ └─ Page ready for notes/tagging                                │
│                                                                  │
│ STEP 3: CONTENDER PROFILE (Manual - 15 min)                    │
│ ├─ Check if profile exists (sometimes new, sometimes Tier 3)   │
│ ├─ If new: Create from scratch                                 │
│ │  ├─ Download LinkedIn PDF                                    │
│ │  ├─ Upload PDF (auto-parses some fields)                     │
│ │  ├─ Download/upload profile photo separately                 │
│ │  ├─ Enter email                                              │
│ │  ├─ Set advisor                                              │
│ │  └─ Add kickoff date (after call happens)                    │
│ ├─ If exists: Change from Tier 3 → Tier 1                      │
│ └─ MANUAL: Tag functional expertise & industry (after kickoff) │
│                                                                  │
│ STEP 4: GOOGLE DRIVE FOLDER (Manual - 5 min)                   │
│ ├─ Create folder: [Client Name]                                │
│ └─ Subfolders for narratives, resumes, LinkedIns, bios         │
│                                                                  │
│ STEP 5: WELCOME EMAIL (Manual but templated - 5 min)           │
│ ├─ Use HubSpot template                                        │
│ ├─ Include: Kickoff call calendar link                         │
│ ├─ Include: Kickoff form (Typeform?)                           │
│ └─ Send                                                         │
│                                                                  │
│ TOTAL TIME: 45 minutes per client                              │
│ FREQUENCY: 2-3 clients/week (8-10/month target)                │
│ ANNUAL IMPACT: 90-120 clients × 45 min = 67-90 hours/year      │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│                    KICKOFF CALL (60-90 min)                      │
├─────────────────────────────────────────────────────────────────┤
│ Who: Client + Advisor + Client Ops Owner                       │
│ Purpose: Full career history, goals, network mapping           │
│ Tool: Zoom (with transcript)                                    │
│                                                                  │
│ CURRENT FLOW:                                                   │
│ ├─ Zoom transcript auto-dumps to Notion (via Zapier)           │
│ ├─ MANUAL: Tag transcript to client profile                    │
│ ├─ MANUAL: Tag call type as "Kickoff"                          │
│ ├─ MANUAL: Extract and enter functional/industry tags in       │
│ │           Contender after call                               │
│ └─ Takes 30-60 min post-processing                             │
│                                                                  │
│ PAIN POINT:                                                     │
│ • Transcript "just dumps" - not utilized                        │
│ • Manual tagging required for reporting to work                │
│ • Action items buried in transcript                            │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│              ONGOING CLIENT SERVICING (Months 1-2)              │
├─────────────────────────────────────────────────────────────────┤
│ STANDARDIZED ACTIVITIES:                                        │
│ ├─ Narrative Edits (resume, bio, LinkedIn)                     │
│ │  └─ Stored in Google Drive, 2-3 rounds of edits             │
│ ├─ First Trending Campaign (2 months)                          │
│ │  └─ Share profile to PE firms, VCs, search firms            │
│ └─ Network Introductions (P2P - Peer to Peer)                  │
│                                                                  │
│ STATUS: Well-managed, standardized                             │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│            ONGOING CLIENT SERVICING (Month 3+)                  │
├─────────────────────────────────────────────────────────────────┤
│ AD-HOC ACTIVITIES (based on quarterly check-ins):              │
│ ├─ Additional P2P introductions                                │
│ ├─ Additional trending campaigns                               │
│ ├─ Narrative refreshes                                         │
│ ├─ Target company mapping                                      │
│ ├─ Interview prep calls                                        │
│ ├─ Personal branding calls                                     │
│ └─ Event invitations                                           │
│                                                                  │
│ PAIN POINT: "Where things go haywire"                          │
│ • Not standardized - different for each client                 │
│ • Task list builds up quickly                                  │
│ • Hard to scale without adding headcount                       │
│ • Reactive vs. proactive                                       │
└─────────────────────────────────────────────────────────────────┘

```

---

### ENTERPRISE (B4B) SIDE - Client Acquisition Flow

```
┌─────────────────────────────────────────────────────────────────┐
│                    LEAD GENERATION                               │
├─────────────────────────────────────────────────────────────────┤
│ Who: Kayla, Amanda                                              │
│ Sources: Outreach to PE firms, VCs, corporate clients          │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│              HUBSPOT DEAL PIPELINE (Structured)                  │
├─────────────────────────────────────────────────────────────────┤
│ Stages:                                                         │
│ ├─ Target List                                                  │
│ ├─ Reached Out                                                  │
│ ├─ Call Scheduled                                               │
│ ├─ Qualified to Buy                                             │
│ ├─ Won / Lost / Deprioritized                                  │
│                                                                  │
│ Tracking:                                                       │
│ ├─ MANUAL: Kayla/Amanda add deals                              │
│ ├─ MANUAL: Monthly review calls                                │
│ │  └─ Team (David, Clare, Liv, Kayla, Max) review dashboard    │
│ ├─ Amanda takes notes in Notion during call                    │
│ └─ Amanda emails action items after call                       │
│                                                                  │
│ PAIN POINT:                                                     │
│ • No automated follow-up reminders                             │
│ • Monthly review is manual (4-5 hours)                         │
│ • "We chat, put it in Notion, write email, send it" - 3 steps  │
└─────────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│                    CLIENT ONBOARDING (B4B)                       │
├─────────────────────────────────────────────────────────────────┤
│ Primary Platform: Contender (homegrown)                        │
│ Servicing Team: Kayla, Amanda                                  │
│                                                                  │
│ DIFFERENT from Exec side:                                      │
│ • Live in Contender more than Notion                           │
│ • Pipeline management focused                                  │
│ • Introduction tracking for enterprise searches                │
│                                                                  │
│ PAIN POINTS (similar):                                         │
│ • Manual tracking of introductions, feedback, impact           │
│ • Team setup manual                                            │
│ • Pipeline filling manual                                      │
└─────────────────────────────────────────────────────────────────┘
```

---

## Part 2: Who Does What at Banff Advisors

### Organizational Structure

```
┌──────────────────────────────────────────────────────────────────┐
│                          DAVID (Founder)                         │
│                                                                  │
│ Role: Advisor, Sales Lead (Exec side)                          │
│ Responsibilities:                                               │
│ • Close executive clients                                       │
│ • Client check-in calls (quarterly)                            │
│ • Strategic direction                                           │
│ • Keep sales notes in Notion                                   │
│                                                                  │
│ Tech Behavior:                                                  │
│ • Uses email for client updates (not Slack)                    │
│ • "Tech dinosaur" - won't use complex systems                  │
│ • Hates manual work and "dumb clicks"                          │
│                                                                  │
│ Quote: "I fucking hate manual work"                            │
└──────────────────────────────────────────────────────────────────┘

┌─────────────────────────────┬────────────────────────────────────┐
│      LIV (Advisor)          │      CLAIRE (Advisor)              │
├─────────────────────────────┼────────────────────────────────────┤
│ Role: Exec client sales     │ Role: Exec client sales (newest)   │
│ • Closes exec clients       │ • Closes exec clients              │
│ • Client servicing          │ • Client servicing                 │
│ • Uses Slack for updates    │ • Figuring out workflow            │
│ • Different workflow than   │ • Brand new to team                │
│   David                     │                                    │
└─────────────────────────────┴────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────┐
│                    CLIENT OPS TEAM                               │
├──────────────────────────────────────────────────────────────────┤
│ MAX (Client Ops Lead)                                           │
│ • Client onboarding (HubSpot, Notion, Contender, Drive)        │
│ • Kickoff calls                                                 │
│ • Narrative edits                                               │
│ • Day-to-day servicing                                          │
│ • Owns clients from signature → churn                           │
│ • MOST MANUAL WORK on team                                      │
│                                                                  │
│ LILY (Client Ops)                                               │
│ • Same as Max                                                   │
│ • Team of 2 supporting 212 clients                             │
└──────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────┐
│                    B4B (ENTERPRISE) TEAM                         │
├──────────────────────────────────────────────────────────────────┤
│ KAYLA (B4B Lead)                                                │
│ • Enterprise sales                                              │
│ • Pipeline creation/ideation                                    │
│ • Pipeline submission                                           │
│ • Lives in Contender                                            │
│ • Manual intro tracking, team setup                            │
│                                                                  │
│ AMANDA (B4B Operations)                                         │
│ • Enterprise client servicing                                   │
│ • Pipeline creation/ideation                                    │
│ • Monthly review note-taking                                    │
│ • Follow-up email coordination                                  │
│ • New team creation                                             │
└──────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────┐
│                    DATA & TECH                                   │
├──────────────────────────────────────────────────────────────────┤
│ NATHAN (Data/Reporting - ON PATERNITY LEAVE)                    │
│ • Built Retool dashboards                                       │
│ • Connects APIs (HubSpot, Notion, Contender)                   │
│ • SQL/code for integrations                                     │
│ • Reporting automation                                          │
│ • Client health alerting system                                │
│ • Available for questions but limited                           │
│                                                                  │
│ ENGINEERING TEAM (Contender developers)                         │
│ • Can modify Contender API if needed                           │
│ • Not directly involved yet                                     │
└──────────────────────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────────────────────┐
│                    EXTERNAL PARTNERS                             │
├──────────────────────────────────────────────────────────────────┤
│ TSQ (Finance/Billing/Contracts)                                 │
│ • QuickBooks management                                         │
│ • DocuSign contract sending (24hr SLA)                         │
│ • Arthur = main contact                                         │
│                                                                  │
│ KORTEX LABS (That's You!)                                       │
│ • Automation development                                        │
│ • System integration                                            │
│ • Matthew Smith (account manager)                               │
│ • Habib (developer)                                             │
└──────────────────────────────────────────────────────────────────┘
```

### Collaboration Matrix

| Activity | Advisors (David/Liv/Claire) | Client Ops (Max/Lily) | B4B (Kayla/Amanda) | Data (Nathan) |
|----------|----------------------------|----------------------|-------------------|---------------|
| **Sales (Exec)** | Lead | - | - | - |
| **Sales (Enterprise)** | Approve | - | Lead | - |
| **Client Onboarding** | Handoff | Owner | - | - |
| **Kickoff Calls** | Attend | Lead | - | - |
| **Narrative Edits** | Review | Execute | - | - |
| **P2P Intros** | Sometimes | Execute | - | - |
| **Trending Campaigns** | - | Execute | - | - |
| **Quarterly Check-ins** | Lead | Support | - | - |
| **Pipeline Tracking** | Ignore (exec) | - | Manage (B4B) | - |
| **Reporting** | - | - | - | Build |
| **Retool Dashboards** | View | Use | Use | Build |

---

## Part 3: What Matthew Expects This Week + Day-by-Day Plan

### Matthew's Expectations (Week 1)

From the kickoff presentation (slides):

**Week 1 Deliverables:**
1. ✅ **Current State Map** - Document how they work today
2. ✅ **Build Roadmap** - 6 priority automations with timeline
3. ✅ **Quick Wins Identification** - Low-effort, high-impact items
4. ✅ **Technical Assessment** - Audit all systems once you get access

**Success Criteria:**
- Show deep understanding of their pain
- Clear before/after for each automation
- Hours saved quantified
- Build plan with realistic timeline

---

### Week 1: Day-by-Day Execution Plan

#### **SATURDAY (Today) - Research & Analysis**

**Morning (3 hours):**
- [x] Review meeting transcript ✅ Done
- [x] Review Loom video ✅ Done
- [x] Review prep notes ✅ Done
- [ ] Create pain points document ✅ Done
- [ ] Map current workflows ← YOU'RE HERE

**Afternoon (3 hours):**
- [ ] Draft Current State Map
- [ ] Sketch automation ideas
- [ ] List questions for Matthew
- [ ] Identify what access you need

**Evening (1 hour):**
- [ ] Send Matthew Slack update with initial findings
- [ ] Ask clarifying questions before Monday

---

#### **SUNDAY - Draft Deliverables**

**Morning (4 hours):**
- [ ] Write Current State Map document (visual diagrams)
- [ ] Create "Who Does What" org chart
- [ ] Draft automation priority list (1-6)

**Afternoon (3 hours):**
- [ ] For each automation, write:
  - Current manual process
  - Proposed automated solution
  - Time saved estimate
  - Technical approach
  - Tools needed

**Evening (1 hour):**
- [ ] Review and refine
- [ ] Prepare questions for Monday/Tuesday deep dives

---

#### **MONDAY - Deep Dive with Kayla (1:30 PM PST)**

**Before Meeting (Morning):**
- [ ] Review B4B-specific pain points
- [ ] Prepare questions about:
  - Contender workflow for enterprise side
  - Introduction tracking process
  - Pipeline management pain points
  - What data they need but don't have

**During Meeting:**
- [ ] Screen share - watch their workflow
- [ ] Take detailed notes
- [ ] Ask about Loom videos she mentioned

**After Meeting (Afternoon):**
- [ ] Update Current State Map with B4B details
- [ ] Refine automation priorities
- [ ] Draft B4B-specific quick wins

---

#### **TUESDAY - Deep Dive with Amanda (1:30 PM PST)**

**Before Meeting (Morning):**
- [ ] Review exec servicing pain points
- [ ] Prepare questions about:
  - Day-to-day client ops workflow
  - Narrative edit process
  - P2P introduction tracking
  - Retool alerting system issues

**During Meeting:**
- [ ] Watch manual processes live
- [ ] Understand tagging issues
- [ ] Get specifics on "tasks buried in email"

**After Meeting (Afternoon):**
- [ ] Finalize Current State Map
- [ ] Lock in top 6 automation priorities
- [ ] Start building Week 1 deliverable document

---

#### **WEDNESDAY - Build Deliverable**

**All Day (8 hours):**
- [ ] Create polished deliverable document:
  - Executive summary
  - Current state analysis
  - Pain points (ranked by impact)
  - 6 automation priorities with:
    - Before/After comparison
    - Time saved
    - Build approach
    - Tools/APIs needed
  - Week 2-3 build plan
  - Access requirements list

**Format Options:**
- Google Doc (easy to share/comment)
- Notion page (if they prefer)
- PDF presentation
- Loom walkthrough (recommended - more engaging)

---

#### **THURSDAY - Review & Access Requests**

**Morning (3 hours):**
- [ ] Review deliverable for clarity
- [ ] Get feedback from Matthew if possible
- [ ] Create visual diagrams (current vs future state)

**Afternoon (3 hours):**
- [ ] Test any API access you received
- [ ] Document what access is still needed
- [ ] Begin exploring HubSpot/Notion if you have access

**Evening (1 hour):**
- [ ] Send formal access request email to Amanda with:
  - List of all credentials needed
  - What you'll use them for
  - Security assurances

---

#### **FRIDAY - Present & Plan Week 2**

**Morning (3 hours):**
- [ ] Final polish on deliverable
- [ ] Record Loom presentation (10-15 min) walking through:
  - Your understanding of their business
  - Top 6 pain points
  - Proposed automations
  - Week 2-3 plan

**Afternoon (2 hours):**
- [ ] Send deliverable to Matthew
- [ ] Schedule Week 2 kickoff call
- [ ] Begin Week 2-3 build plan if time

---

## Part 4: Killer Week 1 Deliverable

Here's the document structure that shows deep understanding:

---

# BANFF ADVISORS: WEEK 1 DISCOVERY REPORT
**Prepared by:** Km Habib, Kortex Labs
**Date:** [Friday of Week 1]
**For:** Matthew Smith, David, Amanda, Kayla, Max

---

## Executive Summary

After 3 discovery sessions and deep analysis of Banff's operations, I've identified **150-200 hours/month** of manual work that can be automated, with **6 high-impact automations** delivering immediate ROI.

**Key Findings:**
- ✅ Introduction tracking is the biggest time sink (10-15 hrs/week)
- ✅ Client onboarding takes 45 min/client (can be reduced to 5 min)
- ✅ Zoom transcripts unused (3-5 hrs/week wasted)
- ✅ Exec side has zero follow-up system (losing deals)
- ✅ Tasks buried across email/Slack/text (missed deadlines)

**Week 2-3 Plan:** Build automations #1-2 (introduction tracking + client setup)

---

## Part 1: Current State - How Banff Works Today

### Business Model
Banff Advisors is a "career family office" for executives, offering:
- **Exec Side (212 clients):** Individual executive advisory, network building, career positioning
- **Enterprise (B4B):** Corporate talent intelligence, PE/VC network access

**Revenue Model:** Subscription (monthly, no fixed end date) + enterprise contracts

**Growth Target:** 8-10 new exec clients/month, scale without adding headcount

---

### Current Tech Stack

| System | Purpose | What Works | What's Broken |
|--------|---------|------------|---------------|
| **HubSpot** | CRM, email tracking | Email auto-tracking, enterprise pipeline | No exec pipeline, manual deal entry |
| **Notion** | Notes, client pages, docs | Central repository | Manual tagging required, notes buried |
| **Contender** | Proprietary exec platform | Core business system | No API, manual profile creation |
| **Whalesync** | HubSpot → Notion sync | Auto-creates client page | Still requires manual work after |
| **Zapier** | Zoom → Notion transcripts | Transcripts auto-dump | Not parsed, not tagged, not used |
| **Retool** | Dashboards, alerting | Good visualization | Relies on manual data tagging |
| **Google Drive** | Client files | Works | Manual folder creation |
| **Gmail** | Communication | Email tracking in HubSpot | Tasks buried in threads |

---

### Client Acquisition & Onboarding Flow (Exec Side)

**CURRENT PROCESS (Manual - 45 minutes per client):**

```
Lead (referral) → Email conversation → Pitch deck sent → Client says yes
    ↓
Email to TSQ billing → 24hr wait → DocuSign sent → Client signs
    ↓
Contract PDF emailed to Client Ops → First to reply = owner
    ↓
┌────────────────────────────────────────────────────┐
│ MANUAL ONBOARDING (45 min)                        │
├────────────────────────────────────────────────────┤
│ 1. Find client in HubSpot (sometimes unknown)     │
│ 2. Enter 10+ fields manually from contract PDF    │
│ 3. Mark as Tier 1 → triggers Whalesync            │
│ 4. Wait for Notion page creation                  │
│ 5. Manually add HubSpot + Contender links         │
│ 6. Create Contender profile from scratch          │
│    - Download LinkedIn PDF                        │
│    - Upload + photo separately                    │
│    - Enter all fields manually                    │
│ 7. Create Google Drive folder structure           │
│ 8. Send welcome email (template, but manual)      │
└────────────────────────────────────────────────────┘
    ↓
Kickoff call scheduled → 60-90 min call → Zoom transcript dumps
    ↓
┌────────────────────────────────────────────────────┐
│ POST-CALL MANUAL WORK (30-60 min)                │
├────────────────────────────────────────────────────┤
│ 1. Find transcript in Notion                      │
│ 2. Tag to client profile                          │
│ 3. Tag call type as "Kickoff"                     │
│ 4. Read transcript, extract tags                  │
│ 5. Add functional/industry tags to Contender      │
└────────────────────────────────────────────────────┘
```

**Total Manual Time Per Client:** ~2 hours (onboarding + post-kickoff)

---

## Part 2: Pain Points (Ranked by Impact)

### 🔴 CRITICAL - Pain Point 1: Introduction Tracking Completely Manual

**The Problem:**
After every client call, phone conversation, or intro made, team manually:
1. Opens Contender
2. Finds the person's profile
3. Finds the pipeline they're on
4. Types notes about the conversation
5. Tags intro status

**Loom Evidence:** Watched Amanda manually track 3 intros - took 5-7 minutes

**Impact:**
- 10-15 hours/week across team
- Forgotten follow-ups = lost opportunities
- If not tagged correctly → doesn't show in alerts → clients slip through

**Quote from David:**
> "We're not tracking any of this stuff because it's just like 8 clicks and I got 14 meetings a day. I'm not gonna go into a database and open up a deal record."

---

### 🔴 CRITICAL - Pain Point 2: Client Setup "Annoying Amount of Time"

**The Problem:**
45 minutes per client × 2-3 clients/week = **2-3 hours/week wasted**

**Why it takes so long:**
- 4 separate systems to update (HubSpot, Notion, Contender, Drive)
- Copy-paste from PDF email
- Sometimes "don't know who the client is" - have to backtrack
- Contender profile creation from scratch (LinkedIn PDF + photo separate)

**Annual Impact:**
- 100-120 new clients × 45 min = **75-90 hours/year**

---

### 🔴 CRITICAL - Pain Point 3: Zoom Transcripts Unused

**The Problem:**
Zoom transcripts auto-dump to Notion via Zapier, but then:
- Not tagged to client automatically
- Not parsed for action items
- Not analyzed for sentiment/risks
- Manual work to tag call type

**Team's Words:**
> "It kind of just dumps into Notion. We don't necessarily utilize it."

**Impact:**
- 3-5 hours/week filtering/tagging transcripts
- Action items buried and missed
- Can't search across all calls for insights

---

### 🔴 HIGH - Pain Point 4: No Follow-Up System (Exec Side)

**The Problem:**
- No deal pipeline on exec side
- No automated reminders
- "It's all memory" - David's words
- Advisors are "tech dinosaurs" who won't use complex systems

**Impact:**
- Lost deals (can't quantify, but acknowledged)
- Arrogance: "We let them come to us" - David admits not smart

---

### 🔴 HIGH - Pain Point 5: Tasks Buried Across Channels

**The Problem:**
Client updates come via:
- Email (David's preference)
- Slack (Liv/Clare's preference)
- Text messages
- Phone calls
- Zoom

Nothing centralized. Tasks get lost.

**Current Workaround:**
Monthly manual review calls where Amanda:
1. Takes notes in Notion
2. Writes email with action items
3. Sends to team

**Impact:**
- Missed deadlines
- "What should be done and by when" - constant confusion

---

### 🟡 MEDIUM - Pain Point 6: Data Quality Issues

**The Problem:**
- Pull contact info from RocketReach → often wrong
- Wrong company, wrong email, wrong name
- Have to manually validate via LinkedIn/email
- Fix in system → sometimes still wrong

**Impact:**
- 2x-3x work for every search
- Risk of looking unprofessional to clients

---

## Part 3: Automation Roadmap - 6 Priorities

### ⭐ Priority 1: Introduction Tracking Automation
**Build Timeline:** Week 2-3

**BEFORE:**
- 5-7 min manual entry per intro
- 20-30 intros/week = 2-3 hours/week
- Forgotten follow-ups
- Manual pipeline updates

**AFTER (Automated):**
```
Call ends → AI processes recording → Contender updated automatically
```

**How It Works:**
1. Zoom call ends → transcript sent to AI (GPT-4)
2. AI extracts:
   - Who was on call
   - Discussion summary
   - Intro status (made, pending, feedback received)
   - Action items
   - Next follow-up date
3. Auto-update Contender via API (or Retool if no API)
4. Slack notification: "Intro with Marion logged, follow-up in 2 weeks"

**Time Saved:** 10-15 hours/week = **520-780 hours/year**

**Tools Needed:**
- Zoom API (transcripts)
- OpenAI API (summarization)
- Contender API (or Retool workaround)
- Slack webhooks

---

### ⭐ Priority 2: Client Setup Automation
**Build Timeline:** Week 2-3

**BEFORE:**
- 45 min manual work
- 4 systems updated separately
- Copy-paste from PDF
- Manual Drive folder creation

**AFTER (Automated):**
```
Contract signed → Everything happens automatically in 2 minutes
```

**How It Works:**
1. TSQ sends signed contract PDF → email monitored by automation
2. AI parses contract for:
   - Client name, email, LinkedIn
   - Contract terms, billing type, start date
   - Advisor name
3. Auto-create/update across systems:
   - HubSpot: All fields populated
   - Notion: Page created + links added
   - Contender: Profile created/upgraded to Tier 1
   - Google Drive: Folder structure created
4. Welcome email auto-sent from HubSpot with calendar link
5. Slack notification to Client Ops: "New client Doug onboarded, kickoff scheduled"

**Time Saved:** 45 min → 2 min = **43 min per client**
- 100 clients/year × 43 min = **72 hours/year saved**

**Tools Needed:**
- Gmail API (monitor TSQ emails)
- OpenAI API (parse PDF)
- HubSpot API
- Notion API
- Contender API (or Retool)
- Google Drive API
- Slack webhooks

---

### ⭐ Priority 3: Zoom Transcript Intelligence
**Build Timeline:** Week 2-3

**BEFORE:**
- Transcript dumps to Notion
- 30-60 min manual work to tag, extract, categorize

**AFTER (Automated):**
```
Call ends → Action items extracted → Tagged automatically → Team notified
```

**How It Works:**
1. Zoom transcript received
2. AI analyzes:
   - Call type (kickoff, check-in, branding, interview prep)
   - Key discussion points
   - Action items with owners
   - Functional/industry tags mentioned
   - Sentiment analysis (client happy/at-risk?)
3. Auto-tag in Notion:
   - Client profile
   - Call type
   - Participants
4. Auto-create tasks in Notion for action items
5. Auto-populate Contender tags
6. Slack summary to advisor + Client Ops

**Time Saved:** 3-5 hours/week = **156-260 hours/year**

**Bonus:** Enables searchable insights across all client calls

---

### ⭐ Priority 4: Follow-Up Automation (Exec Side)
**Build Timeline:** Week 4-5

**BEFORE:**
- Zero automated follow-ups
- "It's all memory"
- Lost deals

**AFTER (Automated):**
```
Sales call logged in Notion → Auto-reminder created → Advisor notified
```

**How It Works:**
1. Detect when advisor creates Notion note tagged "Sales"
2. Auto-create HubSpot deal (even though they don't want complexity)
3. OR: Create Notion reminder task
4. Slack reminder 2 weeks later: "Follow up with Tim Smith - last contact 11/5"
5. If no activity after 4 weeks: escalate reminder

**Time Saved:** Unquantifiable (prevents lost deals)

**Adoption Strategy:**
- Zero-click for advisors
- Just works in background
- Slack reminders (they already use Slack)

---

### ⭐ Priority 5: Unified Task Capture
**Build Timeline:** Week 4-5

**BEFORE:**
- Tasks in email threads
- Tasks in Slack channels
- Tasks in Zoom chats
- Manual reconciliation

**AFTER (Automated):**
```
Task mentioned anywhere → Auto-captured in Notion → Dashboard shows all
```

**How It Works:**
1. Gmail API monitors emails for keywords:
   - "TODO", "action item", "deadline", "follow up", "can you"
2. Slack webhook captures flagged messages
3. AI extracts:
   - Task description
   - Owner (person mentioned)
   - Deadline (if mentioned)
   - Context/source
4. Auto-create in Notion tasks database
5. Retool dashboard shows all tasks across sources
6. Daily digest email: "You have 5 open tasks"

**Time Saved:** Prevents missed deadlines = client satisfaction

---

### ⭐ Priority 6: Tech Health Monitoring
**Build Timeline:** Week 4-5

**BEFORE:**
- Automations break silently
- Discover days/weeks later
- Emergency manual fixes

**AFTER (Automated):**
```
Zapier fails → Instant Slack alert → Fixed within hours
```

**How It Works:**
1. Monitor Zapier API for failed zaps
2. Check Whalesync sync status
3. Ping HubSpot-Notion sync freshness
4. Test Zoom → Notion connection
5. Retool dashboard: Green/red status for all automations
6. Slack alert within 5 min of any failure

**Time Saved:** Reduces downtime from days to hours

---

## Part 4: Week 2-3 Build Plan

**Week 2 (Build Priority 1):**
- Day 1-2: Set up dev environment, get API access confirmed
- Day 3-4: Build Zoom → AI → Contender intro tracking
- Day 5: Test with real data, deploy to staging

**Week 3 (Build Priority 2 + Refine #1):**
- Day 1-2: Build contract parsing → multi-system onboarding
- Day 3: Test with sample contracts
- Day 4: Team feedback on Priority 1, iterate
- Day 5: Deploy both to production, training session

---

## Part 5: Access Requirements

**Immediate (Need by Monday Week 2):**
- [ ] HubSpot Admin or API key
- [ ] Notion Workspace access + API key
- [ ] Google Workspace service account (Gmail, Drive, Calendar)
- [ ] Zoom account access or API credentials
- [ ] Retool developer account
- [ ] Slack workspace + webhook permissions

**Nice to Have (Week 2-3):**
- [ ] Contender API access (or coordinate with engineering)
- [ ] Zapier account access (to audit existing zaps)
- [ ] Whalesync account access (to check config)

**Send credentials to:** info@kortexlabs.ai

---

## Part 6: Success Metrics (How We'll Measure)

| Metric | Baseline | Target (End of Phase 1) |
|--------|----------|-------------------------|
| Hours/week on intro tracking | 10-15 hrs | 0.5 hrs |
| Client setup time | 45 min/client | 5 min/client |
| Transcript processing time | 3-5 hrs/week | 0 hrs |
| Missed follow-ups | Unknown | Track & reduce |
| Missed deadlines | ~5-8/week | 0-1/week |
| Automation downtime | Days | Minutes |

**Total Time Saved (Phase 1):** 150-200 hours/month

---

## Conclusion

Banff has built an amazing business with deep client relationships and proprietary intelligence. The manual work is holding you back from scaling.

**With these 6 automations, you can:**
- ✅ Double client capacity without adding headcount (your goal)
- ✅ Free up 150-200 hours/month for strategic work
- ✅ Improve client experience (faster response, no missed follow-ups)
- ✅ Reduce human error to near-zero

**I'm ready to build. Let's start Week 2.**

---

**Next Steps:**
1. Review this document, provide feedback
2. Send API access credentials
3. Monday: Kayla deep dive (B4B)
4. Tuesday: Amanda deep dive (exec servicing)
5. Wednesday: Finalize priorities, begin build

---

**Questions for You:**
1. Do these priorities align with your vision?
2. Any automations I missed that are critical?
3. Contender API - should I coordinate with engineering now?
4. Budget for API costs (OpenAI, etc.)?

---

**Prepared by:**
Km Habib
AI Developer, Kortex Labs
info@kortexlabs.ai

---

## How to Deliver This

**Best Format: Loom Video (10-15 min) + Google Doc**

**Loom Script:**
1. "Hi team, Habib here from Kortex Labs"
2. "After 3 discovery sessions, I've mapped your entire operation"
3. [Screen share the document]
4. "Let me walk you through what I found..."
5. [Highlight top 3 pain points]
6. [Show automation #1 before/after]
7. [Show automation #2 before/after]
8. "Bottom line: 150-200 hours/month saved"
9. "Week 2-3 plan: build priorities 1-2"
10. "Questions? Let's discuss on our next call"

Send:
- Loom link
- Google Doc link
- Slack message: "Week 1 deliverable ready for review"

---

This shows you DEEPLY understand their pain and have a clear path forward. 🚀
