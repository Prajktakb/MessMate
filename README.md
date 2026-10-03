# MessMate 🍽️

## The annoyance
Hostel/class friends waste time deciding where or what to eat. I noticed this kind of small decision often turns into a long WhatsApp discussion.

## Constraint: #2 — Offline
My PRN ends in **2**, so the app must still work after the first visit with Wi‑Fi turned off. MessMate uses a **service worker** to cache the app shell and **localStorage** to save polls and votes on the device. The UI shows Online/Offline status.

The hosted version is served from Vercel. The project also includes `config.js` and `supabase.sql` for the required hosted-database component; Supabase can be added for online backup/sync without removing the offline-first behavior.

## The great part
**Offline-first voting.** Once the app has been opened once, a user can create/open saved polls and vote with Wi‑Fi off. No account is required.

## Two testers
Show the deployed app to two people without explaining it. Record only what actually happens:
- Tester 1 got stuck at: ______
- Changed: ______
- Tester 2 got stuck at: ______
- Changed: ______

## AI
I used AI to scaffold the HTML/CSS/JavaScript, improve the UI, and help debug the offline flow.

One thing AI got wrong: ____________________
How I fixed it: ____________________

## Not done
- Cross-device real-time sync is not included in the offline local mode.
- No accounts/authentication.
- No advanced moderation/rate limiting.
- Supabase schema is included for the hosted-database requirement; online sync can be extended later.

## Run locally
```bash
npx serve .
```
Open the local URL once, then turn Wi‑Fi off and refresh to demonstrate the offline requirement. For service workers, use `localhost` or a deployed HTTPS URL rather than opening `index.html` directly.

## Environment/config
- `SUPABASE_URL`
- `SUPABASE_ANON_KEY`

Never use a Supabase service-role key in frontend code.

## Stack
HTML, CSS, vanilla JavaScript, Service Worker, localStorage, optional Supabase/Postgres, Vercel.
