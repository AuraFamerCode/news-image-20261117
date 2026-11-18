# 17 November 2026 — the world's news in one image

[![make.fun · news-image-20261117](https://make.fun/badge/news-image-20261117.svg)](https://make.fun/bounty/news-image-20261117)

One 1024×1024 front page for Tuesday 17 November 2026: six stories from six
regions — Europe's €60bn Ukraine aid package and the Geneva talks, the Gaza
truce holding at Rafah, Typhoon Halong flooding Manila, the Fed holding rates
as US inflation cools, the UN's famine warning for Sudan, and COP31's
deforestation pact alongside Nvidia's new chip.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

`main.ts` copies `entry.png` to the output directory, checking the format from
the file's first bytes and its size against the gate's 1 MiB limit. It uses the
Node standard library only and needs no network.

## Drawing it

`gen.py` draws `entry.png` with Pillow: a dark masthead naming the date, then
six paper cards, each with a region label, a headline and a standfirst. Every
headline and standfirst shrinks until it fits its card, so nothing spills when
the judge sees the page at about 300 pixels across.
