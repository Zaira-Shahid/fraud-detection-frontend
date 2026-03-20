# Credit Card Fraud Detection Dashboard

A real-time fraud detection dashboard built with vanilla JavaScript, connected to a live ML-powered API. Visualizes transaction risk, verdict results, and live analytics — all in one place.

**Live Dashboard:** https://fraud-detection-frontend-xi.vercel.app  
**API Repository:** https://github.com/Zaira-Shahid/fraud-detection-api

---

## What It Does

Enter transaction details, hit Analyze, and the dashboard instantly returns a risk score, verdict, and updates the live analytics chart — powered by a real machine learning model running in production.

---

## Features

- Live transaction risk analysis (0–100% risk score)
- Real-time verdict — APPROVED, UNDER REVIEW, or BLOCKED
- Live doughnut chart updating with every transaction
- Transaction log with risk score history
- Stats counter — total analyzed, approved, blocked, under review
- Fully responsive design
- Connected to production FastAPI backend on Railway

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Language | HTML5, CSS3, JavaScript |
| Charts | Chart.js |
| Deployment | Vercel |
| Backend | FastAPI on Railway |

---

## How It Works
```
User fills transaction form
         ↓
POST request to /predict endpoint
         ↓
ML model returns risk score + verdict
         ↓
Dashboard updates — result, chart, log
```

---

## Transaction Fields

| Field | Description |
|-------|-------------|
| Amount (PKR) | Transaction amount |
| Distance from Home | How far from home city (km) |
| Hour of Day | Time of transaction (0–23) |
| Transactions Last Hour | Frequency in last 60 minutes |
| Avg Spend Multiplier | How much vs normal spending |
| New Merchant | First time at this merchant |
| Foreign Country | Transaction from abroad |
| Weekend | Weekend transaction flag |
| Card Age | How old the card is (days) |

---

## Verdict Logic

| Risk Score | Trusted User | Verdict |
|------------|--------------|---------|
| 0–35% | Any | APPROVED |
| 35–65% | Yes | UNDER REVIEW — OTP sent |
| Above 65% | Yes | UNDER REVIEW — OTP sent |
| Above 65% | No | BLOCKED |

---

## Local Setup
```bash
git clone https://github.com/Zaira-Shahid/fraud-detection-frontend.git
cd fraud-detection-frontend
```

Open `index.html` directly in your browser — no build step needed.

---

## Screenshots

| Normal Transaction | Fraud Detected |
|-------------------|----------------|
| Risk: 0% — APPROVED | Risk: 100% — BLOCKED |

---

## Author

**Zaira Shahid**
- LinkedIn: [linkedin.com/in/zaira-shahid-](https://linkedin.com/in/zaira-shahid-)
- GitHub: [github.com/Zaira-Shahid](https://github.com/Zaira-Shahid)
