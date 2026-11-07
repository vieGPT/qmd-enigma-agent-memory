# Files

- [HTTP Transport, REST Routes, and Origin/Host Validation](http-api-and-origin-guard.md) - How qmd mcp --http serves Streamable HTTP MCP plus /health, /query, /search, and /metadata REST routes behind an Origin/Host guard that defends against DNS rebinding; covers bind resolution, guard rules, env allowlists, and rejection responses.
- [MCP Server and Tools](mcp-server.md) - Specifies the QMD MCP server built by createMcpServer and its five tools (query, get, multi_get, status, metadata), with exact zod parameter names, defaults, and branches, plus stdio versus HTTP launch, the instructions cache, and shutdown semantics.
- [SDK / Library Usage](sdk-library.md) - How to use the @tobilu/qmd programmatic API: createStore() options and modes (YAML configPath, inline config, DB-only), the QMDStore search, retrieval, collection, context, indexing, and close methods, config-to-SQLite reconciliation, LLM resource lifecycle, and default DB path rules.
