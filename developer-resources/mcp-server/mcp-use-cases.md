---
description: Learn how to use the SoftwareOne MCP Server for intelligent automation.
---

# MCP Use Cases

The **SoftwareOne Model Context Protocol (MCP) Server** empowers your AI agents to interact directly with the SoftwareOne Marketplace Platform. Instead of manually navigating the portal, you can ask your agent to find products, track orders, analyze spend, and answer technical questions using live documentation.

This guide walks through four common scenarios that demonstrate the power of agentic workflows.

## Prerequisites

Before you begin, ensure you have:

1.  **An MCP Client**: A compatible AI tool like [Claude Desktop](https://claude.ai/download) or an IDE extension (e.g., Cursor, VS Code).
2.  **SoftwareOne API Token**: Your generic API token (starts with `TKN-`) from the [SoftwareOne Portal](https://portal.platform.softwareone.com/).
3.  **Server Configuration**: The MCP server must be running and configured with your `MPT_API_TOKEN`. See the [MCP Server Setup](mcp-server-setup.md) for instructions.

---

## Scenario 1: Intelligent Procurement

**Goal**: Quickly find specific software licenses without browsing the entire catalog.

A client wants to procure "Microsoft 365" licenses but isn't sure of the exact SKU names.

**User Prompt:**
> "Find all Microsoft 365 Business products available in the catalog."

**Agent Action:**
The agent uses the `marketplace_query` tool to search the `catalog.products` resource, using a case-insensitive `ilike` filter.

```javascript
// Tool Call
marketplace_query({
  resource: "catalog.products",
  rql: "ilike(name,*Microsoft 365 Business*)",
  limit: 5
})
```

**Response:**
The agent retrieves the list and summarizes it for the user:

> I found the following Microsoft 365 Business products:
>
> 1.  **Microsoft 365 Business Standard** (SKU: `PRD-M365-STD`) - *Active*
> 2.  **Microsoft 365 Business Premium** (SKU: `PRD-M365-PREM`) - *Active*
> 3.  **Microsoft 365 Business Basic** (SKU: `PRD-M365-BSC`) - *Active*
>
> Would you like to see pricing for any of these?

---

## Scenario 2: Order Tracking

**Goal**: Get a status update on recent purchases.

A procurement manager needs to know if their recent orders have been processed.

**User Prompt:**
> "What is the status of my last 5 orders?"

**Agent Action:**
The agent queries `commerce.orders`, sorting by creation date (`-audit.created.at`) to get the most recent ones.

```javascript
// Tool Call
marketplace_query({
  resource: "commerce.orders",
  order: "-audit.created.at",
  limit: 5
})
```

**Response:**
> Here are your last 5 orders:
>
> *   **ORD-2024-001** (Microsoft 365 E5) - **Completed** (Created: today)
> *   **ORD-2024-002** (Adobe Acrobat Pro) - **Processing** (Created: yesterday)
> *   **ORD-2024-003** (Azure Reservation) - **Completed**
> *   **ORD-2024-004** (AWS Savings Plan) - **Failed** (Action Required)
> *   **ORD-2024-005** (Zoom Pro) - **Completed**

---

## Scenario 3: Spend Analysis & Billing

**Goal**: Identify high-value transactions for a specific period.

A finance user wants to review large invoices from December 2024.

**User Prompt:**
> "Show me all invoices over $1,000 from December 2024."

**Agent Action:**
The agent constructs a complex RQL query. Note the use of **UTC dates** with **3-digit millisecond** precision, and the explicit selection of the `audit` object.

```javascript
// Tool Call
marketplace_query({
  resource: "billing.invoices",
  rql: 'and(gt(totalPrice,1000),gt(audit.created.at,"2024-12-01T00:00:00.000Z"),lt(audit.created.at,"2025-01-01T00:00:00.000Z"))',
  select: "+audit,+totalPrice,+status"
})
```

**Response:**
> I found 2 invoices from December 2024 exceeding $1,000:
>
> *   **INV-US-9988** - $4,500.00 (Dec 15, 2024)
> *   **INV-US-9999** - $1,250.50 (Dec 28, 2024)

---

## Scenario 4: Instant Documentation Access

**Goal**: Answer technical questions without leaving the chat.

A developer is building an integration and forgets how to format dates in the API.

**User Prompt:**
> "How do I format date filters in the API?"

**Agent Action:**
Instead of hallucinating an answer, the agent searches the official documentation using the `marketplace_docs_list` and `marketplace_docs_read` tools.

```javascript
// Tool Call 1: Search
marketplace_docs_list({ search: "date format" })

// Tool Call 2: Read specific page
marketplace_docs_read({ uri: "docs://developer-resources/rest-api/resource-query-language" })
```

**Response:**
> According to the *Resource Query Language* documentation:
>
> **API Date Requirement**: Dates must be in **UTC** and include **3-digit millisecond precision** (e.g., `YYYY-MM-DDTHH:mm:ss.sssZ`).
>
> Example: `eq(audit.created.at,"2023-01-01T00:00:00.000Z")`
### Scenario 5: Proactive Renewal Management

**Goal**: Identify subscriptions that are expiring in the next 30 days to prepare for renewals or contract discussions.

**Query**:
```javascript
// Find active subscriptions expiring before March 1st, 2026
marketplace_query({
  resource: "commerce.subscriptions",
  rql: "and(eq(status,Active),lt(endDate,\"2026-03-01T00:00:00.000Z\"))",
  order: "+endDate",
  limit: 10
})
```

**Response**:
```json
{
  "data": [
    {
      "id": "SUB-9988-7766",
      "name": "Adobe Creative Cloud for Teams",
      "status": "Active",
      "endDate": "2026-02-15T00:00:00.000Z",
      "autoRenew": true
    }
  ]
}
```

---

### Scenario 6: Non-Renewing Subscriptions

**Goal**: List all subscriptions where auto-renewal has been disabled. This is useful for IT teams to ensure critical services aren't accidentally cut off.

**Query**:
```javascript
// Find active subscriptions with auto-renewal disabled
marketplace_query({
  resource: "commerce.subscriptions",
  rql: "and(eq(status,Active),eq(autoRenew,false))",
  limit: 20
})
```

**Response**:
```json
{
  "data": [
    {
      "id": "SUB-1122-3344",
      "name": "JetBrains All Products Pack",
      "status": "Active",
      "endDate": "2026-05-20T00:00:00.000Z",
      "autoRenew": false
    }
  ]
}
```
