# Portfolio page output

Use this when the user asks for a portfolio page, not only a review. Iterates on the review: the same evidence rules apply.

## Order, top to bottom

1. **Opening line.** Use the owner's approved line word for word. For Rachael Quisel:
   "Automating my vacation rental led me to a career I love. Now I help other business owners automate their work and get their time back."
2. **Hero stats.** A bold section with big stat callouts, stated once, here only:
   - **$180,000** gross per year (La Maison Santa Barbara short-term vacation rental)
   - **About 5 hours a week** of her time, thanks to the automations
   Do not repeat these figures elsewhere on the page.
   Under the stats, add the supporting line quoted from airbnbai.rent: "Hosting a thousand guests a year took 20+ hours a week until I automated my workflows. I cut that number down to 5 hours."
3. **La Maison lead video.** Right under the hero, embed `https://airbnbai.rent/assets/la-maison-five-star-standard.mp4` large (poster `la-maison-five-star-poster.webp`) to open the La Maison section.
4. **The automations, one card each.** Never a single grouped highlight. Frame each card as proof of the hero result. Each card has:
   - Title and what it handles for her, in one or two plain sentences.
   - A link to the automation (public workflow guide or video folder).
   - The embedded video, required: `<video autoplay muted loop playsinline preload="metadata" poster="...">`, with the poster as the fallback image, plus a "Watch the video" link to the same file. If no video exists, fall back to a poster or an ffmpeg frame (`ffmpeg -ss 3 -i video.mp4 -frames:v 1 thumb.jpg`). Reference real files only.
   - Time saved, only when a repo states it. If none is stated, leave it out. Never estimate.

## Sources for La Maison

- Public guides: `RachaelQuisel/la-maison-github` `workflows/`
- Videos and posters: `RachaelQuisel/vacation-rental-automation-how-tos` `videos/`
- Preferred embed source: airbnbai.rent assets `https://airbnbai.rent/assets/<name>-1920x1080.mp4` with `<name>-poster.webp`: cleaner-job-texts, cleaning-calendar, tax-prep, guest-door-codes, property-inspection, booking-sync, ops-today, daily-pricing-sync.
- When the how-tos repo has no video for an automation, use the airbnbai.rent site assets (`https://airbnbai.rent/assets/<name>-1920x1080.mp4` and `<name>-poster.webp`, source in `RachaelQuisel/airbnbai`). Example: Booking sync to a shared calendar uses `booking-sync-1920x1080.mp4` and `booking-sync-poster.webp`, with the guide at `la-maison-github` `workflows/booking-sync`.
- The 8 La Maison automations: booking sync, cleaner signups by text, backup cleaner coverage, guest door codes, inspection follow-up, monthly tax prep, Ops Today briefing, daily pricing sync.
- Private code (link only if the reader has access, otherwise link the public guide): `RachaelQuisel/la-maison-github-private`, `RachaelQuisel/la-maison-dynamic-pricing`

## Separate card: Friendly task tracker

After the 8 La Maison cards, in its own section, add one card for the Friendly task tracker. Frame it as a general task tool for property managers, cleaners, or inspectors across many houses, not as a La Maison automation. Say plainly that her own rental is a single home. Video: `https://airbnbai.rent/assets/friendly-task-tracker.mp4`. Thumbnail: a frame pulled with ffmpeg, or `friendly-task-tracker-poster.webp`. Source: `RachaelQuisel/Airtable-AI-Webinar`.

## Patterns that make portfolios stand out

Researched Nov 2, 2026. Apply these on every page:

- **Clear in the first screen.** Who she is, what she does, and the result should be visible without scrolling ([ReadmeDesign](https://readmedesign.com/showcase)).
- **Story first, proof second.** Open with the personal line, then the stats ([ReadmeDesign examples](https://readmedesign.com/blog/best-github-profile-readme-examples)).
- **Real, sourced proof near the top.** Use only figures from a source you opened this run. Verified on airbnbai.rent: Airbnb Guest favorite, 4.97 rating, top 5% of eligible listings. Don't add other ratings or review counts unless a source you can read states them.
- **Same structure on every card.** Start with the result in the title. Add one sentence on what it handles, the video, and links to the video and the process or code ([GitHub Docs](https://docs.github.com/en/account-and-profile/tutorials/using-your-github-profile-to-enhance-your-resume), [Pranjul Rathour](https://pranjulrathour.github.io/blog/github-profile-that-recruiters-read/)).
- **One clear next step.** A "Book a call" button in the hero and again at the end, plus a direct email ([Forbes](https://www.forbes.com/sites/jodiecook/2026/09/08/turn-your-linkedin-profile-into-a-machine-that-sells-for-you/), [Blueberry Media](https://blueberry-media.co.uk/blog/linkedin-profile-optimisation-b2b-clients)).
- **Match LinkedIn.** Keep the opening line and the stats the same as her LinkedIn headline and About section. They follow the same "I help [who] [get what result]" pattern ([Resumeily](https://www.resumeily.com/learning/how-to-write-a-linkedin-profile)).
- **Easy to skim.** Use short lines and no badge walls.

Call to action for Rachael: `https://airbnbai.rent/#contact` and `rachael@xray.tech`.

## Rules

- Dollar amounts inside video scripts are sample data. Never use them as results.
- Don't show private repo contents on a public page.
