# Edy Cu

I build the safety layer that lets AI agents move real money: spend caps, human sign-off, approval revocation and prompt-injection defense. My work is mostly MCP servers and on-chain tooling in TypeScript and Python.

Jakarta, Indonesia (UTC+7) · Open to remote, async-first · [edy.cu@live.com](mailto:edy.cu@live.com) · [LinkedIn](https://linkedin.com/in/edy-cu-tjong) · [edycu.dev](https://edycu.dev)

---

## Proof

| | |
|---|---|
| 🏆 **Track winner, QwenCloud Hackathon 2026** | [Tarmac](https://github.com/edycutjong/tarmac): Track 3, Agent Society. US$7,000 cash prize. [Submission](https://qwencloud-hackathon.devpost.com/submissions/1103857-tarmac) |
| 🔀 **Merged upstream** | [KeeperHub PR #2277](https://github.com/KeeperHub/keeperhub/pull/2277): trace-method availability probe with 38 tests. Two review rounds; shipped in [v3.5.0](https://github.com/KeeperHub/keeperhub/releases/tag/v3.5.0) |
| 🥈 **2nd place, Nansen CLI Build Challenge (week 2)** | [NansenTerm](https://github.com/edycutjong/nansen-term), one of 4 entries, one in every week of the challenge ([all submissions](https://academy.nansen.ai/en/help/articles/6399546-nansen-cli-builds)) |
| 📦 **In use** | [`bagos-mcp-server`](https://www.npmjs.com/package/bagos-mcp-server) on npm, published with provenance and listed in the [MCP Registry](https://registry.modelcontextprotocol.io/?q=bagos) |

## Selected work

**[BagOS](https://github.com/edycutjong/BagOS)**: an MCP server that lets an AI agent trade on Solana without being able to drain the wallet. TypeScript, MCP SDK, @solana/web3.js.
- Every write goes simulate → preview → single-use confirmation → sign → confirm, with per-transaction and per-session SOL caps.
- I found a fake-success bug in v1, deprecated that release, [documented it in the 2.0.0 changelog](https://github.com/edycutjong/BagOS/blob/main/CHANGELOG.md), and added CI gates that make that class of bug unshippable.
- An outside adversarial review found a critical wallet-drain: a cloned repo's `.env` could redirect sign-in, and the sign-in step would sign a transaction. I fixed it in a private fork, shipped 3.0.0, deprecated every affected version on npm, and published [GHSA-g679-3wq7-mh3m](https://github.com/edycutjong/BagOS/security/advisories/GHSA-g679-3wq7-mh3m).
- I made the session cap safe under concurrent calls and fail closed when a trade's outcome is unknown ([postmortem](https://github.com/edycutjong/BagOS/blob/main/docs/postmortem-session-cap.md)).
- 407 tests at 100% line and branch coverage. CodeQL, gitleaks, SLSA provenance on every release.

**[Tarmac](https://github.com/edycutjong/tarmac)**: a group of agents that rebooks passengers after flight disruptions, using sealed-bid seat allocation and a hash-chained audit log that can be re-verified byte for byte in the cloud. Python, Qwen, Alibaba Cloud Function Compute. *Hackathon track winner.*

**[revoker](https://github.com/edycutjong/revoker)**: threat rules that revoke dangerous token approvals on agent, keeper and relayer wallets before a drain contract can use them. Demonstrated on chain through KeeperHub; built for the [Agents Onchain](https://dorahacks.io/buidl/47528) hackathon.

**[aegis](https://github.com/edycutjong/aegis)**: a multi-agent support engine (FastAPI, LangGraph) that investigates through SQL and docs, proposes actions, and stops for human approval before anything destructive.

**[antigen](https://github.com/edycutjong/antigen)**: finds and defuses prompt-injection payloads in a DataHub metadata graph, including invisible-Unicode variants, and maps the blast radius through lineage.

## How I work

- **I ship with AI coding agents, and I verify what they write.** Every claim in a README has to match the code; I've published commits titled *"correct the claims an audit disproved"*. Tests are named after the defects they prevent.
- **I publish failures.** I write postmortems for my own bugs, including ones nobody else reported.
- **Conventional commits, release automation, and security scanning on every repo I keep.**

**Stack:** TypeScript, Python, SQL · MCP, Node.js, FastAPI, Next.js, PostgreSQL · Solana, EVM (Foundry) · GitHub Actions, npm/PyPI trusted publishing, Docker

<!-- EXPERIENCE: fill in from your CV, or delete this block. Only claims you can back with a reference or a link.
## Before this
**Company** · Title · 20XX–20XX: one line with a number in it
-->
<!-- 
<sub>More hackathon builds live at [edycu-hackathons](https://edycu.dev/hackathons).</sub>
-->
