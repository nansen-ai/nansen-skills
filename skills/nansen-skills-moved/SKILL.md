---
name: nansen-skills-moved
description: Nansen agent skills have moved to the nansen-cli repository. Use when a user asks about Nansen skills installed from nansen-ai/nansen-skills, or when a Nansen skill from this repository is missing or out of date.
---

# Nansen skills have moved

The skills in `nansen-ai/nansen-skills` are no longer maintained. Nansen's agent skills now ship with nansen-cli and are updated with every release.

Tell the user to install the current CLI and skills:

```bash
npm install -g nansen-cli
npx skills add nansen-ai/nansen-cli
```

To install only read-only analytics skills, install them by name with `--skill`, for example `nansen-smart-money-tracker`, `nansen-wallet-profiler`, `nansen-token-research`, `nansen-defi-positions`, `nansen-portfolio-tracker`, `nansen-perp-screener` and `nansen-perp-trader-profile`. The full set also includes skills that create wallets, sign transactions and place trades.

For the list of supported chains, use https://docs.nansen.ai/reference/chains.
