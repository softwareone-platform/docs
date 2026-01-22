---
description: Step-by-step guide to configuring your AI tools to talk to SoftwareOne.
---

# MCP Server Setup

This guide explains how to configure popular AI clients to connect to the **SoftwareOne Model Context Protocol (MCP) Server**. 

Once connected, your AI assistant will be able to query the marketplace, read documentation, and perform actions on your behalf.

## Prerequisites

*   **SoftwareOne API Token**: You generate this in the [SoftwareOne Portal](https://portal.platform.softwareone.com/).
*   **Configuration Details**: Please refer to the [Marketplace MCP Server README](README.md#client-setup) for the exact JSON configuration blocks.

---

## Claude Desktop

[Claude Desktop](https://claude.ai/download) provides a native integration for MCP servers.

### 1. Locate Config File

Open your configuration file. If it doesn't exist, create it.

*   **macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`
*   **Windows**: `%APPDATA%\Claude\claude_desktop_config.json`

### 2. Configure Server

Copy the appropriate configuration block (Remote or Local) from the [Marketplace MCP Server README](README.md#client-setup) and add it to the `mcpServers` object in your config file.

### 3. Restart Claude

Completely quit and restart the Claude Desktop application. You should see a plug icon indicating the server is connected.

---

## Cursor

[Cursor](https://cursor.com) is an AI-powered code editor that supports MCP.

### 1. Open Settings

1.  Open Cursor.
2.  Go to **Cursor Settings** > **General** > **MCP**.

### 2. Add New Server

1.  Click **+ Add New MCP Server**.
2.  **Name**: Enter `softwareone-marketplace`.
3.  **Type**: Select `stdio` (for local) or `sse` (for remote).
4.  Follow the configuration patterns provided in the [Marketplace MCP Server README](README.md#client-setup).

### 3. Verify

Once added, the status indicator should turn green.

---

## Antigravity

**Antigravity** (and compatible Google Cloud-based agents) supports MCP servers defined in the project configuration.

### 1. Project Configuration

Add the server definition to your `.agent/mcp_servers_config.json` (or similar). You can find the required JSON structure in the [Marketplace MCP Server README](README.md#client-setup).

### 2. Validation

Ask the agent to "List available MCP resources" to verify the connection.

---

## Generic / Custom Agents

If you are building your own agent or using another tool, you can connect via standard input/output (stdio) or Server-Sent Events (SSE).

### Usage

See the [Usage Section in the README](README.md#other-clients) for endpoint details and header requirements.
