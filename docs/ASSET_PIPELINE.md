# HEARTHHOLD — Making our own 3D assets with ChatGPT + Meshy

Two kinds of assets you can hand me:

## A) 2D images — I use these directly (no extra tools)
Great for: ground/wall **textures**, the **sky**, **UI icons**, flat billboard plants.
- Generate in ChatGPT, download the PNG, drop in `Documents/Hearthhold/assets/`, tell me the filename.

## B) 3D models — ChatGPT image → Meshy → GLB → me  ★ the big one
This is how we get real 3D buildings, props, rocks, barrels, characters, etc.

### Step 1 — Generate the asset image in ChatGPT
Use this template (swap the **bold** part):
> "A **weathered wooden survival watchtower**, single isolated object, centered, full object in frame, 3/4 view slightly from above, plain solid light-gray background, even soft studio lighting, no shadows on the ground, realistic game asset, high detail."

Rules that make Meshy work well:
- ONE object, centered, whole thing visible (not cropped)
- Plain flat background (light gray or white), even lighting, no harsh shadows
- 3/4 view from slightly above (matches our camera)
- Say "realistic game asset" for the style we want

### Step 2 — Turn it into 3D in Meshy (free)
1. Go to **meshy.ai** → sign in → **Image to 3D**
2. Upload your ChatGPT image
3. Settings: **Quality/Topology = low or medium poly** (game-ready), enable **PBR textures**, texture size **1K or 2K**
4. Generate, then **Download → GLB** (GLB = one self-contained file)
- License note: Meshy **free tier = CC-BY** (fine for us now). Stay on free. If we ever need a paid tier, I'll flag the exact cost first.

### Step 3 — Hand it to me
- Drop the `.glb` in `Documents/Hearthhold/assets/models/` and tell me the filename.
- Specs that keep it phone-friendly: **GLB**, **under ~8 MB each**, 1K–2K textures. (If a file is huge like 100 MB+, it's film-res — regenerate at low poly.)

## What Meshy is GREAT at vs. weak at
- ✅ Buildings, walls, towers, barrels, crates, campfires, tools, rocks, **characters/enemies**, furniture — these come out great.
- ⚠️ **Trees / foliage** are the hardest for *any* image-to-3D (leaves confuse it). For trees we may use stylized CC0 packs or flat billboards instead — we'll test and see.

## Best first batch to send me (quick win)
1. A **survival shelter / log cabin**
2. A **wooden defense wall / palisade segment**
3. A **watchtower** (our defense tower)
4. A **barrel** and a **wooden crate** (props)
5. One **rock/boulder**
6. (Test) one **pine tree** — so we can judge if Meshy trees are good enough

Once these are in, the scene stops being "code-built shapes" and becomes real modeled objects — that's the jump to the reference look.
