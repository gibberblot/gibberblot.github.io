# gibberblot.github.io (RL Notes Redirector)

This repository forwards all legacy requests from `https://gibberblot.github.io/rl-notes/` to the new edition of the book hosted at [mastering-rl.github.io](https://mastering-rl.github.io/).

## Structure

To support all deployment configurations on GitHub Pages (whether hosted as the user site repository `gibberblot.github.io` or as the project repository `rl-notes`):
- All redirect files are placed at the repository root (`index.html`, `single-agent/...`, etc.)
- All redirect files are also placed under the `rl-notes/` subdirectory (`rl-notes/index.html`, `rl-notes/single-agent/...`, etc.)
- A smart `404.html` fallback script dynamically maps any missing, bookmarked, or query/hash-tagged URLs directly to the corresponding page on `mastering-rl.github.io`.
- `.nojekyll` is included to disable Jekyll processing on GitHub Pages.

## Deployment

To push changes to GitHub:

### Option A: As `gibberblot.github.io` repository
```bash
git add -A
git commit -m "Redirect rl-notes pages to mastering-rl.github.io"
git remote add origin https://github.com/gibberblot/gibberblot.github.io.git
git push -u origin main
```

### Option B: As `rl-notes` repository (`gh-pages` branch)
```bash
git add -A
git commit -m "Redirect pages to mastering-rl.github.io"
git remote add origin https://github.com/gibberblot/rl-notes.git
git push -u origin main:gh-pages
```
