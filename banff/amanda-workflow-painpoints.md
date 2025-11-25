# AMANDA - Banff for Business (Pipeline Management)

## Current Workflow

```
B4B CLIENT CALL (with Kayla)
       ↓
MANUAL NOTE-TAKING ⚠️
       ↓
  [Tag: call type, client, monthly/etc.]
  [Write action items manually]
  [Add to task tracker] ⚠️
       ↓
RECEIVE CSV FROM KAYLA ⚠️
       ↓
  [Candidate list from Juicebox research]
       ↓
DEDUPLICATION CHECK (MANUAL) ⚠️⚠️
       ↓
┌────────────────────────────────────────────┐
│ FOR EACH PERSON ON LIST:                  │
│  1. Check HubSpot - are they there?       │
│  2. Check Contender - are they there?     │
│  3. Check engagement status               │
│  → Remove duplicates ⚠️                    │
│  → Flag existing relationships            │
└────────────────────────────────────────────┘
       ↓
[Send clean list back to Kayla]
       ↓
LINKEDIN VERIFICATION ⚠️
       ↓
  [Check profiles are current]
  [Fix auto-updater mistakes]
  [Ensure "former" tags correct]
  [Update manually in Contender] ⚠️
       ↓
MONTHLY SALES CATCHUP (with Kayla/David)
       ↓
  [Review HubSpot deal dashboard]
  [Manually take notes in Notion] ⚠️
  [Send follow-up email with assignments] ⚠️
       ↓
  Chat → Notes → Email → Actions
  (3 separate steps) ⚠️
       ↓
NUDGE EMAIL SETUP ✅
       ↓
  🔧 AUTO-NUDGE: "talked 3 days ago" ✅
  (Tool not specified in transcript)
  [Sends to Kayla: publish profile now]
  → Only first nudge, no follow-ups ⚠️
       ↓
LINKEDIN AUTO-UPDATER ⚠️
       ↓
  🔧 "OUTSIDE PARTNER": Pulls LinkedIn data
  (Kayla's exact words - service not named)
  [Updates Contender profiles in batches]
  [Overwrites manual "former CFO" edits] ⚠️
  [Never adds "former" prefix] ⚠️
  → B4B partners complain about stale data
```

## 🔥 TOP PAIN POINTS

| Pain Point | Time Cost | Impact |
|------------|-----------|--------|
| **Manual deduplication** HubSpot + Contender | High per list | Every pipeline request |
| **LinkedIn verification** | Constant | Auto-updater conflicts |
| **Call notes → task creation** | Every call | Manual transcription |
| **Sales catchup: 3-step process** | Monthly | Chat → Notes → Email |
| **Nudge emails: only first reminder** | - | No systematic follow-up |

## 💡 AUTOMATION OPPORTUNITIES

### 🎯 **Priority 1: Auto-Deduplication**
- Upload CSV → instant check across HubSpot + Contender
- Flag duplicates with details: "In HubSpot since 2023, contacted by Max"
- One-click approve clean list

### 🎯 **Priority 2: LinkedIn Auto-Fix**
- Intelligent sync that preserves manual edits
- Auto-add "former" based on end dates
- Alert when profile changes significantly

### 🎯 **Priority 3: Call Notes → Tasks**
- AI extract action items from call notes
- Auto-create tasks in tracker
- Auto-assign based on keywords

### 🎯 **Priority 4: Sales Catchup Streamline**
- Live dashboard replaces monthly review
- Auto-generate follow-up assignments
- One-click email distribution

### 🎯 **Priority 5: Multi-Stage Nudges**
- Day 3: Publish to first pipeline ✅ (exists)
- Day 10: Reminder to publish to 2nd pipeline
- Day 17: Reminder to publish to 3rd pipeline
- Track completion automatically

## 🔧 CURRENT AUTOMATION TOOLS (Verified from transcripts)

| Tool | What It Does (Confirmed) | What's Missing (Confirmed) |
|------|---------------------------|----------------------------|
| **Auto-nudge** | "talked 3 days ago, publish them" | Only 1st reminder, no multi-stage follow-up |
| **Zapier** | Email forward → Active Searches tracker | Still need manual client tagging |
| **"Outside partner"** | LinkedIn auto-updater (batch sync) | Overwrites manual edits, no "former" logic |
| **Retool** | (Kayla pulls intro history from it) | Manual copy/paste needed |
| **Whale Sync** | (Max's side - HubSpot→Notion) | Not used for B4B workflows |

**Note:** Nudge tool & LinkedIn updater names not specified - just described as existing

**Key Issue:** Tools exist but create MORE manual work (fixing auto-updater) ⚠️

## 📊 IMPACT
- **Time saved: 5-10 hrs/week**
- **Accuracy: Eliminate duplicate outreach**
- **Kayla's blocker removed: No more manual dedup wait**
- **Fix LinkedIn conflicts: Stop client complaints**
- **Systems: HubSpot, Notion, Contender, Zapier, Retool**
