# Sunday Tasks - Week 1 Discovery

## Goal for Today
Complete workflow mapping + automation roadmap with technical approaches. This becomes the foundation for your Friday deliverable.

---

## Task Breakdown (7-9 hours total)

### PHASE 1: Workflow Mapping (2-3 hours)

#### Task 1.1: Map Executive Client Journey (45-60 min)
**What to create:**
- Visual diagram of exec client lifecycle from lead → onboarding → servicing → retention
- Identify every touchpoint where data moves between systems

**Systems involved:**
- HubSpot (initial lead/deal)
- Notion (notes, narratives, call logs)
- Contender (client record, intro tracking)
- Google Drive (documents, templates)
- Zoom (discovery calls, check-ins)
- Gmail (communication with client)

**Key milestones to map:**
1. Lead enters system (how? HubSpot form? Referral?)
2. Discovery call scheduled (Calendly? Manual?)
3. Contract signed (TSQ handles this via Arthur)
4. Onboarding kickoff (4 systems updated manually - 45 min)
5. First 2 months (standardized: narratives, trending, LinkedIn)
6. Month 3+ (ad-hoc advisor check-ins, intro requests)
7. Ongoing servicing (P2P introductions, market intel, board prep)

**Output:**
- Simple flowchart (use Excalidraw, Draw.io, or even Google Slides)
- Show WHERE manual work happens (red flags)
- Show WHERE data gets lost/duplicated (yellow flags)

---

#### Task 1.2: Map B4B Client Journey (45-60 min)
**What to create:**
- Visual diagram of B4B enterprise client lifecycle
- Compare to exec side (what's same, what's different)

**Systems involved:**
- HubSpot (enterprise pipeline - more structured than exec side)
- Contender (primary system for B4B per Kayla)
- Notion (pipeline review notes)
- Email (action items after monthly reviews)

**Key milestones to map:**
1. Enterprise lead (PE firm, VC, corporate)
2. Discovery call
3. Contract negotiation
4. Onboarding
5. Monthly pipeline reviews (Amanda takes notes → emails action items = 4-5 hrs manual)
6. Intro requests from enterprise clients
7. Search tracking (who was introduced, feedback loops)

