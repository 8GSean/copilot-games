---
name: adding-a-game
description: Add a new no-build Brick Arcade game that follows the shared controls, accessibility, performance, and navigation rules.
---

# Adding a game

1. Read `CLAUDE.md` and inspect a nearby game for shared patterns.
2. Create `games/<slug>/index.html` and a `thumb.jpg`.
3. Keep the game self-contained and use the existing Three.js import-map version.
4. Add a `CONFIG` object, a `STRINGS` table, keyboard/touch/gamepad input, speech or visual prompts, and local progress storage.
5. Add the game card to `index.html` with the correct relative link.
6. Add a README describing controls, accessibility behavior, and how to run it.
7. Test the game locally and verify that the arcade home button, mute control, and reset behavior work.

Do not add a game-over state, a required reading flow, or a dependency that requires a build step.
