# FD Interest Tracker & Reminder Generator

A privacy-focused, zero-backend web application built to solve the real-world problem of financial interest tracking and leakage prevention. This utility calculates precise future maturity and payout milestone dates down to the exact day count, mapping them out visually and exporting them directly into a unified `.ics` calendar file.

Designed specifically to run 100% client-side in the browser's local RAM memory space, keeping sensitive personal financial details completely secure.

Live Demo: [Insert Your GitHub Pages Link Here]

---

## ✨ Features & Architecture Highlights

* **Privacy-First (Zero-Server Architecture):** No financial parameters, balances, or dates ever leave the user's local machine. The calculator runs entirely within the client-side browser runtime environment.
* **Volatile In-Memory Storage Matrix:** Utilizing volatile structured JavaScript object arrays that mirror standard relational database layouts (`fixed_deposits` parent table and a `calculated_payouts` child table linked via unique timestamp primary keys). 
* **Auto-Destruct Teardown:** For security validation, the absolute second a user compiles and downloads their calendar data streams, a system teardown routine drops and flushes all active records out of memory.
* **Precise Daily Interest Math Engine:** Accurately steps through monthly/quarterly calendar boundary jumps while preserving target day positions and calculates partial-period payouts based on the changing counts of days inside individual blocks (30 vs 31 day month variances).
* **Universal .ics Export Engine:** Dynamically aggregates tabular schema parameters, structures them into unified standard iCalendar raw multi-event string files (`VEVENT`), and pushes them into the browser's download queue via direct memory binary blobs.

---

## 🛠️ Technology Stack

* **Frontend Layout Engine:** Semantic HTML5 Structure
* **Style Sheet Processor:** Tailwind CSS (via CDN compilation)
* **Application Script Engine:** Vanilla JavaScript (ES6+ Standards)
* **Deployment Target:** GitHub Pages (Static Hosting)

---

## 📂 File System Layout

```text
├── index.html          # Core single-file application containing UI layouts, structural components, and script controllers
└── README.md           # Project system architectural documentation