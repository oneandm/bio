<div align="center">

# Liquid Glass Bio Link

✦ ⋆ ˚｡ ⋆ ୨♡୧ ⋆ ｡˚ ⋆ ✦

*frosted glass, floating silver orbs, and one link for everything you are*

<br>

[the vibe](#the-vibe) &nbsp;✧&nbsp; [quick start](#quick-start) &nbsp;✧&nbsp; [make it yours](#make-it-yours) &nbsp;✧&nbsp; [deploy](#deploy) &nbsp;✧&nbsp; [help](#help)

</div>

<br>

## the vibe

a bio link page that's basically a pane of frosted glass floating in a gray void. one file, zero build step, live in like 2 minutes. no cap.

| ˖ what | ✧ how it feels |
| :-- | :-- |
| **liquid glass ui** | frosted blur, glossy edges, and a light glare that follows your cursor or finger. it's giving apple |
| **gray glossy theme** | graphite background with silver orbs drifting behind the glass, so the blur actually has something to flex on |
| **6 socials** | facebook, tiktok, instagram, spotify, telegram, github |
| **spotify playlist** | your music embedded right on the page, bestie |
| **animations** | staggered entrance, spinning avatar ring, brand glow on hover, tiny equalizer bars. `prefers-reduced-motion` is respected so nobody gets dizzy |
| **mobile first** | built for phones, since that's where your visitors are anyway |
| **zero dependencies** | pure html, css, js. the only outside thing is the inter font from google fonts |

<br>

## what's inside

```
.
├── index.html     # everything lives here (html + css + js)
├── vercel.json    # clean urls + a couple of security headers
└── README.md      # you are here ♡
```

<br>

## quick start

```bash
git clone https://github.com/USERNAME/REPO-NAME.git
cd REPO-NAME
python3 -m http.server 3000
```

then open `http://localhost:3000`. or skip all that and just double click `index.html`. both work.

<br>

## make it yours

open `index.html`, scroll to the `CONFIG` object inside the `<script>` tag. that's the only part you need to touch ✦

```js
const CONFIG = {
  name: "Your Name",
  handle: "@yourusername",
  bio: "your bio goes here",
  avatar: "",                                // "avatar.jpg" or a url. empty = your initial
  spotifyPlaylist: "37i9dQZF1DXcBWIGoYBM5M", // the id from open.spotify.com/playlist/<id>
  links: [
    { icon: "instagram", label: "Instagram", sub: "@yourusername",
      url: "https://instagram.com/yourusername", color: "#e1306c" },
    // ...the rest
  ]
};
```

| ˖ you want to | ✧ do this |
| :-- | :-- |
| change the playlist | copy the playlist link, take the id after `/playlist/`, paste it in `spotifyPlaylist`. the playlist must be public |
| add a link | add another object to `links`. icons available: `facebook` `tiktok` `instagram` `spotify` `telegram` `github` |
| add a new platform icon | drop its inline svg into the `ICONS` object, then use that key as `icon` |
| remove a link | delete its object from the array. that's it |
| fix the share preview | edit `<title>` and the `<meta>` tags at the top of the file |
| change the colors | the page bg is the `radial-gradient` on `body`, the orbs are the `.orbs i` rules. go wild, make it blue, i won't judge |

> **heads up:** if visitors aren't logged into spotify in their browser, the embed only plays 30 sec previews. that's a spotify thing, not a bug.

<br>

## deploy

pick your fighter. both are free ♡

<details>
<summary><b>push to github</b></summary>

<br>

```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/USERNAME/REPO-NAME.git
git push -u origin main
```

swap `USERNAME` and `REPO-NAME` with yours, obviously.

</details>

<details>
<summary><b>github pages</b></summary>

<br>

1. go to your repo, then **settings** > **pages**
2. under **source**, pick **deploy from a branch**
3. choose `main` and `/ (root)`, then hit **save**
4. wait a minute. your site is live at `https://USERNAME.github.io/REPO-NAME/`

</details>

<details>
<summary><b>vercel</b></summary>

<br>

1. push the repo to github first
2. go to [vercel.com/new](https://vercel.com/new) and import your repo
3. set **framework preset** to **other**, leave build command and output directory empty
4. hit **deploy**. you're live

every `git push` auto-redeploys after this. lowkey the best part.

prefer the terminal?

```bash
npm i -g vercel
vercel --prod
```

want a custom domain? vercel dashboard > your project > **settings** > **domains**.

</details>

<br>

## help

| ˖ problem | ✧ fix |
| :-- | :-- |
| glass looks flat, no blur | your browser is too old. `backdrop-filter` works on all modern browsers, so update it |
| spotify embed is blank | check the playlist id and make sure the playlist is public |
| icon tile is empty | the `icon` value doesn't match a key in `ICONS`. check the spelling |
| vercel isn't updating | did you actually push? check the deployments tab |

<br>

<div align="center">

✦ ⋆ ˚｡ ⋆ ୨♡୧ ⋆ ｡˚ ⋆ ✦

do whatever you want with it, mit vibes. add a `LICENSE` file if you want it official.

if this helped, leave a star. it's free and it makes me happy ♡

*made with way too much blur*

</div>
