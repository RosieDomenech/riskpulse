# RiskPulse 🛡️

**Author:** Rosie Domenech  
**Date:** April 2026

> *"Am I secure right now?"* — answered in one screen.

**🌐 Live App:** [rosiedomenech.github.io/riskpulse](https://rosiedomenech.github.io/riskpulse)

---

## What Is RiskPulse?

RiskPulse is a **Personal Security Posture Dashboard** -a free Progressive Web App (PWA) that gives individuals and small organizations a simple, at-a-glance view of their security health.

Most cybersecurity tools are built for enterprises. They're complex, expensive, and overwhelming. RiskPulse is different: it's designed for **real people** who just want to know if they're exposed — without needing a security team to interpret the results.

---

## How Is This Different From Antivirus?

This is the most common question — and the most important one to understand.

| | Antivirus | RiskPulse |
|---|---|---|
| **Scope** | One device | All your devices + accounts |
| **What it monitors** | Files & malware | Posture, identity & exposure |
| **Question it answers** | "Is this file safe?" | "Am I safe — right now?" |
| **Approach** | Reactive | Proactive |
| **Examples** | Norton, McAfee, Malwarebytes | ← This app |

**The simplest analogy:**
- 🔒 **Antivirus** = a lock on your front door
- 📷 **RiskPulse** = a security camera system showing every door, window, and who's been in your driveway

They are **complementary, not competing.** Most people already have antivirus. Almost nobody has a personal security posture dashboard. That's the gap RiskPulse fills.

> Antivirus asks: *"Is this file dangerous?"*
> RiskPulse asks: *"Is my entire digital life exposed?"*

---

## How It Works

RiskPulse uses **3 lightweight detection methods** — no agents, no network scanners, no special permissions required:

### 1. 🔗 Auto Device Detection (via Check-In Link)
Share a unique check-in link with anyone. When they tap it on their device, the browser automatically reveals:
- **Device type** — iPhone, MacBook, Windows PC, Android, etc.
- **OS version** — iOS 17.4, Windows 11, macOS 14.3, etc.
- **Browser version**
- **Exact check-in timestamp**

No app install needed. No permissions required. Every browser sends this information freely.

### 2. 🔍 Breach Monitoring (HaveIBeenPwned API)
Enter any email address and RiskPulse checks it against a database of **13+ billion breached accounts** spanning hundreds of real-world data breaches including Adobe, LinkedIn, Equifax, and more.

### 3. 📊 Security Score (0–100)
A real-time score calculated from your actual posture:

| Metric | Score Impact |
|---|---|
| Device inactive (not seen in X days) | −15 per device |
| Outdated OS flagged | −10 per device |
| Known email breach found | −8 per breach |
| No devices tracked yet | −10 |

| Score Range | Status |
|---|---|
| 🟢 80–100 | Looking good |
| 🟡 60–79 | Needs attention |
| 🔴 0–59 | At risk |

---

## Features

- 🛡️ **Security Score** — Live 0–100 score with color-coded risk level
- 💻 **Device Tracker** — Track all your devices, last seen timestamps, OS versions
- 🔗 **Share Check-In Link** — Send a link; recipient's device auto-registers with OS info
- 🔍 **Breach Monitor** — Check emails against HaveIBeenPwned in real time
- 🚨 **Active Alerts** — Flags inactive devices and known breach exposures
- ⚙️ **Custom Thresholds** — Set your own inactivity window and score alert level
- 💾 **100% Local Storage** — All data stays on your device. Nothing is uploaded or shared.
- 📱 **iPhone PWA** — Installs to your home screen, runs like a native app

---

## Install on iPhone (PWA)

1. Open **Safari** and go to [rosiedomenech.github.io/riskpulse](https://rosiedomenech.github.io/riskpulse)
2. Tap the **Share** button (box with arrow)
3. Tap **Add to Home Screen**
4. Tap **Add**

RiskPulse now appears on your home screen with a shield icon and opens fullscreen — just like a native app, no App Store required.

---

## Device Check-In Flow

**For the dashboard owner:**
1. Open RiskPulse → **Devices** tab
2. Tap **🔗 Share Link**
3. Copy or share the link via iMessage, WhatsApp, Email, etc.

**For the person receiving the link:**
1. Tap the link on their device
2. Their device type, OS version, and browser are auto-detected
3. Optionally rename the device (e.g. "Mom's iPhone")
4. Tap **Register** — instantly appears in your dashboard

---

## Enable Live Breach Checking

By default, breach checking runs in demo mode. To enable live data:

1. Get a free API key at [haveibeenpwned.com/API/Key](https://haveibeenpwned.com/API/Key)
2. Open `index.html` and replace `YOUR_HIBP_KEY` with your key

---

## Who Is This For?

- 👤 **Individuals** who want to know if their accounts have been breached
- 👨‍👩‍👧 **Families** who want to track devices for parents, kids, or grandparents
- 🏥 **Small clinics & offices** that need basic device visibility without enterprise MDM
- 🎓 **Higher-ed IT teams** monitoring departmental devices informally
- 🔐 **Security-conscious professionals** who want a personal posture dashboard

---

## Roadmap

- [ ] Push notifications via Service Worker
- [ ] VPN status detection
- [ ] WiFi network risk scoring
- [ ] Splunk integration for security professionals
- [ ] React Native iOS App Store version
- [ ] B2B version for small clinics and offices
- [ ] Subscription tier — $4.99/month (unlimited devices + alerts)

---

## Tech Stack

- **Frontend:** Vanilla HTML/CSS/JS — zero dependencies, zero frameworks
- **Hosting:** GitHub Pages (free)
- **Storage:** Browser LocalStorage — client-side only
- **Breach API:** HaveIBeenPwned v3
- **Detection:** Browser User Agent parsing
- **PWA:** Web App Manifest + Apple meta tags

---

## Privacy

RiskPulse stores all data **locally in your browser**. No data is ever sent to a server, logged, or shared. The only external call made is to the HaveIBeenPwned API when you explicitly check an email address.

---

*Built by Rosie Domenech — cybersecurity professional with 30 years of experience in IT security, vulnerability management, and endpoint protection.*
