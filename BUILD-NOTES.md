# AJs Affordable AC — website

Static site for **AJs Affordable AC**, an air conditioning company on Oahu's
Windward side. Built by GoodcallAI.

Plain HTML and CSS. **No framework, no build step, no JavaScript.** Open any
`.html` file in a browser and it works. Deploys to Vercel as-is. Search engines
read every word of it, which is what ranking it later needs.

---

## Before this can go public — five steps, in order

| # | What | Who |
|---|------|-----|
| 1 | **Get AJ's Hawaii contractor license number.** Hawaii law (HRS §444-9.2) requires the license number in a contractor's advertising. The line is already written and switched off in the footer of every page, behind a `LAUNCH BLOCKER` comment. Fill in the number, delete the comment markers, on all seven pages. | AJ |
| 2 | **Register the domain** in AJ's name and add it in Vercel under **Project → Settings → Domains**. | Adeel |
| 3 | **Point the full-address tags at the real domain.** Every page except `404.html` has a comment in its `<head>` marking the spot. `og:image` (the picture shown when the link is shared) currently uses the temporary address `https://a-js-affordable-ac.vercel.app`: change it to the domain, and add `og:url` and `<link rel="canonical">` as full `https://` links. Add `"url"` and `"image"` to the JSON-LD block in `index.html`. Optionally add a `sitemap.xml`. | Adeel |
| 4 | **Switch off preview mode.** Two places: the `noindex` meta tag in every page (search for `PREVIEW MODE`) and the `X-Robots-Tag` header in `vercel.json`. `robots.txt` already allows crawling; add a `Sitemap:` line to it if you make a sitemap. | Adeel |
| 5 | **Put the website address on his Google Business Profile.** The Website field is empty today. This is what actually sends people to the site. | AJ |

---

## Pages

| File | What is on it |
|------|---------------|
| `index.html` | Cover with the phone number, three quick links, why us (4 points, each backed by a review quote), 3 service cards, 6-photo gallery, 3 reviews, service area, 6 questions. Carries the business schema. |
| `ac-installation.html` | What gets installed, how an install goes (4 steps, each from what customers wrote), 9-photo gallery, 3 install reviews. |
| `ac-repair.html` | Signs to call about, repair-or-replace, what to have ready, 3 reviews. |
| `ac-cleaning-maintenance.html` | Two before/after photos, how a deep cleaning is done, why it matters, 4-photo gallery, 2 reviews. |
| `about.html` | Who AJ is, the three things customers say most, **all 14 Google reviews**. |
| `contact.html` | Form, call/text card with hours, service area, what to have ready. |
| `404.html` | Not-found page. Sends people to the phone. |

The menu uses short labels ("Cleaning", "About") at every screen size. The full
names ("Cleaning & Maintenance", "About & Reviews") did not fit on one line
beside the phone button, and the page titles already carry them.

---

## Facts on the site, and where each one came from

| Fact | Source |
|------|--------|
| Name **AJs Affordable AC** (no apostrophe) | His Google listing, as AJ spelled it |
| Phone (808) 852-0008 | His Google listing |
| Hours: Mon–Fri 7:30am–7pm, Sat 10am–7pm, Sun 9am–3pm | His Google listing, 25 Sep 2026 |
| Installation, maintenance, repair; central and split systems; homes and businesses | The description on his Google listing |
| Cleaning | His own photos, and a review that mentions "maintenance and cleaning" |
| Based on the Windward side | His Google map pin sits in Waiahole. The site names the side of the island, never the exact spot. |
| Service area | See below |

### Service area

Eleven windward towns, north to south: Laie, Hauula, Punaluu, Kaaawa, Waikane,
Waiahole, Kahaluu, Ahuimanu, Kaneohe, Kailua, Waimanalo. Plus "Elsewhere on Oahu?
Call and ask."

