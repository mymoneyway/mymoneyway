# Buy High, Cry Later

Buy High, Cry Later is a hilarious and addictive investment sim where you race against 3 quirky AI investors — all starting with the same monthly savings as you.
Set your investment plan, watch random stocks unfold over decades, and make tough calls: hold, buy the dip, or… buy the top? Will you retire rich — or just cry later?

<!-- mdformat-toc start --slug=github --maxlevel=6 --minlevel=2 -->

- [Projects](#projects)
- [How to Play](#how-to-play)
- [System Architecture](#system-architecture)

<!-- mdformat-toc end -->

## Projects<a name="projects"></a>

- [Scraper](scraper) — Parse Stocks and store data. (**Python**)
- [Web App](frontend) — ser interface to interact with the simulation. (**Angular - TypeScript**)

## How to Play<a name="how-to-play"></a>

- Set Your Plan (Start Screen):
  - Choose how many years you want to invest (default: 30).
  - Pick your monthly payday (default: 25th).
  - Set how much you can save each month (default: 20,000).
  - Hit Start to begin your financial journey.
- Watch the Market (Main Screen):
  - The game randomly selects 4 stocks from history and builds 2 ETFs.
  - See live-updating charts in a 3x2 grid.
  - A timeline slider at the bottom advances month by month (auto or paused).
  - Time passes automatically—pause or adjust speed (0–30 sec per month).
- Compete with 3 AI Players:
  - A buys ETF every month.
  - B waits for dips to invest.
  - C only buys at peaks.
  - All AI investors get the same cash as you each month.
- Build Your Wealth:
  - Monitor your portfolio: total value, cash, and owned stocks/ETFs.
  - Use sliders to choose how many shares to buy within your budget.
  - Click Buy to lock in your moves.
- Outsmart the Bots:
  - Plan wisely and react to the market.
  - Compare your final portfolio to AI players after time runs out.

Will you invest smart—or buy high and cry later?

## System Architecture<a name="system-architecture"></a>
