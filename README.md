# Nakura Industries Private Limited: website

Static website. No build step. `index.html` is the whole site (pages open as `#products`, `#about-us`, `#contact` and so on).

## Files
- `index.html`: the website
- `favicon.ico`, `favicon-48/96/192/512.png`, `apple-touch-icon.png`: icons
- `robots.txt`, `sitemap.xml`: search engines
- `404.html`: not-found page
- `CNAME`: custom domain for GitHub Pages (`nakuraindustries.in`). Delete this file if you do not use that domain.
- `.nojekyll`: tells GitHub Pages to serve files as they are

## Deploy on GitHub Pages
1. On github.com click **New repository**, name it (for example `nakura-website`), keep it Public, and create it.
2. Click **Add file > Upload files**, drag in every file from this folder (including `.nojekyll` and `CNAME` if your file browser shows hidden files), and **Commit changes**.
3. Open **Settings > Pages**. Under **Build and deployment** set Source to **Deploy from a branch**, Branch to `main` and folder `/ (root)`, then Save.
4. Wait a minute or two. The site appears at `https://<your-username>.github.io/nakura-website/`.

## Use nakuraindustries.in
1. In **Settings > Pages > Custom domain** enter `nakuraindustries.in` and Save. Tick **Enforce HTTPS** when it becomes available.
2. At your domain registrar's DNS settings, remove the old records that point to the old UCO site, then add:
   - Four `A` records for `@` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - A `CNAME` record for `www` pointing to `<your-username>.github.io`
3. DNS changes can take from minutes to 24 hours.
4. In Google Search Console, add `nakuraindustries.in`, inspect `https://nakuraindustries.in/`, click **Request Indexing**, and submit `sitemap.xml`. To drop the old UCO snippet use **Removals > Clear cached URL**.

## Edit
- Contact email, phones, address and form delivery: the `CONFIG` block near the top of the script in `index.html`.
- Product names and text: the `C`, `RICE`, `BR`, `CAP`, `HOW` and `WHY` lists in the same script.
- Photos: the `IMG` block in the same script.
- Quote form: with `CONFIG.email` set, it opens the visitor's email app. To send enquiries to a service or CRM, set `CONFIG.endpoint` to its form URL.
