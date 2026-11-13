# Nansen AI Skills (moved)

> [!IMPORTANT]
> **This repository is no longer maintained.** Nansen's agent skills now ship with [nansen-cli](https://github.com/nansen-ai/nansen-cli/tree/main/skills), where they are updated with every CLI release. The skills that used to live here were written for nansen-cli 1.3.1 and no longer match the current CLI.

## Install the current skills

```bash
npm install -g nansen-cli
npx skills add nansen-ai/nansen-cli
```

To install only some skills, pass `--skill`, for example:

```bash
npx skills add nansen-ai/nansen-cli --skill nansen-smart-money-tracker
```

Then connect your Nansen account: open [app.nansen.ai/auth/agent-setup](https://app.nansen.ai/auth/agent-setup), sign in, and paste the message it shows into your agent. You can also run `nansen login`, or set `NANSEN_API_KEY` with a key from [app.nansen.ai/api](https://app.nansen.ai/api).

## Where each old skill went

| Old skill (this repo) | Current skill in nansen-cli |
| --- | --- |
| nansen-router, nansen-core | `nansen-agent-guide` |
| nansen-smart-money | `nansen-smart-money-tracker` |
| nansen-profiler | `nansen-wallet-profiler` |
| nansen-token | `nansen-token-research` |
| nansen-portfolio | `nansen-defi-positions`, `nansen-portfolio-tracker` |
| nansen-hyperliquid | `nansen-perp-screener`, `nansen-perp-trader-profile` |

nansen-cli also includes skills that create wallets, sign transactions and place trades, such as `nansen-trading` and `nansen-wallet-manager`. This repository only had read-only analytics skills. If that's what you want, install the skills listed above by name.

## Supported chains

See [Supported Chains](https://docs.nansen.ai/reference/chains) in the Nansen docs. That page is kept current; this repository no longer lists chains.

## Links

- [nansen-cli](https://github.com/nansen-ai/nansen-cli) and its [skills](https://github.com/nansen-ai/nansen-cli/tree/main/skills)
- [Nansen API docs](https://docs.nansen.ai)
- [Nansen](https://nansen.ai)

The older skills remain in this repository's git history.
