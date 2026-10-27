# Last Exit: Zombie Rescue — Credits

## Code
- Game, custom WebGL2 engine, GPU skinning and character/vehicle loaders: original work (Qədir Bayramov).

## Character rig and animations
- **Universal Animation Library** by Quaternius, CC0 1.0 (public domain), https://quaternius.com
  - Used for the skeleton, skin weights (transferred to our own meshes) and base clips such as Idle, Walk, Jog, Sprint, Pistol_*, Roll, Death01 and Hit_Chest.
  - The zombie clips (Z_Walk, Shamble, Run, Idle, Crawl, Attack), S_Wave and H_RunAim/H_WalkAim are our own Blender edits of these clips.
- Hero, survivor and zombie meshes (assets/chars.glb, including the *_lo crowd LODs) were modelled procedurally in Blender (blender/chars.py). They are not AI-generated.

## Vehicles: AI-assisted geometry (disclosure)
- The vehicle **body geometry** in assets/cars.glb (pickup, sedan, muscle, truck and their `_lo` wreck LODs) was generated with **Tencent Hunyuan3D-2mini**.
  - Input: our own hand-built Blender concept renders (blender/car_concept.py).
  - The meshes were then cleaned, aligned, decimated (about 3k tris) and given materials in Blender (blender/car_clean.py, blender/cars_export.py). The wheels are procedural.
  - Licence: Tencent Hunyuan 3D 2.0 Community License Agreement.
  - The licence does **not** apply in the European Union, the United Kingdom or South Korea. Check the licence terms before distributing in those territories.
  - Required notice: "Tencent Hunyuan 3D 2.0 is licensed under the Tencent Hunyuan 3D 2.0 Community License Agreement, Copyright © 2025 Tencent. All Rights Reserved."
- No AI-generated textures or 2D art are used in the game.

## Environment kit and ground detail (pass 2)
- assets/weapons.glb (pistol, SMG, shotgun, rifle, launcher, flamer, minigun) was hand-modelled procedurally in Blender (blender/weapons.py). Not AI-generated.
- assets/env.glb has 48 environment props: barricades, sandbags, fences, dumpsters, street lights, cones, debris, trash, rooftop AC units and water tanks, fire escapes, awnings, trees, rocks, bushes, pallets, dock cleats and others. They were hand-modelled procedurally in Blender (blender/env_kit.py). They are not AI-generated and contain no third-party assets.
- Ground decals (cracks, oil, blood, manholes, drains, litter, leaves, skids, puddles, potholes, sand, scorch, road arrows, grass and gravel) are drawn procedurally on a canvas at runtime (src/dress.js). No image files are used.

## Tools
- Blender 4.5 (GPL; output belongs to its author), esbuild and Playwright (for tests).
