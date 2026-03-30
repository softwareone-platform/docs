---
description: Step-by-step guide to configuring your AI tools to talk to SoftwareOne.
---

# MCP Server Setup

This topic explains how to configure popular AI clients to connect to the SoftwareOne Model Context Protocol (MCP) Server.

Once connected, your AI assistant will be able to query the marketplace, read documentation, and perform actions on your behalf.

## Prerequisites

Before you begin, ensure you have the following:

* **SoftwareOne API Token** - You can generate this in the [SoftwareOne Portal](https://portal.platform.softwareone.com/).
* **Configuration details** - See [Marketplace MCP Server README](./#client-setup) for the exact JSON configuration blocks.

## Claude Desktop

[Claude Desktop](https://claude.ai/download) provides a native integration for MCP servers.

1. **Locate config file** - Open your configuration file. If it doesn't exist, create it.
   1. **macOS** - `~/Library/Application Support/Claude/claude_desktop_config.json`
   2. **Windows** -  `%APPDATA%\Claude\claude_desktop_config.json`
2. **Configure server** - Copy the appropriate configuration block (Remote or Local) from the [Marketplace MCP Server README](./#client-setup) and add it to the `mcpServers` object in your config file.
3. **Restart Claude** - Completely quit and restart the Claude Desktop application. You should see a plug icon indicating the server is connected.

## Cursor

[Cursor](https://cursor.com) is an AI-powered code editor that supports MCP.

1. **Open Settings** - Open Cursor. Go to **Cursor Settings** > **General** > **MCP**.
2. **Add New Server** - Select **+ Add New MCP Server**.
   1. **Name** - Enter `softwareone-marketplace`.
   2. **Type** - Select `stdio` (for local) or `sse` (for remote).
   3. Follow the configuration patterns provided in the [Marketplace MCP Server README](./#client-setup).
3. **Verify** - Once added, the status indicator should turn green.

## Antigravity

[Antigravity ](https://antigravity.google/)(and compatible Google Cloud-based agents) supports MCP servers defined in the project configuration.

1. **Project configuration** - Add the server definition to your `.agent/mcp_servers_config.json` (or similar). You can find the required JSON structure in the [Marketplace MCP Server README](./#client-setup).
2. Validation - Ask the agent to "_List available MCP resources_" to verify the connection.

## Generic / Custom Agents

If you are building your own agent or using another tool, you can connect via standard input/output (stdio) or Server-Sent Events (SSE).

### Usage

See the [Usage Section in the README](./#other-clients) for endpoint details and header requirements.
