# sn00py.nix

A personal homepage in the spirit of old-school Myspace: clean retro boxes, a terminal header, and a light theme by default with a dark mode toggle. Linux, Nix, Python, cybersecurity, Neon Genesis Evangelion.

**Live site:** https://n0cr1s.github.io

```
[sn00py@nixos:~]$ touch grass
touch: cannot touch 'grass': Permission denied
```

## Features

- Single page: about, interests, blog, music and photos
- Light mode by default, dark mode on a button (the choice is saved only in the visitor's own browser)
- Color palette taken from the avatar: slate blue, cream, sweater maroon and yellow
- Works on desktop and phones, and respects reduced-motion settings
- No cookies, no trackers, no analytics, no third-party requests while the page loads
- Plain HTML and CSS plus a few lines of JavaScript for the theme button. No build step, no dependencies

## Files

| File | What it does |
| --- | --- |
| `index.html` | All the content and structure of the page |
| `style.css` | Layout, colors and both themes |
| `avatar.png` | Profile picture |
| `snoopy-header.png`, `snoopy-about.png`, `snoopy-footer.png` | Decorative stickers |
| `photo-1.png` to `photo-4.png` | Gallery images |

Missing images are skipped automatically, so the page still looks fine without them.

## Editing

- **Text:** open `index.html`, change the words, commit. The site updates within a minute or two.
- **Colors:** the top of `style.css` has two blocks of color variables, one for light mode and one for dark mode.
- **Preview locally:** run `python3 -m http.server` in this folder and open http://localhost:8000.

## Hosting

Hosted for free with GitHub Pages: Settings → Pages → deploy from the `main` branch, `/ (root)`.

## Credits

Site designed and coded by [Claude](https://claude.ai) (Anthropic), based on ideas and content from sn00py.nix.

Peanuts characters are © Peanuts Worldwide LLC / Charles M. Schulz. They appear here as fan art, and this page is not affiliated with or endorsed by the rights holders. Those images are not covered by any license this repository might have.
