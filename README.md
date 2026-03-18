# Badvel Rural Circle — Men Management System

A cloud-based web application built for the **Badvel Rural Circle, Andhra Pradesh Police Department** to manage and track personnel duty assignments in real time across 4 police stations.

---

## 🚀 Live Deployment

Currently in active use by the Badvel Rural Circle, Kadapa District, Andhra Pradesh.

---

## 📋 Features

- **Role-Based Login** — Separate secure access for CI Office and individual police stations (Badvel Rural PS, Atlur PS, B. Kodur PS)
- **Real-Time Cloud Sync** — All data synced live via Supabase backend
- **Duty Assignment** — Assign BB Duty, Routine Duty, Attachment, and Absence with date ranges
- **Double-Booking Detection** — Automatically detects and alerts on conflicting duty assignments
- **Live Dashboard** — Summary counts for Total Force, Available, BB Duty, Attached, Routine, and Absent
- **Advanced Duty View** — View upcoming/future duty assignments before they become active
- **Search & Filter** — Search by name, G.No, or duty type; filter by status
- **Excel Import** — CI Office can upload master roll from Excel/CSV to update the entire database
- **Excel Export** — Export any filtered view to a formatted Excel report
- **WhatsApp Notifications** — Send individual duty notifications directly via WhatsApp
- **Group Report** — Generate and share formatted duty reports to WhatsApp groups
- **Bulk SMS** — Copy all contact numbers or trigger native SMS for bulk messaging
- **History Log** — View complete cloud history of all assignments

---

## 🛠️ Tech Stack

| Technology | Usage |
|---|---|
| HTML / CSS / JavaScript | Frontend — single file application |
| Supabase | Cloud database and real-time backend |
| SheetJS (XLSX) | Excel import and export |
| Google Fonts (Poppins) | Typography |

---

## 🗄️ Database Structure

Two Supabase tables:

**`brc_master`** — Master roll of all personnel
| Column | Type | Description |
|---|---|---|
| ps | text | Police Station name |
| rank | text | Officer rank |
| gno | text | Government number (unique ID) |
| name | text | Officer name |
| cell | text | Mobile number |

**`brc_active`** — Active and historical duty assignments
| Column | Type | Description |
|---|---|---|
| gno | text | Links to master roll |
| duty | text | Duty type or name |
| type | text | duty / routine / attach / absent |
| place | text | Place of duty |
| start_date | date | Assignment start date |
| end_date | date | Assignment end date |

---

## 🔐 Security Note

This application uses Supabase Row Level Security (RLS) to protect data. The publishable API key in the source is intentionally public-facing. Station-level access control is enforced at the application layer via PIN-based login.

---
## 🚀 Live Deployment

**Live Site:** [https://jstmahi.github.io/Badvel-Circle/](https://jstmahi.github.io/Badvel-Circle/)

Currently in active use by the Badvel Rural Circle, Kadapa District, Andhra Pradesh.
---


## 👨‍💻 Built By

**Mahidhar Ramayanam**
B.Tech CSE (AI), Sree Vidyanikethan Engineering College, Tirupati
[LinkedIn](https://linkedin.com/in/mahidharramayanam

---

## 📌 Note

This is a real-world deployment built for operational use by the Andhra Pradesh Police Department. Personnel data is not included in this repository.
