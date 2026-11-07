# Files

- [Agent Retrieval Workflows (CLI Search and Get)](agent-retrieval.md) - How an AI agent should drive the qmd CLI to search, scope, filter, format, and retrieve documents. Covers choosing search, vsearch, or query, collection scoping with -c and includeByDefault, metadata filters, output flags, get and multi-get identifier forms, the 64 KB multi-get size cap, and empty-index behaviour.
- [Hybrid Query Pipeline](hybrid-query-pipeline.md) - Traces the end-to-end plain-text query path in hybridQuery (src/store.ts) - BM25 probe and strong-signal bypass, query expansion, type-routed FTS and vector searches, RRF fusion, chunk selection, reranking, blending, dedup, and minScore/limit filtering.
