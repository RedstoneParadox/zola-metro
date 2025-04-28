+++
title="Guide"
template="index.html"
+++

{% align(align="center") %}
# Guide
{% end %}

This guide will walk you through how to set up Metro for your personal site. Installation instructions for zola themes can be found [here](https://www.getzola.org/documentation/themes/installing-and-using-themes/). 

## Configuration

All of Metro's config options fall under the `extra.metro` category and its subcategories - while this naming scheme is contradictory to the zola docs which would prefer suffixing all options with `metro_` under the `extra` category, this method looks nicer.

```toml
[extra.metro]
darkmode = true # Whether to show the darkmode/lightmode button
```

### Navigation and Socials

All navigation-related configuration is under the `extras.metro.nav` table in your `config.toml`. To add naviation to the header, define each link with the `name` and `path` keys as follows:

```toml
[extra.metro.nav]
site = [
    { name="Home", path="/" },
    { name="Guides", path="/guides/" },
    { name="Posts", path="/posts/" },
]
```

While having to manually set up navigation may seem tedious, it provides flexibility as you get to decide what pages are linked on the nav bar. <br />
Metro allows you to include social media links in the site footer as follows.

```toml
[extra.metro.nav]
socials = [
    { name="Github", url="https://github.com/RedstoneParadox/zola-metro", title="Repository" },
]
```

Where `name` is the name of the social media, `url` is the url for the social media page, and `title` is the tooltip that displays when hovering over the link and is also used for accessibility purposes. An icon for the link must be placed at `static/media/social/name.svg` (lowercase). The github icon and rss icons are included by default. Additionally, the rss feed button will show up automatically.

## Changing Site Colors

The site colors can be changed by changing the following css variables:

```css
html, body {
    /* Lightmode Colors */
    --lightmode-background-color /* Main website background color */
    --lightmode-secondary-background-color /* Background color for header, footer, a few other elements */
    --lightmode-border-color /* Color used for borders and <hr> elements */
    --lightmode-button-select-color /* Color of buttons while held */
    --lightmode-text-color /* Main text color */
    --lightmode-secondary-text-color /* Secondary text color */
    --lightmode-secondary-text-filter /* Secondary text filter */

    /* Darkmode colors */
    --darkmode-background-color
    --darkmode-secondary-background-color
    --darkmode-border-color
    --darkmode-button-select-color
    --darkmode-text-color
    --darkmode-secondary-text-color
    --darkmode-secondary-text-filter

    /* Accent colors */
    --accent-color /* Website accent color */
    --accent-filter /* Accent color filter for icons */
}
```

If you plan on not enabling the darkmode button and using a single color scheme regardless of use preference, change the following variables instead:

```css
html, body {
    /* Site colors */
    --site-background-color
    --site-secondary-background-color
    --site-border-color
    --site-button-select-color
    --site-secondary-text-color
    --site-secondary-text-filter

    /* Accent colors */
    --accent-color /* Website accent color */
    --accent-filter /* Accent color filter for icons */
}
```

