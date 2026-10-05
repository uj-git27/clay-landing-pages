# Clay landing pages

Personalized pre-demo landing pages, one folder per prospect. Each folder is self-contained: `index.html` plus the `clay assets` it uses, so it can be opened from disk or deployed as-is.

| Folder | Prospect | Live URL |
|---|---|---|
| `retool-calli-taylor/` | Calli Taylor, Global Head of Sales Development, Retool | https://clay-retool-calli.vercel.app |
| `retool-sarah-mitchell/` | Sarah Mitchell, Retool (earlier V3 design) | https://clay-retool-sarah-five.vercel.app |
| `linear-marcus-chen/` | Marcus Chen, Linear (earlier V3 design) | https://clay-linear-marcus.vercel.app |

`docs/` holds the account research brief and the writing rules for these pages.

## Deploy a page
From inside a project folder:

```
npx vercel deploy --prod --yes --scope utsav-gtme
```

Deploying to the same Vercel project keeps the same URL.

## Notes
- Private previews. Pages are marked `noindex`.
- The Roobert font files are trial files, for internal previews only.
- The closing button on each page still has a `[CALENDAR LINK]` placeholder.