**Output:**
- Flowchart similar to exec side
- Highlight overlaps (intro tracking affects both sides)
- Note differences (B4B uses HubSpot pipeline, exec doesn't)

---

#### Task 1.3: Map Internal Operations Workflows (30-45 min)
**What to create:**
- How team collaborates internally
- Where tasks get assigned/tracked/lost

**Key workflows:**
1. **Advisor → Ops handoff**
   - David/Liv/Claire have client calls → how do tasks reach Max/Lily?
   - Email? Slack? Notion? (Answer: buried in all 3 = missed deadlines)

2. **Zoom transcript processing**
   - Call ends → transcript auto-dumps to Notion (Zapier)
   - Then what? Manual tagging by call type, client name (30-60 min when multiple calls)
   - If missed, transcript lost in Notion (too many pages)

3. **Retool dashboard updates**
   - Nathan pulls data from Contender into Retool
   - Dashboard alerts when clients need attention
   - BREAKS when call types not tagged in Notion (human error)

4. **Monthly B4B pipeline reviews**
   - Amanda takes notes in Notion
   - Manually emails action items to team
   - 4-5 hours per month

**Output:**
- List of internal workflows with pain points highlighted
- Show dependencies (Retool depends on manual Notion tagging)

---

### PHASE 2: Automation Roadmap (3-4 hours)

#### Task 2.1: Priority 1 - Intro Tracking Automation (45-60 min)
**Current state:**
- 5-7 min manual entry per intro (from Loom video)
- 10-15 hrs/week completely manual
- Advisors have Zoom calls with execs → introductions happen → manually logged in Contender

**Proposed solution:**
1. **Trigger:** Zoom call ends
2. **Process:** Zapier webhook → Download recording/transcript → GPT-4 API
3. **AI extraction:**
   - Who was introduced to whom?
   - What was discussed?
   - Follow-up needed?
   - Call type (networking, intro call, check-in, etc.)
4. **Output:** Auto-update Contender via Retool intermediary + tag in Notion
5. **Notification:** Slack alert to advisor: "3 intros logged from your call with [Client Name]"

**Technical details to document:**
- APIs needed: Zoom, OpenAI, Notion, Slack
- Contender update method: Retool intermediary (Nathan's approach) OR coordinate with engineering
- Estimated cost: ~$0.50-1.00 per call (GPT-4 processing)
- Estimated build time: Week 2-3 (2-4 days)

**ROI:**
- Time saved: 10-15 hrs/week = $450-675/week = $1,800-2,700/month
- Cost: ~$20-40/month (API costs)
- Net savings: $1,760-2,660/month

---

#### Task 2.2: Priority 2 - Client Setup Automation (45-60 min)
**Current state:**
- 45 min across 4 systems when contract signed
- Manual steps:
  1. Create HubSpot deal
  2. Create Notion client page with template
  3. Create Contender client record
  4. Create Google Drive folder with subfolders (Resume, Bio, LinkedIn, Narratives, etc.)

**Proposed solution:**
1. **Trigger:** TSQ sends contract PDF via email (Arthur emails David/team)
2. **Process:** Gmail API monitors inbox → AI parses PDF for client details
3. **AI extraction:**
   - Client name
   - Email
   - Phone
   - Package type (exec advisory, B4B, etc.)
   - Start date
4. **Multi-system updates (parallel):**
   - HubSpot: Create deal, set stage to "Client - Onboarding"
   - Notion: Create page from template, populate fields
   - Google Drive: Create folder structure via Drive API
   - Contender: Create client record via Retool
5. **Notification:** Slack message to Max/Lily: "New client onboarded: [Name]. All systems ready."

**Technical details:**
- APIs needed: Gmail, OpenAI (PDF parsing), HubSpot, Notion, Google Drive, Retool
- Estimated cost: ~$0.10-0.30 per client setup (API costs)
- Estimated build time: Week 3-4 (3-5 days)

**ROI:**
- Time saved: 43 min × 100 clients/year = 72 hrs/year = $3,240/year
- Cost: ~$10-30/year
- Net savings: $3,210-3,230/year

---

#### Task 2.3: Priority 3 - Zoom Transcript Intelligence (30-45 min)
**Current state:**
- Transcripts auto-dump to Notion (Zapier already set up)
- Manual tagging required: call type, client name, action items
- Takes 30-60 min when multiple calls happen simultaneously
- If missed, transcript lost in Notion

**Proposed solution:**
1. **Trigger:** Transcript arrives in Notion (existing Zapier flow)
2. **Enhancement:** Add GPT-4 processing step BEFORE dumping to Notion
3. **AI extraction:**
   - Call type (intro call, check-in, networking, board prep, etc.)
   - Client name(s) mentioned
   - Action items (who needs to do what by when)
   - Key topics discussed
4. **Auto-tagging:** Notion properties auto-populated
5. **Side effect:** Fixes Retool dashboard (depends on correct tagging)

**Technical details:**
- APIs needed: Zapier (already exists), OpenAI, Notion
- Estimated cost: ~$0.50-1.00 per transcript
- Estimated build time: Week 2 (1-2 days)

**ROI:**
- Time saved: 3-5 hrs/week = $135-225/week = $540-900/month
- Cost: ~$20-40/month
- Net savings: $500-860/month
- BONUS: Fixes Retool alerting system (catches at-risk clients)

---

#### Task 2.4: Priority 4 - Exec Follow-Up System (30-45 min)
**Current state:**
- Zero automated follow-ups
- "It's all memory" (quote from meeting)
- Losing deals because no systematic follow-up

**Proposed solution:**
1. **Trigger:** Sales note added to Notion (advisor logs call)
2. **AI extraction:** Determine follow-up timeline
   - "Call back in 2 weeks" → auto-reminder in 2 weeks
   - "Waiting on their decision" → reminder in 1 week
   - "Hot lead" → reminder in 3 days
3. **Reminder delivery:** Slack DM to advisor: "Follow up with [Prospect Name] - it's been 2 weeks since your last call"
4. **Escalation:** If ignored for 3 days, notify David

**Technical details:**
- APIs needed: Notion webhooks, OpenAI, Slack
- Estimated build time: Week 3 (2-3 days)

**ROI:**
- Impact: Unquantifiable but REAL
- Prevents lost deals (each deal = $15k-40k annual client value)
- If saves 1-2 deals/year = $30k-80k revenue saved

---

#### Task 2.5: Priority 5 - Unified Task Capture (30-45 min)
**Current state:**
- Tasks buried in email, Slack, Zoom transcripts
- Team misses deadlines because tasks scattered across channels

**Proposed solution:**
1. **Monitors:**
   - Gmail (action items in emails)
   - Slack (messages with task keywords: "can you...", "need you to...", "by Friday...")
   - Zoom transcripts (action items extracted by Priority 3 automation)
2. **AI extraction:** Identify tasks
   - Who needs to do it?
   - What's the task?
   - When is it due?
3. **Auto-create Notion tasks:** Central task database
4. **Dashboard:** Retool dashboard shows all open tasks by person

**Technical details:**
- APIs needed: Gmail, Slack, Notion, OpenAI
- Estimated build time: Week 4 (3-5 days)

**ROI:**
- Impact: 80% reduction in missed deadlines
- Time saved: 2-3 hrs/week (searching for tasks) = $90-135/week = $360-540/month

---

#### Task 2.6: Priority 6 - Tech Health Monitoring (20-30 min)
**Current state:**
- Automations break silently
- Discovered days later when someone asks "where's the data?"

**Proposed solution:**
1. **Monitors:**
   - Zapier automation runs (via Zapier API)
   - Retool dashboard updates (check last update time)
   - HubSpot → Notion sync (Whalesync status)
2. **Health checks every 15 min:**
   - If automation hasn't run in 6 hours → alert
   - If Retool data stale (> 24 hrs) → alert
3. **Slack notifications:** #tech-alerts channel
4. **Dashboard:** Retool system health page (green/yellow/red status)

**Technical details:**
- APIs needed: Zapier, Retool, Whalesync, Slack
- Estimated build time: Week 4 (1-2 days)

**ROI:**
- Impact: Downtime from days → hours
- Trust in automation increases (team will actually USE the systems)

---

### PHASE 3: Document Everything (2-3 hours)

#### Task 3.1: Create Visual Roadmap (60-90 min)
**What to create:**
- Single-page visual showing all 6 automations
- Timeline: Week 2-3 (Priorities 1-3), Week 4-5 (Priorities 4-6)
- Before/after metrics for each
- Technical architecture diagram (high-level)

**Tools:**
- Use Excalidraw, Figma, or Google Slides
- Make it CLIENT-FRIENDLY (they're not technical)
- Show data flow: System A → AI Processing → System B

**Example layout:**
```
[Current State]          [Automation]           [Future State]
10-15 hrs/week    →   Intro Tracking Auto  →   5 min/week
45 min/client     →   Client Setup Auto    →   2 min/client
3-5 hrs/week      →   Transcript AI        →   Fully automated
```

---

#### Task 3.2: Write Technical Approach Summary (30-45 min)
**What to document:**
For each automation, write:
1. **Current pain point** (with quote from meeting as evidence)
2. **Proposed solution** (1-2 sentences)
3. **Technical approach** (APIs, tools, workflow)
4. **Time saved** (hours/week or hours/month)
5. **Cost estimate** (API costs)
6. **Build timeline** (when it'll be done)
7. **Risk/dependency** (what could block it)

**Format:**
Use clear, scannable format (bullets, bold headers)

**Evidence:**
Reference specific quotes from meeting transcript to show you're not guessing

---

#### Task 3.3: Draft Week 2-3 Build Plan (30-45 min)
**What to document:**
- Week 2: Build Priority 1 (Intro Tracking) + Priority 3 (Transcript Intelligence)
  - Why these two? They're connected (both use Zoom transcripts)
  - Can reuse GPT-4 processing logic
  - Biggest time savings (13-20 hrs/week combined)

- Week 3: Build Priority 2 (Client Setup)
  - Standalone automation
  - Clear trigger (TSQ contract email)

- Week 4-5: Build Priorities 4-6 (if approved)

**What you need to start Week 2:**
- API access to: HubSpot, Notion, Google Workspace, Retool, Zoom
- Test accounts in their systems
- Sample data (anonymized if needed)
- 1 hour with Nathan (when he's back) to understand Retool setup

---

#### Task 3.4: Prepare Sunday Evening Update (15-20 min)
**What to send Matthew:**
- Brief Slack message showing progress
- Attach draft roadmap (Google Doc link or PDF)
- Ask for feedback: "Does this match your vision?"

**Message template:**
```
Matthew,

Finished mapping their complete workflow - exec side and B4B side. Built the automation roadmap.

**6 High-Impact Automations Identified:**

Priority 1: Introduction Tracking Automation
• Saved: 10-15 hrs/week
• Technical approach: Zoom API → GPT-4 → Retool/Contender

Priority 2: Client Setup Automation
• Saved: 43 min per client × 100/year = 72 hrs/year
• Technical approach: Gmail monitors TSQ emails → AI parses PDF → multi-system updates

Priority 3: Zoom Transcript Intelligence
• Saved: 3-5 hrs/week
• Technical approach: Zapier → GPT-4 parsing → auto-tag in Notion + Contender

Priority 4: Exec Follow-Up System
• Impact: Prevent lost deals
• Technical approach: Notion webhooks → reminder engine → Slack

Priority 5: Unified Task Capture
• Impact: 80% reduction in missed deadlines
• Technical approach: Gmail + Slack + Notion → GPT-4 extraction → task dashboard

Priority 6: Tech Health Monitoring
• Impact: Downtime from days → hours
• Technical approach: API health checks → Slack alerts

**Total Impact: 150-200 hrs/month saved**

**Roadmap draft:** [GOOGLE DOC LINK]

Ready for Monday/Tuesday deep dives to validate and refine.

- Habib
```

---

## Resources You'll Need Today

### Reference Documents:
- `d:\cortex\banff\Meeting-Transcript.md` (evidence, quotes)
- `d:\cortex\banff\Answers.md` (pre-call pain points)
- `d:\cortex\banff\loom-transcript.md` (intro tracking workflow)
- `d:\cortex\banff\pain-points-analysis.md` (your analysis from yesterday)

### Tools to Use:
- **Diagrams:** Excalidraw (excalidraw.com) or Google Slides
- **Document:** Google Docs (so Matthew can access it easily)
- **Notes:** Your local markdown files

### Time Management:
- Start: Now
- Phase 1 (Workflow Mapping): 2-3 hours → Done by 12-1 PM
- Break: 30-60 min
- Phase 2 (Automation Roadmap): 3-4 hours → Done by 5-6 PM
- Break: 30-60 min
- Phase 3 (Documentation): 2-3 hours → Done by 9-10 PM
- Send update to Matthew: 10 PM

---

## Success Checklist

By end of today, you should have:
- ✅ Visual workflow diagrams (exec + B4B + internal ops)
- ✅ 6 automation proposals with technical approaches
- ✅ Before/after metrics for each automation
- ✅ Cost estimates (API costs)
- ✅ Build timeline (Week 2-3-4 plan)
- ✅ Risk/dependency identification (Contender API, access needed)
- ✅ Draft roadmap document (Google Doc)
- ✅ Sunday evening update sent to Matthew

---

## Tips for Today

**Stay focused:**
- Turn off distractions (social media, etc.)
- Work in 90-min blocks with breaks
- Reference the transcript often (evidence-based proposals)

**Don't overthink:**
- Draft diagrams don't need to be perfect (you'll refine Wed-Thu)
- Focus on CLARITY over beauty
- Use simple language (David is non-technical)

**Ask yourself:**
- "Would David understand this explanation?"
- "Is this backed by evidence from the meeting?"
- "Does this show clear ROI?"

**Remember:**
- You're not building code today - you're building a PLAN
- The plan is what gets you Week 2-3 work approved
- Quality of thinking > speed

---

## If You Get Stuck

**Problem:** Don't know technical approach for an automation
- **Solution:** Research similar automations (Google: "Zapier + OpenAI + Notion workflow"), document what you find, note it as "needs validation with Nathan"

**Problem:** Not sure about cost estimates
- **Solution:** Use rough estimates (OpenAI GPT-4: ~$0.01-0.03 per API call), note as "estimated - will confirm during build"

**Problem:** Workflow diagram too complex
- **Solution:** Break into smaller diagrams (one per automation)

**Problem:** Running behind schedule
- **Solution:** Focus on Priorities 1-3 first (biggest ROI), document 4-6 at high level only

---

## End of Day Reflection

Before sending update to Matthew, ask yourself:
1. ✅ Does this roadmap solve their biggest pain points?
2. ✅ Are the ROI numbers realistic and backed by evidence?
3. ✅ Is the technical approach feasible with their tech stack?
4. ✅ Have I identified risks/dependencies proactively?
5. ✅ Would Matthew feel confident presenting this to Banff?

If yes to all 5 → **Send it.**

---

**You've got this. Today's work sets up the entire Week 2-3 build plan.**

**Focus. Execute. Ship.**
