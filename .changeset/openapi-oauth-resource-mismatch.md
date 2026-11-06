---
"@executor-js/plugin-openapi": patch
---

OpenAPI OAuth discovery now ignores protected-resource metadata whose `resource` does not cover the probed API URL (RFC 9728 §3.3). A host that publishes OAuth metadata only for a sibling endpoint, such as ElevenLabs' MCP server at `/v1/mcp`, no longer gets an OAuth method on its REST integration that cannot complete a connect.
