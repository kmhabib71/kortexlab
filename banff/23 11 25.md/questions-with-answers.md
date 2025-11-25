# Meeting Questions - ANSWERED FROM EXISTING FILES

## Questions Already Answered from Transcripts/Documents

### Question 1: How is B4B different from the exec side?
**ANSWER (from Meeting-Transcript.md:565):**
Kayla said "on our side of the business, we live in Contender, whereas client services would live maybe more in Notion." B4B operations are primarily in Contender platform for communication with enterprise clients (PE/VC firms).

---

### Question 3: Monthly pipeline reviews - can you explain that process?
**ANSWER (from Meeting-Transcript.md:142-164):**
- Monthly review of HubSpot B4B pipeline dashboard
- Team (Amanda, Kayla, David) goes through dashboard discussing: "where's the status of everyone here, where do we need to follow up, what's the action items"
- Amanda takes notes in Notion "B4B Team note - Sales catch up"
- Then "Amanda will send an email of like, David, you do these follow-ups, Kayla, you do these follow-ups"
- Process: chat about it → write in Notion → write in email → send it out → check on it (multiple manual steps)
- "we're doing a monthly thing...but I'm managing all that manually" - David

---

### Question 7: Client onboarding - walk me through it step by step
**ANSWER (from Meeting-Transcript.md:212-304):**

**Step-by-step process:**
1. Receive contract PDF from TSQ via email
2. First person to respond = client ops owner for that client

3. **HubSpot (10 min):**
   - Find client
   - Add LinkedIn URL
   - Change type to "Current Private Advisor Client"
   - Assign advisor
   - Select transition pathway
   - Enter contract start date
   - Enter billing terms
   - Mark as Tier 1

4. **Notion (5 min):**
   - Whale Sync auto-creates page when HubSpot tier=1 ✓
   - Manually add HubSpot link
   - Manually add Contender link

5. **Contender (15-20 min):**
   - Check if profile exists (might be Tier 3 from prior outreach)
   - If new: Download LinkedIn PDF, upload to Contender
   - Upload photo separately
   - Change tier 3→1
   - Assign advisor
   - Manually tag: functional expertise, industry expertise, target functions/industries

6. **Google Drive (5 min):**
   - Create client folder
   - Create subfolders: Narratives/Resumes/LinkedIns/Bios

7. **Send welcome email (5 min):**
   - HubSpot template with kickoff scheduler link

**Total: 40-60 minutes per client**

**Most annoying part:** Contender has no API - all manual UI clicking (15-20 min)

---

### Question 8: How do tasks arrive from advisors?
**ANSWER (from Answers.md:8-12 & Meeting-Transcript.md:69, 437-442):**

Tasks arrive via multiple fragmented channels:
- **Email/Notion:** "The biggest time suck is acting on a client and needing to sort through notes and emails to pull out tasks"
- **Manual tracking:** introductions, impact, feedback all tracked manually
- **Inconsistent communication:**
  - Liv/Clare use Slack channels
  - David uses email for client updates/comms
  - "the three advisors are kind of figuring out their own workflows. David has had the same workflow for a while, Liv's a little newer, so she has a different one. Claire's brand new, so she has a new one"
  - "that discrepancy can cause some challenges"
- Tasks get buried in email, no centralized system
- From Answers.md: "Tasks getting buried in email" is a major deadline issue

---

### Question 9: P2P introduction process
**ANSWER (from Meeting-Transcript.md:460 & Answers.md:39):**
- After quarterly check-ins, advisor requests: "do a peer to peer, which means introduce this client to another member of the Banff network"
- Listed in pain points as: "Manual back tracking of introductions" (Answers.md:39)
- **ZERO systematic tracking** - completely ad-hoc
- Process details not fully explained - need to ask about actual workflow

---

### Question 10: Zoom transcript workflow
**ANSWER (from Meeting-Transcript.md:415-442):**

**How it works:**
- Zoom transcript dumps to "Banff Advisor kickoff full transcripts" in Notion automatically via Zapier ✓

**Manual steps required:**
- "we have to manually tag this to a client so it gets pulled to their record"
- "we also need to tag that call type as kickoff so that we can mark that the kickoff call did happen"
- Dumping to Notion is helpful (not lost in Zoom cloud), "But the next step is making sure it gets to its proper home in Notion"

**What breaks:**
- If advisor doesn't tag call type → Retool shows ZERO activity for that client
- "If an advisor misses it or doesn't tag it appropriately, that's where things go south"
- Different advisors have different workflows:
  - David launches calls from client page (auto-tags)
  - Liv and Claire have different workflows

**Chaos scenario:**
- "if David's on a call and Max is on a call, and Lily and Liv are on a call and Claire's on a call all at the same time, there can be multiple things getting pulled into Notion at once"

---

