# How Banff Advisors Works in Contender

**Based on Contender Dashboard Data Structure Analysis**

---

## Banff Team Structure

**Executive Advisors** (Client-facing relationship owners):
- **David Boehmer** - Founder & CEO (majority of Tier 1 clients)
- **Clare Buxton** - Executive Advisor
- **Lauren Mello** - Executive Advisor, Brand Strategy
- **Olivia Barth** - Executive Advisor

**Client Services** (Operational support):
- **Max Ravech** - Lead for trending campaigns, P2P curation, quarterly reporting
- **Lily Tympanick** - Onboarding, narrative development, profile management
- **Amanda Chi** - B4B pipeline management, campaign execution

**B4B Leadership**:
- **Kayla Kanipe** - Head of Banff for Business

**Product & Engineering**:
- **Anneliese Pineda Klein** - Product and Design Lead
- **Jessica Wray** - Senior Full-Stack Software Engineer
- **Evgeniy Apushkin** - Staff Backend Engineer
- **Nathan Franklin** - Senior Data Scientist

**External Advisor**:
- **Samantha Lassoff** - Executive Coach

---

## Overview: Banff's Two-Sided Business Model

Contender is Banff's proprietary CRM/ATS system that manages their two core services:

1. **Executive Advisory Services** - 212 Tier 1 executives paying for career advisory, board placement, and peer networking
2. **B4B (Business-for-Business) Network** - 300+ VC/PE firms and search firms looking for executive talent

**Contender serves as the central matching engine between these two sides.**

**Key Distinction in Contender Data:**
- **"Advisor"** field = Executive Advisor (David/Clare/Lauren/Olivia) - strategic relationship owner
- **"Client Owner"** field = Client Services (Max/Lily/Amanda) - operational lead

---

## Tier System Explained

Contender uses a tier system to categorize all 4,981 people in the database:

**Tier 1 - Executive Client** (212 people)
- Paying clients with active Private Advisor contracts
- Receive full service: onboarding, narrative development, trending campaigns, P2P intros, quarterly reports
- Automatically synced to Notion via WhaleSync when marked as Tier 1 in HubSpot
- Generate revenue for Banff

**Tier 1b - Former Client**
- Previously paying clients who have churned
- Maintained in system for potential re-engagement
- Still part of B4B network for introductions

**Tier 2 - Client Referral**
- Warm network referred by Tier 1 clients
- Not yet paying but high conversion potential
- May receive limited B4B introductions

**Tier 2b - 2nd Degree Referral**
- Extended network connections
- Lower priority for outreach

**Tier 3 - Advisor Network** (4,769 people)
- Executives added by "Exact Growth" team through manual research
- Warm contacts but no direct relationship yet
- Supply side for B4B matching (can be submitted to pipelines/trending)
- LinkedIn profiles synced to keep data fresh for B4B partners
- **Pain point**: Manual tagging and data entry to build this database

**Tier 4 - Partner Referral**
- Referred by B4B partners (search firms, investors)
- Potential future clients or network additions

**Tier 5 - Research**
- Cold prospects identified through research
- Lowest priority for engagement

**Critical Workflow Note:**
When a new client signs, Client Services (Max/Lily) must manually change their tier from 3 → 1 in three places:
1. HubSpot (triggers WhaleSync to Notion)
2. Contender (enables full client service features)
3. Google Drive (create client folder)

---

## Tab 1: HOME - Activity Dashboard

### **What It Shows**
Central command center showing real-time activity across all workflows.

### **Key Sections**

**1. My Tasks / Upcoming / Overdue / Completed**
- Task management for Client Services team (Max, Lily, Amanda) and Executive Advisors (David, Clare, Lauren, Olivia)
- Tasks like: "Trend Jose Resendiz," "Jay Collins PE list," "Chantal Rapport NE's"
- Shows workflow coordination between Client Services and Executive Advisors

**2. New Executives (73 in last 30 days)**
- Recent additions to network (Rani Johnson - CIO Workday, Abhi Chakraborty - CFO SellersFi, etc.)
- Shows B4B network growth velocity

**3. Scheduled Intros**
- Tomorrow's scheduled trending campaigns and P2P intros
- Example: "Carlos Minetti → Team Board Advisory Services - NYSE"
- Proves scheduled automation system exists

