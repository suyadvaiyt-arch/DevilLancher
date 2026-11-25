# DevLauncher

A native Android launcher starter project using Kotlin + Jetpack Compose. White Liquid Glass-inspired visual direction.

## Included in v1.0.0 starter
- Android HOME launcher entry point (select DevLauncher as the default Home app)
- Installed app discovery and launch
- App drawer with live search
- Quick-launch home grid
- White / pastel glass-inspired UI
- Settings toggles for glass surfaces and icon labels
- GitHub Actions workflow to build and upload a debug APK

## Build with GitHub Actions
1. Create a GitHub repository named `DevLauncher`.
2. Upload the contents of this folder to the repository root.
3. Open **Actions** and enable workflows if GitHub asks.
4. Run **Build DevLauncher APK** (or push to `main`).
5. Open the completed workflow run and download the `DevLauncher-debug` artifact.
6. Extract the APK and install it on your Android phone.
7. Press Home and choose **DevLauncher** as the Home app.

## Build locally
Requires JDK 17 and Android SDK 35:
```bash
gradle assembleDebug
```

## Important notes
- This is a working starter/MVP, not a finished clone of another launcher.
- Android widgets, lock-screen replacement, system Control Center replacement, 3D depth wallpaper, app locking, and AI assistant are not implemented in this first build. They require separate native Android components, platform permissions, and/or backend services.
- `QUERY_ALL_PACKAGES` is used because a launcher needs to enumerate launchable apps. Google Play distribution has policy restrictions for broad package visibility; review the current Play policy before publishing there.
- Debug APKs are not release-signed. Configure a private signing key in GitHub Actions before publishing a release.
