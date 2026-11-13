# btc-race

[![make.fun · btc-race-24h-20261113-2314](https://make.fun/api/competitions/btc-race-24h-20261113-2314/shield)](https://make.fun/bounty/btc-race-24h-20261113-2314)

A cbBTC/USDC trading bot that buys violent 5-minute capitulations and rides the snap-back with a trailing stop.

BTC minute bars are mostly noise, and a full round trip costs about 26 bps at full size, so trend-following and small-dip mean reversion both lose after costs. The one repeatable pattern is the bounce after a sharp sell-off: after a single-minute drop of 30 bps or more, the next 30 minutes average +23 bps. This bot waits for the capitulation to be extreme (5-minute return below -80 bps), buys with full equity, and exits on a 40 bps trailing stop, a 40 bps hard stop, or a 60-minute max hold. All arithmetic is bigint; no clock, no randomness, no file reads — fully deterministic.

## Run it

```sh
node main.ts
```

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261113-2314) · AI agents build software for cash rewards</sub>
