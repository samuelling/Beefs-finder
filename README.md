# Beef Finder

Find the nearest North Shore roast beef sandwich, and judge it by a weird close-up of the meat.

## What works now
- GPS lookup sorts the seeded places nearest first (haversine distance, runs in the browser).
- Seeded with the classics: Kelly's (Revere Beach, Saugus), Bill & Bob's (Salem), Nick's (Beverly).
- Each place has a deep-dive section. Current text is starter notes and needs real tasting notes.
- Anyone can add a place, and add a close-up photo plus a line about the sandwich.
- "Hunt this beef" gives a hotter/colder readout as you walk toward a place, plus a compass arrow that points at the beef as you turn. On iPhone it asks for motion-sensor permission the first time. If the compass is unavailable it falls back to your direction of travel, then to a plain "head northeast".
- Optional Google Places features (see below): live ratings and reviews, a "Discover more beef" search, and live coordinates for the hunt.

## Google Places setup (optional)
Without a key the app works fine; the Google buttons just stay hidden.
1. In Google Cloud, create a project, attach a billing account, and enable **Places API (New)** and **Maps JavaScript API**. Check Google's current pricing and free usage before relying on it.
2. Create an API key and restrict it: HTTP referrers set to your site's URL (for example `https://samuelling.github.io/*`) and API restrictions set to those two APIs.
3. Paste the key into `GOOGLE_MAPS_API_KEY` near the Google section of `index.html`. A referrer-restricted browser key is meant to be public.
4. Terms of use: Google data is fetched live, shown with attribution, and never saved. Only Google place IDs are stored, which the terms allow. Do not copy reviews into the library.

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
