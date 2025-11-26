# FRIDAY DEMO STRATEGY - DAVID PRESENTATION
## Banff Advisors Automation Pitch

**Goal:** Get David's approval to proceed to Week 1 implementation

**Critical Success Factor:** Show working automation in first 2 minutes

---

## PRE-MEETING PREPARATION (Complete by Thursday EOD)

### 1. Build Working Demo - Automation #2: Meeting Note Auto-Tagger

**What to build:**
A live Make.com scenario that takes a Zoom transcript and auto-tags it to a client in Notion

**Technical Requirements:**

**Step 1: Get Access**
- [ ] Notion API access token
- [ ] Test workspace in Notion
- [ ] Sample Zoom transcript (from Banff or create fake one)
- [ ] Make.com account set up

**Step 2: Create Test Data**
- [ ] Create test client page in Notion: "John Smith - Test Executive Client"
- [ ] Create sample Zoom transcript mentioning "John Smith" and call type "sales discovery"
- [ ] Have this ready to upload during demo

**Step 3: Build Make.com Scenario**

**Scenario Flow:**
```
Trigger: Webhook (manual trigger for demo)
  ↓
Module 1: Receive Zoom transcript text
  ↓
Module 2: OpenAI API - Extract client name and call type
  Prompt: "Extract the client name and call type (sales, check-in, intro) from this transcript: [transcript]"
  ↓
Module 3: Notion - Search for client page
  Search query: Client name from OpenAI
  ↓
Module 4: Notion - Update page
  Add transcript link to client page
  Tag call type
  ↓
Output: Success confirmation
```

**Step 4: Test the Demo**
- [ ] Run through the scenario 3 times to ensure it works
- [ ] Time it (should be under 30 seconds to execute)
- [ ] Have backup screenshots in case live demo fails

**Step 5: Prepare Demo Script**

**What you'll say:**
"Before we dive into the deck, let me show you something that's already working. This is Automation #2 - the meeting note tagger that saves Max 5-6 hours per week.

[Screen share Make.com]

Here's a Zoom transcript from a sales call with John Smith. Right now, someone has to manually read this, figure out who the client is, and tag it to their Notion page.

Watch what happens when I trigger the automation...

[Click Run]

The AI reads the transcript... identifies this is John Smith... tags it as a 'sales discovery' call... and boom - it's now on John's client page in Notion. 30 seconds. Zero manual work.

This is just one of 12 automations we're building. Let me show you the full plan."

---

### 2. Prepare Deliverables

**A. PDF Deck**
- [ ] Export `06 polished deck slide.md` to PDF
- [ ] Test all formatting renders correctly
- [ ] Send to David 24 hours before meeting (Thursday morning)
- [ ] Subject: "Friday Presentation: Banff Operations Transformation"

**B. 1-Page Executive Summary**
- [ ] Create single-page summary (see template below)
- [ ] Print or prepare as PDF attachment
- [ ] Include checkboxes for next steps

**C. Google Slides Version**
- [ ] Convert to Google Slides as backup
- [ ] Share link with comment access for team

---

## DEMO DAY SETUP (Friday Morning)

### Technical Setup Checklist
- [ ] Test internet connection
- [ ] Close all unnecessary browser tabs
- [ ] Open Make.com scenario in one tab
- [ ] Open test Notion workspace in another tab
- [ ] Open Google Slides deck in another tab
- [ ] Test screen share in Zoom/Google Meet
- [ ] Have backup: Screenshots of demo working
- [ ] Silence phone notifications
- [ ] Charge laptop to 100%

### Mental Prep
- [ ] Review David's quotes from transcript
- [ ] Practice demo script 2x
- [ ] Prepare for 3 likely objections:
  1. "What if it breaks?" → Automation #4 (Silent Failure Alerts)
  2. "How long will this take?" → First automation live end of Week 1
  3. "What's the ROI?" → 150+ hrs/month saved = ~1 FTE

---

## PRESENTATION FLOW (30 minutes)

### Minutes 1-3: LIVE DEMO 🎯
**Goal:** Create "holy shit" moment

**Script:**
"David, before we talk strategy, let me show you what's already working."

[Run demo as described above]

"This is just one automation. Here's the full plan for the next 6 weeks."

**Transition to slides**

---

