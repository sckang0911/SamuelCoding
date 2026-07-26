# Samuel Coding Studio

A ten-mission vibe-coding curriculum for a nine-year-old, plus one setup unit.
Single HTML file, no build step, no dependencies.

**Live site:** `https://<your-username>.github.io/samuel-coding-studio/`

---

## How to publish it

1. Create a new repository named `samuel-coding-studio`. Public, no README, no `.gitignore`.
2. Upload `index.html` and this `README.md` to the repo root (drag and drop on github.com works fine).
3. Go to **Settings → Pages**. Under *Build and deployment*, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`. Save.
4. Wait about a minute, then open the URL above. Add it to the home screen of whatever device Samuel uses.

If you prefer the command line:

```bash
git init
git add index.html README.md
git commit -m "Samuel Coding Studio"
git branch -M main
git remote add origin https://github.com/<your-username>/samuel-coding-studio.git
git push -u origin main
```

Then enable Pages as in step 3.

---

## What the page does

- **10-20-10 session timer** — typing warm-up, build, playtest.
- **Typing gate** — the missions stay locked until a words-per-minute score is logged for the current day. Target is 30 WPM. Resets every day.
- **The tower** — one brick per finished game, ten in total, plus a setup brick.
- **Unit 00 · Know Your Studio** — full brief: tools, the two windows, the first build, breaking things on purpose, undo, and the three studio rules.
- **Mission 01 · The Atom Factory** — full brief: electron shells (2 then 8), six build steps with prompts, a patch-note box.
- **Missions 02–10** — goal, skill, and opening prompt. Full briefs get written before each class.

## Where progress is stored

Everything is kept on the device in browser storage — studio name, checked steps, patch notes, WPM history.
Nothing is uploaded anywhere and there is no account.

Consequences worth knowing: a different device starts empty, and clearing browser data wipes the history.
For a weekly class on one tablet or laptop, that is fine.

## Adding a mission brief

Missions live in the `MISSIONS` array in `index.html`. A preview entry looks like this:

```js
{n:2, stars:1, title:"Brick Catcher", learn:"Arrow keys and catching things",
 goal:"...", founding:"..."}
```

To turn it into a full brief, add `ready:true` plus `story`, `rule`, `story2`, `ask`, `steps`, and `play`
in the same shape as mission 1. Nothing else needs to change.
