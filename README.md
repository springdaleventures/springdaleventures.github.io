# springdaleventures.com

Static site for Springdale Ventures. No build step: `index.html` plus the `assets` folder.

## Publish on GitHub Pages
1. Create a repository and upload everything in this folder (keep the `assets` folder as is).
2. In the repository: Settings > Pages > Build and deployment > Source: "Deploy from a branch", Branch: `main`, folder `/ (root)`. Save.
3. To use springdaleventures.com: on the same Pages screen, enter `www.springdaleventures.com` under Custom domain, then point the domain's DNS at GitHub Pages (a `CNAME` record for `www` to `<your-github-username>.github.io`, plus GitHub's four `A` records for the bare domain). Tick "Enforce HTTPS" once it is available.

Old links like /about/, /team/, /brands/ and /contact/ are sent to the matching page by `404.html`.

## Editing
- Text: edit `index.html` directly on GitHub (pencil icon). Each page is a `<div class="view" id="v-...">` block.
- Portfolio brands: the `P` list near the bottom of `index.html`. Each line is
  `[name, logo file, fund ("I", "II", "III"), category, description, exit text, website]`.
  Logos live in `assets/` as `b_<logo file>.png` (black on transparent). Leave exit text empty for active companies.
- Home page logo wall: the `featured` list right below `P`.
- Pitch form: the Contact page embeds the Airtable form `shrlMVv0nMnwOBltE`, same as the old site. Search for `airtable.com/embed` to change it.
