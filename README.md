# graph-app

Give your AI coding assistant a map of your code.

**Score: 64 / 100** on our own [rubric](https://shipitworks.com/how-we-score/). Stage: Beta. Scored 2026-11-08; this record was updated 2026-11-08 from the [product page](https://shipitworks.com/apps/#graph-app).

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
- Not deployed; no live URL. Web app not tested yet: browser e2e and real GitHub sign-in not run
- MCP endpoint run with the official SDK client on a local stack only; not run from an AI assistant
- Benchmarks: 3 of 5 repos (click, marshmallow, toolz) re-scored from saved traces on 2026-11-07, self-run; the tests were not re-run to record new traces, the other engine was not re-run, toolz drove development, TypeScript repos not re-scored
- The references tool's completeness has not been measured (README 'Not done yet')
- Network egress not yet traced: where data goes is read from code, not captured
- No LICENSE and no CHANGELOG on main; source not published, licence not chosen (README)
- CI result on GitHub main not checked; the CI workflow moved to a self-hosted runner on 2026-11-08 (PR #21) and no run result is recorded
- Working copy ~/graph-app has uncommitted changes and a .env; the audited clone is clean

## What changed

- 2026-11-08: Rescored under the per-feature rule against main daaacbf (tag v0.4.1): six features share the 25 feature points equally. The MCP endpoint is Proven locally (official SDK client, exit 0; not run from an AI assistant); engine, API, benchmarks and auth are tested with sample data; the web app is not tested yet (lint and build only). 64/100 on our own rubric, down from 67.
- 2026-11-08: Benchmark misses for toolz added and the three-repo misses list published (PR #12, tag v0.4.1; PR #11, tag v0.4.0). Saved traces re-scored; tests not re-run; self-run.
- 2026-11-08: CI workflow now runs on the self-hosted runner (PR #21, merged after tag v0.4.0, included in v0.4.1). No run result checked.
- 2026-11-08: README now says where data goes and lists what is not done; its test count is dated and the benchmark table matches the saved reports (PRs #1, #6, #9; tags v0.3.0, v0.4.0). Network egress not yet traced.
- 2026-11-08: MCP impact no longer fails on a hub symbol (lists cut to fit; PRs #4, #5; tag v0.1.0). MCP endpoint run end to end with the official SDK client on a local stack (PR #7, v0.1.1); references tool added (PR #8, v0.2.0).
- 2026-11-07: A references tool was added to the MCP endpoint: it lists every call site of a symbol with exact totals. Built; run once against a local stack with the MCP Python SDK (one symbol, total 3, matching grep); not deployed and not run from an AI assistant.

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
