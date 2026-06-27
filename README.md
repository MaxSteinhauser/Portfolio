# Max Steinhauser — Project Portfolio

A static site, one page per project, deployed for free with GitHub Pages.
No build step, no dependencies — just HTML/CSS.

## Structure

```
index.html              homepage, links to every project
gokart/index.html        Go-Kart Rebuild and Mechanical Integration
bicycle/index.html       Motorized Bicycle Conversion
electronics/index.html   Electronics Repair
metromont/index.html     Manufacturing Engineer Intern — Metromont
assets/css/style.css     shared styling for every page
assets/img/<project>/    drop that project's photos here
```

## 1. Create the GitHub repo

1. Go to https://github.com/new
2. Repo name: e.g. `portfolio` (this becomes part of your URL — pick something short)
3. Set it to **Public**, don't add a README/license/.gitignore (this folder already has everything)
4. Click **Create repository**

## 2. Push these files

If you have git installed, from inside this folder:

```bash
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

No git? On the new repo's GitHub page, click **Add file → Upload files**, then drag in everything from this folder (including the `assets` and project folders) and commit.

## 3. Turn on GitHub Pages

1. In the repo: **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: `main`, folder `/ (root)`
4. Save. The site goes live in a minute or two at:

```
https://<your-username>.github.io/<repo-name>/
```

## 4. Your project links

Once Pages is live, each project has its own URL:

- Go-Kart: `https://<your-username>.github.io/<repo-name>/gokart/`
- Bicycle: `https://<your-username>.github.io/<repo-name>/bicycle/`
- Electronics: `https://<your-username>.github.io/<repo-name>/electronics/`
- Metromont: `https://<your-username>.github.io/<repo-name>/metromont/`

**Heads up on the Metromont page:** it only uses wording already on your resume (no new technical detail was added), but it's still a public page about your employer's process. Hold off pushing/linking that one until you've actually gotten the okay tomorrow — easiest way is to just leave the `metromont/` folder out of your initial commit, or delete the card linking to it from `index.html`, until you're cleared.

## 5. Adding photos

For any project once you have photos:

1. Drop the image files into `assets/img/<project>/` (e.g. `assets/img/gokart/1.jpg`)
2. Open that project's `index.html`
3. Find the commented-out `<!-- Photo gallery ... -->` block and delete the `<!--` and `-->` around it
4. Update the `src` paths/filenames to match what you added

Pages with no photos yet just skip that section cleanly — nothing broken or empty-looking.

## 6. Linking from your resume

Once you have the real URL, wrap each project title in `Max_Steinhauser_Resume.tex` with `\href`, for example:

```latex
\resumeSubheading
    {\href{https://<your-username>.github.io/<repo-name>/gokart/}{Go-Kart Rebuild and Mechanical Integration}}{}
    {Personal Project}{}
```

Do this for each of the four `\resumeSubheading` project entries, swapping in that project's URL.
