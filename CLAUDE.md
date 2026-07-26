# CLAUDE.md — Samuel Coding Studio

Read this before touching anything.

## What this is

A ten-mission "vibe coding" curriculum for **Samuel, age 9**, fluent in English.
He never writes code. He writes English prompts to an AI, which writes the code.
He is the **producer**; the AI is his **lead developer**.

His father **Jessy** designed the curriculum and runs the sessions.

The deliverable is a single static page, hosted on GitHub Pages, that Samuel opens
each week and follows on his own.

**Live:** https://sckang0911.github.io/SamuelCoding/
**Repo name is case-sensitive** — `SamuelCoding`, capital S and C.

## Session format — 40 minutes, non-negotiable

| Part | Minutes | What happens |
|---|---|---|
| 1 | 10 | Typing practice (Nitro Type / TypingClub). **Target 30 WPM.** |
| 2 | 20 | Build the week's game by prompting Claude in Artifacts |
| 3 | 10 | Play it, then write one patch note and get it fixed |

The 20-minute build budget is the hardest constraint in the project. It buys about
**five or six prompts**. Any mission brief that needs more than that is wrong and must
be cut down, not squeezed.

## The technical situation

- **One file.** `index.html` — HTML, CSS and JS inline. No build step, no framework, no dependencies.
- **Fonts** load from Google Fonts with system fallbacks. Must stay readable if the CDN is blocked.
- **Storage** goes through the `store` adapter near the top of the script: it uses `window.storage`
  when the file runs inside a Claude artifact, and `localStorage` when hosted. **Keep both paths working.**
- **Single device by design.** No login, no backend, no sync. This was decided and rejected deliberately —
  see `docs/decisions.md`. Do not add accounts, Firebase, Supabase, or any server.
- **Backup and restore** (JSON download / upload) is the only safety net. Don't remove it.

## Where content lives

Mission content is data, in two arrays in `index.html`:

- `UNIT0` — the setup unit, full brief
- `MISSIONS` — missions 1–10. Mission 1 is a full brief; 2–10 are previews.

A preview becomes a full brief by adding `ready:true` plus `story`, `rule`, `story2`, `ask`,
`steps`, and `play`, matching the shape of mission 1. Nothing else needs to change.

`docs/curriculum.md` is the human-readable design record. `index.html` is what ships.
If they disagree, `index.html` wins — but update the doc in the same commit.

## Current state

Working and deployed: session timer, daily 30 WPM gate, tower, Unit 00 and Mission 01 full briefs,
missions 02–10 as previews, learning log with backfill, backup/restore.

**Agreed but not yet built:** the redesign in `docs/redesign-spec.md`. That is the next piece of work.
It has been discussed and signed off in full. Build it from the spec; don't redesign it again.

## House rules for whoever works on this

1. **Nine-year-old, alone at the screen.** Every instruction needs: do this → you should see this →
   if it looks wrong, say exactly this. The third part is what replaces a parent sitting beside him.
2. **No hollow praise.** Encouragement must contain a number about his own past
   ("your typing is up 7 WPM since your first test"). Never "Great job!". Kids detect filler.
3. **Count sessions, never consecutive days.** A streak that breaks over a family holiday
   teaches the wrong lesson about making things.
4. **Never block the road permanently.** He can always park a mission and move on. The lock
   sets a rhythm; it is not a cage.
5. **Plain verbs, sentence case, active voice.** He reads it, so no jargon and no system-speak.
6. **Test the gate after any change to state:** log a WPM score, reload, confirm it survived.

## Visual identity — keep it

LEGO instruction manual crossed with an arcade attract screen. It is deliberate and it is his.

- Graph-paper background, white plates, **3px black outlines**, hard offset shadows with no blur
- Palette: paper `#E7ECF1`, ink `#10161D`, red `#E5322D`, yellow `#FFB703`, blue `#1F6FEB`, green `#1E9E5A`
- Type: Archivo Black (display) / Space Grotesk (body) / JetBrains Mono (prompts, data, labels)
- Prompts are always shown in mono on ink — they are the thing he types, so they look like code
- The tower of bricks is the signature element. Don't dilute it with other progress indicators.

## Deploying

Edit → commit to `main` → GitHub Pages serves it in about a minute.
`.nojekyll` is present so files are served as-is.
