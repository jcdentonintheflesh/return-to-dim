# Return to Dim

**Restore the classic Twitter "Dim" dark blue theme on X.com.**

X removed the beloved Dim theme from the web in February 2026. This brings it back — pixel-perfect, using the original color palette.

Pure CSS. No JavaScript. No tracking. No permissions. Nothing to trust but colors.

---

## Install (30 seconds)

### Step 1: Get the Stylus extension

| Browser | Link |
|---------|------|
| Chrome / Edge / Brave | [Stylus on Chrome Web Store](https://chromewebstore.google.com/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne) |
| Firefox | [Stylus on Firefox Add-ons](https://addons.mozilla.org/en-US/firefox/addon/styl-us/) |

### Step 2: Install the theme

**[Click here to install Return to Dim](../../raw/main/return-to-dim.user.css)**

Stylus will open a preview — click **"Install style"**. Done.

### Step 3: Make sure X.com is set to dark mode

Go to X.com → More → Settings → Display → **Lights out**. The theme converts Lights Out into Dim automatically.

---

## What it does

Overrides X.com's "Lights Out" (pure black) dark mode with the original Dim color palette:

| Element | Lights Out (current) | Dim (restored) |
|---------|---------------------|----------------|
| Background | `#000000` | `#15202B` |
| Cards / surfaces | `#16181C` | `#1E2732` |
| Search / inputs | `#202327` | `#253341` |
| Borders | `#2F3336` | `#38444D` |
| Secondary text | `#71767B` | `#8B98A5` |

Everything else (blue accent, white text, avatars, media) stays the same.

---

## How it works

Three-layer CSS override strategy for maximum coverage:

1. **CSS custom properties** — overrides X.com's `--background`, `--border`, and `--color-gray-*` variables
2. **Inline style selectors** — catches colors set directly by React Native for Web via `style=""`
3. **Atomic class selectors** — fallback for any remaining elements using X's generated `r-` classes

All rules scoped under `body.LightsOut` — the theme only activates when you're in dark mode.

---

## FAQ

**Is this safe?**
Yes. It's pure CSS — there is no JavaScript, no network requests, no permissions, no data collection. The entire source is readable in one file. CSS literally cannot access your cookies, passwords, or DMs.

**Will it break if X.com updates?**
The three-layer strategy makes it resilient. CSS custom properties and inline style selectors survive most X.com rebuilds. If something breaks, open an issue and we'll patch it fast.

**Can I use this with Stylish / other tools?**
The `.user.css` format works with Stylus (recommended). For other tools, copy the CSS between the `@-moz-document` blocks into your tool's editor.

**What about Firefox?**
Fully supported via the Stylus Firefox add-on.

**Does this work on mobile?**
No — this is for the web app only (x.com in a browser). Mobile apps still have Dim built in (for now).

---

## Color Reference

The original Twitter Dim palette, preserved:

```
Primary Background:   #15202B  rgb(21, 32, 43)
Secondary Background: #1E2732  rgb(30, 39, 50)
Elevated Surface:     #253341  rgb(37, 51, 65)
Border / Divider:     #38444D  rgb(56, 68, 77)
Secondary Text:       #8B98A5  rgb(139, 152, 165)
Primary Text:         #E7E9EA  rgb(231, 233, 234)
Accent Blue:          #1D9BF0  rgb(29, 155, 240)
Like (heart):         #F91880  rgb(249, 24, 128)
Retweet:              #00BA7C  rgb(0, 186, 124)
```

---

## License

MIT — do whatever you want with it.