**4. Contender Activity Feed**
- Real-time log of all system actions:
  - "Rani Johnson introduced to Nicole North, Team Talent - Lightspeed"
  - "Amanda Chi created Infrastructure Services executives pipeline"
  - "Sarah Blanchard requested intro with Raj Bagchi"
  - "Added to (Evergreen) CIOs pipeline"

### **What This Reveals About Banff**
- **High-volume operation**: 100+ activities logged per day
- **Two workflows running in parallel**: Exec advisory (P2P intros) + B4B (pipeline submissions)
- **Role separation**: Amanda (Client Services) creates pipelines, Executive Advisors handle P2P relationship management, Kayla/Amanda manage B4B matching operations

---

## Tab 2: TASKS - Workflow Management

### **What It Shows**
All client service tasks organized by team member, client, status, and due date.

### **Task Types by Phase**

#### **Onboarding Tasks (New Client)**
- "Complete client setup across Notion, HubSpot & Contender"
- "Client folder created in Google Drive"
- "Add Background Deep Dive form responses to Contender profile"
- "Add kickoff date to HubSpot & Contender"
- "Conduct post-kickoff debrief"
- "Add compensation to tracker if provided"
- "Send welcome email to client"

#### **Narrative Development Tasks**
- "Update profile with highlights, about & interests"
- "Share narrative edits with client for review"
- "Update LinkedIn, resume, bio or highlights"
- "Ensure client updates LinkedIn profile (if applicable)"
- "Inform B4B/Executive Advisor that the client is ready to be shared"

#### **Ongoing Service Tasks**
- "Send P2Ps" (Peer-to-Peer introductions)
- "Send Trending campaign"
- "Refresh account plan"
- "Collect external feedback"
- "Conduct Performance Diagnosis"
- "Check in with client for feedback on introductions"
- "Share 1-6 peer ideas for approval"

### **Task Ownership**
- **Max Ravech** (Client Services): Lead for trending campaigns, P2P curation, task management
- **Lily Tympanick** (Client Services): Onboarding, narrative edits, profile development
- **Amanda Chi** (Client Services): B4B pipeline management, campaign execution
- **Emma Lane**: Template task generator (batch-created tasks for multiple clients)
- **Samantha Lassoff** (External Executive Coach): Newer team member (full onboarding cycle for JP Durrios)

### **What This Reveals About Banff**
- **673 total tasks** in system (mix of active, overdue, completed)
- **Standardized service delivery**: Same task templates for all clients
- **4-system onboarding**: HubSpot, Notion, Contender, Google Drive (manual coordination)
- **No automation**: All tasks manually created and tracked

---

## Tab 3: PIPELINES - B4B Search Management

### **What It Shows**
2,197 active B4B searches from VC/PE firms and search firms looking for executives.

### **Pipeline Structure**

**Each pipeline has:**
- **Pipeline Name**: "Infrastructure Services executives," "CFO," "(Evergreen) CIOs"
- **Team**: "Team GTCR," "Team Talent - Lightspeed," "Team True Search"
- **Company Type**: Investor (VC/PE) vs. Search (executive search firm) vs. Corporate
- **Industry/Function Tags**: Energy, Fintech, CEO, Marketing, etc.
- **Candidate Count**: Number of execs submitted (0-79)
- **Intro Count**: Number of introductions made
- **Status**: Active, Proactive (evergreen), or Search (one-time)
- **Dates**: Created, Updated, Last Activity

### **Pipeline Categories**

**1. Evergreen Pipelines** (Proactive = Yes)
- "(Evergreen) CIOs"
- "(Evergreen) Energy"
- "(Evergreen) SaaS CFOs"
- Continuous matching, not time-bound

**2. Specific Searches** (One-time placements)
- "CFO, Trewstar"
- "CMO, Supergoop"
- "CEO, Confidential Consumer Digital"

**3. Thought Leader Networks** (Networking, not hiring)
- "SF thought leaders"
- "London thought leaders"
- "2026 Womens Leadership Dinner" (79 candidates!)

