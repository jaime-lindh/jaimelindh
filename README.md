# jaimelindh.com

Academic website for Jaime Lindh, built as a static site (plain HTML/CSS, no build step) for GitHub Pages.

## Structure

```
index.html      Home
research.html   Working papers, publications, book chapter, policy reports
teaching.html   Instructor & TA history
cv.html         Structured CV + PDF download
contact.html    Contact info
styles.css      Shared stylesheet
files/          CV PDF
```

## How to publish this on GitHub Pages

1. **Create a new repository** on GitHub (e.g. `jaimelindh.github.io` if you want the default GitHub subdomain, or any name if you're using your custom domain).
2. **Upload these files** to the repository (drag-and-drop via the GitHub web UI works, or `git push` from the command line).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment," set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
5. Save. GitHub will give you a URL like `https://yourusername.github.io/repo-name/` within a minute or two.

## Pointing your custom domain (jaimelindh.com) at this site

1. In **Settings → Pages**, under "Custom domain," enter `www.jaimelindh.com` (or `jaimelindh.com`) and save. This creates a `CNAME` file in the repo automatically.
2. At your domain registrar (wherever jaimelindh.com is registered — check your Google Sites setup or registrar account), update DNS:
   - For the **apex domain** (`jaimelindh.com`), add `A` records pointing to GitHub's IPs:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - For **www** (`www.jaimelindh.com`), add a `CNAME` record pointing to `yourusername.github.io`.
3. Back in GitHub Pages settings, check **Enforce HTTPS** once DNS has propagated (can take up to 24 hours, often much faster).
4. Once this is live, you can turn off/delete the Google Sites version.

## Editing content later

Each page is plain HTML — open any `.html` file, find the relevant `<div class="entry">` block, and edit the text directly. No build tools or dependencies required.
