# Redesign spec — agreed, not yet built

Signed off by Jessy on 26 July 2026. Implement as written; the open questions were already
asked and answered. Answers are recorded in `decisions.md`.

## Why

The current page shows eleven units, a tower, and a log all at once. Samuel will use it
**alone**, and eleven choices is too many. The redesign leaves one obvious thing to do.

## 1 · Home screen

```
┌────────────────────────────────────────────┐
│  SAMUEL CODING STUDIO        [session timer]│
├────────────────────────────────────────────┤
│  SPEED TEST FIRST        [log today's WPM]  │  gate 1
├────────────────────────────────────────────┤
│  TODAY: MISSION 02 · BRICK CATCHER          │
│  Your goal: catch falling bricks            │
│                      [ START SESSION ▸ ]    │  the only button that matters
├────────────────────────────────────────────┤
│  THE ARCADE                                 │
│  [▶ 01 Atom Factory]  [locked] [locked] ... │
├────────────────────────────────────────────┤
│  LEARNING LOG · 4 sessions · best 26 WPM    │
└────────────────────────────────────────────┘
```

Missions 03–10 are no longer listed as cards. They appear only as locked bricks in the arcade —
he sees the road without being able to wander down it. The current mission card is the only
open door.

Keep: the editable studio nameplate, the 10-20-10 timer, the WPM licence gauge, the log,
backup/restore.

## 2 · The step runner

`START SESSION` opens a full-screen runner. **One step per screen.** Nothing else visible.

Each step has four fields:

| Field | Purpose |
|---|---|
| **DO** | The action, one sentence |
| **TYPE THIS** | The prompt, in mono. He types it; a copy button exists for long ones |
| **YOU SHOULD SEE** | Success criteria in his words, so he can judge it himself |
| **IF NOT** | The exact English to say to Claude to repair it |

Controls: `[ It worked ▸ ]` and `[ It didn't work ]`, plus back to the previous step.
**He can never skip forward.** Progress dots at the top: `Step 3 of 6 ●●○○○○`.

`It didn't work` reveals the IF NOT line. On the **second** press it offers a second repair
angle. Only on the **third** does it mention parking. Most stuck moments are a bad prompt,
not a bad day — parking must stay rare to mean anything.

The existing mission-brief data needs two new fields per step: `see` and `ifnot`.
Mission 1's six steps must be written out this way as part of this work.

## 3 · Gates

Nothing opens unless **both** are true:

1. Today's speed test is logged (already built, keep as is)
2. The previous mission is **built** or **parked**

Unit 00 is never gated — it is where he learns to take the speed test.

## 4 · Finishing, and parking

**Built** — Samuel presses the button himself. His call, his studio. Brick turns green
and the game becomes playable in the arcade.

**Parked** — he gives a reason in one line. Brick goes dashed grey, the reason appears in
the log, and the next mission unlocks. **A parked mission stays resumable**; finishing it later
turns the brick green.

Ten green bricks is what he wants. Parking costs him something visible without costing
him momentum.

## 5 · Encouragement

Never automatic praise. Every message contains a number about **his own past**.

- **On open:** one line, e.g. *"Your typing is up 7 WPM since your first test."*
- **After building:** *"Four games built. Atom Factory took 9 prompts; this one took 5."*
  (Requires counting steps/prompts per mission in the log.)
- **Milestone stamps**, awarded once and shown in the log:
  `First Ship` · `30 WPM Licence` · `Bug Hunter` (first bug he diagnosed himself, awarded on his
  first patch note) · `Five Games` · `Full Studio` (all ten green)
- **End of session card:** what he did today, and the one number that moved.

Sessions counted. Consecutive-day streaks are explicitly rejected.

## 6 · The Arcade

Finished games are committed to the repo as `games/NN-slug.html` — e.g. `games/01-atom-factory.html`.

- A brick becomes a **play button** when its file exists. Detect by attempting to load it;
  fall back to a stored "shipped" flag so a slow network never hides his work.
- `games/index.html` — a shareable arcade page listing everything he has made, so grandparents
  open one link and play. Same visual identity, no chrome from the main app.
- Every mission gains a final **ship** step: download the artifact → upload it to `games/` →
  tick Shipped. Finishing isn't finishing until it ships. This is the most valuable habit
  in the whole project; don't quietly drop it because it's manual.

## Out of scope — decided, do not add

Accounts, PINs, parent login, Firebase/Supabase, cross-device sync, day streaks,
leaderboards, anything that sends Samuel's data off the device.