### **Key B4B Partners** (by pipeline volume)
- **Spencer Stuart**: 46 pipelines, 33 people
- **Russell Reynolds**: 53 pipelines, 42 people
- **Korn Ferry**: 30 pipelines, 28 people
- **Point72 Private Investments**: 36 pipelines, 27 people
- **TPG**: 24 pipelines, 13 people
- **Ontario Teachers' Pension Plan**: 17 pipelines, 13 people
- **Nyca Partners**: 17 pipelines, 12 people

### **What This Reveals About Banff**
- **B4B side is massive**: 2,197 active searches across 178 companies
- **Mix of investors + search firms**: 60% investor-led, 40% search firm-led
- **High-volume matching**: Some pipelines have 70+ candidates submitted
- **Amanda's manual work**: She creates most pipelines ("Amanda Chi created...")
- **Kayla's routing challenge**: Deciding which execs go to which of 2,197 pipelines

---

## Tab 4: TRENDING - Campaign Management

### **What It Shows**
3,239 trending campaigns - customized email blasts promoting executives to B4B partners.

### **Trending Structure**

**Two Views:**
1. **People View**: Lists executives ranked by intro potential
   - Sherry Ann Mohan (#1, 127 score, 22 industries, 28 functions)
   - Jose Resendiz (#2, 74 score, 23 industries, 22 functions)
2. **Campaigns View**: Lists all sent/scheduled campaigns
   - Phil Bishop - Custom - Scheduled today
   - Kaveri Camire - Custom - Published yesterday
   - Peter Jackson - Bi-Weekly - Published yesterday

### **Campaign Types**
- **Bi-Weekly**: Automated recurring campaigns for active job seekers
- **Custom**: One-off targeted campaigns (5-15 specific teams)

### **Campaign Status**
- **Scheduled**: Queued to send (e.g., tomorrow 7 PM)
- **Published**: Already sent to B4B partners

### **Executive Advisor Assignment**
- **DA** (David Boehmer - Founder/CEO): Majority of Tier 1 clients
- **OL** (Olivia Barth - Executive Advisor): Secondary portfolio
- **CL** (Clare Buxton - Executive Advisor): Smaller portfolio
- **LA** (Lauren Mello - Executive Advisor, Brand Strategy): Specialized clients

### **What This Reveals About Banff**
- **3,239 campaigns total** - massive volume
- **Max's 20-30 min per campaign** makes sense (filtering 300+ teams manually)
- **Bi-weekly automation exists** but custom campaigns are manual
- **Trending = primary B4B matching mechanism**

---

## Tab 5: PEER TO PEER - Executive Networking

### **What It Shows**
2,279 P2P introductions between Banff executive clients (not B4B, exec-to-exec networking).

### **P2P Structure**

**Intro Stages:**
1. **Approved**: Client Services (Max/Lily) curated match, Executive Advisor approved (e.g., Tejas Shah → Sundeep Jain)
2. **Scheduled**: Intro email scheduled to send (e.g., Jeff Capone → Sean Cantrell, Dec 15)
3. **Introduced**: Email sent, awaiting connection (e.g., Carrie Wheeler → Laura Miele)

**Match Examples:**
- Tejas Shah (SVP Sales Transformation, Fluence) → Sundeep Jain (Former CPO, Uber)
- Carrie Wheeler (Former CEO, Opendoor) → Laura Miele (President, EA)
- Ana Mendy (VP PayPal) → Denise Leonhard (Zelle GM)

### **What This Reveals About Banff**
- **P2P is exec-side service** (not B4B job matching)
- **2,279 total intros** = high-value networking service
- **Manual curation**: Client Services (Max) suggests matches, Executive Advisors approve
- **Zero automated tracking** (the pain point from discovery calls)

---

## Tab 6: PERFORMANCE - Client Dashboard

### **What It Shows**
Client performance tracking across quarterly activity metrics.

### **"Clients In the Red"**
Executives approaching quarter-end with zero facilitated introductions.

**Examples:**
- Casey Klyszeiko (Fiserv): 4 days until quarterly, 0 intros, 2 P2P
- Tricia Alcamo (FanDuel): 7 days until quarterly, 0 intros
- Ben Walter (JPMorgan): 7 days until quarterly, 3 intros, 2 P2P

### **Client Performance Metrics**

**For each client, Contender tracks:**
1. **Rank**: Relative performance (#1 = David Klein with 75 score)
2. **Score**: Composite engagement metric
3. **Facilitated Intros**: B4B introductions (pipelines + trending)
4. **P2P Intros**: Peer-to-peer executive connections
5. **Requests**: Client-initiated asks
6. **Program**: Active Job Seeker, Passive Job Seeker, Network Builder, Aspiring Board Member, New Role Leader

**Top Performers:**
1. David Klein - 75 score, 5 facilitated, 10 P2P, 10 requests
2. Lex Bayer - 1 score, 3 facilitated, 4 P2P
3. Adrienne Coulson - 50 score, 7 facilitated, 8 P2P

### **Quarterly Tracking**
- **Upcoming Quarterlies**: 10 clients
- **Recently Past Quarterlies**: 18 clients
- Used for quarterly report generation (Max's "riddled with bad data" pain point)

### **What This Reveals About Banff**
- **Data-driven client service**: Tracking every intro, request, and touchpoint
- **Quarterly reporting is core deliverable**: Hence the performance dashboard
- **Max's cross-referencing problem**: Data in Contender doesn't match Notion/HubSpot, requiring manual validation
- **Red flag system**: Proactively identifies clients not getting value

---

## Tab 7: PEOPLE - Executive Database

### **What It Shows**
4,981 people in Contender (mix of Tier 1 executives, Tier 3 network, B4B contacts).

### **Person Profile Structure**

**Example: Jay Cipriano (EVP, SEI)**

#### **Personal Information**
- Full Name, LinkedIn URL, Email, Phone
- Tier: 1 - Executive Client
- **Advisor: David Boehmer** (Executive Advisor - relationship owner)
- **Client Owner: Max Ravech** (Client Services - operational lead)
- Kickoff Date: Jun 26, 2024
- Client Program: Passive Job Seeker
- Referred by: Todd Taylor
- Currently wants intros: Yes
- Pipeline introduction email setting: Manual

#### **Professional Information**
- Headline Role: Executive Vice President and Head of SEI's Institutional business
- Headline Company: SEI
- Industry Expertise: Financial Services
- Functional Expertise: General Management, Other
- Target Industries: Financial Services
- Target Functions: CEO, General Management, Operations
- Operating Role Interest: Passively Seeking
- Board / Advisory Role Interest: Passively Seeking
- Additional Notes: "Open to relocation to a major city in Europe"

#### **Networking Interests**
- Professional: Angel and VC Investing, AI and ML, Education, Entrepreneurship, Private Equity Operating, Disruptive Technology
- Personal: Travel, Outdoor Activities, Gaming, Media, Music, Sports, Academia, Film

#### **Off-Limits**
- Companies: (none for Jay)
- People: Existing Relationship - Todd Taylor, Heidrick & Struggles

#### **LinkedIn Profile Sync**
- Stores full LinkedIn profile data in Contender
- Updated: Apr 19, 2025, 2:21 AM
- Shows Jay's full experience history, education, bio

### **What This Reveals About Banff**
- **Rich candidate profiles**: Far beyond basic CRM data
- **LinkedIn auto-updater exists**: Syncs LinkedIn data to Contender
- **Problem: LinkedIn auto-updater overwrites manual edits** (Amanda's pain point - doesn't add "former" to job titles)
- **Off-limits tracking**: Prevents conflicts of interest
- **Manual email settings**: "Manual" vs auto-send for pipeline intros

---

## Tab 8: COMPANIES - B4B Partner Database

### **What It Shows**
178 B4B companies (investors, search firms, corporate partners).

### **Company Structure**

**Example: ZRG Partners (Search Firm)**
- **Company Name**: ZRG Partners
- **Members**: 4 people (Holly Dobson, Justin Pinchback, Kiel Towns, Tanja Iannarelli)
- **Teams**: 5 (each person has their own "Team")
  - Team Holly Dobson - ZRG Partners
  - Team James Macedonio - ZRG Partners
  - Team Justin Pinchback - ZRG
  - Team Kiel Towns - ZRG Partners
  - Team Michelle Dunne - ZRG Partners

**Company Types:**
- **Premium Investor**: VC/PE firms (VMG Partners, TPG, Lightspeed, Ontario Teachers)
- **Premium Search**: Executive search firms (True Search, Spencer Stuart, Russell Reynolds, Korn Ferry)
- **Premium Corporate**: Operating companies looking for talent (Peloton, NewRez)

**Key Stats:**
- **True Search**: 36 pipelines, 29 people
- **Spencer Stuart**: 46 pipelines, 33 people
- **TPG**: 24 pipelines, 13 people
- **Point72 Private Investments**: 36 pipelines, 27 people

### **What This Reveals About Banff**
- **"Team" = individual recruiter/investor at B4B partner firm**
- **One company → many teams**: TPG has multiple teams (Human Capital - TPG, Team TMT - GTCR)
- **Search firms dominate by volume**: Spencer Stuart (46 pipelines) vs. typical investor (5-10 pipelines)
- **Premium status**: All companies marked "Premium" - likely paid partners

---

## Data Flow: How Banff Works End-to-End

### **1. EXECUTIVE ONBOARDING (Exec Side)**

```
TSQ Contract Signed
    ↓
Manual Entry (Client Services - Max/Lily)
    ↓
HubSpot (billing, tier, Executive Advisor assignment)
    ↓
WhaleSync Auto-Sync
    ↓
Notion (client page created)
    ↓
Manual Entry (Client Services - Max/Lily)
    ↓
Contender (profile, kickoff date, program)
    ↓
Manual (Client Services - Max/Lily)
    ↓
Google Drive (client folder)
    ↓
Tasks Auto-Created in Contender
    ↓
Executive Advisor Kickoff Call (David/Clare/Lauren/Olivia)
    ↓
Narrative Development by Client Services (LinkedIn, resume, bio)
    ↓
"Client ready to be shared" with B4B
```

### **2. B4B MATCHING (B4B Side)**

#### **A. Trending Campaigns (Proactive)**
```
Client Services (Max) decides to trend an executive
    ↓
Manually filters 300+ teams by industry/function
    ↓
Selects 5-15 target teams
    ↓
Custom trending campaign created in Contender
    ↓
Scheduled for "tomorrow 7 PM"
    ↓
Email sent to B4B partners
    ↓
B4B partner clicks "Request Intro"
    ↓
Intro status tracked in Contender
    ↓
Manual follow-up by Client Services (Max/Amanda)
```

#### **B. Pipeline Submissions (Reactive)**
```
B4B partner requests pipeline (e.g., "CFO for portfolio co")
    ↓
Client Services (Amanda) creates pipeline in Contender
    ↓
Client Services/B4B Lead (Amanda/Kayla) manually search Contender for matches
    ↓
Check HubSpot for relationship warmth
    ↓
Check LinkedIn for profile freshness
    ↓
Manually check for duplicates
    ↓
Submit 5-10 candidates to pipeline
    ↓
B4B partner reviews candidates
    ↓
Requests intro for 2-3 candidates
    ↓
Intro facilitated, tracked in Contender
```

### **3. P2P INTRODUCTIONS (Exec Side)**

```
Client Services (Max) identifies potential peer match
    ↓
Checks both execs' interests/goals in Contender
    ↓
Creates P2P entry in Contender
    ↓
Status: "Approved" by Executive Advisor
    ↓
Intro email drafted manually by Client Services
    ↓
Scheduled to send (e.g., "in 6 days")
    ↓
Email sent
    ↓
Status: "Introduced"
    ↓
NO FOLLOW-UP TRACKING (pain point)
```

### **4. QUARTERLY REPORTING**

```
End of quarter approaching
    ↓
Client Services (Max) pulls data from Contender (facilitated intros, P2P intros, requests)
    ↓
Cross-references Notion (meeting notes, tasks)
    ↓
Cross-references HubSpot (billing, tier, dates)
    ↓
Manually validates data accuracy (5-10 min per report)
    ↓
Generates quarterly report
    ↓
Executive Advisor reviews (David/Clare/Lauren/Olivia)
    ↓
Sends to client
```

---

## Key Relationships Between Tabs

### **Home ↔ Tasks**
- Home shows upcoming tasks
- Tasks show full task database
- Tasks auto-created from templates

### **Pipelines ↔ Trending**
- Trending = proactive outreach to B4B partners
- Pipelines = reactive responses to B4B requests
- Both track introductions to same B4B companies

### **People ↔ Performance**
- People = profile data
- Performance = activity metrics over time
- Performance pulls from People + Pipelines + Trending + Peer to Peer

### **Companies ↔ Pipelines**
- Companies = B4B partner organizations
- Each company has multiple "Teams"
- Each team has multiple pipelines

### **People ↔ Peer to Peer**
- P2P only includes people with Tier = "1 - Executive Client"
- Uses networking interests to suggest matches
- Tracked separately from B4B introductions

---

## Pain Points Visible in Data Structure

### **1. Cross-System Manual Entry** (Client Services Team)
- Client Services (Max/Lily/Amanda) manually enter data in HubSpot, then Notion, then Contender, then Google Drive
- WhaleSync only handles HubSpot → Notion
- Contender isolated from automation

### **2. LinkedIn Auto-Updater Issues** (Client Services - Amanda)
- LinkedIn profile sync overwrites manual "former" tags
- Creates "stale profile" incidents with B4B partners

### **3. No P2P Follow-Up Tracking** (Client Services - Max)
- P2P status stuck at "Introduced"
- No Day 7/14 reminder system
- Outcome tracking missing for quarterly reports

### **4. Pipeline Deduplication** (Client Services - Amanda)
- Must manually check if candidate already submitted to pipeline
- No API validation before submission
- 5-7 min per submission

### **5. Trending Campaign Manual Filtering** (Client Services - Max)
- 20-30 min to filter 300+ teams per campaign
- No AI suggestions based on candidate profile
- Pure manual selection

### **6. Quarterly Report Data Validation** (Client Services - Max)
- Contender data doesn't match Notion or HubSpot
- 5-10 min per report to cross-reference
- "Riddled with bad data" - Max's exact quote

### **7. Zoom Transcript Tagging** (Client Services - Max)
- Zapier dumps transcripts to Notion automatically
- No auto-tagging to client profile
- 5-6 hrs/week manual sorting

---

## Automation Opportunities (Based on Data Structure)

### **Home Tab**
- **Activity feed** shows webhook potential for real-time notifications
- **Scheduled intros** prove automation scheduler exists

### **Tasks Tab**
- **Template-based task creation** already exists
- Could auto-create from HubSpot deal stage changes

### **Pipelines Tab**
- **API endpoints exist** for pipeline creation, candidate submission
- Could auto-suggest candidates using AI + Contender filters

### **Trending Tab**
- **Campaign scheduling** already exists
- Could auto-select teams using AI based on candidate profile

### **Peer to Peer Tab**
- **Intro tracking** infrastructure exists
- Could add automated follow-up reminders

### **Performance Tab**
- **Data aggregation** from all tabs
- Could auto-generate quarterly reports with validated data

### **People Tab**
- **LinkedIn sync** already exists
- Could add "former" tag logic to auto-updater

### **Companies Tab**
- **Team structure** maps to API `/api/v1/teams/find`
- Could auto-match candidates to teams

---

## Summary: Banff's Contender Workflow

**Contender is Banff's central nervous system for:**

1. **Client Management**: 4,981 people (212 Tier 1 execs + 4,769 Tier 3 network)
2. **B4B Matching**: 2,197 pipelines across 178 companies
3. **Trending Campaigns**: 3,239 campaigns promoting execs to B4B partners
4. **P2P Networking**: 2,279 executive-to-executive introductions
5. **Performance Tracking**: Quarterly metrics for client reporting
6. **Task Management**: 673 tasks coordinating Client Services and Executive Advisor workflows

**The system works BUT:**
- Heavy manual data entry (4 systems: HubSpot → Notion → Contender → Google Drive)
- No automated deduplication (Amanda's pain point)
- No P2P follow-up tracking (Max's pain point)
- No AI-assisted matching (Kayla's "machine falls apart" pain point)
- No auto-tagging for Zoom transcripts (Max's 5-6 hrs/week pain point)
- Bad data in quarterly reports (Max's 5-10 min per report pain point)

**The API discovery changes everything:**
With Contender's full REST API, all 6 pain points can be automated using Make.com + AI.
