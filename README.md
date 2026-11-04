# 3D gallery

A static page that shows every 3D model for the game. To add one:
1. Shrink it for phones: `npx -y @gltf-transform/cli@4 resize in.glb tmp.glb --width 1024 --height 1024` then `npx -y @gltf-transform/cli@4 webp tmp.glb models/<id>.glb --quality 85`.
2. Add a row to `models.json` (id, name, kind, file, added, note).
3. Deploy (see `docs/design/3d-meshy-setup.md`).

## Review queue
`review.html` lists turnaround images waiting for a yes (`review.json`, images in `review/<id>/`). Rule: `.claude/rules/gallery-always-current.md`.
