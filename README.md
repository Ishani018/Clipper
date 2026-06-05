# Clipper

**A tiny, zero-dependency tool for removing flat backgrounds from sprites and exporting a transparent PNG — losslessly.** Open one HTML file in any browser; your images never leave your machine.

Built for game artists and anyone working with sprites/icons on a solid or near-solid background. Clipper only erases the **background** pixels (sets their alpha to 0) — your subject's pixels are never touched or recompressed, so there's **no quality loss**.

No install. No build step. No server. One file.

---

## Why

Cropping backgrounds out of sprites by hand is slow, and most online tools recompress your art or send it to a server. Clipper does it locally, in seconds, keeping full quality:

- Erases only what you tell it to — the subject stays pixel-perfect
- Exports a clean transparent **PNG**

---

## Tools

- **Magic wand** — click a background area; erases connected pixels of a similar color (flood fill, tolerance-controlled)
- **Color key** — click a color; erases that color everywhere in the image
- **Auto-remove from edges** — one click: flood-fills transparency inward from all four edges (perfect when the subject doesn't touch the border)
- **Restore brush** — paint erased pixels back if you took off too much
- **Edge feather** — softens the alpha boundary for clean anti-aliased edges
- **Tolerance / brush size** sliders, **Undo** (Ctrl/Cmd+Z), **Reset**

---

## Usage

Open `index.html` in a browser.

1. **Upload** a sprite
2. Try **Auto-remove from edges**, then tidy up stray bits with the **Magic wand**
3. Adjust **Tolerance** if it takes too much / too little
4. **Download PNG** — transparent, lossless

Or host it free via GitHub Pages (Settings → Pages → deploy from `main` / root) and use `https://<you>.github.io/Clipper/`.

---

## Keyboard

| Key | Action |
|-----|--------|
| Ctrl/Cmd + Z | Undo |

---

## Notes

Clipper is built for **flat / solid backgrounds** (the common sprite case). For photos with busy, detailed backgrounds you'd want an AI segmentation tool — Clipper deliberately stays simple, fast, and dependency-free.

## License

MIT — see [LICENSE](LICENSE).
