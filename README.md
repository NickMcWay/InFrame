# Cofy

Cofy is a small SwiftUI demo app that captures a **context selfie**: it shoots the scene with the back camera, snaps a selfie with the front camera, and automatically composites the two into a single photo saved to your library.

## Features
- **Camera** – Switches between rear and front cameras to capture the scene and your selfie, then saves the composite (and optionally the originals) to the photo library.
- **Gallery** – Shows previously captured context selfies in a grid. Tap any item for a full-screen preview or explicitly request photo-library access.
- **Settings** – Toggle whether the original scene and selfie photos should also be kept.
- **Advertisement** – Displays a Google AdMob banner at the bottom of the gallery and periodically shows a full-screen interstitial ad with an option to remove ads.

## Getting Started
### Requirements
- iOS 16 or later
- Xcode 15 or later
- Swift 6.1

### Building
1. Clone the repository.
2. Open `Cofy.xcodeproj` in Xcode.
3. Add the [Google Mobile Ads SDK](https://developers.google.com/admob/ios/quick-start) via Swift Package Manager.
4. Replace the placeholder `GADApplicationIdentifier`, `GADBannerUnitID`, and `GADInterstitialUnitID` values in `Cofy/Info.plist` with your own IDs.
5. Build and run on a device or simulator with camera and photo-library permissions.

## Usage
1. Launch the app and allow camera access.
2. In the **Camera** tab, press the shutter button to take a context selfie.
3. Grant photo-library access if prompted.
4. Browse your composites in the **Gallery** tab.
5. Adjust preferences in **Settings**.

## Project Structure
- `CaptureView.swift` – Camera interface and capture logic.
- `GalleryView.swift` – Displays saved context selfies.
- `SettingsView.swift` & `Settings.swift` – User preferences for saving originals.
- `PairStore.swift` – Persists identifiers for captured pairs.
- `ContextSelfieComposer.swift` – Builds the composite image.
- `PhotoSaver+IDs.swift` – Saves images and returns asset identifiers.
- `AdBannerView.swift` – Bridges a `GADBannerView` into SwiftUI.
- `InterstitialAdManager.swift` – Handles loading and presentation of full-screen interstitial ads and upgrade prompt.

## App Store Considerations
- Provide app icons, launch screens, and screenshots.
- Supply a privacy policy and ensure all required `Info.plist` usage descriptions are filled in.
- Configure in-app purchases in App Store Connect for the ad-free upgrade.
- Verify compliance with [App Store Review Guidelines](https://developer.apple.com/app-store/review/guidelines/).

### Privacy & Legal Templates
- [Privacy Policy](PRIVACY_POLICY.md)
- [Terms of Use](TERMS_OF_USE.md)
- [Recommended In-App Disclosures](IN_APP_DISCLOSURES.md)

---
This project is provided for educational purposes. Add a license if you plan to distribute it.
