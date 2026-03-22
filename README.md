# BWolf Homepage

Static website for BWolf Off The Road, hosted on GitHub Pages.

## Repository structure

- `site/index.html` - home page
- `site/dokumenty/index.html` - documents subpage (`/dokumenty`)
- `site/assets/css/styles.css` - styles
- `site/assets/images/` - images and logo

## Local preview

```bash
cd site
python3 -m http.server 4173
```

Open:
- [http://localhost:4173](http://localhost:4173)
- [http://localhost:4173/dokumenty/](http://localhost:4173/dokumenty/)

## Deploy to GitHub Pages

1. Push the repository to GitHub.
2. Go to the repository `Settings` -> `Pages`.
3. Under `Build and deployment` set:
   - `Source`: `Deploy from a branch`
   - `Branch`: `main` (or `master`), folder: `/ (root)`
4. Click `Save`.

> **Note:** GitHub Pages only supports the root (`/`) or `/docs` directory as the source.
> If the site files are in the `site/` folder, you need to either use GitHub Actions
> or rename `site/` to `docs/`.

### Option 1: `docs/` folder

1. Rename the `site` folder to `docs`.
2. Push the changes to GitHub.
3. In `Settings` -> `Pages` set branch `main`, folder `/docs`.

### Option 2: GitHub Actions

Add a `.github/workflows/deploy.yml` file with a workflow that copies the contents of `site/` to the `gh-pages` branch.

## License

MIT — see the `LICENSE` file.
