# SkyMeter Android (WebView) — Build .aab for Play Store

## Requirements
- Android Studio Hedgehog (2023.1+) or newer
- JDK 17
- Internet (first Gradle sync downloads dependencies)

## Open project
1. Open **Android Studio**
2. **File → Open** → select this folder: `SkyMeterAndroid`
3. Wait for Gradle sync to finish

## Run on device / emulator
- Click **Run** (green play) or `Shift+F10`

## Generate Play Store .aab (App Bundle)
1. **Build → Generate Signed Bundle / APK…**
2. Choose **Android App Bundle**
3. Create a new keystore (or use existing):
   - Key store path: choose a safe place
   - Password: set a strong password (SAVE IT)
   - Alias: `skymeter`
   - Validity: 25+ years
4. Select **release** build
5. Finish → `.aab` file will be at:
   `app/release/app-release.aab`

## Upload to Play Console
1. https://play.google.com/console
2. Create app → **SkyMeter**
3. Production / Testing → **Create new release** → upload `app-release.aab`
4. Store listing: use `icon-512.png` from project root artifacts
5. Complete Data safety, content rating, target audience forms

## Package details
- Application ID: `com.skymeter.app`
- Version: 1.0.0 (versionCode 1)
- Min SDK: 24 (Android 7.0)
- Target SDK: 34

## Notes
- App loads local HTML from assets (works offline for UI shell)
- Internet permission used for weather radar, maps, images
- Location permission for local weather (user can deny)
- Change `applicationId` in `app/build.gradle` if the ID is taken on Play Store

## Copyright
© 2026 SkyMeter. Original UI/code proprietary. See in-app Terms.

---

## No PC? Build via GitHub Actions
See **GITHUB_BUILD.md** — phone se repo banao, Actions se `.aab` download karo.
