# Harrison Tang — personal website (static)

A single-page site: `index.html` plus the images in `public/`.
Everything runs client-side — no build step, no server.

## Upload to GitHub
Put **all of these files at the repo root**, keeping the `public/` folder
intact (so paths like `public/food-web/dish-01.jpg` still resolve):

```
index.html
public/… (photo.jpg, the 13 country photos, food-web/dish-01…21.jpg)
```

## Deploy on Vercel
Import the repo, then in the project settings set:
- **Framework Preset:** Other
- **Build Command:** (leave empty / None)
- **Output Directory:** `.` (root)

That's it — Vercel serves `index.html` as the homepage. Point your
`harrisontang.com` domain at the project.

(GitHub Pages also works: it will serve `index.html` automatically.)

## Notes
- Needs internet in the browser: Three.js + the world map + flag icons
  load from CDNs (unpkg / jsDelivr / flagcdn).
- To add/replace travel photos: drop the file in `public/` and update the
  matching entry in `index.html` (search `COUNTRY_BALLS`). Food-wheel
  images live in `public/food-web/` as `dish-01.jpg …`.
