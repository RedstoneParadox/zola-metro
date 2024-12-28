+++
title="Getting Started"
weight=0
+++

This guide will walk you through how to set up Metro for your personal site. Installation instructions for zola themes can be found [here](https://www.getzola.org/documentation/themes/installing-and-using-themes/).

## Navigation

All navigation-related configuration is under the `extras.metro.nav` table in your `config.toml`. To add naviation to the header, define each link with the `name` and `path` keys as follows:

```toml
[extra.metro.nav]
site = [
    { name="Home", path="/" },
    { name="Guides", path="/guides/" },
    { name="Posts", path="/posts/" },
]
```

While having to manually set up navigation may seem tedious, it provides flexibility as you get to decide what pages are linked on the nav bar.

### Social Media Links

Metro allows you to include social media links in the site footer as follows.

```toml
[extra.metro.nav]
socials = [
    { name="Github", url="https://github.com/RedstoneParadox/zola-metro", title="Repository" },
]
```

Where `name` is the name of the social media, `url` is the url for the social media page, and `title` is the tooltip that displays when hovering over the link and is also used for accessibility purposes. An icon for the link must be placed at `static/media/social/name.svg` (lowercase). The github icon is included by default.