# Above All Flooring — handoff at ~60%

**Live:** https://10elizabethbell.github.io/aboveAllFlooring/ · **Repo:** https://github.com/10elizabethbell/aboveAllFlooring · **Built:** 2026-10-18 from Muse brief (run 2026-10-18, FB group sweep)

## What's built
- **World:** the basement in their own photo. Navy-slate wall (page ground), white baseboard, greige carpet. Their stencil AAF logo recolored to trim white (header mark, big in the close). Chalk-line blue only for hover, focus and form outlines.
- **Hero (signature):** a carpet canvas under the baseboard that lays its own vacuum stripes (light/dark by nap direction, like the lines in their photo). Finger or mouse brushes the pile in any direction (`touch-action:none`, rect read every frame, no rebuild on same-size resize). Marks settle back slowly (`RELAX`). Swatch row on the wall (Greige, Oatmeal, Slate, Moss, Cocoa) recolors the carpet and pre-fills "Carpet color you like" in the form.
- **Dividers:** chalk-line strings between sections. Each snaps once when it first comes fully into view (powder line + dust puff) and twangs when a finger or mouse crosses it. Same shared animation loop as the carpet.
- **Sections:** header (logo, tap-to-call number top right), hero (headline, promise, Get a quote + Text a photo of the room), Rooms we carpet (4 rows, each a pre-filled text), Fresh lines on day one (their one photo + Facebook link under it), How it goes (3 steps), quote form (composes a text; shows the message with a copy button as fallback), close (logo + their ad's own line), footer (name, phone, Facebook).
- **Tunables** at the top of each IIFE: carpet `CELL SHADE RELAX BRUSH_R LANE VAC_SPEED IDLE`; chalk `N SPEED DAMP PLUCK SNAP`.

## Assumptions I made
- **Area:** nothing about towns on the page. Burlington County / Marlton is inferred from where the ad was posted, and Muse said not to publish it. The form asks for the town instead.
- **"We" voice:** the ad was posted from Scott Karakashian's personal profile but his role isn't stated, so no person is named and the site speaks as "we".
- **Rooms list** (Basement, Family room, Movie room, Hangout space) comes from the ad's own wording; carpet is the only service on the page.
- **How it goes** is a plausible process (photo → pick carpet + price → install, tidy, ready for movie night). The owner should confirm it: do they bring samples? measure in person? pull up old carpet?
- **"Get a quote"**, not "free quote": the ad doesn't say quotes are free.
- **Texting:** whether the number takes texts is unknown. Texting is the main channel (rows, hero, form); calling is the top-right number and footer.
- **Swatch colors** are generic carpet tones for the demo, not their product line.
- **Colors:** the logo is black-and-white only; the navy wall + greige comes from their job photo.
- **Close line** reuses the ad's words: "There's nothing like stepping onto soft carpet in your basement. Let's bring your vision to life."

## Placeholders and gaps
- **Email:** none found, so there's no footer email. Add it to the footer when the owner gives one (footer only).
- **Photos:** only one (the ad image, 1542×2048). More jobs, and before/afters especially, would make the proof section.
- **Logo:** taken from their FB profile image (720px). A vector would be sharper; the favicon is the AAF mark on navy.
- No hours, prices, reviews, years, insurance, or owner name on the page, because none were found.

## Questions for the owner
- Do you take texts at (609) 923-6269? Is there an email for the footer?
- Which towns do you cover?
- Anything besides carpet (stairs, pad, removal, LVP, hardwood)?
- Do you bring samples to the house? Is the quote free?
- More job photos, and any before/afters?
- Who should the site name as owner?

## Ideas not built (yours to pick)
- **Runner-up world:** rebond carpet pad (the multicolor foam-chip pad under every carpet) as section texture, with a "peel back the corner" reveal on the photo.
- A stencil display face (e.g. Saira Stencil One) for headings to echo the logo. I kept the system stack per house style.
- Before/after slider once pairs exist.
- Carpet shown in perspective (a CSS 3D tilt so it reads as a floor) if Ellie wants more depth.
- A short vacuum sound or haptic on brush (probably too much).
- A "Message us on Facebook" option in the form for people who prefer Messenger (the ad's stated channel).

## Not verified
- Real-device touch on iOS Safari and in Facebook's in-app browser (tested Playwright Chromium + WebKit with simulated touch).
- Real SMS handoff on iOS/Android (links decode correctly in tests).
- Frame rate on old phones (carpet redraws a ~100×75-cell image per frame on phones; should be light).
