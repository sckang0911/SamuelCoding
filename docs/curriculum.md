# Curriculum

Design record. What ships is the `UNIT0` and `MISSIONS` data in `index.html`; keep this in step with it.
**All eleven units are now written in full.**

## The three ladders

Three things climb at once across the course.

**1 · Difficulty of the game** — ⭐ to ⭐⭐⭐, clicker to platformer.

**2 · Science** — one principle per mission, chosen because the game *is* the principle.

**3 · How much wording he is given** — the important one. Every step sits on one of three rungs:

| Rung | What he sees | Counts as |
|---|---|---|
| **COPY** | The full prompt, ready to type | 100% given |
| **FILL** | The prompt with holes: *"Make each brick take ______ seconds to fall"* | 50% given |
| **BUILD** | Only the goal and the checklist. No wording at all. | 0% given |

FILL is the load-bearing middle rung. It teaches that the numbers and verbs are the decisions
and the sentence around them is packaging.

| # | Game | Steps | COPY | FILL | BUILD | Given |
|---|---|---|---|---|---|---|
| 00 | Know Your Studio | 8 | 8 | 0 | 0 | 100% |
| 01 | The Atom Factory | 6 | 6 | 0 | 0 | 100% |
| 02 | Brick Catcher | 6 | 4 | 2 | 0 | 83% |
| 03 | Meteor Dodge | 6 | 3 | 2 | 1 | 67% |
| 04 | Extreme Table Tennis | 6 | 2 | 3 | 1 | 58% |
| 05 | Science Memory Match | 6 | 2 | 2 | 2 | 50% |
| 06 | Angry Blocks | 5 | 1 | 2 | 2 | 40% |
| 07 | Typing Defender | 5 | 1 | 1 | 3 | 30% |
| 08 | Laser Maze Runner | 5 | 0 | 2 | 3 | 20% |
| 09 | T-Rex Dash | 4 | 0 | 1 | 3 | 12% |
| 10 | Tower Climber | 4 | 0 | 0 | 4 | 0% |

**Step count falls as the fade rises.** Writing a prompt from scratch takes roughly three times
as long as copying one, and the 20-minute build window never changes. Missions 02–05 get six steps,
06–08 get five, 09–10 get four.

## The checklist that replaces the prompts

Removing help only works if something takes its place. From mission 02 onward, every BUILD step
shows the same four words and nothing else:

> **WHAT I SEE · WHAT I DO · WHAT HAPPENS · HOW MUCH**

The last one is the hard-won part. *"Faster"* is useless; *"twice as fast"* is a specification.
By mission 08 he should be reciting it unprompted.

## Every step has four fields

| Field | Purpose |
|---|---|
| **DO** (`h` + `note`) | The action, and why it matters |
| **The prompt** (`p` / `fill`+`hint` / `task`+`example`) | Depends on the rung |
| **YOU SHOULD SEE** (`see`) | Success criteria in his words, so he can judge it alone |
| **IF NOT** (`ifnot`) | The exact English to say to Claude to repair it |

`see` and `ifnot` are what let him work without a parent beside him. They are not optional.

## Hints, and why they are counted not punished

A BUILD step he cannot crack would end the session. So after two real attempts, **Show me one**
reveals a worked prompt — and the log records a hint used.

That is measurement, not punishment. *"Mission 05: 3 hints. Mission 08: 0 hints."* is exactly the
kind of own-trajectory number the encouragement rule wants.

## The science, one principle per mission

| # | Principle | Why this game |
|---|---|---|
| 00 | A computer does what you SAY, not what you MEAN | The founding rule of the whole course |
| 01 | Electron shells — 2 then 8, full shells are calm | A counter *is* a shell filling up |
| 02 | Reaction time — about 250 ms, nerves have a speed | He measures his own, then **sets the fall speed from his own number** |
| 03 | Random is not fair — real randomness clumps | Why designers add rules on top of random |
| 04 | Angle in = angle out | And why paddles are not flat, which is what makes it a game |
| 05 | Working memory holds about four things; chunking beats it | He feels the limit while playing 12 cards |
| 06 | Centre of mass — hit low to topple | Where to aim, and why the bottom brick matters most |
| 07 | Practice builds myelin; repetition physically rewires | His own WPM curve is the evidence, sitting in his log |
| 08 | An algorithm — left hand on the wall solves any maze | One rule, no thinking, cannot fail. This is what code *is* |
| 09 | Frames of reference — the runner never moves | Every endless runner is a lie about who is moving |
| 10 | Decomposition — four machines at once | Name the parts, spec each one. The capstone |

Mission 02 is the model: he measures a human, then builds the machine around that measurement.
Science feeding a design decision, in one session.

## Brief structure

Every mission follows the same four beats:

1. **A story with a real principle** — 3 minutes, spoken, ideally drawn on paper
2. **The goal** — one sentence
3. **Four to six steps** — each one prompt or one decision
4. **Play it** — plus one patch note as a proper bug report, and **ship it to the arcade**

## Mission 10 needs a different shape

With nothing given, the session opens with him writing the whole spec **on paper** — four boxes
(player, platforms, camera, difficulty) — before touching the keyboard. Five minutes of thinking,
fifteen of building. That is a graduation and it should look like one.

## Notes for anyone editing this

- Budget is **five or six prompts**, always. Any brief that needs more is wrong and must be cut,
  not squeezed. Never end a session on a broken artifact.
- Teach the **small correction**, not the rewrite. Every `ifnot` field is one sentence about one
  problem, on purpose.
- The studio title screen goes on every game. Ten stamped games is a body of work.
- **Unverified with a real 9-year-old.** Nothing here has been tested on Samuel yet. Mission 06 is
  the predicted difficulty spike; mission 08 is where he first gets a founding prompt with holes
  in it, and mission 09's single FILL step may be too thin a landing before mission 10.
