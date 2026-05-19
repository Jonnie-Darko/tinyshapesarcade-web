# Privacy Policy: More Like Uhh…

**Effective date:** May 2, 2026
**Last updated:** May 18, 2026

This policy describes what information More Like Uhh… ("the app", "we") collects, how it's used, and the third-party services involved. The app is published by Tiny Shapes Arcade, a one-person studio operated by Jonathon Pifher.

If anything here is unclear, email **jonathon@tinyshapesarcade.com**.

---

## What we collect

### A random anonymous player ID
On first launch, the app generates a random UUID (e.g. `7c3e4c2a-…`) and stores it on your device. It's used to:
- Recognize the same player across sessions (so your in-progress game can resume)
- Tie your gameplay to your own backend session (so other players can't impersonate you)

It's not linked to your email, phone number, name, or any account. We can't identify you from it. If you uninstall the app, the ID is gone.

### Your gameplay
When you play, the app sends to our backend:
- Your guesses (the words you type in)
- Which category and difficulty you picked
- Your in-progress score and round number
- Your "ask a question" lifeline text, if you use it

This is the minimum needed to play the game. Your guesses are the input; the AI's responses are the output.

### Daily challenge results
When you finish a daily challenge (Regular Daily or Think Fast Daily), the app sends a short summary to our backend:
- Whether you won or gave up
- Your final score, round count, and total time
- Which lifelines you used (if any)
- The date of the challenge and which mode (Regular or Think Fast)

This is stored so we can show you and every other player anonymous aggregate stats for the day: total players, win rate, median score, fastest time, your rank within those numbers. Aggregates do not identify any individual player. Your random player ID is the only key used, and no real-world identity is tied to it.

### Crash reports
If the app crashes on your phone, an automatic crash report is sent to Firebase Crashlytics. The report contains:
- The crash stack trace (where in the code it broke)
- Your Android version and device model
- A randomly-generated install ID (different from the player ID above)

It does **not** contain your guesses, your secret noun, or any personal info.

### Reports you flag manually
If you tap the report flag (🚩) inside the game, you're sending us:
- The category, secret noun, or word pair you flagged
- The reason you picked from the list
- An optional free-text note (only what you type)

These help us catch bad words or unfair pairs.

---

## What we do NOT collect

- Your name, email, phone number, or any account credentials
- Your location
- Your contacts, photos, microphone, or camera
- Any device identifiers beyond the random IDs above
- Your browsing history or activity outside the app
- Anything from other apps on your device
- Payment info (the app is free, no purchases)

---

## Third parties involved

| Service | What they see | Why |
|---|---|---|
| **OpenAI** (api.openai.com) | Your guesses + lifeline questions, the secret noun the AI is "thinking of" | The game's AI runs on their models (gpt-4o-mini for chat, text-embedding-3-small for warmth comparisons) |
| **Supabase** (supabase.com) | Game session state, shared challenges, cached embeddings | Database backend so your game survives our server restarting |
| **Fly.io** (fly.io) | All HTTP requests + your IP address (for rate-limiting) | Hosts the backend |
| **Firebase / Google** (firebase.google.com) | Crash reports, app install events, your install ID | Crashlytics + App Distribution for closed testing |

Each of these has their own privacy policy:
- OpenAI: https://openai.com/policies/privacy-policy
- Supabase: https://supabase.com/privacy
- Fly.io: https://fly.io/legal/privacy-policy/
- Firebase: https://firebase.google.com/support/privacy

We don't sell your data and don't share it with anyone else.

---

## How long we keep it

- **Active game sessions**: deleted from our backend after 24 hours of inactivity
- **Cached AI responses** (embeddings of common words): kept indefinitely so we don't re-pay OpenAI for the same word twice
- **Crash reports**: kept by Firebase per their default retention (~90 days)
- **Manual reports you submit**: kept while the app is in development, no fixed deletion schedule
- **Daily challenge result rows**: kept indefinitely so leaderboard percentiles stay stable over time. If you want yours removed, email the address above with a rough date range of when you played and I'll find them

Local data on your device (achievements, streak, settings, and any reports you've flagged but haven't sent yet) stays until you uninstall the app or use **Settings → Reset stats**.

---

## Your rights

- **Delete everything**: uninstall the app. Your local data is gone, your random player ID is unrecoverable, any in-progress backend session expires within 24 hours.
- **Reset local stats**: Settings → Danger zone → Reset stats. Wipes your achievements, streak, and game history (does not affect backend sessions).
- **Ask a question or request data deletion**: email jonathon@tinyshapesarcade.com, and I'll respond within a week.

---

## Children

The app is not specifically designed for children under 13. We don't knowingly collect data from children. There's no age gate; the gameplay is general-audience but we don't claim COPPA compliance. If you're a parent and want your child's data removed, email me.

---

## Changes to this policy

If we change anything material, we'll update the "Last updated" date at the top and post the new version at the same URL. Significant changes will be called out in the app's release notes.

---

## Contact

Jonathon Pifher, Tiny Shapes Arcade
**jonathon@tinyshapesarcade.com**
