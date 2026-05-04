# Glance iOS (Capacitor wrapper)

This wraps https://glance-at-me-app.lovable.app as a native iOS app.

## Build the Xcode project

Requires macOS with Node 18+, CocoaPods, and Xcode 15+.

```bash
npm install
npx cap add ios
npx cap sync ios
npx cap open ios
```

That generates `ios/App/App.xcworkspace`. Open it in Xcode, set your signing
team, and Archive → Distribute App for App Store submission.

## Configuration

- App name: **Glance**
- Bundle ID: **com.glance.app**
- Loads: **https://glance-at-me-app.lovable.app**
- Full-screen WebView (no browser chrome)
- Splash screen and app icon support pre-wired in `Assets.xcassets`

## Replacing the icon / splash

Drop your 1024×1024 icon into `ios/App/App/Assets.xcassets/AppIcon.appiconset/`
and your splash image into `Splash.imageset/`. Then run `npx cap sync ios`.