### Question 11: Retool dashboard - what works and what breaks?
**ANSWER (from Meeting-Transcript.md:382-442):**

**What it's supposed to do:**
- Track all client activities: kickoff, check-in, narrative edits, interview prep, personal branding, etc.
- Pulls data from Notion call type field
- Auto-increments activity counters when calls tagged correctly
- Alerts when clients haven't had activities (e.g., no contact in 45+ days)

**What breaks:**
- **Completely dependent on manual tagging**
- "if you don't tag this as the right kind of meeting, not a check-in call or not an interview prep, or you didn't check it as a narrative review, that doesn't go into the dashboard, so then our reporting and our alerting system is all out of whack"
- High human error rate makes entire system unreliable
- Dashboard shows inaccurate data → team stops trusting it

---

### Question 13: Contender limitations
**ANSWER (from Meeting-Transcript.md:543-555):**

**The problem:**
- Nathan: "contender doesn't like to communicate very well" with other tools
- "We have kind of these different data places...Contender kind of has maybe the other half of activities"
- Retool pulls data from all sources (Contender, Notion, HubSpot) and presents it

**Why it's limited:**
- Contender is their own in-house software product
- "It's just right now it's not been developed with that [API communication] in mind"
- "We can change it to communicate better with other tools" - they have engineers who can build it

**Current workaround:**
- "For now, we've just stuck with like, go to retool, pull data from contender" as the basic workflow
- Changes to Contender only happen by going into Contender directly and taking action

---

### Question 15: Whalesync (HubSpot → Notion sync)
**ANSWER (from Meeting-Transcript.md:260-266 & Answers.md:38-39):**

**What works:**
- ✓ Whale Sync automatically creates Notion page when HubSpot client tier is marked as "Tier 1"
- ✓ Pre-populates contract information from HubSpot

**What's still manual:**
- Manually add HubSpot profile link to Notion
- Manually add Contender profile link to Notion
- Client setup involves "hubspot to notion sync" via Whale Sync

**Reliability:** Working but not complete automation

---

### Question 23: Month 1-2 standardized process
**ANSWER (from Meeting-Transcript.md:451-456):**

**The process (WORKS WELL):**
- "if they are brand new, right, their first month in, 1st 2 months in. We're very, very good at making sure that it's standardized"

**What happens:**
1. Kickoff call
2. Narrative edits for them
3. Start introducing them to people in network
4. Trending campaign: "send their profile to our band for business partners, our private equity firms, our venture capital firms"

**Timeline:**
- "That usually takes about 2 months, and that's pretty set in stone and what we're doing each and every day"

**Status:** First 2 months works well because it's standardized - this is NOT the problem area

---

### Question 24: Kickoff call workflow
**ANSWER (from Meeting-Transcript.md:415-422):**

**Automatic part:**
- Zoom auto-dumps transcript to "Banff Advisor kickoff full transcripts" in Notion ✓

