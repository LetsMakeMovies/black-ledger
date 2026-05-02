# Black & Ledger

> *"What is owed must be reckoned."*

A realistic, gothic-themed budgeting web app built for actual human life — bills, debts, fun money, savings goals, and the inevitable surprises. Runs entirely in your browser, stores everything locally, installs to your iPhone home screen as a PWA. No accounts, no servers, no Apple Developer fee.

## Why This Exists

Most budget apps assume you have surplus and choices. This one was built for a real situation: bi-weekly paycheck, real debt across multiple cards, collections, a credit score that needs rebuilding, and a life with a partner, coworkers, and the bar tab on a Saturday night.

It tells you the truth, not what you want to hear.

## Features

### The Reckoning (Today Tab)
- **"Safe to Spend Today"** — the one number that actually matters, accounting for upcoming bills before next paycheck
- This week's fun money tracker
- Upcoming bills with urgency indicators
- Recent activity feed
- Daily insights (over-pace warnings, S/O birthday reminders, debt status)

### Paycheck Allocation
- Visual waterfall: paycheck → bills → debt → savings → buffer → fun money
- "Mark Paycheck Received" auto-allocates to goals & buffer
- Paycheck history
- Knows your bi-weekly rhythm

### Bills
- Track recurring bills with monthly due dates
- Tap to mark paid (per-month tracking)
- Calendar view of the month
- Color-coded urgency (urgent / warning / safe)

### Debt
- **Hybrid strategy engine**: minimums on everything + snowball your smallest credit card
- Avalanche calc available, but recommends snowball for credit-utilization wins
- **Collections handled separately** with pay-for-delete advice (don't pay collections without negotiating)
- Debt-free date projection that updates with every payment
- Credit score tracker with history chart

### Goals
- Multiple savings goals with target dates
- "On pace" / "behind" indicators
- Per-paycheck recommendation math (e.g., "$60/paycheck to hit S/O birthday by July 14")
- Priority levels for auto-allocation
- Pre-populate or add over time

### Insights
- Last 7 days spending bar chart
- 30-day category breakdown (doughnut)
- Week-over-week comparison
- Top category callout

### Memory
- Everything saves to browser localStorage instantly
- Export full data as JSON
- Import to restore or transfer between devices
- Snapshots: freeze a moment in time to compare later

### iOS Home Screen Install
- PWA-enabled with service worker
- Add to Home Screen → launches fullscreen, no Safari chrome
- Works offline once loaded
- Looks and feels native

## Setup Locally

```bash
git clone https://github.com/YOURUSERNAME/black-ledger.git
cd black-ledger
# Open index.html in any browser, or...
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Host It Free

GitHub Pages:
1. Push to GitHub
2. Settings → Pages → Source: `main` branch
3. Visit `https://YOURUSERNAME.github.io/black-ledger`
4. On iPhone Safari: Share → Add to Home Screen

That's it. Free. Forever.

## Add Your Own Data

The onboarding asks for paycheck, frequency, fun money, and buffer. After that, add your bills, debts, and goals from their respective tabs. Everything is editable.

## Stack

- Single-file HTML + vanilla JS — no build step, no framework
- Chart.js (CDN) for visualizations
- Google Fonts: Cormorant Garamond, JetBrains Mono, Inter
- localStorage for persistence
- Service worker for offline / PWA

## Backups

Export your data periodically from Settings → Export JSON. localStorage is durable but not invincible — clearing browser data wipes it. The export is your insurance policy.

## License

Yours. Take it, modify it, ship it. No attribution required, but appreciated.

---

*Memento solvere.*
