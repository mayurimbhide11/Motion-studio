# Alpha · Beta — Interactive Experience

A full-screen, cursor/touch-scrubbed video experience with three scenes
(zebra pattern, grass, soft studio lighting).

## Structure

```
.
├── index.html          the whole experience — layout, styles, and logic
└── videos/
    ├── zebra.mp4
    ├── grass.mp4
    └── soft-lighting.mp4
```

`index.html` references the videos with normal relative paths
(`videos/zebra.mp4`, etc.), so the folder must be pushed as-is — don't
rename or move the `videos` folder without updating the `<source>` tags
in `index.html` to match.

## Deploy with GitHub Pages

1. Create a new repository on GitHub (or use an existing one).
2. Push these files to it, keeping the folder structure above:
   ```
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```
3. On GitHub, go to **Settings → Pages**.
4. Under **Source**, choose the `main` branch and `/ (root)` folder, then **Save**.
5. GitHub will give you a live URL, typically:
   `https://<your-username>.github.io/<your-repo>/`
   (takes a minute or two to go live after the first deploy).

That URL is what you'd link to from your Framer "Play" button.

## Notes

- Videos are real `.mp4` files now (not embedded as base64), so they
  load faster and stream properly instead of blocking on one giant
  HTML download.
- Everything else — responsive layout, touch/cursor scrubbing, the
  rotate-to-landscape prompt on phones, nav arrows/dots — is unchanged
  from the version tested in chat.
