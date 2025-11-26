First thirty minute is with  banff-advisor founder david, rest from banff team, can you tell me what what pain point they are talking and what is the solution with automation, since I'm playing as Automation engineer, I need to know that:



Based on the transcript, here's a breakdown of the pain points and automation opportunities:

## Key Pain Points Identified

### 1. **Sales Pipeline & Follow-up Management**
- **Executive side**: No deal pipeline tracking at all - everything is in people's heads
- Manual follow-up tracking (or none at all on exec side)
- Monthly manual review of enterprise deals in HubSpot/Notion
- Advisors each have different workflows (David, Liv, Claire all do things differently)
- Website inquiries go to Slack but there's no system to ensure follow-up

### 2. **Client Onboarding - Multiple Manual Data Entry Points**
When a new client signs, Max must manually update **4 separate systems**:
- **HubSpot**: Change client type, add LinkedIn, set advisor, pathway, contract dates, billing terms
- **Notion**: Auto-creates via Whalesync, but still needs manual linking of HubSpot/Contender profiles
- **Contender**: Create profile, upload LinkedIn PDF, add photo, tag industries/functions/expertise manually
- **Google Drive**: Create client folder for narratives/resumes

### 3. **Meeting Notes & Call Tagging**
- Zoom transcripts dump into Notion automatically via Zapier
- **But**: Must manually tag each call to the right client profile
- Must manually tag call type (kickoff, check-in, interview prep, etc.)
- If tagging is wrong/missed, the Retool alerting dashboard breaks
- Each advisor has their own workflow, causing inconsistency

### 4. **Client Activity Tracking & Alerts**
- Built a Retool dashboard to track all 212 clients and touchpoints
- Relies entirely on correct manual tagging
- No automated "you haven't contacted this client in X days" alerts that actually work reliably

### 5. **Profile Data Freshness**
- When sharing executive profiles to PE firms/search firms, they send a "snapshot" LinkedIn
- If the person updated their real LinkedIn, Banff's version is outdated
- No system to flag when profiles need refreshing

### 6. **Communication Fragmentation**
- Client updates come via: Email, Zoom calls, text messages, phone calls, Slack
- This information doesn't consolidate into one place automatically

### 7. **Contract Handoff**
- David emails TSQ (external billing team) to send contracts
- 24-hour turnaround delay
- Manual notification back when signed

---

## Automation Opportunities

| Area | Current State | Automation Solution |
|------|--------------|---------------------|
| **Follow-up reminders** | Manual/forgotten | Auto-triggers based on last contact date, deal stage, call notes |
| **Client onboarding** | 4 systems manually | Single intake → auto-populate HubSpot, Notion, Contender, create Drive folder |
| **Call tagging** | Manual after every call | AI analyzes transcript → auto-tags client + call type |
| **Pipeline creation** | None on exec side | Auto-create deal when sales call detected in Notion notes |
| **Profile freshness** | Manual memory | Scheduled LinkedIn scrape → flag changes |
| **Meeting summaries** | Dumps raw into Notion | AI extracts action items, tags to client, updates Retool dashboard |
| **Bulk profile uploads** | Semi-manual CSV | Full automation with AI-enriched tagging of industry/function |

---

## Tech Stack You'll Need Access To
- HubSpot (API)
- Notion (API)
- Retool (admin)
- Google Workspace
- Contender (internal - needs engineer coordination)
- Zapier/Whalesync (to understand existing automations)

The core theme: **they're drowning in manual data entry across disconnected systems**, and human error in tagging breaks their reporting. The win is creating a unified data flow where one action propagates correctly everywhere.