# graph-app

Give your AI coding assistant a map of your code.

**Score: 64 / 100** on our own [rubric](https://shipitworks.com/how-we-score/). Stage: Beta. Scored 2026-11-10; this record was updated 2026-11-10 from the [product page](https://shipitworks.com/apps/#graph-app).

Every number on the product page names the file it came from. The lists below are copied from that page, not rewritten.

**Platform.** Server and web. No Android app. Not deployed.

## What works today

- Engine: parse Python/TS/JS into symbol+call graph (Tested with sample data)
- API + job queue + indexing worker (Tested with sample data)
- MCP endpoint for assistants (Proven)
- Benchmarks vs other engine (5 repos) (Tested with sample data)
- Supabase auth (GitHub sign-in) (Tested with sample data)

## Not done yet

- Web app (sign-in, repos, search, call map, impact) (Not tested yet)
- Half the suite did not execute in the 2026-11-01 audit: 107 of 212 tests skipped because no Postgres was started for TEST_ADMIN_URL. A 2026-11-07 log shows 218 passed with Postgres up, from a dirty tree with no exit code; no clean run of main is recorded
- Not deployed; no live URL. Web app browser test run once on a local stack (proof/web-e2e-local.log, 2026-11-08); real GitHub sign-in, delete-account, other browsers and any deployed server not run
- MCP endpoint run on a local stack only (MCP Python SDK client; Claude Code once, proof/mcp-assistant-local.log, 2026-11-08); no deployed server; Cursor and other assistants not tried
- Benchmarks: all 5 repos re-scored from saved traces and saved compiler-oracle files on 2026-11-07, self-run; the tests and the TypeScript compiler oracle were not re-run, the other engine was not re-run, toolz and react-hook-form drove development
- The references tool's completeness is measured only as a lower bound, self-run, on 4 Python repos (proof/references-recall.log, 2026-11-08, engine 939bba8); the TypeScript recall and precision logs on main name lane-branch commits that are not in main's history; no independent reproduction
- Network egress not yet traced: where data goes is read from code, not captured
- No LICENSE and no CHANGELOG on main; source not published, licence not chosen (README)
- CI on GitHub main: only the latest five runs were read (gh run list, 2026-11-10); the jobs run on a self-hosted runner since 2026-11-08 (PR #21) and their logs were not read
- Working copy ~/graph-app has uncommitted changes and a .env; the audited clone is clean

## What changed

- 2026-11-10: Site copy only: a dated correction now sits under the demo video for the narration line at 0:29. No code or score change.
- 2026-11-10: Land PR #24 merged into main as f2a7cd9 (10 lane PRs included); no feature label changed this round. Tagged v0.5.0 at f2a7cd9.
- 2026-11-08: Rescored under the per-feature rule against main daaacbf (tag v0.4.1): six features share the 25 feature points equally. The MCP endpoint is Proven locally (official SDK client, exit 0; not run from an AI assistant); engine, API, benchmarks and auth are tested with sample data; the web app is not tested yet (lint and build only). 64/100 on our own rubric, down from 67.
- 2026-11-08: Benchmark misses for toolz added and the three-repo misses list published (PR #12, tag v0.4.1; PR #11, tag v0.4.0). Saved traces re-scored; tests not re-run; self-run.
- 2026-11-08: CI workflow now runs on the self-hosted runner (PR #21, merged after tag v0.4.0, included in v0.4.1). No run result checked.
- 2026-11-08: README now says where data goes and lists what is not done; its test count is dated and the benchmark table matches the saved reports (PRs #1, #6, #9; tags v0.3.0, v0.4.0). Network egress not yet traced.

See [CHANGELOG](CHANGELOG.md).

## Demo

[Transcript of the demo (1:50)](https://shipitworks.com/graph-app/transcript/) · video on the [product page](https://shipitworks.com/apps/#graph-app)

The demo voice is AI-generated (ElevenLabs, "Alice") and the demo shows made-up data. The video says so at the end.

## Source code

The source is private for now. This repository holds the public record for the product: this README and a CHANGELOG, and soon a LICENSE. Until the source is public, the [product page](https://shipitworks.com/apps/#graph-app) is the source of truth, and the score above is the one to trust.

## How we work

Say only what we can back. Say what is not finished before anyone asks. Name people, companies and tools to give credit. Collect as little data as possible. We use AI and say so: Claude (by Anthropic) helps write the code and wrote this README.

Full version: [github.com/ShipItWorks](https://github.com/ShipItWorks) · Contact: support@shipitworks.com

---

Drafted with Claude (Anthropic) from the product page on 2026-11-02. Owner review by Robert Sweetman: pending.
