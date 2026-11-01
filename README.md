<div align="center">

<img src="og.jpg" alt="GitPics – see every image in any GitHub folder" width="760">

# GitPics

GitHub gives you filenames. GitPics gives you the pictures.

**Paste any GitHub repo or folder link → thumbnail gallery, instantly.**  
No login. No install. Opens on your phone.

[gitpics.pages.dev →](https://gitpics.pages.dev) &nbsp;·&nbsp; [file a bug](../../issues) &nbsp;·&nbsp; [star it](../../stargazers)

![status](https://img.shields.io/badge/status-live-ff5a1f?style=flat-square)
![license](https://img.shields.io/badge/license-MIT-0b1a33?style=flat-square)
![no login](https://img.shields.io/badge/login-none-008080?style=flat-square)
![free](https://img.shields.io/badge/free-forever-ffd600?style=flat-square&labelColor=0b1a33)

</div>

---

## The problem

Open a GitHub folder with a hundred wallpapers and you get:

```
sunset_001.jpg
sunset_002.jpg
sunset_003.jpg
... (97 more filenames)
```

Click one. Wait. Back. Click another. Wait. Back.  
For a platform built around files, this is a strange blind spot — and after going through it one too many times, I got annoyed enough to write the fix.

## What it does

Paste a repo or folder URL. GitPics reads the folder through GitHub's API, shows every image as a thumbnail with its real aspect ratio, and gives you a full-screen swipe viewer with one-tap download. It runs entirely in your browser — no account, no backend, nothing to install.

## Using it

Put `https://gitpics.pages.dev/#` in front of any GitHub link and open it:

```
https://gitpics.pages.dev/#https://github.com/leouieda/landsat-wallpapers
```

Or open the site and paste the link directly.

## What it does well

| | |
|---|---|
| **Aspect ratios** | Portrait, landscape, 4K — images keep their shape. Square crop is one tap away. |
| **Swipe viewer** | Full-screen, keyboard-navigable, swipeable on touch. |
| **Fast on mobile** | Thumbnails served resized via wsrv.nl; download still gives you the original. |
| **Folder nav** | Browse subfolders and back out. S / M / L grid sizes. |
| **History** | Remembers repos you've opened, stored in your own browser. Nothing hits a server. |
| **Shareable link** | Any gallery has a URL you can copy and send. |
| **Light / dark** | Toggle in the header. |

## Honest limits

- **Public repos only** — private repos require auth, which GitPics doesn't do
- **60 API requests per hour** — each folder costs one; normal use stays well under
- **Git LFS images won't show** — GitHub serves those through a separate mechanism
- **Large folders** — GitHub's API caps the listing; GitPics can only show what it returns

---

## Contributing

This is one HTML file. No build step, no npm, no transpiler. You open `index.html` in a browser and edit it. If you've been looking for a project where the whole codebase fits in one file — this is it.

### What's needed

- [ ] Multi-select + batch download
- [ ] Keyboard shortcut overlay panel
- [ ] Slideshow / autoplay mode
- [ ] Better handling of huge folders (> 1,000 images)
- [ ] Animated WebP thumbnail support

### How to jump in

```bash
git clone https://github.com/[owner]/gitpics
cd gitpics
# open index.html in a browser
# make your change — the whole codebase is that one file
# open a pull request
```

There's no build step to run. No config to set. Open the file. Change something. Send the PR.

### Your contributor badge

Once your PR is merged, this is yours. Pin it to your GitHub profile README, your portfolio, or anywhere you want people to know you shipped something real:

```markdown
[![Contributed to GitPics](https://img.shields.io/badge/contributed%20to-GitPics-ff5a1f?style=for-the-badge&logo=github&logoColor=white)](https://gitpics.pages.dev)
```

[![Contributed to GitPics](https://img.shields.io/badge/contributed%20to-GitPics-ff5a1f?style=for-the-badge&logo=github&logoColor=white)](https://gitpics.pages.dev)

---

## How it works

- Reads folder contents via GitHub's **Git Trees API** — one request, all entries at once
- Loads images from `raw.githubusercontent.com`
- Thumbnails via [wsrv.nl](https://wsrv.nl), a free image proxy — falls back to the raw URL if unavailable
- Recent history stored in `localStorage`; nothing leaves your browser

## Credits

- OG image: Landsat wallpapers from [leouieda/landsat-wallpapers](https://github.com/leouieda/landsat-wallpapers) (CC0 public domain)
- Thumbnails: [wsrv.nl](https://wsrv.nl)
- Typeface: [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk)
- Not affiliated with GitHub. Images belong to their respective repo owners.

## License

[MIT](LICENSE) — do whatever you want with it.

---

<div align="center">

Built out of frustration. Maintained out of stubbornness.

If it saved your thumb some clicks, a ⭐ helps it reach more people.

</div>
