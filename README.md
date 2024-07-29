# Firefox Auto-hide Navbar Feature

ENGLISH | [한국어](README_KO.md)

This userChrome.css snippet provides a feature to automatically hide the address bar and title bar in Firefox browser. The elements appear when you move your mouse to the top, and automatically hide when you move your mouse elsewhere.

## Features

- Auto-hide address bar and title bar
- Show elements on mouse hover
- Smooth transition effect

## Installation

1. Open `about:config` in Firefox settings and set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`.
2. Find your Firefox profile folder (refer to "Profile Folder" in `about:support`).
3. Create a `chrome` folder in the profile folder (if it doesn't exist).
4. Create a `userChrome.css` file inside the `chrome` folder and paste the following code:

```css
#navigator-toolbox:not(:hover) > #titlebar,
#navigator-toolbox:not(:hover) > #nav-bar {
  margin-top: -36px;
  opacity: 0;
}
#titlebar, #nav-bar {
  transition: all 0.3s ease-in-out !important;
}
```

5. Restart Firefox.

## Customization

- Adjust the `-36px` value to change the degree of hiding.
- Adjust the `0.3s` value to change the transition speed.

## Caution

This CSS snippet is based on the latest version of Firefox. Future Firefox updates may affect its functionality.

## Troubleshooting

If the address bar is not visible, move your mouse to the top of the browser. If the problem persists, try "Refresh Firefox" in `about:support`.
