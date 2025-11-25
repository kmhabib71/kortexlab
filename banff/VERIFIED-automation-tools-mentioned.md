# VERIFIED: Automation Tools Mentioned in Transcripts

**Source Documents:**
- Meeting-Transcript.md (First discovery call)
- GMT20251124-191522_Recording.transcript.vtt (Max call)
- GMT20251124-213001_Recording.transcript.vtt (Kayla/Amanda call)
- Answers.md

---

## ✅ EXPLICITLY CONFIRMED

### **WHALE SYNC**
**What was said:**
- Meeting-Transcript.md line 259: Max said "we have a whale sink set up that will automatically go into our Notion database"
- Meeting-Transcript.md line 516: Amanda said "there were a couple of tools that Max mentioned that we didn't get to like screen share with you, and that was like Zapier and whale sync, Those are like how our platforms can talk to each other and automate things across"
- Answers.md line 49: Listed as tool #4

**What it does (confirmed):**
- HubSpot → Notion sync
- When Max marks client as "Tier 1" in HubSpot, Whale Sync auto-creates Notion profile

**What's still manual:**
- Need to manually add HubSpot link to Notion page
- Need to manually add Contender link to Notion page

---

### **ZAPIER**
**What was said:**
- Meeting-Transcript.md line 415: "That's a Zoom transcript that we use Zapier and it pulls it from Zoom and it dumps it into Notion"
- GMT20251124-191522 (Max): "we have a Zap set up. So that we can just forward that email to an active searches email distro, and it goes in here, and it fills out all of these sections"
- Answers.md line 50: Listed as tool #5

**What it does (confirmed):**
1. **Zoom → Notion transcripts**
   - Auto-dumps Zoom call transcripts to Notion
   - Goes to "Banff Advisor kickoff full transcripts" database

2. **Email forward → Active Searches tracker**
   - Forward client job search email → auto-populates Notion database
   - Fills out columns automatically

**What's still manual:**
- Must manually tag transcript to client page (5-6 hrs/week for Max)
- Must manually tag call type (kickoff, check-in, etc.)
- Must manually add client name to Active Searches entries

---

### **RETOOL**
**What was said:**
- Meeting-Transcript.md line 348: David mentioned "Retool, like, how do we know if we've done anything for a client? Oh fuck, there's an alert. Like they're trying to create a way to like create alerts"
- Meeting-Transcript.md line 373: Matthew asked "do you know retool" and Max confirmed they use it
- GMT20251124-191522 (Max): "And we have a retool generator. We can go and select the time frame, past 6 months, and see all..."
- GMT20251124-191522 (Max): Listed in systems "HubSpot, Notion, Contender, Retool"
- Answers.md line 52: Listed as tool #7

**What it does (confirmed):**
- Client Pathway Management Dashboard (tracks 212 exec clients)
- Quarterly report generation from Contender data
- Activity tracking/alerts
- Trending campaign history lookup
- Can select time frames to view data

**What's still manual:**
- Max doesn't trust report data - requires manual verification
- Relies on perfect manual tagging in Notion
- Human error breaks the dashboard

---

### **NUDGE EMAILS**
**What was said:**
- GMT20251124-213001 line 785: Kayla said "these auto… Like, nudge emails, where it's like…"
- GMT20251124-213001 line 789: "okay, you talked to Robert 3 days ago, you should publish him on, you know, your… on your first pipeline"

**What it does (confirmed):**
- Sends automated email reminder "talked to [person] 3 days ago"
- Prompts to publish profile to first pipeline

**What's missing (confirmed):**
- Line 789: "but then after that, there's no follow-up of, like, the next one or the next one"
- Only reminds for FIRST pipeline, no follow-ups for 2nd, 3rd pipelines

**Tool used:** Likely Zapier (mentioned by Amanda as automation tool), but NOT explicitly stated

---

### **LINKEDIN AUTO-UPDATER**
**What was said:**
- GMT20251124-213001 line 853: Kayla said "we do work with a outside partner that does update the LinkedIns"
- GMT20251124-213001 line 869: "the auto-updater will always pick it to be, you know, whatever their most recent role is"
- GMT20251124-213001 line 877: "that auto… that auto-update just takes over. Also, the auto-update never puts former"
- GMT20251124-213001 line 881: "To answer your question, very long-winded, yes, we run into that problem a lot, where we have to manually check their LinkedIns"

**What it does (confirmed):**
- "Outside partner" updates LinkedIn data in batches
- Pulls most recent role from LinkedIn

**Problems (confirmed):**
- Overwrites manual edits (e.g., "former CFO Credit Suisse")
- Never adds "former" prefix even with end dates
- B4B partners complain data is outdated
- Must manually verify and fix constantly

**Tool name:** NOT specified - just called "outside partner" and "auto-updater"

---

### **CLIENT DATA VALIDATION**
**What was said:**
- GMT20251124-191522 (Max): "Client Data Validation" filter (old CTO)

**What it does (confirmed):**
- Filters Notion for empty columns
- Pulls everything into a doc for review
- Shows which Zoom transcripts need tagging

**Who built it:** Old CTO

---

## ❌ NOT MENTIONED / ASSUMED

The following were NOT explicitly mentioned in transcripts:
- Specific Zapier workflow for nudge emails (assumed based on "automation" context)
- Specific name of LinkedIn updater service
- Exactly how Retool pulls from Contender
- Whether Whale Sync is bidirectional or one-way

---

## 📋 COMPLETE TOOL LIST (from Answers.md)

1. Contender
2. Notion
3. HubSpot
4. **Whalesync**
5. **Zappier** (typo in doc)
6. Typeform
7. **Retool**
8. Gmail
9. ChatGPT
10. GoogleDrive
11. Google Sheets
12. Juicebox
13. Rocketreach
14. Google Calendar
15. LinkedIn
16. Quickbooks
17. Pave
18. Zoom
