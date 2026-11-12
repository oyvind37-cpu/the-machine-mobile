# Mobile publication checklist

The Cold Case app is in `cold-case/index.html` and loads `./cases/jorn-berntzen-2004.json` using fetch.

## Deployment
1. Review draft PR #2 and merge into main only after approval.
2. In repository Settings → Pages, set **Source: GitHub Actions**.
3. Go to Actions → **Deploy Finch Cold Case to GitHub Pages** → Run workflow (or merge will trigger it).
4. Confirm the deployed URL shown in the workflow. Expected path if default Pages domain is used: `https://oyvind37-cpu.github.io/the-machine-mobile/`. This is **not verified live**.
5. On iPhone open the confirmed URL in Safari → Share → Add to Home Screen.

**Important:** A GitHub repository can serve only one Pages site at a time. This workflow deploys the `cold-case/` directory as the root Pages site and may replace any previously deployed `the-machine-mobile` Pages homepage. Do not enable/merge until that effect is approved. Alternative: publish as a separate repository or integrate Cold Case as a subfolder into the existing Pages build.

## Validation
- Check data loads and shows 13 entries.
- Search "AMK" and verify result.
- Filter "Historisk kontekst" and "Hovedsaken".
- Open sources from Safari.
- Confirm no private data or identity matching features.
- Verify error message when data file is missing.
