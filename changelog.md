## 2026


### March 5 — Mainnet Launch
---
### Changes

#### Mainnet Migration
- Rez is now live on **Hyperliquid mainnet** with all trades and transactions executing on real funds
- Wallet automatically switches to **Arbitrum mainnet** when approving an agent
- Transaction links now open on the mainnet explorer

#### Authentication & Deployment
- Integrated **Privy** authentication for production sign-in
- Production-ready Docker deployment configured

#### UI Updates
- Testnet mode under maintenance, currently configured for mainnet only. 

### February 25
---
### Changes

#### Branding & Copy
- Updated hero text from "The Future of Perps" to "Your personal Quant for perps"

#### Portfolio & Dashboard
- Relocated logout button to bottom of action buttons
- Added border styling to stat cards (Total Balance, Unrealized P&L, Margin Used)
- Removed desktop "waiting for agent" input section from TradesDashboard

#### Leaderboard
- Replaced leaderboard table with "Coming Soon" placeholder
- Removed mock leaderboard data and helper functions


### February 17
---
### Changes

#### UI Overhaul
- Removed typewriter animation, switched to static content display
- Standardized border radius and background shading across all pages
- Moved `PortfolioHeader` to display consistently across all tabs
- Added `InlineTicker` to Navbar

#### Agent Process Management
- Added `force_stop()` with SIGTERM → SIGKILL fallback for reliable process termination
- Agents no longer auto-start on server startup

#### P&L & Risk Profile
- Changed P&L calculation to use fixed initial deposit ($500) instead of net deposits
- Removed P&L percentage display from PortfolioHeader
- Increased border color intensity on risk profile selector


### February 12
---
### Changes

#### Responsiveness
- Further responsive design improvements across the app

#### Bug Fixes & UI
- General bug fixes
- Updated app icons

#### Stop/Pause Button UI
- Updated stop and pause button interface

### February 10
---
### Changes

#### Invite Code System
- Added invite code functionality for gated access

#### Migration to Prod
- Consolidated completed trades dashboard, P&L calculations, and holding time tracking into production
- Integrated comprehensive documentation suite (overview, getting-started, API reference, concepts, dashboard usage, troubleshooting)

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
