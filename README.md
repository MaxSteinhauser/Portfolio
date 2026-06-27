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

**Heads up on the Metromont page:** it only uses wording already on your resume (no new technical detail was added), but it's still a public page about your employer's process. Hold off pushing/linking that one until you've actually gotten the okay tomorrow — easiest way is to just leave the `metromont/` folder out of your initial commit, or delete the card linking to it from `index.html`, until you're cleared.

## 5. Adding photos

The Go-Kart and Bicycle pages, and the homepage banner, are already wired up for the photos you shared in chat — you just need to save those image files to these exact paths (filenames matter, case-sensitive):

| Photo | Save as |
|---|---|
| Go-kart, front 3/4 view (engine/cage visible, red wheelbarrow behind) | `assets/img/gokart/1.jpg` |
| Go-kart, rear/side view (roll cage, engine underneath) | `assets/img/gokart/2.jpg` |
| Motorized bicycle (Diamondback frame, engine mid-frame) | `assets/img/bicycle/1.jpg` |
| UGA Arch (homepage banner) | `assets/img/banner-arch.jpg` |

Once those 4 files are in place, the Go-Kart gallery, Bicycle gallery, and the homepage hero banner all go live automatically — no HTML edits needed.

For Electronics or Metromont, or any future photos, follow the same pattern for any project on