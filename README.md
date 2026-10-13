# వాక్య దీపం — Telugu Bible & Church Community

A Telugu-first Progressive Web App (PWA) starter for mobile browsers.

## Features in this prototype
- Bible book/chapter navigation and online loading of chapter-and-verse text from the aruljohn/Bible-telugu GitHub repository. The repository lists all 66 books and is marked MIT; validate translation provenance and source data before public distribution. Internet access is required to fetch a chapter.
- Search a reference such as `యోహాను 3:16`.
- Church profile creation with image upload, member list, prayer requests, events, saved verses and a Jitsi meeting entry point.
- PWA manifest, service worker shell caching, app icons and install instructions for Android/iOS.

## Run and publish
1. Upload the entire folder to a static HTTPS host (for example GitHub Pages or another static host). Do not open the HTML as a local `file://` page; service workers and install features require HTTPS or localhost.
2. Visit the hosted URL in Chrome on Android and choose **Install app** or **Add to Home Screen**. On iPhone, open the hosted URL in **Safari**, tap **Share**, then **Add to Home Screen**.
3. Bible chapters are fetched from GitHub over the internet; the current service worker caches the app shell, not the entire Bible text.

## Important limitations
- This is a frontend prototype. Church profiles, member phone numbers, prayer requests and events are saved only in the current browser/device using localStorage; they are not shared securely between users. Do not use real sensitive member data until a secure backend/authentication and role-based access control are implemented.
- Demo mute/unmute controls do not moderate actual Jitsi participants. Real host controls require authenticated moderator integration. A public Jitsi room does not guarantee 200-person capacity.
- Daily verse display is not a scheduled push notification. Reliable 8:00 AM push notifications require notification permission plus a hosted push/scheduling backend.
- No subscription/payment code is included, but hosting, push and large video meetings may incur costs depending on provider and scale.

## Prayer community update
- Prayer requests can be associated with a selected church, marked private for this browser demo, or shared anonymously in the demo church view.
- People can add encouragement/prayer responses to a request and delete a request from the current device.
- A church filter is provided for viewing requests associated with a selected church.
- A consent checkbox is required before saving a request.

**Privacy/security limitation:** these are client-side demo controls only. Data stays in the current browser's localStorage and is not synchronized to other members. There is no real identity verification, server authorization, encryption-at-rest guarantee, or role-based privacy enforcement. Do not enter sensitive real prayer details until a secure backend with authentication, per-church access rules, encrypted transport/storage, abuse reporting, retention/deletion policies, and admin moderation is deployed.
