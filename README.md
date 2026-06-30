# FD Interest Tracker & Reminder Generator

A privacy-focused, client-side web application built to solve the real-world problem of financial interest tracking and leakage prevention. This utility calculates precise future maturity and payout dates, maps them out visually, and exports them directly into a unified `.ics` calendar file.

> *Designed strictly to run 100% locally in your browser's memory. Your sensitive personal financial details never leave your device.*

**Live Demo:** [Check it out on GitHub Pages](https://naina-bhatnagar.github.io/fin-tracker/)

---

## **Project Walkthrough**

https://github.com/user-attachments/assets/f85db8e6-3a55-421d-a5df-8ed007237de6

---

##  Features & Architecture

* **Privacy-First (Zero-Server Architecture):** No financial parameters, balances, or dates are ever sent to a server. The calculator runs entirely within your browser.
* **In-Memory Storage:** Uses temporary JavaScript arrays that act like a standard database—linking a `fixed_deposits` parent table and a `calculated_payouts` child table to keep your data organized while the tab is open.
* **Automatic Data Wipe:** For maximum security, the moment you refresh the page, close the tab, or download your calendar file, a system routine automatically flushes all active records out of memory.
* **Precise Daily Interest Math:** Accurately calculates interest by stepping through monthly and quarterly calendar dates, ensuring exact target payouts.
* **Universal Calendar Export:** Dynamically takes your tracked data and structures it into a standard iCalendar (`.ics`) file. It pushes the file directly to your browser's download queue without needing a backend.

---

## Local Installation & Usage Guide

Since this utility operates with no external backend or database, testing it locally takes less than a minute.

**1. Clone the repository:**

```bash
git clone https://github.com/naina-bhatnagar/fin-tracker.git
cd fin-tracker

```

**2. Launch the interface:**
Simply double-click or open the `index.html` file using any web browser.

**3. Generating Calendar Notifications:**

* Enter your Fixed Deposit details (Principal, Rate p.a., Starting Date, Duration, and Payout Frequency).
* Click **Add Fixed Deposit**. You can add multiple accounts to see them compile chronologically in the summary panel.
* Click **Download Unified .ics File**.
* Transfer the downloaded `.ics` file to your phone (Android/iOS) or laptop. Open it to add all your 9:00 AM interest validation alerts into your preferred app *(Google Calendar, Outlook, or Apple Calendar)*.

---

## Technology Stack

* **Frontend:** Semantic HTML5
* **Styling:** Tailwind CSS (via CDN)
* **Logic & Engine:** Vanilla JavaScript (ES6+)
* **Deployment:** GitHub Pages (Static Hosting)
