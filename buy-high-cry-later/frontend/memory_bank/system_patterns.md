# System Patterns – Buy High, Cry Later

## Architecture

- Frontend-only web application.
- Built using React + Tailwind CSS.
- Charts rendered using Recharts.

## UI Components

- Settings screen (form inputs + start button).
- Main screen with:
  - 4 stock charts (2x2 grid).
  - Large detail chart.
  - Timeline slider.
  - Portfolio panel for Player + 3 AIs.

## State Management

- Local React state for simulation loop.
- AI investment logic triggered on each tick.
