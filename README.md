# graph-app

Give your AI coding assistant a map of your code.

**Score: 67 / 100** on the [ShipItWorks rubric](https://shipitworks.com/how-we-score/). Stage: Beta. As of 2026-11-02, from the [product page](https://shipitworks.com/apps/#graph-app).

Every number on the product page names the file it came from. The lists below are copied from that page, not rewritten.

**Platform.** Server and web. No Android app. Not deployed.

## What works today

- Engine: parse Python/TS/JS into symbol+call graph
- API + job queue + indexing worker

## Not done yet

- Half the suite did not execute: 107 of 212 tests skipped because no Postgres was started for TEST_ADMIN_URL
- Not deployed; no live URL; web e2e, live MCP and real GitHub sign-in never run
- Benchmark numbers in the README were not re-run this pass
- README's test count is stale (says 119); no release tag; CI result on GitHub main not checked

## Demo

[Transcript of the demo (1:50)](https://shipitworks.com/graph-app/transcript/) · video on the [product page](https://shipitworks.com/apps/#graph-app)

The demo voice is AI-generated (ElevenLabs, "Alice") and the demo shows made-up data. The video says so at the end.

## Source code

The source is private for now. This repository holds the public record for the product: this README, and soon a CHANGELOG and LICENSE. Until the source is public, the [product page](https://shipitworks.com/apps/#graph-app) is the source of truth, and the score above is the one to trust.

## How we work

Say only what we can back. Say what is not finished before anyone asks. Name people, companies and tools to give credit. Collect as little data as possible. We use AI and say so: Claude (by Anthropic) helps write the code and wrote this README.

Full version: [github.com/ShipItWorks](https://github.com/ShipItWorks) · Contact: support@shipitworks.com

---

Drafted with Claude (Anthropic) from the product page on 2026-11-02 and reviewed by Robert Sweetman.
