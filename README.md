# Twenty Six Apex Fund — site

Single static landing page (`index.html`) for GitHub Pages, at the custom domain `26apex.com` (see `CNAME`).

## Deploy

1. Create a new, empty GitHub repository (no README/license/gitignore — this folder already has them).
2. From this folder:
   ```
   git remote add origin <your-repo-url>
   git branch -M main
   git push -u origin main
   ```
3. On GitHub: repo **Settings → Pages** → Source: **Deploy from a branch**, branch **main**, folder **/ (root)**.
4. At your domain registrar, point `26apex.com` at GitHub Pages:
   - Four `A` records on the root domain, to:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - (Optional) a `CNAME` record for `www` → `<your-github-username>.github.io`, if you also want the `www` version to resolve.
   - DNS changes can take up to a few hours to propagate.
5. Back in **Settings → Pages**, confirm the custom domain shows as verified, and enable **Enforce HTTPS** once it's available (GitHub provisions the certificate automatically after DNS resolves).

## Notes / open items

- The "Fund documents" link from the original design was removed — that page wasn't provided. Add it back (as `documents.html`, linked from `index.html`) whenever that content is ready.
- No `robots`/indexing preference was set either way; add a `<meta name="robots">` tag to `index.html` if you want to keep this out of search results.
