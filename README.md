# EDY CU

Jakarta, Indonesia · Remote (async-first)
edy.cu@live.com · github.com/edycutjong · linkedin.com/in/edy-cu-tjong · edycu.dev

## SUMMARY

Full-stack engineer specializing in agent infrastructure and MCP (Model Context
Protocol) — building the safety layer that lets AI agents act on real systems:
transaction lifecycles, human-in-the-loop approval, spending caps, approval
revocation, prompt-injection defense. TypeScript · Python · Go · Rust.
14 years shipping software.

## SELECTED PROJECTS

**BagOS — MCP server for Solana** · TypeScript, Solana Web3.js, MCP SDK

- Shipped v2.0.0 to npm with provenance; listed in the official MCP registry.
  Full write-path lifecycle: simulate → approve → sign → send → confirm, with
  per-transaction and per-session spending caps, devnet by default.
- Caught and publicly remediated a fake-success defect in v1: deprecated the
  release, published the postmortem, and added CI gates (tarball audit,
  fabricated-success grep) that make the bug class unshippable.
- 212 tests with enforced 100% coverage; CodeQL and secret scanning clean;
  CI/CD with signed publishing and auto-deprecation.

**aegis — multi-agent support engine with human-in-the-loop** · Python, FastAPI, LangGraph

- Agent investigates issues via SQL and documentation, proposes actions, and
  hard-stops for human approval before any destructive operation.

**revoker — approval hygiene for automated wallets** · EVM

- Threat rules auto-revoke dangerous token approvals on agent, keeper, and
  relayer signers before drain contracts execute; demonstrated on-chain.

**antigen — prompt-injection defense for metadata graphs** · DataHub

- Sweeps catalog entities for jailbreak and exfiltration payloads, including
  invisible-Unicode variants; defuses them in-graph with tamper-evident hashes
  and maps blast radius through lineage.

**armsmith — ARM/Graviton benchmark toolkit** · Python

- Signed releases on PyPI via trusted publishing; versioned documentation.

## SKILLS

**Languages:** TypeScript, Python, Go, Rust, SQL
**Systems:** MCP servers, Solana (Web3.js / Anchor), EVM, Node.js, FastAPI,
Next.js, PostgreSQL, Supabase
**Practices:** CI/CD (GitHub Actions), signed/provenance publishing (npm, PyPI),
CodeQL, enforced coverage gates, Docker
