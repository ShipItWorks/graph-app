# Changelog

Public record of changes to graph-app, written from the product page on shipitworks.com. The source is private. Format: [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Release tags exist on the private repository's default branch.

## 2026-11-07 (release v0.4.0)

- A references tool was added to the MCP endpoint: it lists every call site of a symbol with exact totals. Built; run once against a local stack with the MCP Python SDK (one symbol, total 3, matching grep); not deployed and not run from an AI assistant.
- The README now says where data goes and what is not done, drops an unproven absolute, and matches its measured-results table to the saved reports. The click and marshmallow benchmark numbers were reproduced by re-scoring saved runtime traces (the tests were not re-run), and the engine's misses are listed. Network egress is not yet traced. Release v0.4.0.

Score 67 / 100 on our own rubric, scored 2026-11-01; no score or proof label changed in this update. Product page: https://shipitworks.com/graph-app/
