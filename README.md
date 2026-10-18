# Quantitative Finance — Research Chronicle

## Publish entirely in your browser

1. Create a public GitHub repository named YOUR_USERNAME.github.io. If it already hosts a website, use a NEW repository named quant-chronicle instead; do not overwrite an existing site.
2. Extract the ZIP on your computer. Open the extracted quant-chronicle folder.
3. In GitHub, choose Add file → Upload files. Drag ALL CONTENTS of that folder into the upload area, including _layouts, _notes, assets, and the four track folders. Do not upload the ZIP or the outer quant-chronicle folder itself. Commit changes to main. Preserve the directory structure.
4. Open Settings → Pages. Under Build and deployment choose Deploy from a branch, then main and /(root). Save. GitHub builds Jekyll automatically; no .github folder is required.
5. Wait for the Pages deployment to complete. Your site is https://YOUR_USERNAME.github.io/ (or https://YOUR_USERNAME.github.io/quant-chronicle/ for a project repository).

For a project repository, first edit _config.yml and change baseurl to "/quant-chronicle" (use your actual repository name). For a username.github.io repository, keep baseurl: "". The optional url field may remain empty.

## Check the first deployment

Confirm all four track links work, open each of the three notes, and check equations on both desktop and mobile. MathJax is loaded from a CDN, so equations require network access. GitHub's Actions tab shows the Pages build log if publication fails. A 404 immediately after setup may mean deployment is still running; also check that index.html is at the repository root.

## Add a milestone

Open NOTE-TEMPLATE.txt and copy the front matter and sections. In GitHub choose Add file → Create new file and name it _notes/YYYY-topic.md. Paste the template, edit it, and commit. The indexes update automatically. Use an integer year and one of these exact track values:

- Portfolio Theory
- Asset Pricing & Alpha
- Derivatives
- Market Microstructure & Execution

Use a unique filename. Quote metadata strings. Inline mathematics uses $...$; display mathematics uses $$ on separate lines. Keep one blank line before lists and display equations. Do not put equations in code fences.

## Edit and personalize

- Homepage: index.html
- Site title and description: _config.yml
- About page: about.md
- Appearance: assets/style.css
- Notes: _notes/*.md

You can press . while viewing the repository to use GitHub's web editor. No database, Node dependencies, local software, or custom build workflow is required. The two empty tracks are intentionally ready for new notes.

## Verification limits

The package was checked for valid YAML, note metadata, required sections, expected routes, relative_url use, and ZIP integrity. A full Jekyll build and browser rendering were not available in the preparation environment. The first GitHub Pages build and the visual checks above remain necessary.