### Minutes 4-8: YOUR VISION (Slide 2)

**Goal:** Show you listened and understood

**Script:**
"Everything we're building maps back to what you told us in discovery. You said three things that guide everything:

[Read his quotes from Slide 2]

1. 'I fucking hate manual work. I hate dumb extra clicks.'
2. 'The business can grow and I can hire more mini-mes if we get the data out of my brain.'
3. 'All the insights, all the actions need to end up in the same washing machine.'

That's what this is - your washing machine. One centralized data flow, zero manual clicks, systems that let Clare and Olivia operate like you."

---

### Minutes 9-15: PAIN POINTS (Slide 4)

**Goal:** Let David prioritize, don't tell him

**Script:**
"We talked to you, Max, Kayla, and Amanda. Here's what we heard..."

[Show Slide 4 - don't read it word-for-word]

**Ask David:**
"Which of these hurts most right now? What's costing you the most time or creating the biggest problems?"

[Listen. Take notes. Adjust if needed.]

---

### Minutes 16-22: THE ROADMAP (Slides 5-8)

**Goal:** Show clear 6-week plan with early wins

**Script:**
"Here's how we tackle this. 6 weeks, 12 automations, divided into three phases:

**Week 1-2: Foundation - Quick Wins**
[Show Slide 6]

5 automations that build trust and deliver immediate value:
1. Client onboarding (60 min → 5 min)
2. Meeting note tagger (the one I just showed you - saves Max 5-6 hrs/week)
3. Task extraction from your emails and Liv's Slack
4. Silent failure alerts
5. **Your exec sales pipeline** - the one you mentioned last night

Week 1-2 saves ~60 hours per month immediately.

**Week 3-4: Scale - Tackle the Chaos**
[Show Slide 7]

4 automations for B4B operations:
- P2P intro tracking (Amanda's pain point)
- LinkedIn freshness monitoring
- Data quality validation

Week 3-4 adds another 60 hours/month.

**Week 5-6: Optimize - Enable the Mini-Mes**
[Show Slide 8]

3 automations that transform how advisors work:
- Smart quarterly reports
- Trending campaign AI (automates 'The Machine')
- Workflow standardization

Week 5-6 adds 40 hours/month strategic enablement.

**Total: 150+ hours/month saved. That's almost 1 full-time employee.**"

---

### Minutes 23-27: THE GAME-CHANGER (Slide 9B)

**Goal:** Show technical feasibility with Contender API

**Script:**
"Here's the game-changer we discovered this week: Amanda gave us the Contender API spec.

[Show Slide 9B - API capabilities table]

Contender has 50+ endpoints with full OAuth2 authentication. This means:
- No workarounds through Retool
- Direct automation for everything
- Lower technical complexity
- Lower timeline risk

'The Machine' that Kayla described? It's not a dream - it's an API call away."

---

### Minutes 28-30: NEXT STEPS & THE ASK (Slide 12)

**Goal:** Get explicit approval to proceed

**Script:**
"If you say yes today, here's what happens:

**This Week:**
- Grant API access (Amanda coordinating)
- Set up Make.com and N8N infrastructure

**Week 1:**
- First client auto-onboarded end-to-end
- Meeting tagger live (Max validates)

**Week 2:**
- Your exec sales pipeline live
- 5-6 hours/week saved for Max

**Week 6:**
- All 12 automations operational
- 150+ hours/month saved across team

**The question:** Do we have your approval to start Monday?"

[Pause. Let David respond.]

---

## HANDLING OBJECTIONS

### Objection 1: "What if something breaks?"

**Response:**
"Automation #4 is Silent Failure Alerts. We monitor all connections - Whalesync, Zapier, API integrations. If anything breaks, you get a Slack alert immediately. Weekly health check reports. You'll know before it becomes a problem."

---

### Objection 2: "How long does this really take?"

**Response:**
"First automation goes live end of Week 1. You'll see a real client auto-onboarded through the system. No promises without proof. We build, you validate, then we scale."

---

### Objection 3: "What about Nathan being on paternity leave?"

**Response:**
"Amanda is our primary contact. Nathan offered to hop on calls occasionally if needed. We're working with existing patterns - HubSpot, Notion, Contender API. We're not inventing new systems."

---

### Objection 4: "This sounds expensive - what's the ROI?"

**Response:**
"150 hours/month saved = ~$7,500-$10,000/month in labor cost (assuming $50-65/hr loaded cost). Over 6 months, that's $45K-$60K in operational efficiency. Plus, you can scale services without adding headcount - which maps to your 2026 growth goals."

---

### Objection 5: "We've tried automation before and it didn't stick."

**Response:**
"Three reasons this is different:
1. We mapped YOUR exact workflows from discovery, not generic templates
2. We start with one automation, prove it works, then scale
3. We build monitoring from Day 1 - you know when things break

The demo you just saw? That's real. It works. We're not selling vapor."

---

## POST-MEETING ACTIONS

### If David Says YES:
1. **Immediate (in meeting):**
   - [ ] Confirm Monday kickoff time
   - [ ] Send calendar invite for Week 1 kickoff call
   - [ ] Ask for API access to be granted by EOD Friday

2. **Within 24 hours:**
   - [ ] Send meeting recording (if virtual)
   - [ ] Send action items doc with checkboxes
   - [ ] Send Slack message: "Excited to kick off Monday. API access status?"

3. **Monday:**
   - [ ] Begin Week 1 implementation
   - [ ] Daily standup updates to Matthew/David

---

### If David Says "Let me think about it":
1. **Immediate (in meeting):**
   - [ ] Ask: "What specific concerns do you want to think through?"
   - [ ] Address concerns on the spot if possible
   - [ ] Agree on follow-up timeline: "Can we reconnect Monday morning?"

2. **Within 24 hours:**
   - [ ] Send 1-page summary addressing his specific concerns
   - [ ] Offer to build one more demo if it helps

---

### If David Says NO:
1. **Immediate (in meeting):**
   - [ ] Ask: "What would need to change for this to be a yes?"
   - [ ] Take notes on feedback
   - [ ] Thank him for his time and consideration

2. **Within 24 hours:**
   - [ ] Debrief with Matthew
   - [ ] Send professional close-out email

---

## BACKUP PLANS

### If Live Demo Fails:
- [ ] Have screenshots ready showing the automation working
- [ ] Say: "Let me show you screenshots from when we tested this earlier"
- [ ] Walk through the flow with screenshots
- [ ] Acknowledge: "Demo gods weren't with us today, but here's proof it works"

### If David Gets Pulled Away:
- [ ] Have 1-page summary ready to leave behind
- [ ] Offer to reschedule: "When can we get 30 minutes to walk through this?"
- [ ] Send full deck + recording afterward

### If Tech Issues (Screen Share/Internet):
- [ ] Switch to phone call, talk through the deck
- [ ] Share screen from phone as backup
- [ ] Reschedule if necessary

---

## SUCCESS METRICS

### You know you WON if:
✅ David says "yes, let's start Monday"
✅ David engages with questions (shows interest)
✅ David asks about Week 1 deliverables (thinking ahead)
✅ David commits to granting API access

### You know you're LOSING if:
❌ David is multitasking (checking phone, emails)
❌ David says "send me the deck, I'll review later"
❌ David asks about cost without asking about value
❌ David compares to previous failed automation attempts

**If you're losing:** Go back to the demo. Show, don't tell. Use his words. Make it about mini-mes.

---

## FINAL CHECKLIST - THURSDAY EOD

**Demo Ready:**
- [ ] Make.com scenario tested 3x
- [ ] Test Notion workspace set up
- [ ] Sample transcript ready
- [ ] Demo script practiced 2x
- [ ] Backup screenshots saved

**Deliverables Ready:**
- [ ] PDF deck sent to David
- [ ] 1-page summary printed/ready
- [ ] Google Slides link shared

**Tech Ready:**
- [ ] Screen share tested
- [ ] Internet connection verified
- [ ] All tabs pre-loaded
- [ ] Notifications silenced
- [ ] Laptop charged

**Mental Ready:**
- [ ] David's quotes memorized
- [ ] 3 objections prepared
- [ ] "The Ask" practiced
- [ ] Confidence level: 🔥

---

## THE BOTTOM LINE

**David is a founder who hates manual work.**

Start with a working demo → Use his words → Show Week 1 deliverable → Ask for the yes.

**The deck is backup. The demo is the wow.**

**You got this. 🚀**
