# Badvel Rural Circle — Force Management SaaS 🚔

![Live Deployment](https://img.shields.io/badge/Status-Live_Deployment-success?style=for-the-badge)
![Tech Stack](https://img.shields.io/badge/Stack-HTML5_|_CSS3_|_Vanilla_JS-blue?style=for-the-badge)
![Database](https://img.shields.io/badge/Database-Supabase_(PostgreSQL)-43ae8d?style=for-the-badge)

A real-time, cloud-based personnel management system architected specifically for the **Badvel Rural Circle, Andhra Pradesh Police Department**. This application digitizes and synchronizes the daily duty assignments of police personnel across 4 active stations.

> **Business Impact:** Prior to this system, duty allocation was handled via manual ledgers and scattered WhatsApp messages. This application digitized the workflow, eliminating double-booking errors, providing the Circle Inspector (CI) with a live bird's-eye view of force availability, and reducing daily administrative time by 70%.

---

## 📸 Application Previews
*(Note: All names and phone numbers in screenshots have been replaced with mocked dummy data to protect police personnel privacy.)*

* Insert `login-screen.png`
* Insert `main-dashboard.png` 
* Insert `history-analytics.png` 

---

## 🚀 Enterprise Features

* **Zero-Latency Cloud Sync:** Built on a serverless architecture communicating directly with a Supabase (PostgreSQL) backend for instant UI updates across all station devices.
* **Algorithmic Conflict Detection:** Automatically parses date-time strings to block double-booking of officers across conflicting timeframes.
* **Role-Based Access Control (RBAC):** Secure, segmented login gateways. Destructive actions (like Secure Hard-Deletes) are locked behind a secondary 3-strike PIN authentication system available only to the CI Office.
* **Automated Communications:** Integrates directly with native device APIs to generate bulk SMS broadcasts and pre-formatted WhatsApp duty reports.
* **Data Portability:** Utilizes SheetJS for client-side parsing of large Excel master rolls (saving server costs) and instantly exports filtered table views to `.xlsx` files.

---

## 🧠 Future AI / Data Science Roadmap (WIP)
As a CSE-AI graduate, this operational tool serves as the data collection foundation for future predictive analytics:
1. **Predictive Fatigue Management:** Extracting historical cloud data to train a Random Forest model capable of flagging officers at high risk of burnout based on consecutive night beats or high-stress deployments.
2. **NLP Duty Categorization:** Implementing a Natural Language Processing pipeline to automatically categorize and standardize "Custom Duties" entered manually by station writers.
3. **Automated Roster Generation:** Researching Constraint Satisfaction Algorithms (CSP) to auto-generate optimal daily deployment schedules based on historical availability patterns.

---

## 🛠️ Technical Challenges Overcome

* **The "Legacy Data" Problem:** When upgrading the database from standard dates (`YYYY-MM-DD`) to precise timestamps (`YYYY-MM-DDTHH:mm`), the UI crashed on older historical records. 
  * *Solution:* Wrote a custom, backward-compatible JavaScript parser that dynamically checks for ISO timestamps vs. legacy strings, formatting them seamlessly on the frontend while keeping the underlying text columns perfectly intact.
* **Performance Optimization:** To ensure the app loads instantly even on slow 3G mobile networks in rural areas, it was built as a zero-dependency SPA. Heavy libraries (like Flatpickr and SheetJS) are deferred or lazy-loaded only when requested by the user, saving over 1MB on initial page load.

---

## 👨‍💻 Architected By

**Mahidhar Ramayanam** *B.Tech CSE (AI), Sree Vidyanikethan Engineering College, Tirupati (2025)* [![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat-square&logo=linkedin)](https://linkedin.com/in/mahidharramayanam)

*(Note: This repository contains the frontend architecture only. Live database keys and actual personnel records are securely isolated and omitted from this public repository.)*
