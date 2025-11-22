# How to Present Automation to Clients

## The Story Framework: "Before → Pain → Solution → Result"

---

## Example Story 1: Deal Closes → Client Onboarding

### BEFORE (Manual Process)
"Right now, when David closes a deal in HubSpot, what happens next?

Someone has to:
1. Copy client info from HubSpot
2. Paste it into Notion to create client page
3. Create a Google Drive folder manually
4. Send welcome email (copy-paste template)
5. Add client to billing spreadsheet
6. Notify the ops team on Slack

**Time:** 30-45 minutes per client
**Risk:** Forgot a step? Client falls through cracks."

### THE PAIN
"What if someone's sick? What if it's Friday 5pm and a deal closes? What if you onboard 10 clients in one week - that's 7+ hours of copy-paste work."

### THE SOLUTION (What We Build)
"Here's what happens after automation:

David clicks 'Closed Won' in HubSpot → **Everything else happens automatically in 10 seconds:**

```
HubSpot Deal Closes
    ↓
Webhook triggers automation
    ↓
┌─────────────────────────────────────┐
│ Notion: Client page created         │
│ Drive: Folder structure created     │
│ Gmail: Welcome email sent           │
│ Sheets: Added to billing tracker    │
│ Slack: Team notified                │
└─────────────────────────────────────┘
```

**Time:** 0 minutes (it just happens)
**Errors:** 0 (no copy-paste mistakes)"

### THE RESULT
"You just saved 30 minutes per client.
10 clients/month = 5 hours saved
100 clients/year = 50 hours saved

That's a full work week back. Every year. Forever."

---

## Example Story 2: Weekly Reporting

### BEFORE
"Every Monday, someone spends 2 hours:
- Pulling deal data from HubSpot
- Copying into Google Sheets
- Making charts
- Formatting the report
- Emailing it to leadership"

### THE PAIN
"That's 100+ hours per year on a report. And it's always slightly different format. And sometimes it's late because someone was busy."

### THE SOLUTION
"We build this:

```
Every Monday 8am (automatic)
    ↓
n8n pulls fresh data from HubSpot
    ↓
Updates Google Sheet with formulas
    ↓
Generates charts automatically
    ↓
Emails PDF to leadership
    ↓
Posts summary to Slack
```

Nobody touches it. It just arrives. Every Monday. Perfect format."

### THE RESULT
"2 hours/week × 52 weeks = 104 hours/year saved
That person now does actual client work instead of making reports."

---

## Example Story 3: At-Risk Client Detection

### BEFORE
"How do you know a client is unhappy? Usually... when they cancel. Or complain. By then it's too late."

### THE PAIN
"You're reactive, not proactive. You lose clients you could have saved."

### THE SOLUTION
"We build an early warning system:

```
Daily scan (automatic)
    ↓
Check: Client hasn't logged in for 14 days?
Check: Support tickets increased?
Check: Payment failed?
Check: Usage dropped 50%?
    ↓
YES → Alert account manager immediately
    ↓
Slack notification + Notion task created
```

Now you reach out BEFORE they cancel."

### THE RESULT
"Save 2-3 clients per quarter that would have churned.
If each client is worth $10k/year, that's $30k saved per quarter."

---

## How to Present in the Meeting

### Step 1: Ask About Their Pain
"Walk me through what happens when a deal closes today. Who does what?"

*Let them talk. Take notes. Find the manual steps.*

### Step 2: Reflect the Pain Back
"So if I understand correctly, Sarah spends about 45 minutes per client just doing data entry across 4 systems. And sometimes things get missed?"

*They'll nod and add more pain points.*

### Step 3: Paint the Automated Future
"What if that 45 minutes became zero? What if the moment David marks it 'Closed Won', everything downstream just... happens?"

*Pause. Let them imagine it.*

### Step 4: Show Simple Diagram
Draw or describe:
```
[HubSpot] → [Automation] → [Notion + Drive + Email + Slack]
              (magic)
```

### Step 5: Quantify the Value
"If you close 20 deals a month, and each saves 45 minutes, that's 15 hours monthly. 180 hours yearly. What could Sarah do with an extra month of time?"

---

## Phrases to Use

| Instead of... | Say... |
|---------------|--------|
| "We'll integrate the APIs" | "These systems will talk to each other automatically" |
| "Webhook triggers the workflow" | "The moment X happens, Y happens instantly" |
| "We'll build an n8n automation" | "We'll build a system that runs in the background" |
| "Sync the databases" | "Keep everything up to date automatically" |
| "Real-time data pipeline" | "You'll always see current numbers, not yesterday's" |

---

## Visual: The Automation Stack

```
┌─────────────────────────────────────────────────────────┐
│                    YOUR BUSINESS                        │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  [HubSpot]     [Notion]     [Google]     [Retool]      │
│     CRM         Docs        Sheets      Dashboard      │
│      │            │            │            │          │
│      └────────────┼────────────┼────────────┘          │
│                   │            │                        │
│           ┌───────▼────────────▼───────┐               │
│           │    AUTOMATION LAYER        │               │
│           │    (n8n / Make / Custom)   │               │
│           │                            │               │
│           │  • Triggers on events      │               │
│           │  • Moves data instantly    │               │
│           │  • Zero manual work        │               │
│           └────────────────────────────┘               │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## Questions That Uncover Automation Opportunities

Ask these during the meeting:

1. "What tasks does your team do every single day/week that feel repetitive?"
2. "Where do you copy-paste data between systems?"
3. "What reports take the longest to create?"
4. "What falls through the cracks most often?"
5. "What would you automate if you could wave a magic wand?"
6. "How do you know when something goes wrong?"

---

## Sample Dialogue for the Meeting

**Matthew:** "So let's talk about what happens after David closes a deal."

**Client:** "Well, our ops person Sarah gets notified, then she creates the client folder, updates our tracker..."

**You (taking notes):** "Got it. And how long does that process take Sarah typically?"

**Client:** "Maybe 30-40 minutes? Depends."

**You:** "And how many deals close per month roughly?"

**Client:** "Around 15-20."

**You:** "So that's about 10 hours monthly just on that handoff process. What if we could make that instant - the moment David clicks 'Closed Won', everything Sarah does manually just... happens automatically in the background?"

**Client:** "That would be amazing."

**You:** "That's exactly what we'll build in weeks 2-3."

---

## Key Message to Deliver

> "We're not replacing your team. We're giving them superpowers.
> The boring, repetitive stuff happens automatically.
> Your people focus on what humans do best - relationships, decisions, creative work."
