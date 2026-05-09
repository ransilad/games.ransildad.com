## Why

The site currently shows the Astro starter page instead of a portfolio experience for published and upcoming games. A dedicated arcade-style landing page will give visitors a clear, polished place to discover available titles and track upcoming games.

## What Changes

- Replace the current home page with a Spanish-language game showcase inspired by the mockup in `prd/mockups/stitch_interactive_game_arcade/`.
- Add a hero section that introduces the game universe and provides a prominent visual entry point.
- Add a responsive games grid with one featured playable game and supporting cards for upcoming/in-development games.
- Add visual states for games such as live, upcoming, and in development.
- Preserve Astro as a static site with no new runtime backend requirement.

## Capabilities

### New Capabilities
- `games-arcade-page`: Covers the public home page experience for presenting playable and upcoming games.

### Modified Capabilities

None.

## Impact

- Affects `src/pages/index.astro`, `src/layouts/Layout.astro`, and likely homepage-specific components/styles.
- May replace starter content in `src/components/Welcome.astro` or introduce a new homepage component.
- Uses the existing Astro build flow via `pnpm build`; no API, database, or deployment changes are expected.
