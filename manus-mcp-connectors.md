# MCP Connectors

## What are MCP Connectors

MCP Connectors enable Manus to integrate with external services and tools through the Model Context Protocol (MCP). They act as bridges between Manus and third-party applications, allowing seamless data exchange and action execution across platforms.

MCP Connectors expose external APIs and services as structured tools that Manus can discover and invoke during task execution, without requiring custom integration code for each service.

---

## Why Connect MCP Servers

Connecting MCP servers to Manus unlocks a range of capabilities:

- **Extended reach** — access data and actions from services like Notion, Gmail, Stripe, HubSpot, Google Calendar, and more
- **Automation** — trigger workflows across multiple apps in a single task
- **Real-time data** — read and write live data rather than relying on static context
- **Reduced manual work** — delegate repetitive cross-app tasks to Manus
- **Composability** — combine multiple connectors in a single workflow for end-to-end automation

---

## How MCP Connectors Work

1. **Registration** — An MCP server is registered with Manus, either via a hosted connector or a self-hosted server URL.
2. **Discovery** — When a task is started, Manus queries the connected MCP servers to discover available tools and their schemas.
3. **Selection** — Based on the task requirements, Manus selects the appropriate tools from the available connectors.
4. **Invocation** — Manus calls the selected tools with the required parameters, passing context from the task.
5. **Result handling** — The tool responses are returned to Manus, which incorporates them into the task output or uses them to drive subsequent steps.
6. **Chaining** — Multiple tools from the same or different connectors can be called in sequence to complete multi-step workflows.

---

## Multi-App Workflow Examples

### Notion + Google Calendar

**Use case:** Sync meeting notes from Notion to Google Calendar events.

- Read a Notion database for upcoming meeting entries
- Parse dates, titles, and attendee lists
- Create or update corresponding Google Calendar events
- Write back confirmation links to the Notion records

### Gmail

**Use case:** Automated email triage and response drafting.

- Fetch unread emails matching a filter (e.g., subject keywords, sender domain)
- Summarize thread content
- Draft reply candidates based on task instructions
- Optionally send or save drafts for human review

### Stripe

**Use case:** Revenue reporting and subscription management.

- Query Stripe for recent charges, subscriptions, or customer records
- Generate summary reports (MRR, churn, new signups)
- Trigger actions such as applying coupons or updating subscription plans based on defined rules

### HubSpot + Gmail + Notion

**Use case:** End-to-end CRM and outreach workflow.

- Pull contact segments from HubSpot based on deal stage or lifecycle status
- Draft personalized outreach emails via Gmail for each contact
- Log outreach activity back to HubSpot contact timelines
- Record campaign status and outcomes in a Notion tracker database

---

## Available Connectors

For the full list of supported MCP Connectors and setup instructions, refer to the official Manus MCP Connectors reference documentation.