**Manual parts:**
- "we have to manually tag this to a client so it gets pulled to their record"
- "we also need to tag that call type as kickoff so that we can mark that the kickoff call did happen"
- Dumping to Notion is helpful (things aren't lost in Zoom cloud)
- "But the next step is making sure it gets to its proper home...in Notion"

**Action item extraction:** Not mentioned - need to ask how they currently do this

---

### Question 25: Narrative editing process
**ANSWER (from Meeting-Transcript.md:481-492 & Answers.md:23):**

**Where it lives:**
- Each client has Google Drive folder with subfolders: Narratives, Resumes, LinkedIns, Bios
- "all of that info lives in Google Drive. It doesn't live in Notion, doesn't live in Contender or HubSpot"

**Status:**
- Process is standardized and listed as one of the core activities Client Ops does
- Part of the Month 1-2 standardized process that "works well"

**Details NOT in transcript - need to ask:**
- How feedback is provided (email? Doc comments?)
- How they track "who's waiting on whom"
- Whether clients ghost and how they follow up

---

### Question 26: Trending campaigns - profile staleness
**ANSWER (from Meeting-Transcript.md:311-322):**

**The horror story (in David's words):**
- "we then share whisper people to search firms, private equity firms...Contenders like we're the dealer, we're whispering stuff out"
- "if they update their LinkedIn and we haven't talked to them in 2 years...We actually have to manually make sure and remember, oh fuck, did we update their LinkedIn?"
- "what we're going to send is not live, right? It's a pretend LinkedIn"
- "Is it the right information? Is it up to date? Is it saying the right stuff? There's a lot of manual, and if we don't do it well, **we look like idiots**"

**Major pain point:**
- Profile staleness is a MAJOR embarrassment risk
- Have to manually check if executives updated LinkedIn
- No automated sync from LinkedIn → Contender

---

### Question 27: Month 3+ ad-hoc requests (THE CHAOS ZONE)
**ANSWER (from Meeting-Transcript.md:457-463):**

**When it happens:**
- "Where the fall off happens. And where things go a little haywire and where we start getting reactive is after that [Month 2]"
- "around 5-6 months in, we have check-in calls with clients every quarter"

**What advisors request:**
- "around the 2nd quarter, we'll get an update from David after check-in calls saying:"
  - "do a peer to peer"
  - "do another trending campaign"
  - "do another narrative edit refresh"
  - "do a target mapping, map out some companies of interest that they would find interesting"

**The problem:**
- "That sort of ad hoc Task list builds up pretty quickly and it's really hard to standardize it for each client"
- "It really depends on where a client is, what they're looking to do. How urgent they need it done"
- Goes from standardized (Month 1-2) → reactive/chaotic (Month 3+)

---

### Question 29: Zoom transcript chaos
**ANSWER (from Meeting-Transcript.md:426-429):**

**The scenario:**
- "if David's on a call and Max is on a call, and Lily and Liv are on a call and Claire's on call all at the same time, there can be multiple things getting pulled into Notion at once"

**The problem:**
- Multiple transcripts dump simultaneously
- Creates chaos trying to figure out which transcript belongs to which client
- Process takes time to sort through and tag correctly

**Time cost:** Quote mentions "30-60 min" but need to verify exact source

---

### Question 30: Task management - email/Slack/Zoom fragmentation
**ANSWER (from Meeting-Transcript.md:437-442 & Answers.md:69):**

**The fragmentation:**
- "the three advisors are kind of figuring out their own workflows"
  - David: has had same workflow for a while
  - Liv: a little newer, different workflow
  - Claire: brand new, has new workflow
- "that discrepancy can cause some challenges"

**Communication channels:**
- From Answers.md:69: "Liv/Clare using slack channels and David using email client updates and comms"
- Advisors launch calls differently - some auto-tag to client, some don't
- From Answers.md:65: "Tasks getting buried in email" causes missed deadlines

**The result:**
- Tasks buried across email, Slack, Zoom transcripts
- No centralized system
- Things fall through cracks

---

### Question 36: Google Drive workflow
**ANSWER (from Meeting-Transcript.md:481-492):**

**Structure:**
- "we have a Google Drive for each client...all lives here"
- "when a new client signs, they get one of these Folders"
- Contains subfolders: Narratives, Resumes, LinkedIns, Bios
- "this houses all of their narrative edits, their resumes, their LinkedIns, their bios"

**Creation:**
- Folder creation is **manual** (part of the 40-60 min onboarding process)

**Details NOT in transcript - need to ask:**
- How they share with clients
- Version control issues

---

### Question 41: B4B pipeline reviews - Amanda's role
**ANSWER (from Meeting-Transcript.md:139-164):**

**The process:**
- Monthly review of HubSpot B4B pipeline dashboard
- Team (Amanda, Kayla, David) "go through this dashboard and just kind of walk through where's the status of everyone here, where do we need to follow up, what's the action items"

**Amanda's specific role:**
- Takes notes in Notion during call (in "B4B Team note - Sales catch up")
- After call: "Amanda will send an email of like, David, you do these follow-ups, Kayla, you do these follow-ups"

**The manual nightmare:**
- Process: "we chat about it, we put it here [Notion], we write it in an email, we send it out, we check on the [dashboard]" - multiple manual steps
- "we're doing a monthly thing...but I'm managing all that manually" - David
- Time: Need to verify "4-5 hours" claim

---

## Summary: Questions with FULL answers vs. PARTIAL answers

### ✅ FULLY ANSWERED (Can validate, add depth):
1. How is B4B different from exec side
3. Monthly pipeline reviews
7. Client onboarding step-by-step
8. How tasks arrive from advisors
10. Zoom transcript workflow
11. Retool dashboard issues
13. Contender limitations
15. Whalesync
23. Month 1-2 process
24. Kickoff call workflow
26. Trending campaign staleness
27. Month 3+ ad-hoc chaos
29. Zoom transcript chaos
30. Task management fragmentation
36. Google Drive workflow
41. B4B pipeline reviews

### ⚠️ PARTIALLY ANSWERED (Need more details):
9. P2P intro process (know it exists, not the detailed workflow)
25. Narrative editing (know where it lives, not the tracking/ghosting details)

### ❌ NOT ANSWERED (Need to ask):
2. B4B client lifecycle walkthrough
4. How whispers are tracked
5. Top 3 B4B pain points
6. B4B intro requests workflow
12. Where would 10 hours back per week come from
14. Notion organization details
16. Data living in wrong places
17-22. All priority/automation questions
28. Retool tagging frequency
31. Client check-in call improvements
32-34. P2P detailed workflow questions
35. Notion organization exec side
37. Email communication tracking
38-40. Automation priority questions
42. Action item accountability
43-45. Access/closing questions
