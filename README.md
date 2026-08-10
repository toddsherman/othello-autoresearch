# Othello, Overnight — an AI agent's research journey

A static site replaying a multi-night experiment: an AI agent teaches a small GPT
to play Othello, five minutes at a time, then we look inside the trained model.

- **Act I — learning to compress**: the agent minimizes `val_bpb`; legal play emerges then diverges.
- **Act II — learning to play**: the agent maximizes complete legal games (62.7%).
- **Act III — looking inside**: a linear probe shows the Othello board is represented inside the model at 92.8% per-square accuracy.

## Structure
`index.html` is **self-contained** — the run data is inlined, so the page works
standalone and when proxied under a subpath (e.g. `todd.sh/Othello`). It is
generated from run telemetry in the [autoresearch fork](https://github.com/toddsherman/autoresearch)
(`site/index.html` + `site/data.js`, inlined). To regenerate: rebuild `data.js`
with `site/build_data.py`, then inline it into `site/index.html`.

Deploy: static, no build. On Vercel: framework preset "Other".
