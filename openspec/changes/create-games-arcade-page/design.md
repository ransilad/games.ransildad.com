## Context

The current Astro home route (`src/pages/index.astro`) renders the starter `Welcome.astro` content. The requested change is a Spanish-language game portfolio page based on `prd/mockups/stitch_interactive_game_arcade/`, with a premium dark arcade/gallery aesthetic and no backend requirement.

The implementation should stay within the existing Astro static-site setup, use `pnpm build` as verification, and avoid adding framework or styling dependencies unless the final design cannot be implemented with local Astro/CSS.

## Goals / Non-Goals

**Goals:**

- Replace starter content with a polished game showcase homepage.
- Reflect the mockup's elevated dark arcade direction: deep slate surfaces, glass-like cards, crisp borders, geometric typography, and restrained accent colors.
- Present at least one playable/featured game and additional upcoming or in-development games.
- Work well on desktop and mobile using responsive layout behavior.
- Keep the site static and simple to maintain.

**Non-Goals:**

- No authentication, player accounts, persistent search/filter state, game backend, or CMS integration.
- No dynamic inventory of games from a database or external API.
- No requirement to exactly copy Tailwind markup from the mockup; the mockup is visual direction, not a dependency decision.

## Decisions

- Implement the arcade page as Astro markup and component-scoped/global CSS rather than adding Tailwind. The mockup uses Tailwind CDN for prototyping, but this repository has no Tailwind dependency and the required visual system can be represented directly in CSS with less setup.
- Keep game data close to the homepage implementation for now. The site only needs a small curated list, so a local array or inline Astro data is simpler than a content collection or JSON pipeline.
- Prefer replacing or bypassing `Welcome.astro` instead of extending it. The existing component is starter content and does not represent product architecture.
- Use static links for game actions. Playable games should expose a clear call to action, while unavailable games should communicate their status without implying they can be launched.
- Update document metadata in `Layout.astro` as needed so the homepage no longer advertises Astro starter branding.

## Risks / Trade-offs

- [Risk] The mockup references external fonts and remote image URLs that may not be suitable for production. -> Mitigation: use resilient font stacks or explicitly load approved web fonts, and replace remote placeholder imagery with local assets or CSS treatments where possible.
- [Risk] A static list of games can become repetitive to update as the catalog grows. -> Mitigation: keep the data structure easy to extract into a content collection later.
- [Risk] Search UI can imply functionality that does not exist. -> Mitigation: either implement client-side filtering for the static cards or omit/disable search until it is meaningful.
- [Risk] Visual polish may reduce accessibility if contrast, focus states, or semantic structure are overlooked. -> Mitigation: preserve semantic headings, visible focus styles, accessible labels, and sufficient color contrast.
