---
name: personalized-landing-page
description: How to research and write a personalized pre-demo landing page for one Clay prospect. Use when building or rewriting a prospect page in this project. Covers what to do, what not to do, what is required, and what is not.
---

# Personalized landing page for one prospect

Learned from building `retool-calli-taylor.htm` (October 2026). The user rejected two drafts for content before approving the direction, so the content rules below matter more than the design rules.

## The one-line brief
A short note from the AE to one real person, in that person's own working language, tied to the goals they are measured on, with proof. It is not a copy of clay.com.

## Do
1. **Work on one account at a time.** Confirm the account and the contact with the user before building.
2. **Verify the contact is a real person at the company.** The CSV names could not be verified. Find the real buyer with a people search and confirm their current title.
3. **Find the reader's goals in their own company's words.** The best source is the job post for their role. Next best: their team's job posts, their own LinkedIn posts, and the company's launch posts.
4. **Collect two levels of signal.** Company level (launches, hiring, stated goals) and individual level (start date, their own posts). Four to six signals is enough.
5. **Open on the prospect and their problem, not on the AE.** The user rejected "I'm Utsav, the AE who'll run your demo" as too salesy. Use "I" sparingly later on the page.
6. **Use plain, short sentences.** One sentence per table cell. Each card gets a headline, a one-line goal, one or two sentences, and one "on the call" line.
7. **Tie each use case to a goal or KPI the reader owns.** For an SDR leader: predictable pipeline, meetings that become opportunities, pipeline per SDR, SE time.
8. **Use the reader's vocabulary.** SDR, BDR, AE, SE, quota, qualified, discovery, signups. Not Clay's product vocabulary.
9. **Prove each use case with a published Clay story.** Company, one number, one sentence on how. Take the numbers from clay.com/customers and link the story.
10. **Label opinion as opinion.** Facts go in one column with a source. The AE's interpretation goes in another, marked as "my take".
11. **Test every link, then test the quote.** A link must return 200 and the quoted words must be on the live page.
12. **Preview locally before deploying.** Open the file in the user's browser and wait for approval.

## Do not
1. **Do not write like a product page.** No "one system, four moves", no feature tour, no marquee of logos, no stats strip. The user called this "a replica of the Clay website".
2. **Do not write long.** The approved draft has about 700 visible words. The rejected one had about 1,260.
3. **Do not use abstract or invented phrasing.** Rejected examples: "Claygent checks the question the form can't answer", "Fit and intent land in one score", "Our read".
4. **Do not invent facts about the prospect.** No made-up numbers, tools, team sizes or processes. If it is a guess, say "I'm guessing".
5. **Do not link a page you have not opened.** Job posts close and redirect. One job post returned 404 and another redirected to a generic listing.
6. **Do not trust a LinkedIn post URL from a search snippet.** The suffix can be garbled. Use `https://www.linkedin.com/feed/update/urn:li:activity:<id>` instead.
7. **Do not trust an article's date.** One "September 2026" layoffs article described 2023 events. Check the content against other sources.
8. **Do not raise sensitive events** (layoffs, acquisitions) unless the user asks for them.
9. **Do not promise a duration or "no slides".** No exclamation marks, no emoji, no competitor names, no banned words from the tone guide.
10. **Do not redesign.** The user approved the visual design. Change the words, not the layout.
11. **Do not deploy, or build other accounts, without being asked.**
12. **Do not ask the prospect to prepare data.** "Bring 50 signups" was rejected as homework nobody will do. Offer two equal options: bring your own list and we qualify it on the call, or we build one live from signals.
13. **Do not label things with the page's own numbering.** "Hex · Way 3" meant nothing to the user. Label a case study with what it is about in plain words, such as "Hex · Account alerts".

## Required on the page
- The real contact's name, and the AE speaking in the first person.
- A signal table: 4 to 6 sourced rows, tagged company or "You", each with a date.
- Three ways Clay helps, each tied to one goal.
- Three case studies, each with a number and a link.
- What happens on the call, and what to bring.
- One clear button to book.
- `noindex`, and the private-preview footer line.

## Not required
- Marquee, stats strip, section intro paragraphs.
- Customer quotes inside the case cards.
- More than three use cases.
- A source link for a page that has closed. Keep the fact, drop the link, and say it has closed.

## Checks before showing the user
1. Every link returns 200.
2. Every quote is on the live page (or the source is marked as closed).
3. No exclamation marks, banned words, or duration claims.
4. Screenshot at 1440px and at 390px (use an iframe for 390px). The hero headline must sit below the clay props.
5. Visible word count is near 700.

## Technical notes
- The hero video is sized by width (`height: auto`) with `padding-top: 27vw` on the hero content. If the video is sized to the hero's height, a taller table pushes the props under the headline.
- Keep one HTML head and CSS. Swap only the `<body>` when rewriting copy.
- Research tools that worked: Exa (people search, page fetch), Firecrawl (case studies with a direct-quote query, brand colors).


## Publishing (learned 2026-10-06)
- **Vercel:** build a folder with the page as `index.html` plus only the `clay assets` files it references, then run `npx vercel deploy --prod --yes --scope utsav-gtme` from that folder. Redeploying to the same project keeps the same URL. Check the page and every asset return 200 as an anonymous visitor.
- **GitHub:** one private repo, `uj-git27/clay-landing-pages`, with one self-contained folder per prospect. Local clone: `Desktop\Bootprint\clay-landing-pages`. Leave out the prospect CSV and the assets zip. Git identity is set for that repo only.
- **Only add what the user is working on.** The first push included the older Sarah and Linear pages, and the user asked for Calli only.
- **Button wording:** "Confirm demo time", not "Confirm my demo time".
- Deploy and push only after the user approves the local preview.

## Current status (as of 2026-10-06)
- **Active prospect:** Calli Taylor, Global Head of Sales Development, Retool. This is the only account being worked on.
- **Source file:** `retool-calli-taylor.htm` in the project folder. Content and design are approved by the user.
- **Live:** https://clay-retool-calli.vercel.app (Vercel project `clay-retool-calli`).
- **GitHub:** https://github.com/uj-git27/clay-landing-pages (private), folder `retool-calli-taylor/` plus `docs/`.
- **Open:** the closing button still has the `[CALENDAR LINK]` placeholder. Three card buttons still use "my" ("Qualify my list", "Research my accounts", "Test my rule"); the user has not asked to change them.
- **Left as they are, by the user's choice:** the older Sarah Mitchell and Marcus Chen sites are still live on Vercel, the research brief in the repo still names Sarah Mitchell, and the first commit in the repo history still holds the Sarah and Linear folders.
- **Not built:** Linear, Loom, Webflow and Airtable pages in the new format. Research and real contacts for them are in `account-research-brief.md` and `CLAUDE.md`.
