# Copilot instructions for Brick Arcade

## Project shape

- The arcade is a no-build collection of browser games.
- Each game lives in `games/<slug>/index.html` and is self-contained.
- Keep tweakable values in a nearby `CONFIG` object and player-facing text in a `STRINGS` table.
- The co-op relay lives in `server/` and is a Cloudflare Worker with a Durable Object.

## Game rules

- Make the game fun within five seconds.
- Never add a lose state, game-over screen, failing timer, or lives.
- Prefer pictures, icons, sound, and speech over text.
- Preserve keyboard, touch, and standard gamepad controls.
- Keep interactions forgiving with large hitboxes, magnet pickups, and forgiving camera behavior.
- Preserve local progress keys and wrap `localStorage` access in `try/catch`.
- Keep rendering light enough for school Chromebooks: pixel ratio at most 1.5, low-poly assets, and few draw calls.

## Change workflow

1. Read the relevant game README and the affected code section before editing.
2. Make the smallest change that satisfies the request.
3. Preserve existing controls, translations, save data, and offline behavior.
4. For co-op changes, read `server/PROTOCOL.md` and maintain backward-compatible messages.
5. Test the changed path in a browser when possible, including keyboard and gamepad behavior.
6. Run the smallest relevant automated test and inspect the final diff.

## Review standards

Flag changes that introduce a lose state, break an input modality, duplicate game constants, add a dependency without need, expose secrets, or send unbounded network data. Explain the issue and propose a no-lose alternative when a request conflicts with the game rules.
