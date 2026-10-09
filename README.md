# Medico AI 💊

**Medicine reminders in your language.**  
Medico is a lightweight, browser-based medicine reminder prototype designed to help people track scheduled medicines using English and Hindi voice reminders.

> **Important:** Medico is a reminder tool, not a medical device. It does not diagnose conditions, prescribe medicines, or recommend or change doses. Enter medicine instructions exactly as written on your prescription. Ask a doctor or pharmacist if anything is unclear.

## ✨ Features

- **Hindi and English interface** — switch between English and हिन्दी.
- **Voice reminders** — hear medicine reminders in English, Hindi, or both using your browser's speech synthesis.
- **Medicine schedule** — add a medicine name, time, and prescription instructions; review or delete saved medicines.
- **Dose status** — mark a reminder as taken, snooze it, or view pending and missed statuses.
- **Follow-up reminders** — configure a follow-up interval and a later reminder interval.
- **Caregiver support** — optionally save caregiver details and give or revoke consent for preparing a follow-up message.
- **Manual caregiver messaging** — opens the device's messaging app with a prepared SMS; you remain in control and must send it yourself.
- **Find nearby care** — shortcuts to Google Maps and OpenStreetMap searches for hospitals, clinics, pharmacies, diagnostic labs, and ambulance services.
- **Activity history** — review reminder-related events.
- **Data export and deletion** — export app data as JSON or delete data stored by this app in the current browser.
- **Emergency shortcut** — provides a direct phone link to call India's emergency number, 112.
- **Responsive layout and theme support** — adapts to smaller screens and supports light/dark appearance preferences.

## 🧰 Tech

This prototype is implemented as a single HTML file:

- HTML5
- CSS (responsive layout, CSS custom properties, light/dark theme support)
- Vanilla JavaScript
- Browser `localStorage` for persistence
- Web Speech API (`speechSynthesis`) for spoken reminders
- `sms:` links for user-initiated caregiver messages
- Google Maps and OpenStreetMap search links

It currently has **no server, database, account system, cloud synchronization, or AI/LLM integration**. “Medico AI” is the project name; the uploaded prototype's features are implemented in the browser.

## 🚀 Run locally

No package installation or build step is required.

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. Add medicines using the instructions and time on the prescription.
4. Open **Voice & settings** to choose the reminder language and test available voices.

For the best experience, use a current version of Chrome, Edge, Safari, or Firefox. Voice availability and behavior vary by browser and operating system. Your device may need a Hindi text-to-speech voice installed.

### Reminder behavior

- Voice reminders run only while the page is open in the browser.
- The page checks reminder schedules periodically; it is not a guaranteed background alarm.
- Browser notifications may depend on permission and browser support.
- Closing the page or browser can prevent reminders from running on time.
- Reminder data is stored in the browser's local storage. It does not automatically sync to another device.

## 🌐 Publish with GitHub Pages

1. Create a GitHub repository, for example `medico-ai`.
2. Add the HTML file to the repository and rename it to `index.html`.
3. Add this `README.md`.
4. Open **Settings → Pages** in the repository.
5. Under the build/deployment settings, select **Deploy from a branch**, choose your main branch and the root (`/`) folder, then save.
6. Wait for GitHub Pages to publish the site and open the URL shown in the Pages settings.

The app can be hosted as a static site because the current prototype does not require a backend. Features that depend on browser APIs may behave differently on mobile devices or in embedded browsers.

## 🔐 Privacy and consent

- Medicine, settings, caregiver details, and activity history are saved in `localStorage` in the browser used by the app.
- Anyone with access to the same browser profile may be able to access that stored data.
- Exported JSON files may contain sensitive health information. Store and share them carefully.
- The caregiver feature is consent-based. Revoking consent disables the app's caregiver escalation flow.
- The app prepares an SMS link; it does **not** automatically send messages or confirm delivery.
- Clearing browser data may remove saved app information.

## 🩺 Safety

- Enter medicine names, times, and instructions exactly as shown on a clinician-provided prescription.
- Medico does not verify prescriptions, calculate doses, identify pills, or advise whether a medicine is appropriate.
- If a prescription is unclear or a dose is missed, contact a doctor or pharmacist for guidance rather than relying on the app.
- Nearby-care links are search shortcuts. Medico does not verify providers, opening hours, or availability.
- In a genuine emergency in India, call **112** directly. Do not wait for this app.

## 🛣️ Possible future improvements

- Progressive Web App (PWA) support and more reliable notifications
- Accessible onboarding and larger text options
- Automated tests for scheduling, data export, and consent flows
- Optional secure backend and cross-device sync, with authentication and strict access controls
- Integrations for verified healthcare directories and consent-based caregiver notifications

These are future ideas, not features currently provided by this single-file prototype.

## 🤝 Contributing

Issues and pull requests are welcome. When proposing changes, prioritize accessibility, privacy, and safe handling of health information. Do not add features that invent or alter medical dosage instructions.

## 📄 License

No license has been specified yet. Add a `LICENSE` file before presenting this project as open source under a particular license.
