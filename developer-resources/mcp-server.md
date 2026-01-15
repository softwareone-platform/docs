---
description: Learn about the Marketplace MCP Server and how to use it to connect AI assistants to the SoftwareOne Marketplace API.
---

# Marketplace MCP Server

The **Marketplace MCP Server** is an open-source Model Context Protocol (MCP) server designed to connect AI assistants (like Antigravity, Cursor, and Claude) to the SoftwareOne Marketplace API.

> **In simple terms:** Think of it as teaching your AI assistant to "speak" the SoftwareOne Marketplace language. Once connected, you can ask questions like "How many subscriptions do we have?" or "What's the status of our last order?" — and get real answers instantly, without logging into the portal.

## What is the Model Context Protocol (MCP)?

The **Model Context Protocol (MCP)** is an open standard that allows AI assistants to connect to external data and systems. Instead of building custom integrations for every tool, MCP provides a universal language for AI models to:

*   **Read context**: Access documents, databases, and logs.
*   **Take action**: Execute commands or query APIs on your behalf.
*   **Stay secure**: You control what the AI can see and do through explicit permissions.

By using the Marketplace MCP Server, you turn the entire SoftwareOne Marketplace API into a toolset that your AI assistant understands natively.

## Why use the Marketplace MCP Server?

This server eliminates the need to manually browse portals or write one-off scripts for common tasks.

*   **Instant Answers**: Ask "What is the status of order ORD-123?" or "Show me active Microsoft subscriptions" and get immediate, accurate results without leaving your IDE.
*   **Data Exploration**: Explore available API resources and schemas interactively. Not sure what fields are on a `Product`? Just ask "Show me the schema for catalog.products".
*   **Automation**: Quickly generate reports or find IDs needed for your scripts/terraform configurations by asking "List all Azure subscriptions in the US region".

---

The server is **hosted and managed by SoftwareOne**, so you can connect to it immediately without running any local infrastructure.

> [!NOTE]
> The server complies with our [OpenAPI Specification](https://api.platform.softwareone.com/public/v1/openapi.json), which serves as the source of truth for all available data and operations.

## Prerequisites

*   **SoftwareOne Marketplace API Token**: You will need a valid API token to authenticate requests. This is like a password that proves you are allowed to access your organization's data. You can generate a token from your account settings in the SoftwareOne Marketplace Portal.

> [!TIP]
> Not sure where to find your token? Contact your SoftwareOne account administrator or check the Marketplace Portal documentation for "API Tokens."

## Client Setup

To use the hosted Marketplace MCP Server:

### Antigravity & Cursor

Add the following configuration to your MCP settings file (e.g., `~/.cursor/mcp.json` or Antigravity config).

> [!IMPORTANT]
> Replace `{your-token-goes-here}` with your actual Marketplace API token.

```json
{
    "mcpServers": {
        "softwareone-marketplace": {
            "url": "https://mcp.platform.softwareone.com/mcp",
            "transport": "mcp",
            "timeout": 30000,
            "headers": {
                "X-MPT-Authorization": "{your-token-goes-here}",
                "X-MPT-Endpoint": "https://api.platform.softwareone.com/public"
            }
        }
    }
}
```

### Other Clients

For clients that support server-sent events (SSE) or remote HTTP transports, use the URL:
`https://mcp.platform.softwareone.com/mcp`

Ensure you provide the required `X-MPT-Authorization` header with your request.

## What You Can Ask

Once connected, you can ask your AI assistant questions in plain English. The assistant will translate your questions into precise API queries.

> [!TIP]
> **New to this?** Start with simple questions like "What products are available?" or "Show me my subscriptions." The AI will guide you from there. You don't need to memorize any commands!

### 📦 Product Catalog

**User:** "Find Microsoft 365 products that are active."

**Assistant:** I found several active Microsoft 365 products. Here is an example:

*   **Name**: Microsoft 365 Business & Enterprise
*   **ID**: `PRD-XXXX-XXXX`
*   **Vendor**: Microsoft (`ACC-XXXX-XXXX`)
*   **Status**: Published

**User:** "Show me the schema for catalog products."

**Assistant:** The `catalog.products` resource has the following fields:
*   `id` (string): Unique identifier
*   `name` (string): Product name
*   `status` (enum): Published, draft, etc.
*   `vendor` (object): Vendor details

### 🛒 Orders & Subscriptions

**User:** "List the last 5 orders for customer CUST-123."

**Assistant:**
1.  **Order ORD-5555** (Created: 2024-03-01): 10x Office 365 E3
2.  **Order ORD-5554** (Created: 2024-02-28): 1x Azure Plan
...

### 🔍 Discovery

**User:** "What resources are available in the billing API?"

**Assistant:** I can help you with:
*   `billing.invoices`: Retrieve invoice summaries.
*   `billing.statements`: Access billing statements and charges.

## Troubleshooting

*   **Authentication Errors**: Double-check your `X-MPT-Authorization` header. The token should typically start with `idt:`. If you copied the token from the portal, make sure there are no extra spaces.
*   **"I don't know how to do that"**: If the assistant is unsure, ask it to "List available tools" or "Show available resources" to refresh its context.
*   **No results returned**: Try rephrasing your question. For example, instead of "Find order 123", try "Show me the order with ID ORD-123".

## Frequently Asked Questions

**Do I need to be a developer to use this?**
No! Once someone sets up the connection for you, you can ask questions in plain English. The AI does the technical work.

**Is my data secure?**
Yes. The server uses your personal API token, which means it only accesses what you're already authorized to see. No data is stored on the MCP server itself.

**Can I use this on my phone?**
The MCP server works with AI tools like Antigravity, Cursor, and Claude Desktop. These are typically used on computers, but if your AI client supports mobile, it will work there too.

**What kind of questions can I ask?**
Anything related to your SoftwareOne Marketplace data: orders, subscriptions, products, billing, agreements, and more. If you're not sure, just ask "What can you help me with?"

## Open Source & Contributing

The server implementation is open source and available on GitHub at [softwareone-platform/mpt-mcp](https://github.com/softwareone-platform/mpt-mcp). We welcome contributions! You can also clone the repository if you prefer to run the server locally or customize it for your needs.
