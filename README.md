# Onegin

Give your AI coding assistant a map of your code.

**Score: 64 / 100** on our own [rubric](https://shipitworks.com/how-we-score/). Stage: Beta. Scored 2026-11-12; this record was updated 2026-11-18 from the [product page](https://shipitworks.com/onegin/).

Every number on the product page names the file it came from. The lists below are copied from that page, not rewritten.

**Platform.** Server and web. No Android app. Not deployed.

## What works today

- Engine: parse Python/TS/JS into symbol+call graph (Tested with sample data)
- API + job queue + indexing worker (Tested with sample data)
- MCP endpoint for assistants (Proven)
- Benchmarks vs other engine (5 repos) (Tested with sample data)
- Supabase auth (GitHub sign-in built; a real GitHub sign-in has not been run) (Tested with sample data)

## Not done yet

- Web app (sign-in, repos, search, call map, impact) (Not tested yet)
- On 2026-11-18 a review ran the suite at commit d4f8864 with Postgres up: 389 passed, 0 failed, 0 skipped (pytest). The scorecard's own run logs are older: a 2026-11-07 log shows 218 passed, from a dirty tree with no exit code
- Not deployed; no live URL. Web app browser test run once on a local stack (proof/web-e2e-local.log, 2026-11-08); real GitHub sign-in, delete-account, other browsers and any deployed server not run
- MCP endpoint run on a local stack only (MCP Python SDK client; Claude Code once, proof/mcp-assistant-local.log, 2026-11-08); no deployed server; Cursor and other assistants not tried
- Benchmarks: all 5 repos re-scored from saved traces and saved compiler-oracle files on 2026-11-07, self-run; the tests and the TypeScript compiler oracle were not re-run, the other engine was not re-run, toolz and react-hook-form drove development
- The references tool's completeness is measured only as a lower bound, self-run, on 4 Python repos (proof/references-recall.log, 2026-11-08, engine 939bba8); the TypeScript recall and precision logs on main name lane-branch commits that are not in main's history; no independent reproduction
- Network egress not yet traced: where data goes is read from code, not captured
- No LICENSE and no CHANGELOG on main; source not published, licence not chosen (README)
- CI on GitHub main: only the latest eight runs were read (gh run list, 2026-11-11); the jobs run on a self-hosted runner since 2026-11-08 (PR #21) and their logs were not read
- The developer's working copy has uncommitted changes and a local settings file that is not in the repository; the audited clone is clean

## What changed

- 2026-11-18: A review at commit d4f8864 ran the test suite with Postgres (389 passed, 0 failed, 0 skipped) and ran the find-references tool on a real repository, so that target was removed from Where it's going. The sign-in line now says a real GitHub sign-in has not been run. No feature label or score changed.
- 2026-11-11: Merged into the product: a log of a run of the assistant check script was added. In it, the Claude Code assistant called two of the MCP endpoint's tools on a local stack and answered with a caller and line that matched a direct call; it is one assistant, one prompt and a local stack, read from the repository's log and not re-run here. This scorecard round did not run it, so no feature label or score changed (PR #31). Scorecard row: "MCP endpoint for assistants" (works true, Proven) covers the endpoint; the saved log of the assistant run is not scored beyond that row.
- 2026-11-11: Merged into the product: the engine now also reads Go, Java and Rust code (checked with fixture tests and a hand check of 36 sampled links on 3 repositories; no recall or precision figure yet), a repeat index re-reads only the files that changed, and the query tools accept a precise mode. No feature label or score changed (PRs #26 and #25).
- 2026-11-10: Site copy only: a dated correction now sits under the demo video for the narration line at 0:29. No code or score change.
- 2026-11-10: Land PR #24 merged into main as f2a7cd9 (10 lane PRs included); no feature label changed this round. Tagged v0.5.0 at f2a7cd9.
- 2026-11-08: Rescored under the per-feature rule against main daaacbf (tag v0.4.1): six features share the 25 feature points equally. The MCP endpoint is Proven locally (official SDK client, exit 0; not run from an AI assistant); engine, API, benchmarks and auth are tested with sample data; the web app is not tested yet (lint and build only). 64/100 on our own rubric, down from 67.

See [CHANGELOG](CHANGELOG.md).

## Demo

[Transcript of the demo (2:12)](https://shipitworks.com/onegin/transcript/) · video on the [product page](https://shipitworks.com/onegin/)

The demo voice is AI-generated (ElevenLabs, "Bella") and the demo shows made-up data. The video says so at the end.

## Source code

The source is private for now. This repository holds the public record for the product: this README and a CHANGELOG, and soon a LICENSE. Until the source is public, the [product page](https://shipitworks.com/onegin/) is the source of truth, and the score above is the one to trust.

## How we work

Say only what we can back. Say what is not finished before anyone asks. Name people, companies and tools to give credit. Collect as little data as possible. We use AI and say so: Claude (by Anthropic) helps write the code and wrote this README.

Full version: [github.com/ShipItWorks](https://github.com/ShipItWorks) · Contact: support@shipitworks.com

---

Drafted with Claude (Anthropic) from the product page on 2026-11-02. Owner review by Robert Sweetman: pending.
