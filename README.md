# Manoj Tiwari — Mobile App (PWA)

This folder is a complete installable mobile app (Progressive Web App) built from your brochure.

## What's inside
- `index.html` — the app itself (Home, Services, Enquire, Documents, Contact)
- `manifest.json` — tells phones how to install it (name, icon, colors)
- `sw.js` — service worker, makes the app open instantly and work offline
- `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png` — app icons

## Features
- **Home** — quick intro, call/WhatsApp buttons, key stats
- **Services** — all 9 services from your brochure
- **Enquire** — a form that opens WhatsApp or email pre-filled with the client's details, so you get organised enquiries instead of vague messages
- **Documents** — clients pick a file (invoice, GST notice, statement) and tap "Share document" to send it straight to WhatsApp, email, or Drive via their phone's native share sheet
- **Contact** — phone, email, office, WhatsApp

## How to make it installable on phones (required step)

A PWA can only be installed from a real website address — not from a file on your computer. You need to put these files online first. Any of these work and are free:

### Option A — Netlify (easiest, no account needed for a quick test)
1. Go to https://app.netlify.com/drop
2. Drag this whole folder onto the page
3. Netlify gives you a live link (e.g. `https://manoj-tiwari-app.netlify.app`)
4. Open that link on a phone → tap browser menu → **"Add to Home Screen"** / **"Install app"**

### Option B — GitHub Pages (best if you want a permanent free address)
1. Create a GitHub repository and upload these files
2. In the repo settings, enable **GitHub Pages** for the main branch
3. GitHub gives you a link like `https://yourname.github.io/repo-name/`

### Option C — Your own domain
Upload the files to any web host (the same place your current brochure website lives works fine). Once it's served over **https://**, visitors on mobile will automatically get an "Install app" / "Add to Home Screen" prompt.

## Editing content later
All the text, phone numbers, and services live directly in `index.html` — open it in any text editor and search for the text you want to change (e.g. search for "98303 83777" to update the phone number everywhere).

## About the Documents tab
Since this is a web app (not a native app with server storage), the "Share document" button uses the phone's built-in **share sheet** — the client picks the file, taps Share, and chooses WhatsApp/Email/Drive themselves. Nothing is uploaded to a server or stored anywhere; it goes directly from their phone to whichever app they choose. This works on most modern Android and iOS browsers (Chrome, Safari 15+). On older browsers, the tab falls back to direct WhatsApp/email links with instructions.
