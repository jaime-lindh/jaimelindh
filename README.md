# jaimelindh.com

Academic website for Jaime Lindh — plain HTML/CSS static site, no build step, ready for GitHub Pages.

## Structure

```
index.html      Home (bio, research)
teaching.html   Teaching (instructor & TA history)
contact.html    Contact info
styles.css      Shared stylesheet
files/          CV PDF
```

## Uploading to your existing GitHub repo

1. Go to your `jaimelindh` repository on GitHub.
2. For each file below, click on the existing file of the same name in the repo, click the pencil (Edit) icon, delete the contents, and paste in the new version — or use **Add file → Upload files** and drag the whole folder to overwrite everything at once (drag the folder itself, not individual files, so the `files/` subfolder path is preserved).
3. Commit the changes (a short message like "Update site content" is fine).
4. If your repo is currently set to **Private**, go to **Settings → General → Danger Zone → Change visibility → Public** when you're ready to publish. GitHub Pages on a free account only works with public repos, and your site will be offline until you do this.
5. GitHub Pages will rebuild automatically within a minute or two. Your site is live at:
   `https://jaime-lindh.github.io/jaimelindh/`

## Custom domain (jaimelindh.com)

If you want to point your existing domain at this site instead of the `github.io` URL:

1. In the repo, go to **Settings → Pages**, and under "Custom domain," enter `www.jaimelindh.com` (or `jaimelindh.com`). This creates a `CNAME` file automatically.
2. At your domain registrar, update DNS:
   - **Apex domain** (`jaimelindh.com`): add `A` records pointing to:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - **www subdomain**: add a `CNAME` record pointing to `jaime-lindh.github.io`.
3. Back in GitHub Pages settings, check **Enforce HTTPS** once DNS has propagated.
4. Once live, you can retire the old Google Sites version.

## Editing content later

Every page is plain HTML — open the file, find the relevant text between tags, and edit directly. No dependencies or build tools required. Avoid editing anything inside `<...>` angle brackets; only the text between tags is safe to change freely.
