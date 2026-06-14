# HEARTHHOLD — Design Doc (working title)

**A survival city-builder with the waiting deleted.** Build by day, defend by night. Every build, upgrade, and tech advance is **instant** — you pay resources, it happens *now*. The only clock is the day/night rhythm you control. No 8-hour timers, no speed-ups, no pay-to-skip. It's the Clash of Clans / Whiteout Survival loop with the "tyranny of the timer" ([reviewers' words](https://orcz.com/whiteout-survival-review-strategy-survival-and-the-tyranny-of-the-timer/)) removed, fused with the build-by-day/defend-by-night tension of They Are Billions & City Defense Z.

## Core loop
1. **Day** — gather (assign villagers to forests/rocks/farms), build (walls, towers, houses, camps), upgrade, advance Age. All instant.
2. **Begin Night** (your call) — a horde spawns at the map edges and paths to your **Hearth**. Walls block, towers fire, defenders fight.
3. **Survive** → loot + the map opens up → next night is bigger. Lose if the Hearth falls.

The genius of "instant": the strategic decision is **what to spend on before the next night**, not "how long until my barracks finishes." Tension comes from the horde, not a countdown.

## Pillars
- **Worker economy (Age-of-Empires-lite):** villagers are population; assign them to resource nodes to gather. Houses raise the cap. Idle villagers do nothing — put them to work.
- **Base defense (tower-defense DNA, reused from WAVEFRONT):** walls reshape the enemy path; towers auto-fire; placement is everything.
- **Instant progression:** upgrade any building on the spot; spend at the Forge to advance Age (I→II→III…), unlocking better tiers — no wait, ever.
- **Escalation:** each night adds count/HP/new enemy types; bosses on milestone nights.

## Resources
- **Wood** (forests) — walls, basic buildings
- **Stone** (rock piles) — towers, upgrades
- **Food** (farms/berries) — supports population (each villager eats; need food income to grow)
- **Gold** (loot from kills) — Age advances & elite upgrades

## Buildings (v0.1 → later)
- **Hearth** ★ — your core; protect it (start with it)
- **House** — +population cap (instant villager)
- **Lumber Camp / Quarry / Farm** — boost gather rate / produce food
- **Wall & Gate** — block/redirect the horde, has HP
- **Arrow Tower** — auto-fire defense *(v0.1)*
- **Cannon Tower, Frost Tower, Forge (Age-up), Barracks (trainable defenders)** *(later)*

## v0.1 vertical slice (first playable, ship now)
Map + Hearth · 3 resource types + tap-to-assign gathering villagers · build House / Wall / Arrow Tower (instant) · flow-field horde pathing that walls actually redirect · auto-firing towers · escalating nights · lose-on-Hearth-death · resources & day counter. Proves the whole vibe.

## Build order after v0.1
Lumber/Quarry/Farm economy → Forge + Ages → more towers + Cannon/Frost → trainable defender units → enemy variety + bosses → meta (best night survived on the WAVEFRONT-style global leaderboard) → themes (reuse the 10-universe skin system) → mobile landscape + self-updater (reuse WAVEFRONT infra).

## Tech notes
Single-file canvas game, same architecture as WAVEFRONT (DPR-aware, offscreen sprite cache, game-icons.net art CC-BY). Enemy pathing = BFS flow-field from the Hearth over walkable tiles, recomputed when walls change; enemies follow the gradient and attack whatever blocks them. Deploy: GitHub Pages, self-updating client. 100% free; no real-world timers, no ads, no pay-to-win.
