# 💍 Our Wedding — Budget Tracker

> A self-contained single-page wedding budget app with Firebase sync, interactive charts, and a mobile-first dark UI.

![Stack](https://img.shields.io/badge/Firebase-Firestore%20%2B%20Auth-orange) ![UI](https://img.shields.io/badge/UI-Tailwind%20CSS-blue) ![Charts](https://img.shields.io/badge/Charts-Chart.js-purple) ![Deploy](https://img.shields.io/badge/Deploy-Single%20HTML%20file-green)

---

## Overview

A complete wedding finance tracker built in one `index.html` file. Vendors, budgets, and expenses are stored in Firebase Firestore with real-time sync across devices. All UI lives in a 420px mobile-first container that adapts gracefully to desktop.

---

## Four Main Views

| View | Description |
|------|-------------|
| 🏠 **Dashboard** | Doughnut chart of spend vs budget. Paid, owed, and per-source breakdowns. |
| 📊 **Statistics** | All logged expenses with sorting and a category-level spending chart. |
| ✅ **Planning** | Budget plan cards by category. Search, filter, and track vendor status. |
| 👥 **Vendors** | Vendor directory with contact info, budget, and Planning/Contacted/Finalized status. |

Navigation between views is handled by a fixed bottom bar. The central **+** button opens a quick-action sheet.

---

## Modals (Slide-up Sheets)

| Modal | Purpose |
|-------|---------|
| **Log Expense** | Category, amount, payment type (UPI / Cash / Card / Bank), date, notes, and source account. |
| **Budget / Vendor Plan** | Estimated vs locked budget, vendor name, contact person, phone, and status. |
| **Source Detail** | Spending trend chart + full transaction history for a payment source. |
| **Category Detail** | All vendors in a category with budgets and status indicators. |
| **Add Action Sheet** | Entry point from the central + button — choose "Log Expense" or "Add Budget/Vendor". |
| **Confirm Delete** | Deletion confirmation with Cancel/Delete to prevent accidental data loss. |

All modals follow a consistent pattern: dark overlay, slide-up sheet, sticky header with a close button, and independently scrollable content.

---

## Tech Stack

| Library | Role |
|---------|------|
| **Firebase Auth** | Email/password login |
| **Firebase Firestore** | Cloud data storage and real-time sync |
| **Chart.js** | Doughnut and line charts |
| **Tailwind CSS** | Utility styling with a custom neon color palette |
| **Plus Jakarta Sans** | Primary typeface (Google Fonts) |

---

## Key Design Decisions

- **Single file** — CSS, JS, and HTML in one `index.html`. No build step or separate server required.
- **Mobile-first** — 420px max-width container, fixed bottom navigation, slide-up modals.
- **Dark theme** — Custom neon accent palette: yellow (primary actions), pink, cyan, purple, orange, and green for status indicators.
- **Data adapter** — Normalizes inconsistent Firestore field names and fills missing defaults on every load.
- **Central state object** — All budget plans, expenses, and categories are tracked in a single JS state that updates charts and UI in real time when data changes.

---

## Color Palette

| Color | Usage |
|-------|-------|
| Neon Yellow | Primary actions, active nav tab |
| Pink | Secondary actions, central + button gradient |
| Cyan | Future / upcoming items |
| Purple | Planning stage status |
| Orange | Contacted status |
| Green | Finalized status |

---

## Authentication

Login is handled by Firebase Authentication using email and password. The login screen sits above all content at a high z-index and is dismissed on successful auth. A logout button is available in the top-right header.

---

## File Structure

```
index.html
├── <head>        — Tailwind config, Chart.js, Google Fonts
├── <style>       — Custom CSS (animations, modals, scrollbar, radio styles)
├── Login screen  — Full-screen overlay
├── Header        — Sticky, blur backdrop, greeting + logout
├── Tab views     — Dashboard · Statistics · Planning · Vendors
├── Bottom nav    — 4 tabs + central action button
├── Modals (×6)   — Expense · Plan · Source detail · Category · Action sheet · Confirm delete
└── <script>      — Firebase init, state management, chart rendering, CRUD operations
```
