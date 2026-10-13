# వాక్య దీపం — Telugu Bible & Church Community (Starter)

Telugu-first, mobile-friendly browser app prototype.

## Included in this prototype
- Telugu home screen and daily promise verse card
- Bible navigation interface listing all 66 books and their chapter counts
- Sample verse display for a few chapters only
- Local church profile creation with image upload
- Local church discovery and join-request demo
- Local prayer request form
- Local event creation and Jitsi meeting-room link generation
- Saved verse list, notification permission prompt, and JSON export
- Responsive layout for iPhone Safari and desktop browsers

## Important limitations
This is a frontend starter, not a production-ready hosted service:
- The complete Telugu Bible text is NOT bundled yet. Most chapters intentionally show a notice instead of pretending the full text is available.
- Church profiles, prayer requests, events, and saved verses are stored in the current browser/device only. They do not sync between users.
- Admin authentication, secure role checks, moderation, cloud image storage, backend APIs, and privacy controls are not implemented.
- The 8 AM card is shown when the app opens. Scheduled push notifications require hosting, a service worker, push subscription storage, and a scheduled server-side sender.
- Jitsi meeting links can be generated, but 200-person capacity is not guaranteed by a public/free room. Validate provider limits and test capacity before advertising 200 attendees.

## Bible data research
A public GitHub project lists all 66 Telugu Bible books as JSON: https://github.com/aruljohn/Bible-telugu
Before bundling any text, verify the exact repository license and the translation's redistribution rights. A separate FreeBiblesIndia Telugu repository is CC BY-SA 4.0 but currently describes the New Testament only: https://github.com/FreeBiblesIndia/Telugu_Bible

## Run locally
Open `index.html` in a modern browser. For iPhone use Safari. Some browser features (sharing, notifications) require HTTPS or a supported browser context.

## Suggested production architecture
- Frontend: this responsive PWA
- Auth + database: Supabase or Firebase free tier (check current limits)
- Image storage: cloud object storage with strict upload limits
- Daily 8 AM notification: scheduled backend job, with each user's timezone stored
- Meetings: Jitsi integration, after confirming capacity and acceptable terms
- Admin: verified church admin role; users cannot self-assign admin permissions
