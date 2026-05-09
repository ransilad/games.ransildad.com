# AGENTS.md

## Project Facts
- Astro 6 site, ESM-only package (`"type": "module"`).
- Use pnpm; `pnpm-lock.yaml`, `.npmrc`, and `pnpm-workspace.yaml` are the package-manager sources of truth.
- Node is pinned to `v24.15.0` in `.node-version`; `package.json` only enforces `>=22.12.0`.
- `pnpm-workspace.yaml` only allows dependency build scripts for `esbuild` and `sharp`; keep that in sync with `.npmrc` if dependency build approvals change.

## Commands
- Install: `pnpm install`.
- Dev server: `pnpm dev` (`astro dev`, default `localhost:4321`).
- Production verification/build: `pnpm build` outputs to `dist/`.
- Preview built output: `pnpm preview`.
- Astro CLI: `pnpm astro ...`; there is no separate lint, test, or typecheck script configured.

## Structure
- `src/pages/` contains Astro routes; the current home route is `src/pages/index.astro`.
- `src/layouts/Layout.astro` owns the document shell, favicon links, and page title.
- `src/components/Welcome.astro` is still the starter homepage component; do not assume it reflects final product architecture.
- `public/` is for static files served from the site root; imported assets live under `src/assets/`.

## Existing Instruction Sources
- There was no pre-existing root `AGENTS.md`, `CLAUDE.md`, Cursor rules, Copilot instructions, CI workflow, or root `opencode.json` when this file was created.
- Repo-local OpenCode skill dependencies are tracked separately under `.opencode/` and `skills-lock.json`; they are not app runtime dependencies.
