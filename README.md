# Beef Finder

Find the nearest North Shore roast beef sandwich, and judge it by a weird close-up of the meat.

## What works now
- GPS lookup sorts the seeded places nearest first (haversine distance, runs in the browser).
- Seeded with the classics: Kelly's (Revere Beach, Saugus), Bill & Bob's (Salem), Nick's (Beverly).
- Each place has a deep-dive section. Current text is starter notes and needs real tasting notes.
- Anyone can add a place, and add a close-up photo plus a line about the sandwich.

## Known limits
- Contributions are saved in the contributor's browser (localStorage) only. Nobody else sees them yet.
- Coordinates are approximate. Verify each address before trusting the distances.
- Photos must be the contributor's own. The app does not pull images from the web.

## Next steps
1. Shared backend for uploads (for example Supabase or Firebase: a table for places and notes, a bucket for photos).
2. Moderation: a simple approve queue so open contributions stay on-topic.
3. Verify addresses and expand the seed list: more of the North Shore, plus the Lynn, Peabody, Danvers and Saugus spots.
4. Real deep dives: meat cut, slicing, roll, sauce ratio, the signature order.

## Run it
Open `index.html` in a browser. GPS needs HTTPS or localhost, so GitHub Pages works well.
