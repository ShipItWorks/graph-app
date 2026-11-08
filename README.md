# graph-app

Give your AI coding assistant a map of your code.

**Score: 67 / 100** on our own [rubric](https://shipitworks.com/how-we-score/). Stage: Beta. Scored 2026-11-01; this record was updated 2026-11-07 from the [product page](https://shipitworks.com/apps/#graph-app).

Every number on the product page names the file it came from. The lists below are copied from that page, not rewritten.

**Platform.** Server and web. No Android app. Not deployed.

## What works today

- Engine: parse Python/TS/JS into symbol+call graph
- API + job queue + indexing worker

## Not done yet

- Half the suite did not execute: 107 of 212 tests skipped because no Postgres was started for TEST_ADMIN_URL
- Not deployed; no live URL; web e2e, live MCP and real GitHub sign-in not run
- Benchmark numbers in the README were reproduced from saved traces on 2026-11-07; the benchmark tests were not re-run to record new traces
- README test counts are now dated (2026-11-07); the release tag is on the default branch only; CI result on GitHub main not checked
- Working copy ~/graph-app has uncommitted changes and a .env; the audited clone is clean

## What changed

- 2026-11-07: A references tool was added to the MCP endpoint: it lists every call site of a symbol with exact totals. Built; run once against a local stack with the MCP Python SDK (one symbol, total 3, matching grep); not deployed and not run from an AI assistant.
- 2026-11-07: The README now says where data goes and what is not done, drops an unproven absolute, and matches its measured-results table to the saved reports. The click and marshmallow benchmark numbers were reproduced by re-scoring saved runtime traces (the tests were not re-run), and the engine's misses are listed. Network egress is not yet traced. Release v0.4.0.

Full list with release tags: [CHANGELOG](CHANGELOG.md).

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
