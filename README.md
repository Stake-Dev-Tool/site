# stakedevtool.com

Marketing site for [Stake Dev Tool](https://github.com/Stake-Dev-Tool/stake-dev-tool),
built with [TanStack Start](https://tanstack.com/start), React and
Tailwind CSS v4.

> Source-visible, all rights reserved — see [LICENSE](LICENSE). The
> product itself (desktop app, cloud server, CLI) lives in
> [Stake-Dev-Tool/stake-dev-tool](https://github.com/Stake-Dev-Tool/stake-dev-tool)
> and is open source.

## Develop

```bash
pnpm install
pnpm dev          # http://localhost:3000
```

## Deploy

Vercel builds and deploys automatically: pushes to `main` go to
production (stakedevtool.com), any other branch gets a preview URL.
There is no manual deploy step.

## Structure

- `src/routes/`: one file per page — `index` (home), `features`, `cloud`,
  `pricing`, `cli` (CLI + MCP install), `open-source`, plus the legal set
  (`legal`, `terms`, `privacy`, `refunds`).
- `src/components/TestViewFigure.tsx`: the hero figure — the same mini
  slot front at three resolutions inside one app window, with a live SSE
  event ticker.
- `src/styles.css`: design tokens (spruce/mint/amber palette, Bricolage
  Grotesque + Geist type) and the few custom CSS pieces.

The site takes no payments — checkout happens in the dashboard
(app.stakedevtool.com) through Stripe. Keep pricing copy in sync with the
server's plan limits.
