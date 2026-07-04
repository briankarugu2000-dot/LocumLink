# LocumLink

LocumLink is a web application designed to optimize medical facility operations across Kenya. It connects understaffed clinics and hospitals with a network of verified, on-call locum doctors and nurses, replacing manual coordination with a digital ecosystem.

---

## Features

* **Grid Architecture:** Built with utility wrappers to scale across mobile, tablet, and desktop monitors.
* **Image Pipelines:** Uses responsive visual elements fetched directly from public imagery distribution nodes.
* **Visual Identity:** Features brand color accents and component animations such as card translation depth scales.
* **Shift Board:** A job board where facilities post open shifts and locum professionals browse, filter, and apply — backed by a real API and database.
* **Page Suites:** Includes routing for platform operations:
    * index.html: Landing page with integrated call-to-actions.
    * about.html: Enterprise overview containing vision tracks and leadership panels.
    * jobs.html: Shift board for posting shifts, applying, and tracking application status.
    * pricing.html: Tiered subscription models with functional matrices.
    * contact.html: Engagement interface with structured inquiries forms.

---

## Architecture and Tech Stack

The front-end is engineered using the following stack:

| Core Technology | Purpose | Utilization |
| :--- | :--- | :--- |
| HTML5 | Structural Layout | Semantic organization across all platform subpages. |
| Tailwind CSS | Interface Styling | Utility-first compilation providing layout constraints. |
| Vanilla JavaScript | Client Logic | Filtering, modals, and API communication on the shift board. |

The back-end (`server/`) is a small Express API on Node.js, using Node's built-in SQLite module for storage:

| Core Technology | Purpose | Utilization |
| :--- | :--- | :--- |
| Node.js + Express | API Server | Serves REST endpoints for jobs and applications. |
| SQLite (`node:sqlite`) | Database | Persists jobs and applications; no native build step required. |

---

## Project Directory Structure

```text
LocumLink/
├── index.html          # Landing Page
├── about.html          # About Us and Leadership Board
├── jobs.html           # Shift Board (post shifts, apply, track status)
├── pricing.html        # Subscription Plans
├── contact.html        # Contact and Support Intake Form
├── server/             # API + database backend
│   ├── server.js       # Express routes
│   ├── db.js           # SQLite schema and seed data
│   ├── package.json
│   └── README.md        # Backend setup and deployment guide
└── README.md           # Technical Documentation and Setup Guide
```

---

## Running the Shift Board Locally

```bash
cd server
npm install
npm start
```

This starts the API on `http://localhost:3000`. Then open `jobs.html` (via any static file server) — it's already configured to talk to that API. See `server/README.md` for endpoint details and deployment options.