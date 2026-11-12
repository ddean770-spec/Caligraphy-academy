# Calligraphy Academy / Ink & Flourish

A native Kotlin Android starter for S Pen calligraphy practice.

## Build an APK for free using GitHub Actions (phone-only workflow)

You do not need Android Studio or a paid Replit plan. GitHub Actions can run the Android build in the cloud.

1. On your Android phone, open https://github.com and create a free account (if needed).
2. Create a new repository named `calligraphy-academy`. Choose **Public** for the simplest free Actions usage, or Private if you prefer to keep the source private (GitHub's free plan includes a limited monthly Actions allowance for private repositories).
3. On the new repository page, choose **Add file → Upload files**.
4. Extract this ZIP on your phone first, then upload the *contents* of the `ink-flourish` folder into the repository root. Make sure `.github/workflows/build-apk.yml` is included. Some mobile file pickers hide dot-folders; if so, create `.github/workflows` in GitHub using Add file and create `build-apk.yml`, then paste the workflow from this project.
5. Commit the files to the `main` branch.
6. Open the repository's **Actions** tab. Select **Build Android APK** and tap **Run workflow** if it has not started automatically.
7. Wait for the run to finish with a green tick. Open that run, scroll to **Artifacts**, and download `calligraphy-academy-debug-apk`.
8. Extract the downloaded artifact ZIP on your phone. Tap `app-debug.apk` to install it. If Android asks, allow your browser or file manager to install unknown apps for this installation.

## What this first version includes

- Native Android `MotionEvent` stylus detection and pressure-based stroke width.
- Guided letter practice with baseline, x-height and ascender guides.
- Starter lessons across Copperplate, Modern, Italic, Gothic and flourishing.
- Local practice-check count.

## Current limitations

This is an early prototype, not a finished calligraphy tutor. Feedback is heuristic (stroke bounds/continuity/pressure), not full handwriting recognition or a professional grade. The first build should be tested on the target S Pen device before expanding it.

## Build requirements

- JDK 17
- Gradle 8.9
- Android SDK Platform 35 and Build Tools 35.0.0
- Android Gradle Plugin 8.7.3
