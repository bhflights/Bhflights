# BHFlights Android 2.0

Native Android/Kotlin implementation of the BHFlights three-tab concept.

## Primary navigation
- Flights: first screen; Skyscanner widget loads immediately.
- Buddy: exact flight/date matching UX and safety wall; secure Firebase backend should be configured before production posting.
- AI Help: local fallback + remote `https://bhflights.com/bhf_knowledge.json`, autocomplete and topic cards.

## Build
Open the `android` folder in Android Studio and sync Gradle. Build the `app` module.

## Firebase
The current Android build intentionally does not include a hard-coded Firebase credential. Configure Firebase/App Check and a server-side endpoint before enabling production Travel Buddy writes. Do not make the Realtime Database publicly readable.

## Privacy
Flight WebView uses a no-cache session, clears cookies/history/WebStorage, and disables third-party cookies. This minimizes local persistence; it does not guarantee that third-party servers cannot observe requests.
