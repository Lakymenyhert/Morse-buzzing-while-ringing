# MorseVibApp v2 - Auto-build ready project (for Android 14 / Xiaomi)

This project detects incoming calls, looks up the caller name in Contacts,
converts the name to Morse code, and plays the Morse pattern as vibration.
The pattern repeats after a 2000 ms pause until the call is answered or rejected.

**Features in v2**
- Standard Morse timing, but with 4 sliders (dot, dash, letter gap, word gap) adjustable between 10 ms and 1000 ms.
- Repeat pause (fixed at 2000 ms) after each Morse sequence; pattern repeats while the call is ringing.
- UI in Hungarian with simple instructions.
- GitHub Actions workflow included: when you push this repo to GitHub, Actions will build a debug APK and expose it as an artifact.

**How to get an APK automatically (no Android Studio needed on your PC)**
1. Create a new GitHub repository (private is fine).
2. Upload the contents of this folder (push via git or upload ZIP) to the repo root.
3. In the repo, go to Actions → you'll see the "Android CI" workflow. Trigger it by pushing (or re-run).
4. After the workflow finishes, go to the Actions run → Artifacts → download `app-debug.apk`.
5. Transfer the APK to your Xiaomi phone and install (allow installing unknown apps).

**Xiaomi-specific notes**
- On MIUI, you may need to disable battery optimization for this app (Settings → Apps → MorseVibApp → Battery saver → No restrictions)
- Allow app to run in background and grant Contacts + Phone + Vibrate permissions on first run.

**If you'd rather I build the APK for you**
- I can't run builds from here, but this repo and workflow will build it automatically on GitHub. If you prefer, I can guide you step-by-step while you push the repo and retrieve the artifact.
