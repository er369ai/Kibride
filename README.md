# KibRide

A ride-hailing platform built for North Cyprus, live on the App Store and Google Play.

**This repository documents the project. The source belongs to Ringos Technology and is not published here.**

### What it is

KibRide is a taxi booking service covering North Cyprus, with separate passenger and driver applications and a marketing site on a custom domain.

- **Google Play** — [com.kibride.passenger.android](https://play.google.com/store/apps/details?id=com.kibride.passenger.android)
- **App Store** — published
- **Site** — [kktc.kibride.com](https://kktc.kibride.com)

### My role

Mobile developer. I built and shipped the applications, and I am the listed developer contact on the Google Play store listing.

### How it's built

| Area | Technology |
|---|---|
| Shared logic | Kotlin Multiplatform, targeting Android and iOS from one codebase |
| Authentication | Firebase Authentication |
| Data | Cloud Firestore |
| Ride state | Firestore real-time listeners for live trip updates |
| Apps | Separate passenger and driver clients |

### Notes

Kotlin Multiplatform meant the ride model, state machine and API layer were written once and shared across both platforms, with native UI on each. The real-time ride state — matching, acceptance, live position and trip completion — was the most demanding part of the build, since it has to stay consistent across two devices and survive a dropped connection.
