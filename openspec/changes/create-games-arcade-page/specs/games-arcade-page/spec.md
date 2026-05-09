## ADDED Requirements

### Requirement: Spanish Arcade Home Page
The system SHALL replace the starter homepage with a Spanish-language arcade portfolio page for showcasing the creator's games.

#### Scenario: Visitor opens the home page
- **WHEN** a visitor navigates to `/`
- **THEN** the page presents a game-focused hero and game catalog instead of Astro starter content

### Requirement: Mockup-Inspired Visual Direction
The system SHALL use the visual direction from `prd/mockups/stitch_interactive_game_arcade/`, including a dark premium arcade aesthetic, geometric headings, refined card surfaces, and restrained accent colors.

#### Scenario: Visitor views the page on desktop
- **WHEN** the homepage is rendered on a desktop viewport
- **THEN** the page uses a polished dark arcade layout with prominent hero content and card-based game presentation

### Requirement: Responsive Game Catalog
The system SHALL display games in a responsive catalog that highlights a featured playable game and includes secondary cards for upcoming or in-development games.

#### Scenario: Desktop catalog layout
- **WHEN** a visitor views the catalog on a desktop viewport
- **THEN** the featured game receives stronger visual emphasis than secondary games

#### Scenario: Mobile catalog layout
- **WHEN** a visitor views the catalog on a mobile viewport
- **THEN** the game cards remain readable and usable in a single-column or otherwise mobile-appropriate layout

### Requirement: Game Availability States
The system SHALL clearly communicate each game's availability state, including live/playable, upcoming, and in development where applicable.

#### Scenario: Visitor compares game cards
- **WHEN** the visitor scans the catalog
- **THEN** each game card exposes a visible status label or equivalent state indicator

### Requirement: Playable Game Action
The system SHALL provide a clear action for any live/playable game and avoid presenting unavailable games as playable.

#### Scenario: Visitor chooses a live game
- **WHEN** a game is marked as live or playable
- **THEN** the card includes an actionable control to play or open the game

#### Scenario: Visitor views an unavailable game
- **WHEN** a game is upcoming or in development
- **THEN** the card communicates its unavailable state without a misleading playable action

### Requirement: Static Astro Implementation
The system SHALL remain compatible with the existing static Astro build workflow.

#### Scenario: Production build runs
- **WHEN** `pnpm build` is executed
- **THEN** the site builds successfully without requiring a backend service or runtime API
