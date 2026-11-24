# ClearView: Video Browser for Android

**An Android browser built for watching video on the web. "Pin Page" helps keep unexpected pop-ups and redirects from taking you away from the player.**

[Google Play](https://play.google.com/store/apps/details?id=org.clearview.prototype) · [Product website](https://clearviewbrowser.com/)

| Project | Details |
| --- | --- |
| **Status** | Live on Google Play |
| **My role** | Independent developer of the Android app and billing backend, including testing and release |
| **Stack** | Kotlin, Android WebView, Google Play Billing, Node.js, Google Cloud Run |

| Browser and page controls | On-device history |
| --- | --- |
| <img src="screenshots/browser.jpg" width="275" alt="ClearView showing its address bar, Pin Page button and a website"> | <img src="screenshots/history.jpg" width="275" alt="ClearView History dialog with two visited pages and a Clear History button"> |

## What I built

- **Android client in Kotlin with WebView.** A custom navigation policy decides how new windows and redirects are handled, which is what makes page pinning work.
- **On-device history.** Browsing history stays on the device and can be cleared from the History dialog.
- **Paid subscription (Plus).** Adds a filter for known advertising addresses, sold through Google Play Billing.
- **Server-side purchase verification.** A Node.js service on Google Cloud Run verifies Google Play purchases before granting subscription access.

## How I tested it

I verified both subscription flows on a Pixel Fold using Google Play's billing test tools.

- After renewal, subscription access survived an app restart.
- After a refund with revocation, the app removed access to the paid filter.

## Skills demonstrated

Kotlin · Android WebView · in-app subscriptions · REST backend on Google Cloud Run · Node.js · end-to-end billing tests · Google Play release

> This repository is a public showcase. The production source code is private.
