# Product Requirements Document (PRD): Bonk Run Demo

## Overview
A web-based 3D endless runner where Bonk, a coin-shaped avatar, rolls down a procedurally generated slope, dodging obstacles and gaps. The demo showcases core gameplay and Bonk's crypto-themed design.

---

## Target Platform
- Web browsers (Chrome, Firefox, Safari)
- Desktop and mobile compatible

## Purpose
- Demonstrate core gameplay and Bonk's crypto aesthetic
- Lightweight, playable demo for showcasing

## Objectives
- Smooth 3D endless runner mechanics (rolling, left/right movement, dodging)
- Highlight Bonk's unique, crypto-inspired design
- Futuristic, blockchain-inspired visuals (neon colors, circuit patterns)
- Lightweight, cross-browser compatibility

## Key Features
- **Gameplay:** Bonk auto-rolls forward; player controls horizontal movement (arrow keys/A/D)
- **Slope:** Procedurally generated with random gaps, turns, and obstacles (e.g., red blocks)
- **Speed:** Gradually increases to raise difficulty
- **Collisions:** Hitting obstacles or falling ends the game
- **Score:** Based on time/distance survived, displayed in real-time
- **Visuals:** 3D environment, ambient/directional lighting, neon/circuit patterns
- **Demo Scope:** Single level, no menu, basic score tracking, game-over state
- **Crypto Theme:** Neon colors, digital/blockchain patterns

## User Stories
- As a player, I want to control Bonk's horizontal movement to dodge obstacles and gaps.
- As a player, I want the game to get harder as I survive longer.
- As a developer, I want a modular codebase for easy feature expansion.

## Technical Requirements
- HTML, JavaScript, and Three.js (CDN: https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js)
- Compatible with Chrome, Firefox, Safari
- Optimized for desktop (keyboard) and mobile (touch, if possible)
- No external assets or file I/O; use Three.js primitives
- All code in a single `index.html` file with embedded `<script>`

## Monetization (Optional)
- Suggest blockchain integration (e.g., NFTs) for full version; exclude for demo

## Deliverables
- Playable demo: Bonk, procedural slope, obstacles, score, game-over state
- On-screen instructions (e.g., "Use arrow keys to move left and right")
- `prd_bonk_run.md`: This PRD
- `index.html`: Complete game demo

## Game Files & Structure
- **Scene Setup:** Three.js scene, camera, renderer, ambient/directional lighting
- **Bonk Avatar:** Cylinder (coin), gold/silver material, rolling animation
- **Slope Generation:** Procedural, connected planes/boxes, random gaps/turns
- **Obstacles:** Cube-shaped, red/contrasting color
- **Player Movement:** Auto-roll forward, left/right control (arrow keys/A/D)
- **Camera:** Third-person, follows Bonk
- **Collisions:** Detect with obstacles or falling off
- **Score System:** Time/distance survived, real-time display
- **Game Over:** Display text and final score
- **Instructions:** Show at start/game-over
- **Three.js Primitives Only:** No external models/assets
- **CDN:** Use Three.js via provided CDN
- **Responsive:** Full-screen, modern browser support
- **All code in `index.html`**

## Code Structure (Functions)
- `init()`: Scene, camera, renderer, player, initial slope
- `generateSlope()`: New slope segments, random gaps/turns/obstacles
- `updatePlayer()`: Player movement (horizontal, auto-roll)
- `checkCollisions()`: Collisions with obstacles/falling
- `updateScore()`: Increment/display score
- `gameLoop()`: Main loop (requestAnimationFrame)
- **Comments:** Explain key code sections

## Additional Details
- **Bonk Coin:** Cylinder, small height, rolling rotation
- **Slope:** Segmented, recycled for performance
- **Camera:** Smooth follow, third-person
- **Performance:** Simple shapes, efficient logic
- **Output:**
  - `prd_bonk_run.md`: This PRD
  - `index.html`: Playable demo 