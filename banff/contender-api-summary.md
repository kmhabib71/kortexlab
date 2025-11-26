# Contender API - What You Need to Know (Simple Summary)

## DON'T READ THE 32,000 LINE JSON. Read This Instead.

Amanda sent you Contender's OpenAPI specification. Here's what matters:

---

## ✅ GOOD NEWS: Contender HAS a Full API

**Authentication:** OAuth2 (standard, easy to integrate with Make.com)

**Base URL:** Their domain + `/api/v1/`

**Format:** REST API with JSON responses

---

## Key API Endpoints (What You Can Automate)

### 📋 **Candidates (Executive Profiles)**

**What you can do:**
- ✅ Search candidates: `GET /api/v1/candidates/find`
- ✅ Filter candidates: `POST /api/v1/candidates/filter`
- ✅ Get candidate details: `GET /api/v1/candidates/{candidate_uuid}`
- ✅ Update candidate: `PATCH /api/v1/candidates/{candidate_uuid}`
- ✅ Upload resume: `POST /api/v1/candidates/{candidate_uuid}/resume`
- ✅ Update image: `POST /api/v1/candidates/{candidate_uuid}/image`
- ✅ Import candidates: `POST /api/v1/candidates/import`

**For your roadmap:**
- Client onboarding: Auto-create candidate profiles ✅
- Profile updates: Sync LinkedIn data ✅
- Bulk uploads: Network growth automation ✅

---

### 🤝 **Introductions & Recommendations**

**What you can do:**
- ✅ Get introductions: `GET /api/v1/introductions/{recommendation_uuid}`
- ✅ Update intro status: `PATCH /api/v1/introductions/{recommendation_uuid}`
- ✅ Get recommendations: `GET /api/v1/recommendations/find`
- ✅ Create recommendation: `POST /api/v1/recommendations`
- ✅ Share recommendations: `POST /api/v1/share/recommendations`
- ✅ Track feedback: `POST /api/v1/candidates/{candidate_uuid}/feedback`

**For your roadmap:**
- P2P intro tracking: Full automation possible ✅
- B4B intro tracking: 5-7 min manual → automated ✅
- Follow-up reminders: Track intro status via API ✅

---

### 🏢 **Teams (B4B Partners)**

**What you can do:**
- ✅ List teams: `GET /api/v1/teams`
- ✅ Find teams: `GET /api/v1/teams/find`
- ✅ Get team details: `GET /api/v1/teams/{team_slug}`
- ✅ Get team pipelines: `GET /api/v1/teams/{team_slug}/pipelines`
- ✅ Get team activity: `GET /api/v1/home/teams/{team_uuid}/activity`

**For your roadmap:**
- Trending campaigns: Auto-select teams based on candidate profile ✅
- Smart routing: "The Machine" automation fully possible ✅
- Partner matching: AI + API = automated suggestions ✅

---

### 📊 **Pipelines (B4B Searches)**

**What you can do:**
- ✅ List pipelines: `GET /api/v1/pipelines/find`
- ✅ Get pipeline details: `GET /api/v1/pipelines/{pipeline_slug}`
- ✅ Get team pipelines: `GET /api/v1/teams/{team_slug}/pipelines`
- ✅ Submit to pipeline: `POST /api/v1/submissions/pipelines`

**For your roadmap:**
- Pipeline filling: Automate candidate submission ✅
- Amanda's deduplication: Check via API before adding ✅
- Kayla's routing: Auto-schedule pipeline submissions ✅

---

### 🏢 **Companies**

**What you can do:**
- ✅ Search companies: `GET /api/v1/companies/find`
- ✅ Get company details: `GET /api/v1/companies/{company_slug}`
- ✅ Get company members: `GET /api/v1/companies/{company_slug}/members`

**For your roadmap:**
- Target company mapping: Automate research ✅
- Off-limits checking: API validation ✅

---

### 👥 **People (Advisors, Team Members)**

**What you can do:**
- ✅ Get current user: `GET /api/v1/people/current`
- ✅ Find people: `GET /api/v1/people/find`
- ✅ Get advisors: `GET /api/v1/people/advisors`

**For your roadmap:**
- Task assignment: Know who's who via API ✅
- Cross-team visibility: See who talked to whom ✅

---

### 📅 **Scheduled Jobs (Trending Campaigns)**

**What you can do:**
- ✅ Trending schedule: `GET /api/v1/trending_schedule`
- ✅ Scheduled intros: `GET /api/v1/jobs/scheduled_intros`
- ✅ Scheduled P2P intros: `GET /api/v1/jobs/scheduled_p2p_intros`
- ✅ Auto introductions: `GET /api/v1/jobs/auto_introductions`

