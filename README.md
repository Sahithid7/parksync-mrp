# 🅿️ ParkSync — Modernizing the City of Riverton's Parking Permit & Enforcement Operations

### A Data-Driven Analytics Solution

[![Project Site](https://img.shields.io/badge/Live-Project%20Site-7c3aed?style=for-the-badge&logo=githubpages&logoColor=white)](https://ganesh79810.github.io/final/)
[![Live Dashboard](https://img.shields.io/badge/Live-Analytics%20Dashboard-2563eb?style=for-the-badge&logo=googlechrome&logoColor=white)](https://ganesh79810.github.io/MRP_DASHBOARD/)
[![Solution Prototype](https://img.shields.io/badge/Live-Solution%20Prototype-22c55e?style=for-the-badge&logo=figma&logoColor=white)](https://ganesh79810.github.io/prototype/)
[![Course](https://img.shields.io/badge/Course-IS%205960-orange?style=flat-square)](#)
[![University](https://img.shields.io/badge/Saint%20Louis%20University-Spring%202026-003DA5?style=flat-square)](#)
[![Status](https://img.shields.io/badge/Status-Completed-success?style=flat-square)](#)
[![Infrastructure Cost](https://img.shields.io/badge/Infrastructure%20Cost-%240.00-brightgreen?style=flat-square)](#)

---

## 📌 Overview

The City of Riverton relies on a **legacy parking permit system** that batch-uploads
permit data to officer handheld devices only **every 2–4 hours**. During this gap,
residents whose permits have *already been approved* — but haven't yet synced to a
device — are issued **wrongful citations**, triggering disputes, wasted staff hours,
and resident frustration.

**ParkSync** is a real-time, event-driven sync solution that closes this gap, replacing
slow batch CSV uploads with near-instant permit propagation to enforcement devices —
at **zero infrastructure cost**.

This repository contains the full Master's Research Project (MRP) submitted for
**IS 5960 — Information Systems**, Saint Louis University, Spring 2026.

---

## 👥 Project Information

| | |
|---|---|
| 🎓 **Course** | IS 5960 — Information Systems |
| 🏫 **University** | Saint Louis University |
| 📅 **Term** | Spring 2026 |
| 🧑‍🏫 **Faculty Advisor** | Dr. Tatiana Cardona |
| 💡 **Solution Name** | ParkSync |

### 🤝 Team Members & Roles

| Name | Role |
|---|---|
| Ganesh Kommineni | 🗂️ Project Manager |
| Sachin Jignesh Patel | 📊 Business Analyst |
| Hujjur Rahaman Shaik | 🔍 Data Analyst |
| **Sahithi Devineni** | 🏗️ System Architect |
| Aditya Vardhan Anne | 🎨 Prototype Designer |

---

## 🚨 The Problem

> Riverton's legacy parking system batch-uploads permit approvals to officer devices
> only once every **2–4 hours**. Residents with valid, *just-approved* permits are
> cited as violators simply because their device hasn't synced yet.

This sync gap produces measurable, costly impact across the city — drawn from a
1,200-record synthetic dataset modeling a full year of operations:

| 📈 Metric | Current Value |
|---|---|
| 🚫 Erroneous Citation Rate | **35.9%** (431 wrongful citations) |
| ⏱️ Average Device Sync Latency | **101.4 minutes** |
| 📄 Disputes Filed | **547** |
| 🧑‍💼 Staff Hours Wasted Annually | **~182 hours** |
| ⚖️ Dispute Dismissal Rate | **59.8%** |

---

## 💡 The Solution — ParkSync (Real-Time Sync)

ParkSync replaces the legacy batch-upload pipeline with an **event-driven, real-time
permit synchronization** layer — so the moment a permit is approved, every officer's
device knows about it.

| ✅ What Changes | Impact |
|---|---|
| Batch sync (2–4 hrs) → Event-driven sync | Devices updated in **under 2 minutes** |
| Wrongful citations | **86% reduction** (431 → ~60) |
| Disputes filed | **80% reduction** (547 → ~110) |
| Staff time | **145 hours recovered annually** |
| Infrastructure investment required | **$0.00** |

### 🔗 Live Links

- 🌐 **Project Site:** [ganesh79810.github.io/final](https://ganesh79810.github.io/final/)
- 📊 **Analytics Dashboard:** [ganesh79810.github.io/MRP_DASHBOARD](https://ganesh79810.github.io/MRP_DASHBOARD/)
- 🖼️ **Solution Prototype:** [ganesh79810.github.io/prototype](https://ganesh79810.github.io/prototype/)

---

## 🧰 Tech Stack

| Layer | Tools |
|---|---|
| 🐍 Dataset Generation | Python 3, Pandas, NumPy |
| 📊 Visualization | Chart.js 4.4.1 |
| 🌐 Front End | HTML, CSS, JavaScript (single-file dashboard) |
| ☁️ Hosting | GitHub Pages (free, $0 infrastructure cost) |

---

## 📊 Dashboard Pages

The analytics dashboard is organized into five focused views:

1. **🏠 Overview** — KPI summary cards, citation outcome donut chart, and zone-by-zone
   latency bar charts for an at-a-glance picture of the problem.
2. **🔬 Analysis** — Dose-response chart correlating sync latency with citation error
   rate, plus monthly trend lines across the full year.
3. **⚖️ Before vs After** — Side-by-side comparison of the legacy batch system against
   the projected ParkSync real-time model.
4. **🔎 Data Explorer** — Searchable, filterable table exposing all 1,200 underlying
   records for transparency and deep inspection.
5. **📉 Latency Deep Dive** — Latency distribution histogram, officer-level breakdowns,
   and a latency-vs-error scatter plot.

---

## 🏛️ System Architecture (TOGAF Framework)

ParkSync's architecture is modeled using the **TOGAF** enterprise architecture
framework across four layers:

| Layer | Description |
|---|---|
| 🏢 **Business Layer** | Permit issuance, field enforcement, dispute resolution, and reporting/analytics workflows |
| 🗄️ **Data Layer** | `PERMITS` → `CITATIONS` → `DISPUTES`, linked by shared identifiers |
| ⚙️ **Application Layer** | Data Ingestion → Analytics Engine → Visualization → Dashboard UI |
| 🖥️ **Technology Layer** | GitHub, GitHub Pages, Python, Chart.js, CSV/JSON data interchange |

### 🗂️ Entity Relationship Diagram (ERD) Summary — City of Riverton Parking Dataset

```text
┌────────────────────────┐          ┌──────────────────────────────┐          ┌───────────────────────────┐
│        PERMITS         │          │          CITATIONS           │          │         DISPUTES          │
├────────────────────────┤          ├──────────────────────────────┤          ├───────────────────────────┤
│ • Permit ID            │          │ • Citation ID                │          │ • Dispute ID              │
│ • Vehicle Plate        │          │ • Vehicle Plate              │          │ • Citation ID             │
│ • Applicant Type       │          │ • Citation DateTime          │          │ • Dispute Filed           │
│ • Parking Zone         │          │ • Parking Zone               │          │ • Dispute Filed Date      │
│ • Permit Submission Dt │          │ • Officer ID                 │          │ • Dispute Resolution Date │
│ • Permit Approval Date │          │ • Device Sync Latency (min)  │          │ • Dispute Outcome         │
│ • Permit Status        │          │ • Permit Visible On Device   │          │ • Dispute Resolution Days │
└──────────┬─────────────┘          │ • Erroneous Citation         │          │ • Admin Handling Time(min)│
           │                        │ • Citation Amount            │          └─────────────┬─────────────┘
           │   Vehicle_Plate (1)    │ • Payment Status             │   Citation ID (1)      │
           └───────────────────────▶└──────────────┬───────────────┘◀──────────────────────┘
                                                    ▲
                                                    │
                                          (joins back to DISPUTES)

Relationships:
  • PERMITS  ⇄ CITATIONS   joined on Vehicle_Plate  (1:1 lookup — links a citation back to its source permit)
  • CITATIONS ⇄ DISPUTES   joined on Citation ID    (1:1 lookup — links a dispute back to the citation that triggered it)
```

---

## 📐 Key Performance Indicators (KPIs)

| KPI | Current | Target |
|---|---|---|
| **ECR** — Erroneous Citation Rate | 35.9% | < 5% |
| **DSL** — Device Sync Latency | 101.4 min | < 2 min |
| **DRR** — Dispute Resolution Rate | 59.8% | < 15% |

---

## 🗃️ Dataset

The analysis is powered by a **synthetic dataset** generated to realistically model
a full year of Riverton parking operations:

- 📦 **1,200** synthetic records
- 🧬 **21** variables per record
- 🗺️ **4** parking zones
- 📅 **12 months** of data (calendar year 2024)
- 🛠️ Generated programmatically using **Python**, **Pandas**, and **NumPy**

**Citation error probability formula:**

```text
P(error) = 0.05 + (latency × 0.003)
```

This formula models the realistic relationship between how long a permit approval
takes to sync to an officer's device (`latency`, in minutes) and the probability that
the resident is wrongfully cited in that window — forming the statistical backbone of
the dose-response analysis on the dashboard.

---

## 📁 Project Structure

```text
parksync-mrp/
├── index.html        # Single-file project website (overview, research, architecture, roadmap, etc.)
├── README.md         # This file — full project documentation
└── .gitignore        # Ignores OS/log artifacts (.DS_Store, Thumbs.db, *.log)
```

> 📊 The interactive analytics dashboard and solution prototype are hosted in their
> own repositories and deployed via GitHub Pages — see the **Live Links** above.

---

## ⚖️ Ethical Considerations

Building a data product around municipal enforcement carries real responsibility to
the residents it affects. ParkSync was designed with the following principles in mind:

- 🔐 **Privacy** — All underlying data is **synthetic**; no real resident, vehicle, or
  officer information was collected, stored, or exposed at any stage of this project.
- ⚖️ **Equity** — The dataset and analysis span all four parking zones equally, so that
  improvements in citation accuracy benefit residents city-wide rather than concentrating
  gains in any single neighborhood.
- 🔍 **Transparency** — The Data Explorer page exposes the full underlying dataset,
  and this README documents the exact formula used to model citation errors, so that
  any reviewer — technical or not — can audit how the conclusions were reached.
- 🧭 **Accountability** — Recommendations focus on *closing the sync gap* rather than
  increasing enforcement, directly reducing the harm (wrongful citations and disputes)
  experienced by residents.

---

## 📚 References

- City of Riverton legacy parking system documentation *(course-provided case material, IS 5960)*
- Chart.js Documentation — [chartjs.org](https://www.chartjs.org/)
- The Open Group, *TOGAF® Standard, 10th Edition* — [opengroup.org/togaf](https://www.opengroup.org/togaf)
- Pandas Documentation — [pandas.pydata.org](https://pandas.pydata.org/)
- NumPy Documentation — [numpy.org](https://numpy.org/)
- GitHub Pages Documentation — [docs.github.com/pages](https://docs.github.com/en/pages)

---

## 🙌 Acknowledgments

Submitted in partial fulfillment of the requirements for **IS 5960 — Information
Systems** at **Saint Louis University**, under the guidance of **Dr. Tatiana Cardona**.
Special thanks to the entire ParkSync team for their collaboration across research,
analysis, architecture, and design.

---

<p align="center">
  <i>Built with 💙 by the ParkSync team — Spring 2026</i>
</p>
