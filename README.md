# iGaming Payment & Fraud Risk Analysis (2025)

## 📌 Project Overview
An end-to-end data analysis project based on a dataset of **10,055 transactions** across 4 payment providers (PSP) and 10 countries. The purpose of this project is to simulate real-world Junior Payment Operations & Fraud Analyst tasks: monitoring payment health (Success/Approval Rates), discovering payment gateway technical outages, and detecting complex fraud patterns.

---

## 📊 Key Performance Indicators (KPIs) Discovered
* **Total Processed Volume:** €5,590,234
* **Global Success Rate (SR):** 64.9%
* **Global Approval Rate (AR):** 75.6%
* **Overall Chargeback Ratio:** 0.66%
* **Fraud Rate:** 3.82%

---

## 🚨 Critical Incidents & Anomalies Investigated

### 1. Card Testing / Velocity Attack (Player PL00001)
* **Pattern:** 25 rapid successful deposits within 50 minutes using **27 unique card BINs** from Germany.
* **Risk Score:** 85+ (Critical).
* **Action Recommended:** Immediate account freeze, full device fingerprint audit, and blacklisting of the associated compromised BIN ranges.

### 2. Coordinated Friendly Fraud Spike (Brazil)
* **Pattern:** A critical chargeback surge up to **4.2%** in June 2025 via `Provider_B`, heavily concentrated in the Mastercard BIN range (`500000–559999`).
* **Action Recommended:** Tighten anti-fraud filters for LATAM traffic on `Provider_B`, implement velocity checks, and enforce mandatory 3DS verification for this specific BIN pool.

### 3. Payment Provider Technical Outage (Provider_D)
* **Pattern:** Success Rate dropped to **45.8%** (benchmark is 65%+), while average response time spiked to **13.9 seconds** (SLA breach due to gateway/provider timeouts).
* **Action Recommended:** Temporarily suspend cascading/routing to `Provider_D` and reroute traffic to `Provider_C` (Top performer with 73.4% SR) until the technical SLA is restored.

---

## 🛠️ Hard Skills Applied
* **Advanced Data Analytics:** Pivot Tables, Data Aggregation, and Trend Analysis.
* **Excel Functions Used:** `XLOOKUP`, `SUMIFS`, `COUNTIFS`, `IF`, `AVERAGE`.
* **Domain Knowledge:** Payment Flows (PSP, Acquirer, Issuer, 3DS), Anti-Fraud Scenarios (Multi-accounting, Bonus Abuse, Card Testing), Risk Scoring, and Regional Fraud Specifics (LATAM/Europe).
