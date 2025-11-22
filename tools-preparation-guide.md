# Tools Preparation Guide for Kortex Labs Meeting

## 1. HubSpot (CRM Platform)

### What It Is
Customer Relationship Management (CRM) - tracks leads, deals, contacts, companies, and sales pipeline.

### Key Concepts
| Term | Meaning |
|------|---------|
| **Contact** | A person (name, email, phone) |
| **Company** | A business (can have multiple contacts) |
| **Deal** | A potential sale (has stages: New → Qualified → Proposal → Closed Won/Lost) |
| **Pipeline** | Visual stages a deal moves through |
| **Workflow** | Automated actions (if X happens, do Y) |
| **Properties** | Custom fields on contacts/deals/companies |

### HubSpot API Basics
```
Base URL: https://api.hubapi.com

Authentication: Bearer token (API key or OAuth)

Common Endpoints:
- GET /crm/v3/objects/contacts - List all contacts
- POST /crm/v3/objects/contacts - Create contact
- GET /crm/v3/objects/deals - List all deals
- POST /crm/v3/objects/deals - Create deal
- PATCH /crm/v3/objects/deals/{id} - Update deal stage
```

### What You'll Likely Build
- Sync deals to Notion/Google Sheets when stage changes
- Auto-create tasks when deal closes
- Trigger notifications on new leads
- Pull deal data for dashboards

### Quick Links
- API Docs: https://developers.hubspot.com/docs/api/overview
- Deals API: https://developers.hubspot.com/docs/api/crm/deals
- Workflows: https://developers.hubspot.com/docs/api/automation/workflows

---

## 2. Notion (Documentation/Wiki/Database)

### What It Is
All-in-one workspace - docs, databases, wikis, project tracking. Clients use it for SOPs, client info, task management.

### Key Concepts
| Term | Meaning |
|------|---------|
| **Page** | A document (can contain text, databases, embeds) |
| **Database** | A table with properties (like spreadsheet) |
| **Block** | Everything in Notion is a block (paragraph, heading, image) |
| **Property** | Column in a database (text, date, select, relation) |
| **Relation** | Link between two databases |

### Notion API Basics
```
Base URL: https://api.notion.com/v1

Authentication: Bearer token (Integration token)
Header: Notion-Version: 2022-06-28

Common Endpoints:
- GET /databases/{id}/query - Get database items
- POST /pages - Create a page/database row
- PATCH /pages/{id} - Update a page
- GET /blocks/{id}/children - Get page content
```

### What You'll Likely Build
- Create client pages automatically when deal closes
- Sync HubSpot contacts → Notion database
- Update project status from external triggers
- Generate reports in Notion

### Quick Links
- API Docs: https://developers.notion.com/
- Database Query: https://developers.notion.com/reference/post-database-query

---

## 3. Retool (Internal Tools Builder)

### What It Is
Low-code platform to build internal dashboards, admin panels, and tools quickly. Connects to APIs and databases.

### Key Concepts
| Term | Meaning |
|------|---------|
| **App** | A dashboard/tool you build |
| **Component** | UI element (table, button, form, chart) |
| **Query** | Data fetch from API/database |
| **Resource** | Connection to external service (API, DB) |
| **Transformer** | JavaScript to transform data |

### How It Works
1. Connect data sources (HubSpot API, PostgreSQL, Google Sheets)
2. Drag-drop UI components
3. Write queries to fetch/update data
4. Bind components to query results
5. Deploy for team use

### What You'll Likely Build
- Client dashboard showing all deals/status
- Admin panel to manage client data
- Reporting tool pulling from multiple sources
- Internal ops tools for the team

### Quick Links
- Docs: https://docs.retool.com/
- API Integration: https://docs.retool.com/docs/apis

---

## 4. Google Workspace APIs

### Key APIs You'll Use

| API | Purpose |
|-----|---------|
| **Sheets API** | Read/write spreadsheets |
| **Drive API** | Create/manage files and folders |
| **Gmail API** | Send emails, read inbox |
| **Calendar API** | Create events, check availability |

### Google Sheets API Basics
```
Base URL: https://sheets.googleapis.com/v4/spreadsheets

Authentication: OAuth 2.0 or Service Account

Common Operations:
- GET /{spreadsheetId}/values/{range} - Read cells
- PUT /{spreadsheetId}/values/{range} - Write cells
- POST /{spreadsheetId}/values/{range}:append - Add rows
```

