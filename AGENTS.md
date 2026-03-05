# AGENTS.md — Cyberpunk 2048

## Goal
Transform the classic 2048 game (gabrielecirulli/2048) into a cyberpunk-themed experience with neon visuals, dark atmosphere, and futuristic aesthetics, while keeping the original gameplay intact.

## Tech Stack
- Pure HTML / CSS / JavaScript (no build step)
- Google Fonts: Orbitron (futuristic headings), Share Tech Mono (tile numbers)
- Hosted on GitHub Pages (root `/`)

## Architecture
```
/
├── index.html          # Main game page (modify <head> to add cyberpunk fonts/styles)
├── style/
│   ├── main.css        # Original styles (keep, minimal edits)
│   └── cyberpunk.css   # NEW: cyberpunk theme overrides
├── js/
│   └── application.js  # Game logic (do NOT break game mechanics)
└── AGENTS.md
```

## Cyberpunk Design Spec
- **Background**: `#0a0a0f` (near-black)
- **Grid background**: `#12121f`
- **Tile color scheme by value**:
  - 2: `#1a1a2e` / neon text `#00f5ff` (cyan)
  - 4: `#16213e` / neon text `#00f5ff`
  - 8: `#e94560` (neon red-pink)
  - 16: `#ff6b35` (neon orange)
  - 32: `#f7b731` (neon yellow)
  - 64: `#e94560` (deep neon red)
  - 128: `#a29bfe` (neon purple)
  - 256: `#6c5ce7` (violet)
  - 512: `#fd79a8` (pink)
  - 1024: `#00cec9` (teal)
  - 2048: `#fdcb6e` with pulsing glow animation
- **Fonts**: Orbitron for headings/score, Share Tech Mono for tile numbers
- **Effects**:
  - Tile box-shadow with matching neon color glow
  - Scanline overlay (CSS pseudo-element on body)
  - Merge animation: scale + glow burst
  - Grid border: 1px solid rgba(0, 245, 255, 0.3)

## Global Acceptance Criteria
1. Game is fully playable (all original mechanics work)
2. Cyberpunk visual theme applied (dark bg, neon tiles, correct fonts)
3. Tile colors match the spec above
4. Scanline overlay visible on the game board
5. Site loads and works at https://aw-apps.github.io/cyberpunk-2048/
6. No JavaScript console errors on load
7. Mobile-responsive layout preserved
