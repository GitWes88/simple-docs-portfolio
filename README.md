# Docs-as-code portfolio (simple)

**Live site:** <https://GitWes88.github.io/simple-docs-portfolio/>

This project documents a fictional command-line tool called **Tidy**. The tool is invented, but the workflow is real: the docs are Markdown in Git, checked automatically, and published to GitHub Pages every time a change is merged.

## What this demonstrates

| Docs-as-code practice | Where to look |
| --- | --- |
| Plain-text source in version control | The `docs/` folder |
| Clear content types | A tutorial, a how-to guide, and a reference page |
| Automated Markdown linting | `.markdownlint-cli2.yaml` |
| Builds that fail on broken links | `strict: true` in `mkdocs.yml` |
| Continuous deployment | `.github/workflows/docs.yml` |

## Run it locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000>. The page reloads when you save a file.

## Publish your own copy

1. Create a public GitHub repository named `simple-docs-portfolio` and push this project to it.
2. Replace every `YOUR-USERNAME` in `README.md` and `mkdocs.yml` with your GitHub username.
3. Open **Settings > Pages** in your repository and set **Source** to **GitHub Actions**.
4. Push to `main`. The workflow checks the docs, builds the site, and deploys it.

## Make it yours

- Replace Tidy with a real tool you use, or with an open source project that needs better docs.
- Make your changes through pull requests, even when you're the only contributor. The history shows your review process.