Chosen by **driving time from his map pin, not a straight-line radius**. The
Ko'olau mountains make a 10-mile circle the wrong shape on Oahu: it would take
in Mililani and Wahiawa (almost an hour's drive) and cut out Waimanalo and Laie.
These are the towns on his side of the mountains within about 45 minutes, by a
route planner with no traffic. One review is from Kailua. **AJ has not confirmed
this list.** Correct it when he sees the site.

---

## Reviews

All 14 reviews on his Google profile as of 25 September 2026.

- **Word for word, spelling included.** Typos such as "professionl." and "He went
  out of his to get the job done" are the reviewers' own. Do not correct them;
  the site says the quotes are word for word. Only the apostrophes and quote
  marks were set in typographic style, and double spaces and the screen's line
  wraps inside sentences were removed.
- **Names are first name + last initial** (Gay T., James S.). Two reviewers use
  handles on Google and appear as those handles: `j808702`, `schylarwong`.
- **Two are shown only in part**: Gay T. and Hadassah & Ana S. Google cut them
  off at "More" and the full text was not captured. Each ends in "…" and says
  "Shown in part" with a link to Google. If the full text is captured later,
  replace them.
- Star ratings are not counted anywhere, and there is no review count, so
  nothing goes stale when new reviews come in. No `aggregateRating` in the
  schema either: Google does not allow a business to mark up its own reviews.

---

## Photos

24 photos plus the cover and the link-preview image, all from the links to his
Google profile, cropped and compressed. **All hidden metadata (including any GPS
location) was stripped** when they were re-saved.

The cover photo (link 38) had words scratched into the customer's concrete
pad, which looked like names. That strip is **blurred for privacy** in
`cover.jpg`, `cover-mobile.jpg` and `og-image.jpg`.

Left out on purpose. Do not add these back without asking AJ:

| Link # | Why |
|--------|-----|
| 17, 23, 26, 29, 43 | Look like a customer's uploads, not AJ's: they match the photos on j808702's review and were posted as one batch. Both videos are in this set. |
| 5 | A family's names on Christmas stockings |
| 10 | A client's framed photograph of a person |
| 8 | A man working on a unit. Nobody knows if it is AJ. **Worth asking**: a real photo of AJ would help the About page. |
| 6, 12, 14, 16, 25, 27, 30 | Dark, blurry or unclear |
| 1, 35 | Would need cropping (wall lettering; a reflection in glass) |
| 31 | Near-duplicate of 19 |

---

## The contact form

Posts straight to **Web3Forms** as a normal HTML form. No JavaScript.

- Access key `a9d05928-993d-4cca-905a-5817f4d2543c` in `contact.html`
- **Messages currently go to Adeel's inbox, not AJ's.** Before launch, give AJ
  his own Web3Forms key (so his inquiries reach him) and swap the value.
- The key is shared with GoodcallAI's other forms: 250 submissions a month
  between all of them on the free tier.
- The destination email address appears nowhere in the code.
- A hidden `botcheck` field catches basic spam bots.
- After sending, Web3Forms shows its own thank-you page.

---

## Left out until AJ approves

Rebates (Hawaii Energy "Clean Energy Ally"), financing, coupons, manufacturer
certification badges, awards, prices. Each is only allowed on the page if AJ
actually has it.

## Questions for AJ

1. His Hawaii contractor license number (launch step 1).
2. **Can (808) 852-0008 receive text messages?** The site offers "Call or text"
   everywhere. If it is a landline, texts
   will fail silently: remove the `sms:` links and the texting FAQ.
3. Is the service area list right?
4. Are all the photos his own jobs? (The home page calls them "Jobs we've done".)
5. Is the man in photo 8 him? Is there a photo of him he'd like on the site?
6. Is his business name spelled "AJs" or "AJ's", and is it an LLC?
7. Does a deep cleaning include the outdoor coil? The cleaning page only says
   it *can* be cleaned and to ask him.
8. Does he offer anti-corrosion coating as a service? One review says he
   coordinated it; the site says no more than that.
9. Is he a Hawaii Energy Clean Energy Ally? Does he offer financing? Any
   manufacturer certifications or awards? Any offer he wants to run?
10. Which email should website messages go to?

---

## Design

| Token | Value | Use |
|-------|-------|-----|
| `--ink` | `#062a3f` | Header, footer, dark sections |
| `--ocean` | `#0b4a6f` | Brand blue, links and buttons on light |
| `--sun` | `#ffc72c` | Call buttons, call bar, CTA band, accents on dark |
| `--sky` | `#e7f1f7` | Alternate light sections |
| `--paper` | `#f7fafc` | Page background |

Yellow is never used as text on white (1.6:1). Every text color pairing was
checked against WCAG AA (4.5:1) and passes.

Fonts are **self-hosted** (`assets/fonts/`), no Google Fonts request: Outfit for
headings, Inter for text. Both are under the SIL Open Font License; the license
files sit next to the fonts.

Spelling is plain Hawaiian place names without diacritics (Oahu, Kaneohe),
matching what people type into Google and what the local competitors use.
"Mahalo" appears only in thank-you lines, the way AJ uses it himself.

---

## Files that are not part of the site

- `.vercelignore` keeps **this file** off the live site. Without it, Vercel
  would publish it at `/BUILD-NOTES.md` for anyone to read.
- `favicon.ico` sits at the root for browsers that ask for it by name; the
  SVG icon is used everywhere else.

## Preview mode, and why robots.txt allows crawling

The temporary address is kept out of Google by the `noindex` meta tag on every
page and the `X-Robots-Tag` header in `vercel.json`. `robots.txt` deliberately
does **not** block crawling: Google only obeys `noindex` on pages it is allowed
to fetch, and a blocked page can still appear in results as a bare link.

## Housekeeping

**The GitHub repo is public.** These notes and the full photo history can be
read by anyone. Make it private: GitHub → the repo → **Settings** → **General**
→ **Danger Zone** → **Change visibility** → **Private**. Vercel deploys private
repos as well.

## Live preview

**https://a-js-affordable-ac.vercel.app** (Vercel project `a-js-affordable-ac`).
Checked live on 25 September 2026: all pages load, `/BUILD-NOTES.md` returns 404,
every page carries `noindex` and the `X-Robots-Tag` header, and every image
matches the repo byte for byte.

## Deploying to Vercel

This session has no Vercel login, so it cannot do this step. It takes about two
minutes:

1. Go to **vercel.com/new** and sign in with the same GitHub account.
2. Find **adeelshahzad5852-gif/AJs-Affordable-AC** and click **Import**.
3. Leave everything on its defaults: Framework Preset **Other**, Root Directory
   `./`, and no build, output or install command. It is plain HTML.
4. Click **Deploy**.

The only branch in the repo is `claude/great-franklin-ru98dm`, so it is the one
Vercel publishes. Every push to it redeploys the site.