**For your roadmap:**
- Trending campaigns: Can read/write schedules ✅
- "The Machine": Automated scheduling fully possible ✅

---

## 🎯 What This Means for Friday's Roadmap

### **OLD PLAN (Before API Spec):**
> "Contender has limited API, we'll use Retool workaround"

### **NEW PLAN (With API Spec):**
> "Contender has full REST API with 50+ endpoints. Direct integration possible for:"
> - ✅ Client onboarding (create profiles via API)
> - ✅ P2P intro tracking (full CRUD via API)
> - ✅ B4B intro tracking (eliminate 5-7 min manual entry)
> - ✅ Trending campaigns (auto-select teams, schedule via API)
> - ✅ "The Machine" (smart routing with API automation)
> - ✅ Profile updates (sync LinkedIn via API)

---

## 🔑 What You Tell David Friday

**OLD:**
> "Contender doesn't have an API, so we'll work around it using Retool as an intermediary for some automations."

**NEW:**
> "Great news - Contender has a comprehensive REST API with OAuth2 authentication. Amanda provided the OpenAPI spec with 50+ endpoints. We can integrate directly for client onboarding, intro tracking, trending campaigns, and network routing. No workarounds needed - full automation is possible."

---

## 📋 How to Use This in Week 2

**You DON'T need to:**
- ❌ Read the 32,000 line JSON
- ❌ Memorize every endpoint
- ❌ Build anything this week

**You DO need to:**
- ✅ Know API exists (it does!)
- ✅ Know key capabilities (candidates, intros, teams, pipelines)
- ✅ Tell David "full integration possible"
- ✅ In Week 2, use Make.com's "HTTP Request" module with these endpoints

---

## 🛠️ Week 2 Technical Approach

**Make.com Integration:**
1. Get OAuth2 token from Contender API (`/api/v1/token`)
2. Use "HTTP Request" module in Make.com scenarios
3. Call endpoints like:
   - `POST /api/v1/candidates/import` (onboarding)
   - `GET /api/v1/recommendations/find` (intro tracking)
   - `POST /api/v1/share/recommendations` (trending campaigns)

**Authentication:**
- Amanda will provide OAuth2 credentials
- Store token in Make.com data store
- Refresh when expired (standard OAuth2 flow)

---

## ✅ Update Your Roadmap NOW

**In friday-grand-roadmap-for-david.md, change:**

### Technology Stack Section:

**OLD:**
```
| **Contender** | ⚠️ Limited API | Use Retool as intermediary |
```

**NEW:**
```
| **Contender** | ✅ Full REST API | Direct Make.com integration via OAuth2 |
```

### Contender Strategy Section:

**DELETE THIS:**
> "Contender has limited API access. We'll use Retool as intermediary..."

**REPLACE WITH:**
> "Contender has a comprehensive REST API (OpenAPI spec provided by Amanda):
> - 50+ endpoints for candidates, introductions, teams, pipelines
> - OAuth2 authentication (standard integration)
> - Direct Make.com integration via HTTP modules
> - Full CRUD operations available
>
> This means ALL automations can integrate directly with Contender:
> - Client onboarding: Auto-create profiles via `/api/v1/candidates/import`
> - P2P tracking: Full intro lifecycle via `/api/v1/introductions` endpoints
> - Trending campaigns: Auto-scheduling via `/api/v1/trending_schedule`
> - Network routing: Smart suggestions using `/api/v1/teams/find`"

---

## 🎉 Bottom Line

**You worried:** "Contender has no API, how do we automate?"

**Reality:** Contender has a FULL, comprehensive REST API with everything you need.

**For Friday:** Confidently say "Direct Contender integration is possible for all automations."

**For Week 2:** Use Make.com HTTP modules to call these endpoints.

**You're golden.** 🎯

---

## Quick Reference: Key Endpoints by Use Case

| Use Case | Endpoint | Method |
|----------|----------|--------|
| Create candidate profile | `/api/v1/candidates/import` | POST |
| Search candidates | `/api/v1/candidates/find` | GET |
| Get intro details | `/api/v1/introductions/{uuid}` | GET |
| Update intro status | `/api/v1/introductions/{uuid}` | PATCH |
| Find teams | `/api/v1/teams/find` | GET |
| Submit to pipeline | `/api/v1/submissions/pipelines` | POST |
| Get trending schedule | `/api/v1/trending_schedule` | GET |
| Share recommendations | `/api/v1/share/recommendations` | POST |

**You don't need more than this for Friday's presentation.**
