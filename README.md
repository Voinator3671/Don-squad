# Slingshot Squad — Phaser 3 + Matter.js

A responsive browser prototype with 20 JSON-defined levels, drag/release slingshot aiming, Matter.js rigid-body blocks, material durability, target collisions, character-specific flight abilities, sequential unlocks, local progress saving, and mouse/touch-friendly controls.

## Run locally
1. Install Node.js 20 or newer.
2. Extract this folder and open a terminal in it.
3. Run `npm install`.
4. Run `npm run dev` and open the local URL printed by Vite.
5. For a production build, run `npm run build`; preview it with `npm run preview`.

## Your images
- The five crops from your first collage are in `public/assets/characters/character-1.jpg` through `character-5.jpg`. They are rectangular crops and keep the original backgrounds; faces are not redrawn or background-removed.
- Your second image is `public/assets/target.jpg` and is used as the target.
- To replace a character, keep the same filename and dimensions/aspect ratio as you prefer. Character selection cycles through all five.

## Edit levels
Edit `src/data/levels.json`. Each level has `name`, `shots`, `targets` (`[x,y]`), and `blocks` (`[x,y,width,height,material]`). Materials: `wood`, `glass`, `stone`. Canvas coordinates are 1024×640; ground is around y=600. Keep target/block structures on the right half and test each change in-browser.

## Configure abilities
Edit `useAbility()` in `src/main.ts`. Character ability types are assigned by the character's order (0–4): turbo, boost, power pop, dash, bounce. This prototype applies ability effects to the projectile's real Matter.js velocity/force.

## Notes
This is a working starter prototype, not a commercial-ready game. Physics and interactions are real, but the level layouts and collision tuning should be playtested on target browsers; the included 20 levels are hand-authored starting layouts, not formally solver-verified. Facial blinking/expression animation, audio assets, and a dedicated level editor are not included yet. The target art retains the supplied photo background exactly as requested.
