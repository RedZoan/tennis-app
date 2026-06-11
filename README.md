# Tennis Match Tracker

A Progressive Web App for tracking MPSSAA high school tennis matches in real time. Designed for Mixed Doubles but supports all 9 courts (singles, doubles, and mixed).

## Features

**Live Match Tracking**
- Dynamic scoreboard with standard tennis scoring (0/15/30/40/AD) and automatic tiebreak logic
- Support for Standard format (best of 3) and Pro Set format (8 games, 7pt or 10pt tiebreaker)
- Per-player quick-entry buttons: Ace, Winner, Error, Double Fault
- Full point-by-point timeline with timestamps
- Edit any previous entry, hold-to-confirm undo (0.6s), or swipe left on the timeline to undo
- Haptic feedback on point entry

**Multi-Court Support**
- 9 pre-configured courts: 4 singles, 4 doubles, 1 mixed doubles
- Track Win/Loss results and player names for each court
- Automatic match result calculation from court outcomes

**Season Analytics**
- Win/loss record with donut chart and match history strip
- Per-court and per-player performance breakdown
- Player stat sparklines across the season
- By-opponent breakdown and detailed match view with full timeline

**GitHub Sync (Admin Mode)**
- Authenticate with a GitHub Personal Access Token
- Push match CSVs to the `/matches` folder so all visitors see live data
- Export/import matches as CSV for record-keeping

**PWA**
- Works fully offline — single HTML file, no external dependencies at runtime
- Add to home screen on iOS and Android
- Optimized for phones in both portrait and landscape

## Tech Stack

- Vanilla JavaScript, HTML5, Tailwind CSS — no frameworks, no build step
- `localStorage` for local data; GitHub Contents API for shared sync
- CSV for match data format

## Getting Started

1. Clone or download the repo
2. Open `index.html` in any modern browser — that's it

To enable GitHub sync, click the key icon in the season view and enter a Fine-grained Personal Access Token with **Contents: Read and write** access to this repo.

## Match Data

Saved matches live in the [`/matches`](matches/) folder as CSV files. Each file contains the final score, per-court results, player stats, and a full point-by-point timeline.

## License

MIT
