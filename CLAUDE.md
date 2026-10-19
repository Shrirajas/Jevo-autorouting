# Jevo

Jevo is a local model router for coding agents (a rebrand of Jevonian). `jevo-claude` runs
Claude Code through it: Jev picks the model for every turn, and the vendored
`vendor/jev-skill-router` suggests the best-fitting installed skill.

- **Setting this up on a new machine?** Follow [SETUP.md](SETUP.md) step by step. Ask the human
  for every API key; never invent or commit one.
- Build and test: `pnpm install && pnpm build && pnpm test`.
- The CLI command, config paths, env vars and model ids still say `jevonian`; only the
  user-facing name is Jevo. Keep it that way so existing setups keep working.
