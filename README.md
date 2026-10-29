# Signal Social

A lightweight live event / party social matching web app with a QR-code TV host screen and mobile guest interface.

## Features

- Live TV room dashboard, join QR code, anonymous aggregate counts and light status
- Mobile nickname and short personal code setup
- Identity and reciprocal looking-for preference filters
- Optional photo uploads, swipe/pass, and code-based interest
- Mutual matches unlock direct WebRTC peer chat
- Red, yellow and green availability lights; no photos or names on the TV
- No sample participants or simulated matchmaking data

## Launch at an event

1. Publish this repository through **Settings → Pages → Build and deployment → Deploy from a branch**, using `main` and `/ (root)`.
2. Open the Pages URL on the TV / host computer and select **Host an event**.
3. Keep the TV's browser page open. Guests scan its QR code and join on their own devices.
4. Ensure devices have internet access; WebRTC signaling needs a connection to the PeerJS Cloud service.

## Hosting notes

The app is static and runs entirely in `index.html`. It loads PeerJS and a QR code library from a CDN. Browser-to-browser connections are peer-to-peer where available, but the app currently depends on a live host tab for coordination and an external PeerJS signaling service. Some networks may need TURN infrastructure for reliable connectivity. Use a dedicated backend for larger events or production privacy/security guarantees.

## Privacy and event safety

Participants control their own nickname, code, photos, lights and interest actions. Matches require mutual interest, and unmatching closes access to the in-app chat. This is an experimental prototype; do not assume it offers verified identities, age verification, moderation, or guaranteed message persistence. Only use at consenting, age-appropriate events.
