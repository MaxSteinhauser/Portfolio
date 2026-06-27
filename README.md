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
assets/css/site.css      shared styling for every page
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

**Heads up on the Metromont page:** it only uses wording already on your resume (no new technical detail was added), but it's still a public page about your employer's process. Hold off pushing/linking that one until you've actually gotten the okay tomorrow — easiest way is to just leave the `metromont/` folder out of your initial commit, or delete the card linking to it from `index.html`, until you're cleared. The same goes for the two Metromont photos below — only add real photos once you've confirmed it's fine to post them publicly.

## 5. Adding photos

Every gallery is live by default — no commenting/uncommenting HTML required. Just drop image files at the exact paths below (filenames matter, case-sensitive) and they'll appear next time the page loads:

| Photo | Save as |
|---|---|
| Go-kart — starting condition | `assets/img/gokart/before.jpg` |
| Go-kart — after the rebuild | `assets/img/gokart/after.jpg` |
| Motorized bicycle | `assets/img/bicycle/1.jpg` |
| UGA Arch (homepage banner) | `assets/img/banner-arch.jpg` |
| Electronics repair (optional, 2 slots) | `assets/img/electronics/1.jpg`, `assets/img/electronics/2.jpg` |
| Metromont — in-house cost-reduction tool | `assets/img/metromont/cost-reduction-tool.jpg` |
| Metromont — emergency-designed replacement part | `assets/img/metromont/emergency-design.jpg` |

The Go-Kart page renders its two photos as a labeled **Before / After** comparison rather than a plain gallery.

Until a given image file actually exists at its path, the browser shows a broken-image icon with the alt text in its place — that's expected and harmless, it disappears the moment you add the real file.

For any other project, just save files into `assets/img/<project>/` matching the `src` paths already in that page's `index.html`.

## 6. Linking from your resume

Once you have the real URL, wrap each project title in `Max_Steinhauser_Resume.tex` with `\href`, for example:

```latex
\resumeSubheading
    {\href{https://<your-username>.github.io/<repo-name>/gokart/}{Go-Kart Rebuild and Mechanical Integration}}{}
    {Personal Project}{}
```

Do this for each of the four `\resumeSubheading` project entries, swapping in that project's URL.
