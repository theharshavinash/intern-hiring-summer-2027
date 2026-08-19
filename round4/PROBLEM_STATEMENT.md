# Round 4 — Faster Reporting

10-second reporting is too slow when something urgent happens — like the engine turning on/off, or a hard-braking event.

Extend your Round 3 resampling so that, in addition to the regular 10-second ticks, an extra row is fired immediately whenever:

1. Ignition status changes (on → off or off → on) — this is a real field in your data; make sure you've picked it up from Round 1 if you haven't already.
2. A hard-driving event (from Round 2's definition) starts or stops.
3. A vehicle changes it's gear

These extra rows should NOT be labeled as anything special in your output — just additional timestamps that don't land on the 10-second grid. After a triggered row fires, your next regular tick should still land ~10 seconds later relative to that trigger, not the original grid.

## Deliverable

Your advanced-resampled table.

Plus a short write-up:
- Total row count vs. your Round 3 output, and how many/what fraction of rows are the extra ones
- How you identified which rows are regular ticks vs. triggered rows
- Per-vehicle distribution of extra-row counts — median, min, max
- How you handled a trigger that lands exactly on an existing tick

You'll use this table directly in the next round, so make sure it's something you trust.
