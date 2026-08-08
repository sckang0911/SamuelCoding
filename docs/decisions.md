# Decisions

Settled. If you find yourself proposing one of the rejected options, read the reason first.

| # | Decision | Rejected alternative | Why |
|---|---|---|---|
| 1 | Ten independent games, no final project | One large end-of-term project | A 9-year-old finishes ten things. Ten finished games beat one unfinished ambitious one. |
| 2 | English prompting throughout | Chinese, or bilingual | Samuel is fluent, AI precision is higher in English, and he practises describing logic in English as a side effect. |
| 3 | Claude Opus 5 with Artifacts | Claude 3.5 Sonnet (in the original plan) | Two generations newer; one-shots these games far more reliably, which matters when the build window is 20 minutes. |
| 4 | Unit 00 teaches the environment first | Straight into mission 1 | He needs to know the two windows, the version arrows, and that undo makes experimenting free. |
| 5 | Typing target 30 WPM. The test is **offered every session, never required** | A hard gate before missions unlock | A 25-word prompt takes 2½ min at 10 WPM and 50 sec at 30, so speed is build time — but see #13. The gate was built, then removed. |
| 6 | Single device, browser storage, JSON backup | Accounts and a backend (Firebase/Supabase) | Rejected by Jessy. Avoids storing a child's data with a third party and avoids owning a system. One "studio computer" also gives the studio a physical home. |
| 7 | Samuel declares a mission finished himself | Parent approval; or auto-check of steps | His studio, his call. Parent approval turns his hobby into something he needs a referee for. |
| 8 | He can park a failed mission with a reason | Hard lock until finished | A hard lock turns one bad Saturday into the end of the project. Parked bricks stay resumable and visibly grey. |
| 9 | One step per screen in the runner | All steps scrollable | Alone at the screen he will skim, miss step 3, and get lost at step 5. |
| 10 | Encouragement always cites a number from his own past | Automatic praise on every action | Constant praise stops carrying information and reads as hollow. |
| 11 | Count sessions, never consecutive days | Day streaks | Streaks punish holidays and illness and make a hobby anxious. |
| 12 | Games shipped as files in `games/` | Leaving them inside Claude chats | Otherwise his finished work is stranded and unplayable. Shipping is also the lesson. |
| 13 | **No gates at all.** Every unit is open from day one, in any order | Sequential unlock; the speed-test gate; parent approval | Reversed by Jessy after they were built. A curriculum he chooses is a hobby; one that admits him a door at a time is school. Nothing blocks him. |
| 14 | Samuel sets his own help level with a three-way dial | A fixed fade tied to mission order | Follows from #13 — if he can start at mission 07, help can no longer be decided by sequence. The written fade is now the default, not the rule. |

## Known soft spots

- **Nothing enforces order now.** The 100%→0% fade is written into the briefs, so jumping straight
  to mission 09 means meeting BUILD steps with no practice at them. The help dial is the mitigation.
  Watch whether he reaches for it or just gets stuck.
- **The typing test is easy to skip.** If WPM stops climbing, that is why. The answer is that it is
  *offered* prominently every session, not a return to blocking.
- **Mission 6 (Angry Blocks) is the real difficulty jump**, not mission 10 — a physics engine is the
  first time the AI produces something he can't fully predict. Keep its scope small:
  one tower, three shots.
- **Mission 1 step 3** asks for 8 electrons. Watch whether the payoff arrives before his patience
  runs out; cut to a smaller shell if not.
- **Manual ship step.** Downloading and uploading a file each week is friction. If it starts getting
  skipped, that is a signal to make it easier, not to drop it.
