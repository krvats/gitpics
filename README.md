<div align="center">

<img src="og.jpg" alt="GitPics: see every image in any GitHub folder" width="760">

# GitPics

GitHub gives you filenames. GitPics gives you the pictures.

**Paste any GitHub repo or folder link, get a thumbnail gallery.**  
No login. No install. Works on your phone.

[Open GitPics](https://gitpics.pages.dev) · [Report a bug](https://github.com/krvats/gitpics/issues/new/choose) · [Star it](https://github.com/krvats/gitpics)

![license](https://img.shields.io/badge/license-MIT-0b1a33?style=flat-square)
![no login](https://img.shields.io/badge/login-none-008080?style=flat-square)
![contributions welcome](https://img.shields.io/badge/PRs-welcome-ff5a1f?style=flat-square)

</div>

---

## Why I made this

I was going through a repo with a hundred wallpapers and all GitHub showed me was this:

```
sunset_001.jpg
sunset_002.jpg
sunset_003.jpg
... (97 more)
```

Click one, wait, go back, click the next. It got old fast, so I wrote the fix.

## What it does

Paste a repo or folder link. GitPics reads the folder through GitHub's API and shows every image as a thumbnail in its real shape, with a full-screen swipe viewer and one-tap download. It all runs in your browser. No account, no backend.

Put `https://gitpics.pages.dev/#` in front of any GitHub link and open it:

```
https://gitpics.pages.dev/#https://github.com/leouieda/landsat-wallpapers
```

## What's in it

- **Real aspect ratios.** Portrait, landscape, 4K all keep their shape. Square crop is one tap away.
- **Swipe viewer.** Full-screen, keyboard friendly, swipeable on touch.
- **Quick on mobile.** Thumbnails come resized through wsrv.nl; download still gives you the original.
- **Folder navigation.** Dive into subfolders and back out. S / M / L grid sizes.
- **History.** Repos you've opened are remembered in your own browser only.
- **Shareable.** Every gallery has a link you can copy.
- **Filter and sort.** Search names, flip the order, sort by size, or shuffle.
- **Select and zip.** Tick the ones you want, or zip a whole folder, built in your browser.
- **Slideshow.** Autoplay through a folder.
- **Shortcuts.** Press `?` on the site to see them. You can also paste a link anywhere on the page.
- **Light and dark.**

## Honest limits

- Public repos only (private ones need auth, which GitPics doesn't do)
- GitHub allows 60 API requests an hour without a token. Each folder costs one.
- Git LFS images won't show
- Huge folders: GitHub caps the listing, so GitPics can only show what it gets back

---

## Come build it with me

The whole project is one HTML file. No build step, no npm, no framework. Open `index.html` in a browser and start editing.

**You don't have to write code to help.** Testing on your phone, finding repos that break it, fixing wording, suggesting design ideas and telling a friend all count. New to open source? This is a good first PR. I'll help you get it merged.

### Things that still need building

- [ ] Huge folders (1,000+ images) without the partial list
- [ ] Animated WebP and GIF thumbnails
- [ ] Optional GitHub token for a higher rate limit
- [ ] Cancel and progress bar for big zips
- [ ] Translations

Pick one and say so in an [issue](https://github.com/krvats/gitpics/issues/new/choose) so we don't double up. Or bring your own idea.

### How to jump in

```bash
git clone https://github.com/krvats/gitpics
cd gitpics
# open index.html in a browser, change something, refresh
# then open a pull request
```

More in [CONTRIBUTING.md](CONTRIBUTING.md).

### Your contributor badge

Once your PR is merged, this is yours for your profile, portfolio or CV:

```markdown
[![Contributed to GitPics](https://img.shields.io/badge/contributed%20to-GitPics-ff5a1f?style=for-the-badge&logo=github&logoColor=white)](https://gitpics.pages.dev)
```

[![Contributed to GitPics](https://img.shields.io/badge/contributed%20to-GitPics-ff5a1f?style=for-the-badge&logo=github&logoColor=white)](https://gitpics.pages.dev)

---

## How it works

- Reads folders with GitHub's Git Trees API, one request for all entries
- Loads images from `raw.githubusercontent.com`
- Thumbnails via [wsrv.nl](https://wsrv.nl), a free image proxy, with a fallback to the raw URL
- Recent history lives in `localStorage`

## Credits

- OG image: Landsat wallpapers from [leouieda/landsat-wallpapers](https://github.com/leouieda/landsat-wallpapers) (CC0)
- Thumbnails: [wsrv.nl](https://wsrv.nl)
- Typefaces: [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) and [Caveat](https://fonts.google.com/specimen/Caveat)
- Not affiliated with GitHub. Images belong to their repo owners.

## License

[MIT](LICENSE). Do whatever you want with it.

---

<div align="center">

Built out of frustration. Maintained out of stubbornness.

If it saved you some clicks, a [star](https://github.com/krvats/gitpics) helps other people find it.

</div>
