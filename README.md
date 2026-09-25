# VoxelCraft ⛏️

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.md)
[![WebGL2](https://img.shields.io/badge/Graphics-WebGL2-blue.svg)](https://www.khronos.org/registry/webgl/specs/latest/2.0/)
[![Vanilla JavaScript](https://img.shields.io/badge/Dependencies-Zero-brightgreen.svg)]()
[![AI Powered](https://img.shields.io/badge/Code-Claude%20Sonnet%205-purple.svg)]()

**VoxelCraft** is a lightweight, zero-dependency, single-file 3D voxel sandbox game built entirely with modern **WebGL2** and vanilla JavaScript. Run it directly in any modern desktop or mobile web browser with zero installation or build steps.

Featuring infinite procedural terrain generation, smooth lighting with ambient occlusion, realistic fluid propagation, mob AI, crafting, smelting, storage, synthesized Web Audio sound effects, mobile touch joystick support, and an extensible modding engine (**VCMF v2.0**).

---

## 🌟 Key Features

- **Single-File Architecture**: Complete engine, procedural textures, audio synthesizer, and shaders in one HTML file.
- **Pure WebGL2 Rendering**:
  - High-performance chunk meshing with 28 bytes/vertex packed buffers.
  - Smooth light propagation (Sky Light + Block Light) with 4-level Ambient Occlusion (AO).
  - Volumetric celestial atmosphere: dynamic sun/moon phases, stars, clouds, and depth fog.
  - Underwater & lava fog tints with realistic surface caustics.
- **Procedural World Generation**:
  - Multi-octave Perlin & 3D simplex-style noise terrain.
  - Multiple distinct biomes: Forest, Desert, Taiga, Snowy Plains, Mountains, Plains, Cherry Grove, and Jungle.
  - Cave systems, ore veins (Coal, Iron, Gold, Diamond, Lapis, Crimson), villages, and ruined portals.
- **Physics & Gameplay**:
  - Survival & Creative game modes with double-tap flight.
  - Authentic AABB collision resolution with auto step-climbing and sneak-edge protection.
  - Cellular automaton fluid simulation for Water and Lava (including obsidian & cobblestone generation).
  - Falling gravity blocks (Sand & Gravel).
  - Explosions with realistic entity knockback and block fragmentation physics.
- **Entities & Mob AI**:
  - Hostile mobs: Swamp Zombie, original Bomb Golem with fuse countdown.
  - Passive livestock: Pigs, Cows, and Shearing Sheep (with color genetics).
  - Item drops with floating magnetic pickup physics and stack merging.
- **Crafting & Industry**:
  - 2x2 player inventory grid & 3x3 Crafting Table grid with pattern matching.
  - Functional Furnace with fuel burn timer and smelting progress.
  - Barrel storage containers.
- **Procedural Audio Engine**:
  - 100% synthesized procedural sound effects using the Web Audio API (no heavy MP3/WAV downloads).
- **Persistent Storage**:
  - IndexedDB-backed world saving with automatic RLE chunk compression. Multi-world management support.
- **Bilingual Interface**:
  - Full runtime language switching between **English** and **Japanese (日本語)**.
- **Mobile Friendly**:
  - Responsive on-screen virtual analog joystick, touch camera look, quick action buttons, and inventory touch interaction.

---

## 🎮 Controls

### Desktop (Keyboard & Mouse)
- Movement: W, A, S, D
- Jump / Swim Up: Space
- Fly (Creative): Double-tap Space
- Sneak / Descend: Shift
- Sprint: Ctrl + W
- Break Block / Attack: Left Click (hold to mine)
- Place Block / Use / Eat: Right Click
- Pick Block (Creative): Middle Click
- Hotbar Selection: 1 - 9 or Mouse Wheel
- Open Inventory / Crafting: E
- Drop Held Item: Q (Ctrl + Q drops full stack)
- Chat / Commands: T or /
- Toggle Debug Overlay: F3
- Toggle HUD: F1
- Camera Zoom: Hold C

### Mobile (Touch Controls)
- Move: Drag left half of screen (drag far to sprint)
- Look: Drag right side of screen
- Place / Use / Attack: Tap
- Mine / Eat: Long press
- Jump / Sneak: Bottom-right buttons (▲ / Sneak)
- Inventory / Pause / Chat / Drop: Top-right buttons
- Split / Place single in Inventory: Long press slot

---

## 🧩 VCMF v2.0 (VoxelCraft Modding Framework)
VoxelCraft includes a built-in live JavaScript modding engine inspired by Minecraft Forge.
Mods can be loaded via the in-game MOD Manager with support for:
- Custom blocks, items, crafting recipes, and procedural 16x16 textures.
- Event hooks: tick, blockBreak, blockPlace, chatMessage, playerDeath, playerRespawn, mobSpawn, mobDamage, mobDeath, itemPickup, itemCraft, worldSave, worldLoaded.
- Cancelable pre-events: blockBreaking, blockPlacing, mobSpawning, playerDamaging.
- Forge-style live data access via api.raw (G, W, player, mobs, drops, etc.).
- Engine function direct invocation via api.fn (setB, gB, explode, damageMob, etc.).
- System equation overrides via api.override('blockDrops' | 'miningSpeed' | 'fuelValue' | 'playerDamage' | 'mobDamage').

---

## 📜 Credits & Licensing
1. **Codebase License**: MIT License (c) 2024-2026 VoxelCraft Contributors.
2. **AI Authoring Disclosure**: Coded with AI assistance by Anthropic Claude Sonnet 5.
3. **External Textures**: Luanti (formerly Minetest) "Minetest Game" by celeron55 and contributors, licensed under Creative Commons Attribution-ShareAlike 3.0 Unported (CC BY-SA 3.0). Built-in procedural textures are used when offline.
4. **Typography**: DotGothic16 by Fontworks Inc., SIL Open Font License 1.1.
