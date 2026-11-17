# Image asset map

Production images will be stored locally and referenced through `next/image`.

## Planned folders and names

- `brand/logo.svg`
- `hero/home-hero-desktop.webp`
- `hero/home-hero-mobile.webp`
- `categories/mens.webp`
- `categories/womens.webp`
- `categories/training.webp`
- `categories/footwear.webp`
- `products/<product-slug>.webp`
- `promos/mothers-day.webp`
- `promos/runners.webp`
- `story/brand-story.webp`
- `editorial/<article-slug>.webp`

## Rules

- Do not hotlink images from the reference website.
- Prefer AVIF or WebP for photos and SVG for the logo.
- Export only the sizes the layout uses.
- Keep the Hero image within the initial performance budget; lazy-load below-the-fold images.
- Replace temporary assets with licensed production assets before deployment.
