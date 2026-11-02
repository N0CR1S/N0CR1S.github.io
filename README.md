# sn00py.nix

![avatar](images/avatar.png)

> rebuild switch // one more rebuild switch // it works on my machine

**sn00py.nix** is my personal website: a small corner of the internet about NixOS, ricing, music and Neon Genesis Evangelion. It started as my SpaceHey profile and was rebuilt as a standalone site in a Y2K terminal style: periwinkle background, parchment cards, CRT scanlines, tickers, a cassette deck and a lot of fake shell sessions.

## About me

I run NixOS on Hyprland with the Caelestia shell, and the whole machine rebuilds from one config. I got here through Mint, Debian, Fedora, Arch, Void, Gentoo and FreeBSD, and broke something on every single one. Nix is the first place where breaking things is cheap. I write Python and Bash when I have to, I'm better at Linux than at coding, and security is next on my list: fundamentals first, tools after.

Away from the keyboard: piano, a lot of music (Linkin Park, Radiohead, Nirvana, Måneskin and more), maths, physics, chemistry and biology, psychology, hiking, climbing, skiing, snowboarding, kickboxing, Russian literature (I can't speak the language yet) and art museums.

## What's on the site

| Section | What it is |
|---|---|
| **Header** | Two scrolling tickers, the SN00PY.nix masthead on top of `snoopy-header.png`, and a sticky menu |
| **Side column** | Avatar, links, interests and "Who I'd like to meet"; stays on the left and scrolls along |
| **who is this guy** | The about terminal: `whoami`, `cat about.txt`, `neofetch` |
| **rice gallery** | Screenshots of my desktop setups (`photo-1` to `photo-4`) |
| **what happens when the pc is off** | Hobbies and interests, formatted like a text file |
| **side a, on loop** | A tape deck playing *i hate you* by h4rtbrkr (YouTube embed, Spotify link) |
| **fortune cookie** | Russian literature and philosophy quotes (Dostoevsky, Tolstoy, Nietzsche, Camus) |
| **secrets** | Clickable shell commands with easter eggs: `sudo rm -rf /`, `cowsay`, `ping`, `systemctl status magi`, `man piano`, `todo.txt` |
| **Footer** | Colophon on top of `snoopy-footer.png` |

## Design

- **Palette:** taken from `avatar.png`: periwinkle `#6e7ba2`, parchment `#f4ead6`, Joe Cool red `#a43a45`, sunshine gold `#f0c96a`, ink `#1d1618`.
- **Fonts:** Anton (headlines), Bodoni Moda (italic subtitles), Space Mono (text), VT323 (LCD displays), all from Google Fonts.
- **Layout:** a fixed-width side column next to a content area that fills the rest of the screen. The content is a CSS grid that rearranges itself to the available width, and on phones everything stacks into one column.
- **Tech:** plain HTML and CSS. No JavaScript, no build step, no dependencies. Animations respect `prefers-reduced-motion`.

## Project structure

```
.
├── index.html
├── style.css
├── README.md
└── images/
    ├── avatar.png
    ├── photo-1.png ... photo-4.png    # rice screenshots
    ├── snoopy-header.png              # header background
    ├── snoopy-about.png               # picture in the about terminal
    └── snoopy-footer.png              # footer background
```

## Run locally

Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy on GitHub Pages

1. Push this folder to a GitHub repo (for example `sn00py.github.io`).
2. Go to **Settings → Pages** and choose *Deploy from a branch*, then `main` and `/ (root)`.
3. After a minute the site is live at `https://<username>.github.io/`.

## Customize

- Colors and fonts: the variables at the top of `style.css`.
- Side column width: `.layout` in `style.css`.
- Rice screenshots: replace `images/photo-*.png` and edit the captions in `index.html`.
- Music: change the YouTube id in the `<iframe>` and the Spotify link.

## Elsewhere

- TikTok: [@sn00py.nix](https://www.tiktok.com/@sn00py.nix)
- SpaceHey: [spacehey.com/sn00py](https://spacehey.com/sn00py)

## Credits and notes

- Snoopy, Joe Cool and Woodstock are © Peanuts Worldwide (PNTS). This is a fan page and is not affiliated with them.
- The YouTube player needs one click, because browsers block autoplay.
- For a fully offline site, download the fonts and load them with `@font-face`.
