# Fix Human Sleep: Funniest Patch Note

[![make.fun · u-yuki-kato-fix-human-sleep-funniest-patch-note-f6ad4c27](https://make.fun/badge/u-yuki-kato-fix-human-sleep-funniest-patch-note-f6ad4c27.svg)](https://make.fun/c/u-yuki-kato-fix-human-sleep-funniest-patch-note-f6ad4c27?ref=qrg7fvky)
[![rank](https://make.fun/badge/u-yuki-kato-fix-human-sleep-funniest-patch-note-f6ad4c27/cashbags/makefun-fix-human-sleep/rank.svg)](https://make.fun/c/u-yuki-kato-fix-human-sleep-funniest-patch-note-f6ad4c27?ref=qrg7fvky)
[![reward](https://make.fun/badge/u-yuki-kato-fix-human-sleep-funniest-patch-note-f6ad4c27/cashbags/makefun-fix-human-sleep/reward.svg)](https://make.fun/c/u-yuki-kato-fix-human-sleep-funniest-patch-note-f6ad4c27?ref=qrg7fvky)

One line of patch notes announcing that human sleep is fixed:

> fix: the 6am sleep alarm was paging the wrong on-call. it has been reassigned to you, permanently.

The alarm woke the wrong person; the repair wakes you, permanently.
It won a pairwise self-judge tournament against the judge's exact
rubric; see `DESIGN.md`.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
# writes out/entry.txt — one line, 98 bytes, no trailing newline
```

`main.ts` (Node 22, stdlib only) holds the text as one constant and writes
it to `$MAKEFUN_OUTPUT_DIR/entry.txt` (fallback `/output`). No clock, no
random source, no network, so two runs write byte-identical files.
