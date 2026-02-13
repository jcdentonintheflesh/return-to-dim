# Return to Dim

X killed the Dim theme on web. This is a CSS-only userstyle that brings it back.

## Install

1. Install [Stylus for Chrome/Edge/Brave](https://chromewebstore.google.com/detail/stylus/clngdbkpkpeebahjckkjfobafhncgmne) or [Stylus for Firefox](https://addons.mozilla.org/en-US/firefox/addon/styl-us/)
2. **[Click here to install the theme](https://raw.githubusercontent.com/jcdentonintheflesh/return-to-dim/main/return-to-dim.user.css)** and hit "Install style"
3. Make sure X.com is set to **Lights out** (Settings > Display). The theme converts it to Dim.

## What it does

Swaps out the pure black Lights Out palette for the original Dim colors:

| | Lights Out | Dim |
|-|-----------|-----|
| Background | `#000000` | `#15202B` |
| Cards | `#16181C` | `#1E2732` |
| Inputs | `#202327` | `#253341` |
| Borders | `#2F3336` | `#38444D` |
| Secondary text | `#71767B` | `#8B98A5` |

Blue accent, white text, avatars, media all stay the same.

## How it works

Three layers of CSS overrides so nothing slips through:

1. **CSS custom properties** on `:root` (catches everything using `var()`)
2. **Inline style attribute selectors** (catches React Native for Web's `style=""`)
3. **Atomic class selectors** (fallback for X's generated `r-` classes)

Only activates in dark mode.

## FAQ

**Is this safe?**
Yes. No JS, no network requests, no permissions required. Just CSS. Can't read your cookies or DMs.

**Will it break when X updates?**
CSS variables and inline style selectors survive most rebuilds.

**Other tools besides Stylus?**
Copy the CSS inside the `@-moz-document` block into whatever you use (Stylish, userChrome, etc).

**Firefox?**
Works with Stylus for Firefox.

**Mobile?**
Web only. Mobile still has Dim built in (for now).

## Colors

The original Dim palette:

```
Background:   #15202B  rgb(21, 32, 43)
Cards:        #1E2732  rgb(30, 39, 50)
Inputs:       #253341  rgb(37, 51, 65)
Borders:      #38444D  rgb(56, 68, 77)
Muted text:   #8B98A5  rgb(139, 152, 165)
Text:         #E7E9EA  rgb(231, 233, 234)
Blue:         #1D9BF0  rgb(29, 155, 240)
Heart:        #F91880  rgb(249, 24, 128)
Retweet:      #00BA7C  rgb(0, 186, 124)
```

## License

MIT
