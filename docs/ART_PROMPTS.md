# HEARTHHOLD — Art Generation Prompts

Generate each in ChatGPT image-gen (or Midjourney/Flux). Save as PNG, drop into
`/Users/matthewhalle/Downloads` (or paste here) and tell me the asset name — I copy
it to `assets/sprites/<name>.png`, auto-remove the background if needed, and it
appears in-game with **zero code changes**.

## The 5 rules that keep everything consistent (paste these with EVERY prompt)
1. **Angle:** 3/4 semi-top-down view, camera looking down at ~50°, same angle as a tabletop diorama.
2. **Style:** hand-painted semi-realistic stylized mobile-game art, rich detailed texture, cozy survival vibe (think *Last Day on Earth* meets a painted board game).
3. **Lighting:** soft warm daylight from the upper-left, gentle shadows on the model itself.
4. **Background:** plain solid white OR transparent, NOTHING else — no ground, no cast shadow, no grass, no text, no UI, no border.
5. **Framing:** a single centered object, square image, filling ~80% of the frame.

> Reusable style tag to append to any prompt:
> *"— 3/4 semi-top-down view (~50° camera), hand-painted semi-realistic stylized mobile game art, rich texture, soft warm light from upper-left, single centered object on a plain white background, no shadow, no ground, no text, square."*

---

## CHARACTERS

### `villager` — your worker/survivor
A rugged frontier survivor standing upright, seen from a 3/4 top-down angle: weathered green hooded coat, leather satchel/backpack, sturdy boots, a small hatchet on the belt, determined friendly face. Full body, standing, slight heroic proportions (big head, sturdy body) so it reads at small size. *(append style tag)*

### `enemy` — basic horde creature
A feral nocturnal monster the size of a person: hunched, gaunt grey-purple skin, tattered rags, glowing red eyes, clawed hands, menacing but stylized (not gory). Standing/lunging pose, full body, reads clearly as a threat at small size. *(append style tag)*

### `boss` — hulking brute (every 5th night)
A massive armored brute monster, twice the size of the basic enemy: thick muscled body, cracked bone armor plates, heavy fists, glowing eyes, a few spikes. Imposing silhouette, full body, standing. *(append style tag)*

---

## BUILDINGS  (match the cabin you already made)

### `house` — DONE ✅ (your log cabin)

### `wall` — palisade segment
A single sturdy defensive wall segment of sharpened vertical timber logs lashed together, pointed tops, weathered wood, a horizontal support beam. Short straight segment meant to tile side-by-side. *(append style tag)*

### `arrow` — arrow tower
A tall wooden watchtower: four log legs, a railed platform up top, a small peaked shing/thatch roof, a quiver of arrows visible. Defensive, rustic, same wood tone as the cabin. *(append style tag)*

### `cannon` — cannon tower
A squat fortified stone-and-wood emplacement with a dark iron cannon barrel angled upward, reinforced base, a few cannonballs stacked beside it. Heavier and more metal than the arrow tower. *(append style tag)*

### `farm` — crop plot
A small tilled farm plot: rows of rich brown soil with green leafy crops and golden wheat sprouting, a low wooden border fence, maybe a tiny scarecrow. Low and flat (it sits on the ground). *(append style tag)*

### `hearth` — the central fire core *(optional, currently procedural)*
A large central campfire on a raised circular stone platform: stacked burning logs, glowing embers, a protective ring of stones, maybe a cooking tripod. The heart of the camp. *(append style tag — but you CAN keep the flame animated, so generate it with LOW flames / mostly embers.)*

---

## NATURE  (these tile the world — generate 1 of each, variety optional)

### `pine` — pine/conifer tree
A tall healthy pine tree, layered dark-green needled branches, visible brown trunk, slightly stylized conical shape, painted texture. *(append style tag)*

### `oak` — leafy broadleaf tree
A full round-canopy oak/broadleaf tree, lush green clustered leaves, thick gnarled brown trunk, dappled light on top. *(append style tag)*

### `bush` — shrub
A small rounded leafy green bush/shrub with a few berries. *(append style tag)*

### `rocks` — stone resource deposit
A cluster of grey granite boulders with a few glinting mineral veins (the mineable stone node), mossy at the base. *(append style tag)*

---

## GROUND  (special — this one is DIFFERENT)

### `ground` — seamless grass texture
A **seamless tileable** top-down grass texture, lush green meadow with subtle dirt patches, small flowers, painted detail, even lighting, NO objects, NO shadows. **Must tile seamlessly (edges wrap).** Flat top-down (NOT angled). Square. *(do NOT append the 3/4 angle tag — ground is flat top-down and must be seamless/tileable.)*

---

## Priority order (most visual impact first)
1. `villager`  2. `enemy`  3. `pine` + `oak`  4. `ground`  5. `arrow` + `wall`  6. `cannon` + `farm`  7. `boss`  8. `bush` + `rocks`  9. `hearth`

Generate whatever you like in any order — drop them in and I wire each one as it arrives.
