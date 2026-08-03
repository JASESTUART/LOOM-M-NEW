# Embedding men.html in GoHighLevel

The men's page is hosted on GitHub Pages:
**https://jasestuart.github.io/LOOM-M-NEW/men.html**

Use the same full-screen iframe pattern as the other pitch pages. Paste this
into a GHL **Custom Javascript/HTML** element, then Save → Publish.

```html
<style>
  html, body { margin:0; padding:0; background:#05070d; }
  #bba-frame { position:fixed; inset:0; width:100%; height:100%; border:0; }
</style>
<iframe id="bba-frame"
  src="https://jasestuart.github.io/LOOM-M-NEW/men.html"
  title="Better Body Academy"
  allow="autoplay; fullscreen; picture-in-picture; encrypted-media"
  allowfullscreen></iframe>
```

Notes:
- `position:fixed; inset:0` makes the iframe fill the whole browser window;
  the page scrolls inside the iframe and all nav anchors work natively.
- The `allow="autoplay; fullscreen; ..."` attribute is required so the hero
  video autoplays and the fullscreen button works inside the embed.
- Do NOT paste the raw HTML into GHL — the page relies on relative asset and
  image paths that only resolve on GitHub Pages.
