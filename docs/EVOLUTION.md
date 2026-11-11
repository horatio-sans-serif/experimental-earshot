# Earshot evolution

Append-only. One dated entry per turn that changed something. Each entry: subject, then claims,
questions, risks and annotations.

## 2026-10-18 — concept, home and first production chosen

**Subject:** a self-organizing array of solar 5 W speakers that turns an authored scene into a
walk-through sound environment.

**Claims**
- Pipeline: scene tool → content (CC0/NASA clips, TTS, synthesis) → world model (the medium) →
  renderer → speaker nodes → listener walking.
- Rendering for an irregular array with no sweet spot: distance-based amplitude panning (DBAP,
  Lossius 2009) for near sources; far sources from every node with per-node distance delay and air
  low-pass, so direction comes from first arrival. Wave field synthesis needs cm spacing: not
  feasible.
- Self-location: nodes chirp in turn, time of arrival gives pairwise distance, multidimensional
  scaling gives the map; a phone walk sets levels. Clocks must agree within ~1 ms.
- Nothing is streamed: stems pre-loaded to SD, scene-clock messages broadcast, each node renders
  its own feed.
- Mars ground truth exists: Perseverance recordings (NASA); Maurice et al. 2022, Nature: ~240 m/s
  below ~240 Hz, ~250 m/s above, strong high-frequency loss, ~20 dB quieter.

**Decisions (Brian, 2026-10-18)**
- First production: browser simulator (yard, nodes, walking listener, headphones).
- Home: this repo.
- Purpose: rehearse real places. So rehearsal comes before spectacle, and every scene needs a stop
  control, an intensity ramp and a pace the listener sets.

**Questions**
- Which real place or situation is the first scene?
- Yard size and shape, for the sim map.
- Does a "rehearsal" scene need recordings of the real place, or is a convincing generic version
  enough?

**Risks**
- Small drivers give little below ~150 Hz; one subwoofer node is the likely fix.
- Neighbours and the local noise ordinance.
- Clock sync over Wi-Fi jitter.
- Solar endurance in autumn and winter.
- For rehearsal, a scene that overwhelms is worse than one that underwhelms.

**Annotations**
- Draft rubric (decision: is a 4-node prototype worth ~$300?): node position error < 0.5 m
  (numeric); clock offset < 1 ms (numeric); walker points within 30° of a virtual source (human);
  believability ≥ 4/5 (human, Brian); 3 h/evening for 7 days on solar (numeric); property-line SPL
  under the ordinance (numeric). For rehearsal add: Brian rates "this felt like the real place"
  and "I stayed in control" (human).
- Origin: idea journal `~/.claude/ideas/journal/2026-10-18.md`, entry 261018-5.
