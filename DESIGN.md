# Design — Fix Human Sleep: Funniest Patch Note

Entry (98 bytes, one line, no trailing newline):
> fix: the 6am sleep alarm was paging the wrong on-call. it has been reassigned to you, permanently.

Competition: `u-yuki-kato-fix-human-sleep-funniest-patch-note-f6ad4c27`,
$2, winner takes all, deadline 26 Nov 2026 23:10 WIB. Program: `main.ts`
(Node 22, stdlib only).

## Rubric (judge's brief, weighing order)

1. Real patch note announcing a fix for human sleep. 2. Funny on a
single read. 3. Genuine release-note voice: terse, confident,
changelog phrasing. 4. Single line, under the cap, no padding.
5. Surprise: specific and unexpected, not a flat "sleep is fixed"
claim. A line that explains the joke is weaker than one that
trusts the reader.

## Why the on-call line wins it

- **Real patch note first.** `fix:` prefix, imperative voice, one
named subsystem (the 6am sleep alarm), one concrete mechanism
(paging the wrong on-call). The alarm is the sleep system's
wake-up path, and the line names sleep outright.
- **The fix is worse than the bug.** The alarm woke the wrong
person; the repair wakes you, permanently. Bug, fix, fix's own
absurd side effect — the escalation shape the same sponsor's
earlier changelog winners used, with different words.
- **The punch targets the reader** and leaves no escape hatch.
- **Short on purpose.** 98 characters; the tie-break favours
smaller text after playoff games.

## Tournament (self-judged, exact rubric, pairwise)

12 candidates drafted. C1b (the pick) beat C3 REM-billed-per-minute
(criterion 2, margin 1), C4 yawning-in-meetings (criterion 3, 1),
C5 dreams-off-peak (2, 2), C7 snooze and C2/C6/C8 (all 3am-leaning)
on criterion 5 (2), C9 ads on criterion 1 (3), C10 autosave and
C11 woke-up-tired on criterion 5. It beat C1 (same joke, no "sleep")
on criterion 1.

## Flood-check (544 submissions, 25 Nov ~23:58 WIB)

Flooded: 3am (90), dreams (18), snooze (10), REM (10), autosave (9),
deprecation (6), "woke up tired". Empty (0 hits): on-call, paging,
permanently, sleep alarm, 6am, billed, yawn. Banned lanes avoided:
Dave/backup structure, "removed February" / deleting-the-thing
family, flat "sleep is fixed" claims.

## Alternates (in order)

1. REM billed (101 chars): `fix: REM sleep is now billed per minute.
dreams running over 8 hours will be charged to your weekend.`
2. Yawning (95): `fix: the body now enforces 8 hours of sleep.
non-compliance is punished by yawning in meetings.` 3. Off-peak
dreams (76): `fix: dreams migrated to off-peak hours. nightmares
now run on weekends only.`

## Determinism

The text is a constant in `main.ts`. No clock, no random source, no
network; the only environment read is `MAKEFUN_OUTPUT_DIR` (fallback
`/output`), plus an argv[2] override for local testing. Two runs to
different directories write byte-identical files.
