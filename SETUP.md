# Arise-in Profile Kit — Setup

## 1. Put the files in your GitHub profile repository

Your profile repository should be named exactly:

```text
Arise-in/Arise-in
```

Copy `README.md`, `assets/hero.svg`, and the `.github/workflows/` folder into that repository.

## 2. Replace placeholders

Search the README for `YOUR_` and replace the values you want to publish:

- `YOUR_UNIVERSITY_NAME`
- `YOUR_ANILIST_USERNAME`
- `YOUR_MAL_USERNAME`
- `YOUR_CHESS_COM_USERNAME`
- `YOUR_LICHESS_USERNAME`
- `YOUR_LINKEDIN_USERNAME`
- `YOUR_PORTFOLIO_URL`

You can delete any badge/row you do not want to use.

## 3. Enable lowlighter/metrics

Create a GitHub personal access token and add it to the profile repository as this Actions secret:

```text
METRICS_TOKEN
```

For public-profile metrics, use the least privileges necessary. Only add extra scopes if you intentionally want metrics from private repositories or organizations.

Then open **Actions → GitHub Metrics → Run workflow** once. The workflow creates `github-metrics.svg` in your profile repository and refreshes it daily.

## 4. Generate the animated comet contribution graph

Open **Actions → Comet Contribution Graph → Run workflow** once.

The action publishes the animated files to a `comet-graph` branch. The README already points to:

```text
https://raw.githubusercontent.com/Arise-in/Arise-in/comet-graph/comet.svg
```

It also includes the reduced-motion SVG for visitors who prefer less animation.

## 5. GitHub Actions permission

If a workflow cannot push generated files, check:

**Repository Settings → Actions → General → Workflow permissions → Read and write permissions**

The workflow files already request `contents: write`.

## 6. Final check

After the first workflow runs:

1. Open your GitHub profile in a logged-out/private browser window.
2. Confirm `hero.svg`, `github-metrics.svg`, the activity graph and comet graph render.
3. Confirm your AniList/MAL/chess links no longer contain placeholders.
4. Remove any sections you do not want recruiters or visitors to see.

The design is intentionally split between a professional resume-style core and animated personality sections so the profile does not become a wall of badges.
