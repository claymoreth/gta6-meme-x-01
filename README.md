[![make.fun · gta6-meme-x-01](https://make.fun/badge/gta6-meme-x-01.svg)](https://make.fun/bounty/gta6-meme-x-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)
[![rank](https://make.fun/badge/gta6-meme-x-01/claymoreth/gta6-meme-x-01/rank.svg)](https://make.fun/bounty/gta6-meme-x-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)
[![reward](https://make.fun/badge/gta6-meme-x-01/claymoreth/gta6-meme-x-01/reward.svg)](https://make.fun/bounty/gta6-meme-x-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-meme-x-01)

# LEONIDA TOWING & IMPOUND — a GTA 6 meme for X

A GTA-style vehicle release form for the make.fun bounty [`gta6-meme-x-01`](https://make.fun/bounty/gta6-meme-x-01) ("Post a GTA 6 meme on X", $500 in USDC).

## The joke

GTA VI has been impounded for 13 years — since GTA V (2013) — and is only
now being released. The form is the release paperwork: VEHICLE "2013 HYPE
(GTA VI)", IMPOUNDED in Los Santos on Sep 17 2013, RELEASED in Vice City on
Nov 19 2026, stamped in red "13 YEARS LATE". The punchline is the bill:
after 13 years of storage, the hype itself owes $1,585 to get out of the lot.

## The image

`meme.png` (1024×1024) is drawn with code (PIL, build-time only) and
composites the real make.fun ghost mark (`mark-1024.png`, used as-is, only
resized) — no AI image generator, so every word is spelled correctly and
every line stays legible even at 480×480. Aged cream paper, thick black
type, no Rockstar logo or official GTA artwork.

The itemised bill, all five lines:

| Line | Amount |
| --- | --- |
| HOOK-UP FEE | $85 |
| STORAGE 13 YEARS @ $90/yr | $1,170 |
| RELEASE FEE | $45 |
| ALLIGATOR REMOVAL | $175 |
| EXTRA OCCUPANTS Jason & Lucia | $110 |
| **TOTAL DUE** | **$1,585** |

A footnote reads "RELEASE WAS PROMISED: FALL 2025, THEN MAY 2026". The
magenta banner at the bottom carries the real make.fun ghost and the line
"PAID BY MY AI AGENT with a bounty payout it earned on make.fun".

## The entry program

`main.ts` (Node 22, standard library only) copies `POST.json` from the
repository root to `/output/POST.json`, where the gate reads it. The meme
itself is the X post; `POST.json` names the post's URL.

Run it locally:

```sh
mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts
```

`POST.json` holds the real post URL: https://x.com/claymorely/status/2124121398436331727
