# FD Interest Tracker & Reminder Generator

A privacy-focused, zero-backend web application built to solve the real-world problem of financial interest tracking and leakage prevention. This utility calculates precise future maturity and payout dates, mapping them out visually and exporting them directly into a unified `.ics` calendar file.

> *Designed specifically to run 100% client-side in the browser's local RAM memory space, keeping sensitive personal financial details completely secure.*

Live Demo: [GitHub Pages Link](https://naina-bhatnagar.github.io/fin-tracker/)

---

## Features & Architecture Highlights

* **Privacy-First (Zero-Server Architecture):** No financial parameters, balances, or dates ever leave the user's local machine. The calculator runs entirely within the client-side browser runtime environment.

* **Volatile In-Memory Storage Matrix:** Utilizing volatile structured JavaScript object arrays that mirror standard relational database layouts 

> `fixed_deposits` parent table and a `calculated_payouts` child table linked via unique timestamp primary keys. 

* **Auto-Destruct Teardown:** For security validation, the moment a user refreshes or compiles and downloads their calendar data streams, a system teardown routine drops and flushes all active records out of memory.

* **Precise Daily Interest Math Engine:** Accurately steps through monthly/quarterly calendar boundary jumps while preserving target day positions.

* **Universal .ics Export Engine:** Dynamically aggregates tabular schema parameters, structures them into unified standard iCalendar raw multi-event string files (`VEVENT`), and pushes them into the browser's download queue via direct memory binary blobs.

---

## File System Layout

```text
├── index.html          # Core single-file application containing UI layouts, structural components, and script controllers
└── README.md           # Project system architectural documentation

```

---

## Local Installation & Usage Guide

Since this utility operates with no external node backend environments or active database integrations, testing it locally takes less than a minute.

1. **Clone the repository directory tree:**
```bash
git clone https://github.com/YOUR_USERNAME/fin-tracker.git
cd fd-interest-tracker
```

2. **Launch the interface:**
Simply double-click or open the `index.html` file using any web browser.

3. **Generating Calendar Notifications:**
* Enter your Fixed Deposit criteria (Principal, Rate p.a., Starting Date, Duration, Payout Frequency).

* Click **Add Fixed Deposit**. You can add multiple accounts all at once to see them compile together chronologically in the summary panel.

* Click **Download Unified .ics File**.

* Transfer the downloaded `.ics` file to any personal phone (Android/iOS) or laptop and tap to add all the 9:00 AM interest validation alerts into your preferred calendar app *(Google Calendar, Outlook, or Apple Calendar)*.

---

## Technology Stack

* **Frontend Layout Engine:** Semantic HTML5 Structure
* **Style Sheet Processor:** Tailwind CSS (via CDN compilation)
* **Application Script Engine:** Vanilla JavaScript (ES6+ Standards)
* **Deployment Target:** GitHub Pages (Static Hosting)
