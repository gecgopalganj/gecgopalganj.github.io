# Where to put images, logo & other static files

Copy your **images, logo, and other static assets** into the **`public`** folder. Files here are served from the site root.

## Recommended structure

```
public/
├── images/           ← Put images here
│   ├── logo.png      ← College logo (used in header)
│   ├── hero.jpg      ← Hero / banner images
│   ├── gallery/      ← Gallery photos (optional subfolder)
│   └── ...
├── favicon.ico       ← Browser tab icon (optional, put in public/)
└── data/             ← Already used for timetable data
```

## How to reference them

- **Logo**: Put the college logo as **`public/images/logo.png`**. The header will show it automatically.
- **Other images**: Use paths starting with `/` in your code, e.g.:
  - `/images/hero.jpg`
  - `/images/gallery/campus.jpg`
- **Favicon**: Put **`favicon.ico`** in **`public/`** (same level as `index.html`). Browsers will pick it up if you add `<link rel="icon" href="/favicon.ico">` in `index.html`.

## Notes

- Files in `public/` are **not** processed by Vite; they are copied as-is into the build.
- Use **`public/images/logo.png`** for the header logo. If the file is missing, the logo area is hidden.
- For a different logo filename (e.g. `logo.svg`), update the `src` in `src/components/Layout.tsx` to `/images/logo.svg`.
