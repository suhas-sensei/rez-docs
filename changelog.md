## 2026
### February 3
---
### Changes

#### Completed Trades Dashboard
- Sort/filter dropdown with options: Date, P&L, Holding Time, Entry Price, Exit Price, Quantity
- Filter icon in status bar header next to trade count
- Entry → Exit price display for each trade
- Quantity with dollar value in brackets (e.g., `Qty: 0.00555 ($439.17)`)
- "View Transaction" link to Hyperliquid testnet explorer
- Limit display to 150 most recent trades
- Show completed trades when agent is stopped

#### P&L Calculation
- `fetchTotalPnL()` function using Hyperliquid's `clearinghouseState` and `userNonFundingLedgerUpdates` APIs
- Total P&L now matches Hyperliquid UI (`accountValue - deposits`)

#### Holding Time
- FIFO matching of opening fills to closing fills
- `formatHoldingTime()` helper for human-readable duration

### Changed

#### API
- Added `hash` field to trade data from Hyperliquid fills API
- Added `tid` (trade ID) field
- Added `dir` field to identify Close Long/Close Short trades
- Win rate calculation now only counts closing fills

### Fixed

- Stats showing incorrect P&L values ($0.8 instead of $81)
- Sorting not working due to React state/render timing issues
- Small decimal precision handling in quantity sorting


### January 29

---

### Global Currency & Timezone Support

#### Highlights
-  Unified currency conversion across dashboard
-  Timezone-aware timestamps for logs & trades
- Centralized formatting via global contexts

####  Updated Areas
- Portfolio balance & P&L
- Live & historical charts
- Aggregate ticker bar
- Agent stats & messages
- Positions, trades & transactions
- Token info & market metrics

#### Settings
- Change **display currency** (auto-converted from USD)
- Select **timezone** (applies to all timestamps)
- Save / discard changes safely

> All prices, balances, and timestamps now reflect your selected preferences consistently across the app.
---
### January 28

---

###  Portfolio UI & Agent Stats Update

- Added visual **Agent Stats Circles** in Growth view  
-  Removed Agent Stats tab from dashboard  
-  Logout support with session reset  
-  Wallet address display with copy action  
-  Improved spacing, scrolling, and responsiveness

> Performance insights are visually informative with metrics.
