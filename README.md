# Unipex Sports website

React + Vite + Tailwind CSS 4 + Framer Motion + Lucide.

    npm install
    npm run dev        # local development
    npm run build      # production build in /dist
    npm run build:single   # one self-contained HTML file in /dist-single

## Where to change things

| What | File |
| --- | --- |
| Phone, address, hours, rating, map links, socials | `src/config/site.js` |
| All page copy, categories, custom jersey options | `src/config/content.js` |
| Every photograph | `src/config/media.js` |

## Adding real photographs

1. Put the image in `public/images/` (for example `hero.jpg`).
2. In `src/config/media.js` set that slot's `src` to `/images/hero.jpg`.

Empty slots render a labelled pitch-marking placeholder. Use photographs the
shop owns or has permission to use. The Google Maps listing could not be read
automatically (it needs JavaScript), so no store photos were copied from it.

## Confirm before publishing

- Opening hours, the 2012 founding year, and the Google rating and review count
  (`site.verify` lists them). Set `site.founded.show` to `false` to hide the year.
- Reviews: paste genuine ones into `reviews.quotes` in `content.js`
  (`{ author, text, date }`). Until then the section shows the rating and the
  themes customers mention, not invented quotes.
- Social links: add verified URLs to `site.socials`. None are shown today.
- Custom jersey: the preview is an illustration. Printing options, prices and
  turnaround are not promised anywhere on the site.

## Structure

    src/config      business facts, copy, image registry
    src/lib         WhatsApp/tel links, message builder, colour helper
    src/hooks       scroll, body lock, escape key, active section
    src/components  ui (Button, Media, Marquee...), layout, sections, custom, seo
