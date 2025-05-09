# Buy High, Cry Later – Frontend

<!-- mdformat-toc start --slug=github --maxlevel=6 --minlevel=2 -->

- [Game Overview](#game-overview)
  - [Screen 1 – Settings](#screen-1-%E2%80%93-settings)
  - [Screen 2 – Gameplay](#screen-2-%E2%80%93-gameplay)
    - [Timeline](#timeline)
    - [Player Panel (Right Side)](#player-panel-right-side)
  - [Investment Logic](#investment-logic)
  - [ETF Creation](#etf-creation)
- [Memory Bank](#memory-bank)

<!-- mdformat-toc end -->

## Game Overview<a name="game-overview"></a>

**Buy High, Cry Later** is a browser-based investment simulation game built with React, Tailwind CSS, and Recharts. The game challenges players to grow their virtual portfolio over time while competing with three AI investors.

### Screen 1 – Settings<a name="screen-1-%E2%80%93-settings"></a>

The player starts by configuring their investment plan:

- **Years to invest** – default: `30`
- **Salary date** – default: `25`
- **Monthly savings** – default: `20,000`

Click the **Start** button to launch the simulation.

### Screen 2 – Gameplay<a name="screen-2-%E2%80%93-gameplay"></a>

- The game randomly selects 4 stocks from a predefined dataset.
- A 2x2 grid displays their price history as interactive charts.
- A larger chart shows more detail for a selected stock or ETF.

#### Timeline<a name="timeline"></a>

- A slider at the bottom represents the passage of time (month by month).
- Left label: months passed; right label: months remaining.
- A pause/play button includes a dropdown to adjust interval (0, 5, 10, 20, 30 seconds).
- The slider advances by 1 month, pausing as configured.

#### Player Panel (Right Side)<a name="player-panel-right-side"></a>

- 4 avatars: **You**, **A**, **B**, **C**
- Each avatar displays:
  - Total portfolio value
  - Cash on hand
  - Value in stocks/ETFs

### Investment Logic<a name="investment-logic"></a>

Each month:

- All players receive their monthly savings.
- AI behaviors:
  - **A** buys ETF immediately.
  - **B** waits and buys at the next dip.
  - **C** buys at the next peak.

Player options:

- Pause the game at any time.
- Use sliders to choose how many shares to buy across 4 stocks and 1 ETF.
- Real-time updates reduce your available cash as sliders are adjusted.
- Confirm purchases with the **Buy** button.

### ETF Creation<a name="etf-creation"></a>

At the start of the game:

- Two ETFs are generated based on the selected stocks:
  - **ETF 1**: equally weighted (25% each)
  - **ETF 2**: weighted by market cap or randomized weights

> The game runs entirely on the frontend and uses mock historical data for local development. No server is required.

______________________________________________________________________

## Memory Bank<a name="memory-bank"></a>

- [Project Brief](memory_bank/project_brief.md): core requirements and goals.
- [Product Context](memory_bank/product_context.md): purpose, UX goals.
- [Active Context](memory_bank/active_context.md): current tasks, decisions, next steps.
- [System Patterns](memory_bank/system_patterns.md): achitecture, design patterns, relationships.
- [Tech Context](memory_bank/tech_context.md): dev setup, constraints, tools.
- [Progress](memory_bank/progress.md): current status, what’s done, issues.
