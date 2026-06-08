# iGaming Payment Operations & Anti-Fraud Analysis (2025)

## Project Overview
This project is an end-to-end data analysis focused on payment monitoring and fraud detection. Using a dataset of 10,055 transactions across 4 payment service providers (PSPs) and 10 countries, I simulated core tasks of a Payment Operations / Fraud Analyst: tracking system health, identifying gateway outages, and investigating fraud patterns.

## Global Portfolio Metrics (KPIs)
* Total Volume: €5,590,234
* Success Rate (SR): 64.9%
* Approval Rate (AR): 75.6%
* Chargeback Ratio: 0.66%
* Fraud Flag Rate: 3.82%

## Incident Investigations

### Case 1: Velocity Attack / Card Testing (Player PL00001)
* **Anomaly:** Player account generated 25 successful deposits within 50 minutes. The operations triggered a critical Risk Score (85+) due to the use of 27 unique card BINs from Germany on a single account.
* **Resolution:** Immediate account suspension, device fingerprint audit, and blacklisting of the compromised BIN ranges to prevent further card-testing attempts.

### Case 2: Coordinated Friendly Fraud Spike (Brazil Market)
* **Anomaly:** A severe chargeback spike reaching 4.2% was detected in June 2025. The issue was strictly isolated to Provider_B and heavily concentrated within the Mastercard BIN range (500000–559999).
* **Resolution:** Implemented temporary volume limits for LATAM traffic on Provider_B, introduced stricter velocity checks, and enforced mandatory 3DS for the affected Mastercard BIN pool.

### Case 3: Gateway SLA Breach (Provider_D Technical Outage)
* **Anomaly:** Provider_D's Success Rate dropped to 45.8% (against an internal benchmark of 65%+). Investigation showed the provider's average response time spiked to 13.9 seconds, causing massive timeouts and session abandonments.
* **Resolution:** Suspended cascading/routing rules for Provider_D and redirected the traffic flow to Provider_C (top performer with 73.4% SR) until the technical team confirms SLA restoration.

## Tech Stack & Domain Knowledge
* **Data Analytics:** Advanced Excel (Pivot Tables, XLOOKUP, SUMIFS, COUNTIFS, IF, AVERAGE), data validation, and trend monitoring.
* **Domain Expertise:** Payment flows (PSP, Acquirer, Issuer, Routing, Cascading), Anti-Fraud mechanics (Multi-accounting, Bonus Abuse, Account Takeover), and risk mitigation.
