---
'@mastra/pg': patch
---

Reduce PostgreSQL round trips when an agent saves messages between tool calls. Each batch now validates and touches all affected threads in one query, while preserving per-step persistence and rollback on missing threads.
