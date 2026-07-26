# Curriculum

Design record. What ships is the `UNIT0` and `MISSIONS` data in `index.html`; keep this in step with it.

## The arc

Each mission teaches one **transferable idea**, not just one game. The prompting skill column
is the real curriculum — the games are the excuse.

| # | Game | New technical idea | New prompting skill | Brief |
|---|---|---|---|---|
| 00 | Know Your Studio | The tools, the two windows, undo | Writing a first spec at all | Written |
| 01 | Particle Clicker / Atom Factory ⭐ | Click → counter → feedback | What you see, what you do, what happens | Written |
| 02 | Brick Catcher ⭐ | Keyboard input, collision | Describing controls precisely | Preview |
| 03 | Meteor Dodge ⭐⭐ | Randomness, lose condition | Asking for difficulty curves | Preview |
| 04 | Extreme Table Tennis ⭐⭐ | Bounce angles, simple opponent | Tuning numbers by percentage | Preview |
| 05 | Science Memory Match ⭐⭐ | Game state, what's face up | Rules as if/then steps | Preview |
| 06 | Angry Blocks ⭐⭐⭐ | Gravity, force, collapse | Describing *feel*, not just rules | Preview |
| 07 | Typing Defender ⭐⭐⭐ | Text matching, live input | Connecting two systems he knows | Preview |
| 08 | Laser Maze Runner ⭐⭐⭐ | 2D movement, walls | Reproducing a bug exactly | Preview |
| 09 | T-Rex Dash ⭐⭐⭐ | Jump physics, scrolling illusion | Iterating toward a target | Preview |
| 10 | Tower Climber ⭐⭐⭐ | Camera follow, moving platforms | A full spec from scratch, unaided | Preview |

## Brief structure

Every mission follows the same four beats. Jessy specified this shape:

1. **A story with a real principle** — 3 minutes, spoken, ideally drawn on paper.
   Science where the game allows it; otherwise a principle of building.
2. **The goal** — one sentence, what he is making today.
3. **Five to eight steps** — each one prompt or one decision.
4. **Play it** — plus one patch note written as a proper bug report.

## Unit 00 · Know Your Studio

**Principle:** a computer does exactly what you SAY, not what you MEAN.
"Make it bigger" is a bad instruction; "make the ball twice as wide" is a good one.
The real skill of the whole course is describing a machine clearly enough that someone else
can build it — that works on developers, robots, AI, and parents.

Steps: warm up hands → first speed test (with the 30 WPM reasoning) → open claude.ai and check
the model says Opus 5 → learn the two windows and what an artifact is → build the studio front door →
change one thing and watch it rebuild wholesale → **break it on purpose and undo** → sign the three
studio rules.

The undo step is the most important one in the unit. Once he knows he cannot permanently ruin
anything, he will try anything.

**The three studio rules:** one problem per message · say exactly what you see, not "it's broken" ·
play it before you complain about it.

## Mission 01 · The Atom Factory

**Science:** nucleus positive and heavy, electrons negative and fast, held like a magnet holding bees.
Electrons sit in shells like seats in a stadium — **shell 1 has 2 seats, shell 2 has 8**.
One electron is hydrogen, two is helium, ten is neon. Full shells make the calmest atoms in the
universe — the noble gases. Nearly all of chemistry is atoms swapping electrons to fill their seats.

**Hook question:** helium balloons are safe, hydrogen balloons explode — both are gases, so what's
different about their shells?

**Goal:** click the nucleus to knock electrons loose, fill shell 1, then shell 2, levelling up
hydrogen → helium → neon.

Steps: start the engine (the long founding prompt) → fill shell 1 → fill shell 2 → add the juice
(shake and flash) → producer's call (one addition of his own, unaided) → stamp it with the studio
title screen.

**Success test** is not a polished game. It's whether he can answer *"why is neon a happy atom?"*
at dinner and point at something he made.

## Notes for writing missions 02–10

- Budget is **five or six prompts**. Steps 5 and 6 are always the flex; a working game beats a
  complete checklist. Never end a session on a broken artifact.
- Teach the **small correction**, not the rewrite. "The electrons are behind the nucleus, put them
  in front" — one sentence, one problem. That habit is the actual curriculum.
- The studio title screen goes on every game. Ten stamped games is a body of work.
- Science hooks still unassigned: Brick Catcher could go to gravity and terminal velocity, or to
  reaction time. Not yet decided.
