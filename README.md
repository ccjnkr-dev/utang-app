# Utang for Android

A native Java Android app. Records and the light/dark preference stay on the phone in Android private app storage. Android automatic backup is disabled; manual JSON export/import is available in Settings. Exported JSON is unencrypted. The app requires no internet permission or account.

## Build and install

Open the project in Android Studio with Android SDK 36, Build Tools 36 and JDK 17 or newer. The wrapper uses Gradle 9.4.1 with Android Gradle plugin 9.2.0. Run `./gradlew :app:assembleDebug` (or `gradlew.bat :app:assembleDebug` on Windows). The resulting debug APK is `app/build/outputs/apk/debug/app-debug.apk`.

For an installable review build, see [`downloads/Utang-review.apk`](downloads/Utang-review.apk). This APK is signed with a development key and is not a Play Store release. Version 1.5 uses the same development key as previous review builds, so it can update those installations; a freshly built Android Studio debug APK may use another key and require uninstalling the review build first. Back up your records in Settings before uninstalling or clearing app data.

## Features

Swipe an unpaid record left for a partial payment or right for a full payment. On-screen buttons provide the same choices. All payments require confirmation and record the selected paid date. Paid and unpaid totals are separate for "Owed to me" and "I owe".

The sidebar contains About, with the app description, developer contact, AI credit, and privacy/terms information. CCJNKR Development is the stated developer; contact developmentccjnkr@gmail.com. The app has no advertising, tracking, analytics, third-party libraries, or network permission. The launcher icon is original artwork generated for Utang.

Version 1.5 keeps the current page when the device rotates, stacks totals on narrow screens, adjusts card layouts for small phones, and gives every payment, edit, and delete action a full-width touch target. The menu slides in and out, section changes fade and move gently, and the app follows the Android animation setting. The same icon appears in the header, menu, empty states, and About screen.

The main page has Owed to me and I owe tabs, headed Utang nila and Utang ko respectively. Both unpaid and paid records appear in each direction, with dates shown on settled records. The sidebar has Utang, Logs, Settings, and About; About includes an external Facebook contact button provided by the owner. The native design uses navy, teal, and mint with a more distinctive system type hierarchy in both themes.

Imported backups are validated before they replace your records; invalid dates, duplicate record IDs, or payment totals exceeding their record amount are rejected. The app does not send saved debts to the developer.
