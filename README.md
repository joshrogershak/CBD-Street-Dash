# CBD-Street-Dash

the best game on ts platform no lie 

---

## Requirements — read before opening the project

**Unity version: `6000.3.5f2`** — everyone must use this version.

Open Unity Hub → Installs → make sure `6000.3.5f2` is installed. If Unity Hub prompts you to upgrade the project to a different version when you open it, **do not upgrade** — install the matching version instead. Mismatched Unity versions silently rewrite project files and are the #1 cause of merge conflicts on a team.

You also need:
- **GitHub Desktop** (or Git) to sync changes

---

## First-time setup

1. Clone the repo (GitHub Desktop → File → Clone repository → CBD-Street-Dash).
2. In Unity Hub → **Add → Add project from disk** → select your cloned `CBD-Street-Dash` folder.
3. Open it with Unity **6000.3.5f2**.

>  **Keep individual files under 100 MB.** GitHub blocks any single file over 100 MB. Idk what you would do if you do have a file bigger but try to keep it under 100mb 

---

## Daily workflow

**Pull → Work → Commit → Push.** In that order, every time.

1. **Pull first.** Before you touch anything, open GitHub Desktop → **Fetch origin → Pull origin**. This gets everyone's latest changes so you're not working on top of an old version.
2. **Work** in Unity.
3. **Commit** often, with a clear message describing what you changed.
4. **Push** as soon as you've committed, so teammates can pull your work.

> If you skip the pull-first step and push, you'll create conflicts. Always pull before you start.

---

## Branches

We work on **branches**, not directly on `main`.

- `main` is the stable, always-working version. Nobody commits directly to it.
- Each person/feature gets its own branch, e.g. `player-movement`, `ui-menu`, `level-design`.
- When a feature is done and tested, it gets merged into `main` via a **Pull Request** on GitHub.

**To start work:**
1. In GitHub Desktop → **Current Branch** dropdown → **New Branch**.
2. Base it on `main`, name it after your task (e.g. `enemy-spawning`).
3. Do your work, commit, and push that branch.
4. On github.com, open a **Pull Request** to merge your branch into `main`. Get a teammate to glance over it, then merge.
5. Delete the branch after merging, and everyone pulls the updated `main`.

---

## don't edit the same scene at once

Unity **scene** (`.unity`) and **prefab** files do **not** merge cleanly in Git. If two people edit the same scene simultaneously, one person's work can be lost or the file can break.

To avoid this:
- **Coordinate** in the group chat before opening a shared scene — "I'm working in MainLevel.unity, hands off."
- **Split work** into separate scenes or prefabs per person where possible.
- Keep scene changes small and push them quickly so the scene isn't "locked" by you for long.