### What You'll Likely Build
- Sync HubSpot deals → Google Sheet for reporting
- Auto-create folders for new clients
- Send automated emails on triggers
- Calendar booking integrations

### Quick Links
- Sheets API: https://developers.google.com/sheets/api
- Drive API: https://developers.google.com/drive/api

---

## 5. Automation Platforms (n8n / Make / Zapier)

### Comparison
| Platform | Best For | Pricing |
|----------|----------|---------|
| **Zapier** | Simple automations, non-technical users | Expensive |
| **Make** | Complex multi-step workflows, visual | Mid-price |
| **n8n** | Self-hosted, unlimited, technical users | Free (self-host) |

### Key Concepts
| Term | Meaning |
|------|---------|
| **Trigger** | Event that starts workflow (new row, webhook, schedule) |
| **Action** | What happens (create record, send email, call API) |
| **Webhook** | URL that receives data from external services |
| **Filter** | Condition to continue or stop workflow |

### What You'll Likely Build
- HubSpot deal closed → Create Notion page → Send Slack message → Add to Google Sheet
- Daily report generation
- Client onboarding automation sequence

---

## 6. Webhooks (Critical Concept)

### What It Is
A URL that receives data when something happens. Instead of constantly checking "did anything change?", the system pushes data to you.

### How It Works
```
1. You create endpoint: https://yourserver.com/webhook/hubspot
2. Tell HubSpot: "When deal closes, POST to this URL"
3. HubSpot sends JSON data to your URL
4. Your code processes it and takes action
```

### Example Webhook Payload (HubSpot Deal)
```json
{
  "dealId": "123456",
  "properties": {
    "dealname": "Banff Advisors Contract",
    "amount": "50000",
    "dealstage": "closedwon"
  }
}
```

---

## Quick Reference: Common Integration Patterns

### Pattern 1: CRM → Documentation
```
HubSpot Deal Closes
  → Webhook triggers
  → Create Notion page with client info
  → Create Google Drive folder
  → Send welcome email
```

### Pattern 2: Data Sync
```
Every hour (scheduled):
  → Fetch all open deals from HubSpot
  → Update Google Sheet
  → Refresh Retool dashboard
```

### Pattern 3: Client Onboarding
```
New client in HubSpot
  → Create Notion workspace
  → Generate welcome docs
  → Assign tasks in project tool
  → Send automated emails (Day 1, 3, 7)
```

---

## Questions to Ask About Each Tool

### HubSpot
- What pipeline stages do you use?
- Any custom properties I should know?
- Do you use HubSpot workflows already?

### Notion
- How is your workspace structured?
- What databases do you want synced?
- Who needs access to what?

### Retool
- Do you have existing Retool apps?
- What dashboards do you need most urgently?
- Who will use these tools (technical or non-technical)?

### Google Workspace
- What sheets contain critical data?
- Any existing automations I should know about?
- Email templates you use frequently?

---

## Before the Meeting Checklist

- [ ] Understand what a CRM does (HubSpot)
- [ ] Know what Notion databases look like
- [ ] Watch 1-2 Retool tutorials (YouTube, 10 min each)
- [ ] Understand webhooks concept
- [ ] Know difference between Zapier/Make/n8n
- [ ] Have notepad ready for client workflow notes

---

## YouTube Tutorials to Watch (Quick)

| Tool | Search Term | Time Needed |
|------|-------------|-------------|
| HubSpot | "HubSpot CRM tutorial 2024" | 15 min |
| Notion API | "Notion API tutorial for beginners" | 10 min |
| Retool | "Retool tutorial build dashboard" | 15 min |
| n8n | "n8n automation tutorial" | 10 min |
| Webhooks | "What are webhooks explained" | 5 min |

---

## Common Terms Client Might Use

| They Say | They Mean |
|----------|-----------|
| "Sync" | Copy data from A to B automatically |
| "Trigger" | When X happens, do Y |
| "Pipeline" | Stages a deal/client moves through |
| "Handoff" | Transfer from one team/system to another |
| "Visibility" | Dashboard to see what's happening |
| "Manual work" | Copy-paste, data entry they hate doing |
| "At-risk client" | Client who might leave/cancel |
| "Onboarding" | Process when new client starts |
