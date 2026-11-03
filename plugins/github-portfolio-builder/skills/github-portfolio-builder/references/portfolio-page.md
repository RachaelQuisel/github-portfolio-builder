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
3. **The automations, one card each.** Never a single grouped highlight. Frame each card as proof of the hero result. Each card has:
   - Title and what it handles for her, in one or two plain sentences.
   - A link to the automation (public workflow guide or video folder).
   - A thumbnail: the video's `poster.png`, or a frame pulled from the video with `ffmpeg -ss 3 -i video.mp4 -frames:v 1 thumb.jpg`. Reference real files only.
   - Time saved, only when a repo states it. If none is stated, leave it out. Never estimate.

## Sources for La Maison

- Public guides: `RachaelQuisel/la-maison-github` `workflows/`
- Videos and posters: `RachaelQuisel/vacation-rental-automation-how-tos` `videos/`
- When the how-tos repo has no video for an automation, use the airbnbai.rent site assets (`https://airbnbai.rent/assets/<name>-1920x1080.mp4` and `<name>-poster.webp`, source in `RachaelQuisel/airbnbai`). Example: Booking sync to a shared calendar uses `booking-sync-1920x1080.mp4` and `booking-sync-poster.webp`, with the guide at `la-maison-github` `workflows/booking-sync`.
- The 8 La Maison automations: booking sync, cleaner signups by text, backup cleaner coverage, guest door codes, inspection follow-up, monthly tax prep, Ops Today briefing, daily pricing sync.
- Private code (link only if the reader has access, otherwise link the public guide): `RachaelQuisel/la-maison-github-private`, `RachaelQuisel/la-maison-dynamic-pricing`

## Separate card: Friendly task tracker

After the 8 La Maison cards, in its own section, add one card for the Friendly task tracker. Frame it as a general task tool for property managers, cleaners, or inspectors across many houses, not as a La Maison automation. Say plainly that her own rental is a single home. Video: `https://airbnbai.rent/assets/friendly-task-tracker.mp4`. Thumbnail: a frame pulled with ffmpeg, or `friendly-task-tracker-poster.webp`. Source: `RachaelQuisel/Airtable-AI-Webinar`.

## Rules

- Dollar amounts inside video scripts are sample data. Never use them as results.
- Don't show private repo contents on a public page.
