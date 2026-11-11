# Changelog

Public record of changes to graph-app, written from the product page on shipitworks.com. The source is private. Format: [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Release tags exist on the private repository's default branch.

## 2026-11-10 (release v0.5.0)

- 2026-11-10: Site copy only: a dated correction now sits under the demo video for the narration line at 0:29. No code or score change.
- 2026-11-10: Land PR #24 merged into main as f2a7cd9 (10 lane PRs included); no feature label changed this round. Tagged v0.5.0 at f2a7cd9.

Score 64 / 100 on our own rubric, scored 2026-11-10. Product page: https://shipitworks.com/apps/#graph-app

## 2026-11-08 (release v0.4.1)

- 2026-11-08: Rescored under the per-feature rule against main daaacbf (tag v0.4.1): six features share the 25 feature points equally. The MCP endpoint is Proven locally (official SDK client, exit 0; not run from an AI assistant); engine, API, benchmarks and auth are tested with sample data; the web app is not tested yet (lint and build only). 64/100 on our own rubric, down from 67.
- 2026-11-08: Benchmark misses for toolz added and the three-repo misses list published (PR #12, tag v0.4.1; PR #11, tag v0.4.0). Saved traces re-scored; tests not re-run; self-run.
- 2026-11-08: CI workflow now runs on the self-hosted runner (PR #21, merged after tag v0.4.0, included in v0.4.1). No run result checked.
- 2026-11-08: README now says where data goes and lists what is not done; its test count is dated and the benchmark table matches the saved reports (PRs #1, #6, #9; tags v0.3.0, v0.4.0). Network egress not yet traced.
- 2026-11-08: MCP impact no longer fails on a hub symbol (lists cut to fit; PRs #4, #5; tag v0.1.0). MCP endpoint run end to end with the official SDK client on a local stack (PR #7, v0.1.1); references tool added (PR #8, v0.2.0).

Score 64 / 100 on our own rubric, scored 2026-11-08. Product page: https://shipitworks.com/apps/#graph-app

## 2026-11-07 (release v0.4.0)

- A references tool was added to the MCP endpoint: it lists every call site of a symbol with exact totals. Built; run once against a local stack with the MCP Python SDK (one symbol, total 3, matching grep); not deployed and not run from an AI assistant.
- The README now says where data goes and what is not done, drops an unproven absolute, and matches its measured-results table to the saved reports. The click and marshmallow benchmark numbers were reproduced by re-scoring saved runtime traces (the tests were not re-run), and the engine's misses are listed. Network egress is not yet traced. Release v0.4.0.

Score 67 / 100 on our own rubric, scored 2026-11-01; no score or proof label changed in this update. Product page: https://shipitworks.com/graph-app/
