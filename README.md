# Clay landing pages

Personalized pre-demo landing pages for Clay.com. One page per prospect, sent by the account executive before the demo to help close the deal. These are private previews, not public marketing pages.

| Folder | Prospect | Live URL |
|---|---|---|
| `retool-calli-taylor/` | Calli Taylor, Global Head of Sales Development, Retool | https://clay-retool-calli.vercel.app |

`docs/` holds the account research brief and the writing rules for these pages.

## How a page is built
- Each folder is self-contained: a single `index.html` with inline CSS, a small JS snippet that plays videos on scroll, and the `clay assets/` files it references. It opens straight from disk.
- Structure: hero with a docked signal table, play cards tied to the table, Clay case studies, demo plan, closing call to action.
- The signal table uses the prospect's brand colors, pulled from their live site CSS. Each row is a sourced signal with a link and date.

## Rules
Full detail in `docs/personalized-landing-page-skill.md`.
- Every fact is sourced. Nothing about the prospect is invented, and interpretation is labelled as such.
- Written in first person from the AE, in plain short sentences, with each use case tied to a goal the reader owns.
- Clay voice: no exclamation marks, no emoji, no competitor names, no duration or "no slides" claims.

## Deploy a page
From inside a project folder:

```
npx vercel deploy --prod --yes --scope utsav-gtme --name clay-retool-calli
```

Use the same project name to keep the same URL. Production deploys are public to anyone with the link, so the page is marked `noindex`.

## Status and open items
- The closing button still has a `[CALENDAR LINK]` placeholder.
- The Roobert font files are trial files, fine for private previews but they need a licence for anything public.
- The prospect CSV and the asset zip are gitignored and live outside the repo.
