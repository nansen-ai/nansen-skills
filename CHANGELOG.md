# Changelog

## [2.0.0] - 2026-11-10

### Deprecated
- This repository is no longer maintained. Nansen's agent skills now ship with [nansen-cli](https://github.com/nansen-ai/nansen-cli/tree/main/skills). Install them with `npx skills add nansen-ai/nansen-cli`.

### Removed
- `claude-code/`, `openclaw/` and `references/`. They targeted nansen-cli 1.3.1, and their chain lists were out of date. They remain in git history.

### Added
- `skills/nansen-skills-moved`, which points agents that install from this repository to the nansen-cli skills.
- MIT `LICENSE`, matching nansen-cli.

## [1.0.2] - 2026-02-16

### Updated (CLI v1.3.1 compatibility)
- **`references/schema.json`** — Regenerated from `nansen-cli@1.3.1`. Now includes composite commands, correct return fields, and new global options
- **`profiler search`** — Removed "Currently unavailable" marker (fixed in CLI v1.3.1)
- **`profiler related-wallets`** — Removed CLI bug warning (invalid `filters` field fixed in CLI v1.3.1)
- **`profiler pnl-summary`** — Removed CLI bug warning (invalid `filters` field fixed in CLI v1.3.1)
- **`profiler perp-positions`** — Removed CLI bug warning (invalid `pagination` field fixed in CLI v1.3.1)
- **`token flow-intelligence`** — Removed CLI bug warning (invalid `pagination` field fixed in CLI v1.3.1)

### Added
- **`profiler batch`** — New composite command: profile multiple addresses in one operation
- **`profiler trace`** — New composite command: multi-hop BFS counterparty tracing
- **`profiler compare`** — New composite command: compare two wallets (shared counterparties, tokens)
- **`token transfers`** — Documented `--from`, `--to`, and `--enrich` options (new in CLI v1.3.1)
- **Global options** — Documented `--format csv`, `--cache`, `--cache-ttl`, `--stream` in `commands.md` and Claude Code CLAUDE.md

## [1.0.1] - 2026-02-15

### Fixed
- **Chain list** — Removed `zksync` and `unichain` (API rejects both); updated count from 20 → 18 in all files
- **Field names in `commands.md`** — Updated all `Returns` fields to match actual API responses (e.g., `balance` → `token_amount`, `balance_usd` → `value_usd`, `tx_hash` → `transaction_hash`, `wallet_address` → `trader_address`, etc.)
- **`profiler pnl`** — Marked as "Currently unavailable" (returns 404)
- **`profiler search`** — Marked as "Currently unavailable" (returns 404)
- **`profiler transactions`** — Documented required `--date` parameter (undocumented in schema)
- **`token flows`** — Documented required `--date` parameter
- **`token who-bought-sold`** — Documented required `--date` parameter
- **`profiler related-wallets`** — Documented CLI bug (sends invalid `filters` field)
- **`profiler pnl-summary`** — Documented CLI bug (sends invalid `filters` field)
- **`profiler perp-positions`** — Documented CLI bug (sends invalid `pagination` field)
- **`token flow-intelligence`** — Documented CLI bug (sends invalid `pagination` field)
- **`token jup-dca`** — Documented as Solana-only
- **`portfolio defi`** — Updated return structure to match actual `summary` + `protocols` format
- **Schema `returns` arrays** — Note: `schema.json` returns arrays are from upstream CLI and contain idealized names; see `commands.md` for accurate field names
- **Claude Code docs** — Updated to match OpenClaw skill changes

## [1.0.0] - 2026-02-15

### Added
- **`references/` directory** — shared API docs, cached schema, chain list, label definitions, and example responses
- **`references/schema.json`** — cached `nansen schema` output; skills reference this instead of running the command each time
- **`references/examples/`** — truncated JSON response examples for each major command domain
- **`openclaw/nansen-router/`** — routing/orchestrator skill that acts as the entry point for all Nansen queries
- **`CHANGELOG.md`** — this file

### Changed
- **OpenClaw skills** — refactored to be concise (routing + rules + examples); detailed parameter docs moved to `references/`
- **Claude Code skills** — streamlined per-domain `.md` files; reference shared `references/` directory
- **`README.md`** — updated to reflect new structure, router skill, and references directory

### Removed
- **`nansen-cluster-detective`** — removed from both openclaw/ and claude-code/ (not validated; delegation gap, param bugs). Will be re-added after validation.
