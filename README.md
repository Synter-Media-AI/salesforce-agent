# Salesforce CRM MCP Starter Kit — Manage Salesforce with AI

[![MCP Compatible](https://img.shields.io/badge/MCP-compatible-blue)](https://modelcontextprotocol.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform: Salesforce](https://img.shields.io/badge/Platform-Salesforce-00A1E0)](https://www.salesforce.com)

**Connect enterprise sales data to your ad campaigns.** Open this repo in Amp, Cursor, or VS Code and query Salesforce opportunities, leads, and accounts with AI — then sync closed-won customers to ad platforms for account-based marketing.

---

## Why Salesforce + AI for Advertising?

Salesforce is the world's #1 CRM with 150,000+ enterprise customers. It holds the most valuable data for B2B advertising: which accounts are in your pipeline, which deals closed, what the contract value was, and how long the sales cycle took.

For enterprise B2B, this data transforms your advertising. Instead of targeting "people interested in enterprise software," you can target employees at the exact companies your sales team is pursuing. This is account-based marketing (ABM) — and Salesforce is the data foundation.

The challenge is getting Salesforce data *out* and *into* ad platforms. SOQL queries, OAuth tokens, field mapping, and data transformation make it a developer-heavy task. An AI agent handles the entire pipeline.

**Best for:** Enterprise B2B sales teams, ABM programs, companies with complex multi-touch sales cycles, syncing closed-won accounts to LinkedIn for lookalike targeting.

---

## Quick Start (30 Seconds)

### Amp / Cursor / VS Code (Copilot)

1. **Get a free API key** at [syntermedia.ai/developer](https://syntermedia.ai/developer)
2. **Set the key:**
   ```bash
   export SYNTER_API_KEY=syn_your_key_here
   ```
3. **Open this repo** in your editor
4. **Start chatting** — MCP tools are pre-configured in `.mcp.json`

### Claude Desktop

Copy `claude_desktop_config.json` to your Claude config directory and replace the API key:

- **macOS:** `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows:** `%APPDATA%\Claude\claude_desktop_config.json`

---

## What You Can Do

| Capability | Example |
|-----------|---------|
| **Pipeline Overview** | "Show me all opportunities closing this quarter, sorted by amount" |
| **ABM Account Lists** | "Export our Tier 1 target accounts to LinkedIn for matched audience targeting" |
| **Closed-Won Sync** | "Sync all closed-won accounts from last year to Google Customer Match" |
| **Lead Routing Analysis** | "Which lead source has the highest close rate?" |
| **Account Intelligence** | "Show me everything we know about Acme Corp — contacts, deals, activities" |
| **Pipeline Attribution** | "Which campaigns generated the most pipeline dollar value?" |
| **Revenue Reporting** | "What's our average deal size by industry?" |
| **Contact Enrichment** | "Find all contacts at Fortune 500 accounts with no recent activity" |
| **Churn Risk** | "Which customers haven't had a check-in call in 90+ days?" |
| **Offline Conversions** | "Send closed-won deals back to Google Ads and LinkedIn for conversion attribution" |

---

## Example Conversations

### 1. Account-Based Marketing with LinkedIn

> **You:** Our sales team identified 200 target accounts. I want to run LinkedIn Ads specifically to employees at these companies.
>
> **Agent:** I'll extract the account data from Salesforce and build a LinkedIn ABM campaign. Let me pull your target accounts...
>
> Found 200 accounts with the tag "Tier 1 Target." Here's the breakdown:
> - Enterprise (5000+): 78 accounts
> - Mid-Market (500-4999): 89 accounts
> - Growth (100-499): 33 accounts
>
> **What I'll do:**
> 1. Export company names and domains from Salesforce
> 2. Upload to LinkedIn as a Matched Audience (expected 80-85% match rate)
> 3. Layer targeting: Decision-makers only (Director+ in IT, Engineering, or Procurement)
> 4. Recommended campaign structure:
>    - **Tier 1 (78 enterprise accounts):** Higher budget, thought leadership content
>    - **Tier 2 (89 mid-market):** Product-focused content, demo CTAs
>    - **Tier 3 (33 growth):** Self-serve trial CTAs
>
> **You:** Just do Tier 1 for now. $3,000/month budget.
>
> **Agent:** Uploaded 78 accounts to LinkedIn — 67 matched (86%). Created campaign targeting Director+ at matched accounts. With an audience of ~8,400 professionals, $3,000/month will deliver ~4-6 impressions per person per month — perfect for ABM awareness saturation.

### 2. Offline Conversion Import for Campaign Attribution

> **You:** My Google Ads reports show 50 conversions this quarter, but Salesforce shows 30 closed-won deals. Why the discrepancy?
>
> **Agent:** The discrepancy is because Google Ads tracks online conversions (form fills, demo requests) while Salesforce tracks closed revenue. These are different stages in your funnel.
>
> **The fix: Offline Conversion Import.** I'll send your Salesforce closed-won deals back to Google Ads so it can see which ad clicks eventually led to revenue.
>
> **How it works:**
> 1. Export closed-won opportunities from Salesforce with the original lead's GCLID (Google Click ID)
> 2. Upload to Google Ads as offline conversions with deal value and close date
> 3. Google Ads attributes revenue back to the original campaign, ad group, and keyword
>
> **Impact:** Instead of optimizing for "demo requests" (which may or may not close), Google Ads can optimize for "closed-won revenue." This shifts budget toward keywords that generate revenue, not just leads.
>
> **Your data shows:**
> - "Enterprise data platform" generated 8 demo requests but only 1 deal ($45K)
> - "Data analytics for healthcare" generated 3 demo requests and 3 deals ($180K)
> - Without offline conversion import, Google Ads would allocate more budget to the first keyword. With it, Google correctly identifies the healthcare keyword as 4x more valuable.

### 3. Pipeline Forecasting for Budget Planning

> **You:** I need to plan next quarter's ad budget. What does the pipeline look like?
>
> **Agent:** Let me analyze your Salesforce pipeline and historical close rates...
>
> **Q3 Pipeline Summary:**
> | Stage | Opportunities | Total Value | Weighted Value | Avg Close Rate |
> |---|---|---|---|---|
> | Prospecting | 45 | $2.7M | $270K | 10% |
> | Qualification | 28 | $2.1M | $630K | 30% |
> | Proposal | 14 | $1.4M | $840K | 60% |
> | Negotiation | 8 | $960K | $768K | 80% |
> | **Total Pipeline** | **95** | **$7.16M** | **$2.51M** | — |
>
> **Budget recommendation based on pipeline data:**
> - You need 45 new opportunities per quarter to maintain growth (based on last 4 quarters)
> - Your cost per opportunity from ads is $420 (from Salesforce source tracking)
> - Required ad budget: $420 × 45 = **$18,900/month**
>
> **Channel allocation (based on close rates by source):**
> | Channel | Pipeline Created | Close Rate | Budget Allocation |
> |---|---|---|---|
> | Google Ads | $3.2M | 22% | $8,000/month |
> | LinkedIn Ads | $2.8M | 28% | $7,000/month |
> | Content Syndication | $1.1M | 12% | $3,900/month |
>
> LinkedIn generates smaller pipeline but closes at a higher rate. Worth the premium CPCs.

### 4. Customer Churn Risk and Retention Advertising

> **You:** Which customers are at risk of churning? Can we use ads to save them?
>
> **Agent:** Pulling customer health signals from Salesforce...
>
> **At-risk customers (21 accounts, $1.8M ARR):**
>
> | Signal | Count | ARR at Risk |
> |---|---|---|
> | No activity logged in 90+ days | 12 | $890K |
> | Support tickets 3x above average | 5 | $420K |
> | Contract expires within 60 days | 8 | $680K |
> | NPS score declined (8→5 or lower) | 4 | $310K |
>
> **Retention ad strategy:**
> 1. Create a Salesforce list of 21 at-risk accounts
> 2. Upload to LinkedIn as a Matched Audience
> 3. Run ads showcasing: new features they haven't adopted, customer success stories from similar companies, ROI calculator for their use case
> 4. Complement with personalized email sequences
>
> **Why ads for retention?** Your champion at the account might be an advocate, but the CFO who approves renewal doesn't know your value. Ads ensure the decision-maker sees your success stories and product improvements before renewal conversations begin.

### 5. Multi-Touch Attribution from Salesforce

> **You:** Which marketing touches actually influence deals? Not just first touch or last touch.
>
> **Agent:** Let me pull campaign member data from your closed-won opportunities this year...
>
> **Multi-touch attribution (47 closed-won deals, $4.2M revenue):**
>
> | Campaign Type | Influenced Deals | Influenced Revenue | Avg Touches per Deal |
> |---|---|---|---|
> | Paid Search | 31 | $2.8M | 2.1 |
> | LinkedIn Ads | 24 | $2.4M | 1.8 |
> | Webinars | 19 | $1.9M | 1.4 |
> | Content Downloads | 28 | $2.2M | 3.2 |
> | Email Nurture | 33 | $2.9M | 4.7 |
> | Industry Events | 8 | $1.1M | 1.0 |
>
> **Key insight:** Deals that closed involved an average of **4.3 marketing touches** across 3.1 different channels. No single channel deserves full credit.
>
> **The highest-impact combination:** Paid Search (first touch) → Content Download → Email Nurture → LinkedIn Ad → Webinar → Deal Closed. This 5-touch path appears in 38% of your closed-won deals.
>
> **Budget implication:** Cutting any channel would break the multi-touch chain. But email nurture (4.7 touches per deal) and content downloads (3.2 touches) are doing the most middle-of-funnel work.

---

## Salesforce Tips for Ad Targeting

1. **Sync closed-won accounts to LinkedIn Matched Audiences.** Your best customers look like your future customers. A Lookalike audience from closed-won accounts on LinkedIn targets similar companies at similar companies.
2. **Import offline conversions to Google Ads.** This teaches Smart Bidding which clicks lead to actual revenue, not just form fills. The difference in lead quality is dramatic.
3. **Build ABM lists from pipeline data.** Your sales team's target accounts should be your ad targeting list. Don't waste money on companies that aren't in your ICP.
4. **Track original source rigorously.** Salesforce's "Lead Source" field is your ground truth for channel attribution. Make it mandatory on lead creation.
5. **Suppress existing customers.** Don't pay to advertise to companies you've already sold to. Export your customer list and add as exclusion audiences.
6. **Use deal size for bidding.** Import deal values as offline conversion values. Google and LinkedIn can then optimize for revenue, not just lead volume.
7. **Refresh target account lists quarterly.** Your pipeline changes constantly. ABM audiences should reflect current sales priorities, not last quarter's targets.

---

## FAQ

### Is there an MCP for Salesforce?
Yes — this repo pre-configures the Synter MCP server for Salesforce CRM operations. Works with Amp, Cursor, VS Code, and Claude Desktop.

### Can AI query Salesforce data?
Yes. The agent can query opportunities, contacts, accounts, leads, and campaign members using SOQL — all through natural language.

### Can I sync Salesforce data to ad platforms?
Yes. The agent exports Salesforce contacts and accounts, then uploads them as Custom Audiences to Google Ads, Meta, and LinkedIn.

### Do I need Salesforce admin access?
You need at least read access to the objects you want to query (Opportunities, Contacts, Accounts). Admin access is not required.

### How does offline conversion import work?
The agent matches Salesforce closed-won deals to ad platform clicks using GCLIDs (Google), email addresses (Meta/LinkedIn), or other identifiers. This attributes revenue to specific ad campaigns.

---

## Related Repos

- [hubspot-agent](https://github.com/Synter-Media-AI/hubspot-agent) — SMB CRM alternative
- [linkedin-ads-agent](https://github.com/Synter-Media-AI/linkedin-ads-agent) — ABM on LinkedIn
- [google-ads-agent](https://github.com/Synter-Media-AI/google-ads-agent) — Offline conversion import
- [audience-sync-agent](https://github.com/Synter-Media-AI/audience-sync-agent) — Multi-platform audience sync
- [attio-crm-agent](https://github.com/Synter-Media-AI/attio-crm-agent) — Modern CRM for startups
- [cross-platform-ads-agent](https://github.com/Synter-Media-AI/cross-platform-ads-agent) — Multi-channel attribution

---

## License

MIT — see [LICENSE](LICENSE) for details.

Built by [Synter](https://syntermedia.ai) · [Get API Key](https://syntermedia.ai/developer) · [Documentation](https://syntermedia.ai/docs)
