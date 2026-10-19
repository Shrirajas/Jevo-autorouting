# Vendored: jev-skill-router

Source: https://github.com/shimo4228/jev-skill-router (MIT, see LICENSE), commit `ad3b942`.
Only `scripts/` is vendored; tests, evals and the plugin wrapper stay upstream.

Jevo runs `scripts/route.py` as the `UserPromptSubmit` hook of `launch claude`
(see `src/skillroute.ts`), so a fresh clone needs nothing besides `python3`.

Local change to upstream:

- `scripts/route.py`: `JEV_ROUTER_INJECT_BUDGET_S` overrides the 3 s inject budget
  (`inject_budget_s`). Two Jev calls over a ~120-skill roster took 2.5-3.4 s, so the
  fixed 3 s dropped good suggestions. Jevo sets 5 s.
