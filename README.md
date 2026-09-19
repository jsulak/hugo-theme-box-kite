# Box Kite

A minimal blog theme derived from the Hugo Minos theme. Requires Hugo 0.166.0 or later; tested with 0.166.0.

## Installation

```sh
git submodule add https://github.com/jsulak/hugo-theme-box-kite.git themes/box-kite
```

Configure your site:

```toml
theme = "box-kite"
locale = "en-US"

[params]
  author = "Your name"
  customCSS = ["css/custom.css"]

[pagination]
  pagerSize = 10

[markup.highlight]
  style = "tomorrow-night"
```

Code highlighting uses Hugo's built-in renderer. Add a language identifier to fenced code blocks to enable highlighting. No browser-side highlighting library is loaded.

## Options

Set `params.noPostNavigation = true` to hide the next/previous post links.

Optional Disqus comments use the current Hugo services configuration:

```toml
[services.disqus]
  shortname = "your-shortname"
```

Post front matter supports:

- `featuredImage`: image URL displayed on the homepage.
- `hidden: true`: exclude the page from the homepage listing.
- `omitDate: true`: hide the date on the individual page.
- `nocomment: true`: disable Disqus on the individual page.

## Upgrading from the legacy theme

Author information now comes from `params.author`. Disqus uses `services.disqus.shortname`. Post navigation uses Hugo's current `Next` and `Prev` methods.

The legacy Universal Analytics, Smart TOC/jQuery, KaTeX, and Highlight.js integrations have been removed. The `googleAnalytics`, `smartToc`, and `katex` options are no longer supported by this theme. Use Hugo's built-in highlighting configuration as shown above.

## Credits and license

Maintained by James Sulak. Based on [Carson Ip's Hugo Minos port](https://github.com/carsonip/hugo-theme-minos) of [PPOffice's Hexo Minos theme](https://github.com/ppoffice/hexo-theme-minos).

Licensed under the MIT License; see [LICENSE.md](LICENSE.md).
