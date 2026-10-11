# Baby Moves — Phase 0 voice feasibility test

This is a temporary test harness, not the production app.

## Recommended way to test on a phone

Speech recognition and microphone access require a secure context. Do not open the page from a phone using a plain LAN URL such as `http://192.168.x.x:8000` and expect it to work. Publish this folder temporarily to an HTTPS static host (for example a temporary Cloudflare Pages project) or use a trusted HTTPS preview environment.

1. Open the HTTPS URL on the actual phone.
2. Record phone model, OS version, browser and browser version.
3. Start listening and allow microphone access.
4. Test each approved command individually in the selected language.
5. Test unknown speech, a longer sentence containing “kick”, background noise, and restart after stopping.
6. Run the lock-screen test three times: start listening, lock for 30–60 seconds, unlock and inspect the status/log. Repeat with battery saver enabled if applicable.
7. Test again after switching to another app and returning.
8. Write down outcomes. The page does not persist test transcripts or logs.

## Important
- The browser speech-recognition service may process audio externally. This harness does not prove that speech recognition is offline.
- The API may be missing, disabled, or behave differently by browser and OS.
- A page that visually appears to be listening may not actually be receiving audio after the screen locks. Confirm by speaking test phrases while locked, then checking whether the expected results were received.
- Do not use this test harness for clinical decisions.
- Font CSS imports Google Fonts for visual parity; this can be removed for a purely offline diagnostic page.
