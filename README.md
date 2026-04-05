# SecureCheck 🛡️

**Author:** Rosie Domenech  
**Date:** April 2026  
**Description:** Personal Security Posture Dashboard — a Progressive Web App (PWA) that answers "Am I secure right now?" in one screen.

**Live App:** https://rosiedomenech.github.io/securecheck

---

## Features

- 🛡️ **Security Score** — 0-100 score based on device health + breach exposure
- 💻 **Device Tracker** — Track all your devices, flag inactive or outdated OS
- 🔍 **Breach Monitor** — Check emails against HaveIBeenPwned database
- 🚨 **Active Alerts** — Real-time flags for inactive devices and new breaches
- 📱 **iPhone PWA** — Add to home screen, works like a native app
- 💾 **Local Storage** — All data stays on your device, never uploaded

---

## Install on iPhone

1. Open **Safari** and go to the live app URL
2. Tap the **Share** button
3. Tap **Add to Home Screen**
4. Tap **Add**

It now appears on your home screen like a native app!

---

## Setup HaveIBeenPwned API

To enable live breach checking:

1. Get a free API key at [haveibeenpwned.com/API/Key](https://haveibeenpwned.com/API/Key)
2. Open `index.html` and replace `YOUR_HIBP_KEY` with your key

---

## Roadmap

- [ ] VPN status detection
- [ ] WiFi risk scoring
- [ ] Push notifications (Service Worker)
- [ ] Splunk integration for enterprise
- [ ] React Native iOS app
- [ ] B2B version for small clinics & offices
- [ ] Subscription tier ($4.99/month)

---

## Tech Stack

- Vanilla HTML/CSS/JS — zero dependencies
- Progressive Web App (PWA)
- Local Storage for persistence
- HaveIBeenPwned API v3
- GitHub Pages for hosting
