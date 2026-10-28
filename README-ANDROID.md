# Ledger Android wrapper project

This Android Studio project packages the existing Ledger HTML/CSS/JavaScript app and its `assets/icons/3d/` PNG files inside an Android WebView. It does not migrate the app to a different framework.

## Build an installable APK
1. Open Android Studio on a computer.
2. Choose **Open** and select this extracted project folder (the one containing `settings.gradle`).
3. Allow Gradle sync and install Android SDK Platform 35 if prompted.
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. The debug APK will be under `app/build/outputs/apk/debug/app-debug.apk`.

The APK has not been compiled or runtime-tested in this environment because Android SDK/Gradle build tools are not installed here. The app stores data using the existing web app's browser storage; WebView storage persistence should be tested on the target device. Google Fonts require an internet connection; the app's bundled assets load locally.

## Build from a phone using GitHub Actions (no Android Studio needed on the phone)
1. Create a GitHub repository and upload the contents of this folder to it.
2. Open the repository's **Actions** tab and select **Build Ledger APK**.
3. Tap **Run workflow** (or wait for the first push build to finish).
4. Open the completed workflow run, find **Artifacts**, and download `ledger-debug-apk`.
5. Extract the artifact ZIP to get `app-debug.apk`, then install it on your Android phone. Android may ask you to allow installs from your browser/files app.

This produces a debug APK for personal testing, not a Play Store release-signed APK.
