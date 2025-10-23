# ToggleWidget (Android App Widget)

**2×1 home screen widget** that toggles between a button “Показать текст” and a centered “Hello World” text.
- Light gray background (#E0E0E0)
- Rounded white button with subtle stroke
- State persists per widget instance until tapped again

## Files
- `app/src/main/java/com/egorf/togglewidget/ToggleWidgetProvider.kt` — widget logic (RemoteViews + SharedPreferences per `appWidgetId`)
- `app/src/main/res/layout/widget_toggle.xml` — layout with Button + TextView (swap visibility)
- `app/src/main/res/xml/widget_info.xml` — declares 2×1 sizing, no auto updates
- `AndroidManifest.xml` — registers `AppWidgetProvider` + intent filters
- Gradle build with Kotlin (AGP 8.6, Kotlin 2.0, compile/target SDK 35)

## Build (any machine or CI with Android SDK)
```bash
# Java 17 required
# With Gradle wrapper (recommended) — add wrapper if not present:
gradle wrapper --gradle-version 8.7
./gradlew assembleDebug
# APK: app/build/outputs/apk/debug/app-debug.apk
```

> This zip does not contain the Gradle wrapper binaries. If you use CI, ensure Gradle is installed or add a wrapper first.
