# Backstabbr Chancery

A custom dark theme for [Backstabbr](https://backstabbr.com), the online Diplomacy site. It tidies the game page into a flatter, more consistent interface: an ink-blue palette with brass accents, a map that fits your screen, a clearer orders list and a cleaner action bar.

It is a userstyle: plain CSS that a browser extension applies to backstabbr.com. It does not change how the site works, it only changes how it looks.

> Not affiliated with or endorsed by Backstabbr or Tile Games.

## Features

- **Balanced 50/50 layout.** The map and the orders panel split the full width of the screen evenly, like the site's own grid, and the panel stays in view while you scroll.
- **Calmer map colors.** The bright lavender sea and beige land are toned down so units, supply centers and labels stand out.
- **Clearer units and labels.** Units get a light outline and shadow, and map labels have a soft halo.
- **Legend chips.** Each power has a chip tinted with its own color. Army and Fleet are neutral chips drawn with CSS shapes.
- **Separate action buttons.** Hold, Move, Convoy and Support are four distinct buttons with clear disabled and selected states.
- **Cleaner orders panel.**
  - It stays in view while you scroll.
  - Country names line up with their color squares.
  - Order lines have even spacing, and the highlighted order has comfortable side padding.
  - The active tab has a single brass underline.
- **Consistent styling everywhere.** Cards, buttons, forms, dropdowns, modals, alerts, tooltips and the footer share one palette and one small set of corner radii.
- **Your fonts stay the same.** The theme does not import or override any fonts.
- **Responsive and accessible.** It adapts to small screens, shows clear keyboard focus, and respects reduced-motion settings.

## Install

1. Install the [Stylus](https://add0n.com/stylus.html) extension for Chrome, Edge, Firefox or Opera.
2. Install the theme in one of two ways:
   - **From the file:** open `backstabbr-chancery.user.css` from this repository, choose **Raw**, and Stylus will offer to install it.
   - **Manually:** in Stylus, choose **Write new style**, paste the contents of `backstabbr-chancery.user.css`, and save.
3. Refresh backstabbr.com.

### Optional: automatic updates

Add these lines to the header at the top of the file, using your own GitHub details, so Stylus can offer updates when you publish a new version:

```css
@homepageURL  https://github.com/YOUR-USERNAME/backstabbr-chancery
@updateURL    https://raw.githubusercontent.com/YOUR-USERNAME/backstabbr-chancery/main/backstabbr-chancery.user.css
```

Remember to raise `@version` each time you publish a change.

## Customize

All the main settings are variables at the top of the file, under `:root`.

| What | Where | Notes |
| --- | --- | --- |
| Accent color | `--brass`, `--brass-hi`, `--brass-ink` | Change all three together |
| Surface colors | `--ink`, `--panel`, `--panel-2`, `--panel-3`, `--line` | Page, cards, controls, borders |
| Corner radii | `--r-sm`, `--r-md`, `--r-lg` | Details, controls, containers |
| Map height | `--map-h` | Raise the number you subtract from `100vh` to make the map smaller |
| Minimum map width | the `max(850px, ...)` value in the map column rule | Keeps the legend on one line |
| Original map colors | the `#map svg > image` rule | Delete that rule to remove the color toning |

## Compatibility

- Built for the game page at backstabbr.com, including sandbox games.
- Uses `color-mix()` and `:has()` for the legend chip colors, which work in current versions of Chrome, Edge, Firefox and Safari. In older browsers the chips fall back to plain dark chips.
- Backstabbr's own CSS sets some styles with inline values and high-priority rules, so this theme uses `!important` in several places. If a site update changes its markup, some selectors may need adjusting. Please open an issue if that happens.

## Contributing

Bug reports and screenshots are welcome. When reporting a problem, please include:

- your browser and version,
- your window size,
- a screenshot of the problem,
- the page address, with any private game IDs removed.

## License

[MIT](LICENSE)
