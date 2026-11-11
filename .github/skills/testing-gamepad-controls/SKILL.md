---
name: testing-gamepad-controls
description: Review and test keyboard, touch, and standard gamepad controls for Brick Arcade games.
---

# Testing controls

For every changed interaction, identify the equivalent keyboard, touch, and standard gamepad action. Use the mapping in `CLAUDE.md`:

- A=0, B=1, X=2, Y=3
- LB=4, RB=5, Back=8, Start=9

Verify:

1. The action has a forgiving hitbox or threshold.
2. Releasing a button or stick cannot leave the action stuck.
3. Start/Escape returns home and Back/M toggles mute.
4. Touch controls do not cover important game content.
5. The action still works when co-op is disconnected.

Report unsupported hardware assumptions instead of silently treating them as tested.
