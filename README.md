# Othello, Overnight — an AI agent's research journey

A static site replaying a multi-night experiment: an AI agent teaches a small GPT
to play Othello, five minutes at a time, then we look inside the trained model.

- **Act I — learning to compress**: the agent minimizes `val_bpb`; legal play emerges as a side effect, then diverges.
- **Act II — learning to play**: the agent maximizes complete legal games (62.7%).
- **Act III — looking inside**: a linear probe shows the Othello board is represented inside the model at 92.8% per-square accuracy.

Built on a fork of [karpathy/autoresearch](https://github.com/karpathy/autoresearch).
Two files, no build step: `index.html` + `data.js` (generated from run telemetry).

## Deploy
Static — deploy the repo root to any static host. On Vercel: import the repo, no framework, output = root.
