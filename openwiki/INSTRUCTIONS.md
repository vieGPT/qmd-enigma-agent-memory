---
type: Repository guide
title: QMD Wiki Instructions
description: Brief for an agent-facing wiki of QMD, scoped by the project's official documentation and grounded in its source at commit 86d2365.
tags: [documentation, repository, code-wiki, qmd]
---

A code wiki for this local repository. Prioritize a concise quickstart, architecture overview, source map, key workflows, domain concepts, operations/runbook notes, testing guidance, and integration points. Inspect git history to understand reasoning behind code changes and the progression of the repository. Keep pages grounded in the repository structure and recent code changes. Prefer practical navigation for engineers over generic summaries.

Readers are AI coding agents that install, configure, use and debug QMD and need exact answers from the source. Cover, in this order of priority (the sections of the project's official documentation, README.md):

1. Quick Start and installation (README.md Quick Start, Installation, Development) — bin/, src/, root package files
2. Using with AI Agents, MCP Server and HTTP Transport (MCP tool parameters, Origin and Host validation, LLM residency) — src/, test/
3. SDK / Library Usage (createStore modes, search, retrieval, collections, context, indexing, types, lifecycle) — src/
4. Usage: Collection Management, Configuring index.yml, trust gating for checked-in .qmd config, automatic update commands — src/, scripts/
5. Search Commands, Metadata Filtering, Metadata Discovery, Output Format and Examples — src/, test/
6. Architecture, Score Normalization and Fusion (RRF, top-rank bonus, position-aware blending) — src/, test/
7. Requirements, GGUF Models, Custom Embedding Model and Model Configuration (EmbeddingGemma and Qwen3 prompt formats, reranker, query expansion) — src/, scripts/, finetune/
8. Data Storage, Environment Variables, How It Works (indexing, embedding, smart and AST-aware chunking, query flow), Index Maintenance and Benchmarking — src/, tools/, test/

Name settings, tool parameters and API fields exactly as the code and the wire format spell them, with their defaults.

Do not document: marketing text, translations (none appear in the layout), contributor process, generated or vendored code, fine-tuning weights and training artifacts under finetune/, evaluation corpora under test/eval-docs/, the CHANGELOG.md release prose, and images or other binary assets.

Conditions: describe behaviour with its conditions, exceptions and fallback paths. Write "always", "never", "every", "only" or "guarantees" only when the code has no other branch; otherwise name the branch (for example "unless …", "when … is unset, it falls back to …"). Give an order of steps only as the code runs it.

Evidence: cite this repository at commit 86d2365; prefer bounded line ranges (`repo://path#Lx-Ly`) over whole files. A Claim about what happens in a function cites the lines of every branch it describes, including the early returns and error paths, not only the main path.
