# AGENTS.md — earshot

Started 2026-10-18. Concept plus (planned) browser simulator; no hardware. Read `README.md`, then
`docs/EVOLUTION.md`.

## Commands

- `npm test` — hermetic node tests in `test/`. No dependencies, no `node_modules`.
- `npm run sim` — `python3 -m http.server 4802 --directory sim`. Must be HTTP (ES modules).

## Rules

- Keep the core modules (positioning, sync, renderer, medium) pure: no DOM, no Web Audio. Node
  firmware will be ported from them.
- Every node is an actor that talks only in serializable messages; the sim, ESP-NOW and Wi-Fi carry
  the same envelope (see `~/projects/actors/bitparty-ts`).
- Sim and voice code may be copied from `~/projects/experimental/bloopsaball`; do not import across
  repos.
- Rehearsal scenes must always have a stop control and an intensity ramp. This is the product's
  first use, not a nice-to-have.

## Traps

- Inherited from bloopsaball: the desktop app's Browser pane throttles `requestAnimationFrame` to
  ~2 fps while hidden. Show the pane or drive the sim by steps from the console.
