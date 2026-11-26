# Satu Garis on Solana

Daily one-stroke puzzle — trace a shape in one continuous line without lifting your finger or retracing an edge. One new puzzle every day, for every player. Streaks and leaderboard, now on Solana.

> **Dev3pack Global Hackathon 2026 (27–29 Nov)** — Track: **Best App Overall**
> Status: pre-hackathon scaffolding. Built 27–29 Nov 2026.
> Original game (Reddit Devvit app, live playtest): https://www.reddit.com/r/satu_garis_dev/?playtest=satu-garis

## How it works

- **Daily puzzle** — one shape per day, same for everyone. Trace it in one stroke: no lifting, no retracing an edge.
- **Streaks** — play every day to keep your streak alive. Each completed day is recorded on-chain.
- **Leaderboard** — daily and all-time rankings, readable on-chain.

## Solana integration (built during the hackathon)

- **Wallet login** — connect with a Solana wallet (Phantom / Solflare). No email, no password.
- **Streaks on-chain** — every completed daily puzzle sends a memo transaction to Solana recording the day + wallet. Your streak is verifiable on-chain, not just in our database.
- **Leaderboard on-chain** — rankings derived from on-chain completion records.

## Project structure

```
app/        Web app (game client: puzzle board, daily puzzle, streaks UI)
program/    Solana program (Anchor) — streak + leaderboard accounts
```

## Development

Prerequisites: Node.js 22+, Solana CLI, Anchor.

```bash
# app
cd app
npm install
npm run dev

# program
cd program
anchor build
anchor deploy --provider.cluster devnet
```

## License

MIT
