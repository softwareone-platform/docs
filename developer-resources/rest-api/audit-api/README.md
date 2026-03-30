---
description: Use the Audit API to track and retrieve activity logs programmatically.
---

# Audit API

The **Audit API** enables you to track and retrieve activity logs across the Marketplace Platform, so you have full visibility into key actions taken by users or systems.

With this API, you can create new audit records programmatically, retrieve a list of logged events for monitoring or compliance purposes, and get detailed information about specific events.&#x20;

<a href="https://editor-next.swagger.io/?url=https://api.platform.softwareone.com/public/v1/audit/openapi.json" class="button primary">Try API</a><a href="https://api.platform.softwareone.com/public/v1/audit/openapi.json" class="button secondary">Download API</a>

## Core Concepts

The Audit API is built around the following core resources:

* **Audit record** - Represents a detailed record of an event that took place within the platform.
* **Audit event type** - Represents the event that occurred within the platform.

## Collections

The API is organized into collections, each containing a set of operations. Access to these operations varies by role, depending on whether you are a `client`, `vendor`, or `operations` user.&#x20;

Refer to the following capability matrix to see which roles are authorized to perform specific operations within each collection:

### Audit Records

<table><thead><tr><th width="251">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List audit records</td><td>✅ </td><td>✅</td><td>✅</td></tr><tr><td>Get audit record</td><td>✅</td><td>✅</td><td>✅</td></tr><tr><td>Create audit record</td><td>❌</td><td>✅</td><td>✅</td></tr></tbody></table>

### Audit Event Type

<table><thead><tr><th width="251">Capability</th><th width="155">Client</th><th width="130">Vendor</th><th>Operations</th></tr></thead><tbody><tr><td>List audit event types</td><td>✅</td><td>✅</td><td>✅</td></tr></tbody></table>
