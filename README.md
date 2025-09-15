# 🥝 Woogle — Woolworths NZ Analytics Health Check Prototype

Woogle is a prototype **analytics health check dashboard** that blends **BigQuery data, anomaly detection, and LLM-powered conversational insights** into a single, approachable interface. It’s designed to help analytics teams, marketers, and stakeholders quickly spot issues, understand context, and take action.

---

## ✨ Features

- **💬 Talk to Woogle (Olive)**
  - Conversational interface powered by an LLM (demo simulated in this prototype).
  - Ask natural language questions like:
    - “Summarise anomalies in the last 7 days”
    - “Why did add_to_cart drop yesterday?”
    - “Compare revenue vs forecast for last week”
   
    +---------+        +----------------+        +-----------------+        +-------------+
|  User   | -----> |   Olive (LLM)  | -----> |   MCP (BigQuery)| -----> |   BigQuery  |
+---------+        +----------------+        +-----------------+        +-------------+
     |                   |                          |                          |
     | Ask in NL         | Generate SQL + context   | Secure query execution   | Return results
     |------------------>|------------------------->|------------------------->|----------------
     |                   |                          |                          |
     | <---------------- | <----------------------- | <----------------------- |
     |  Plain-English     |   Structured results     |   Query output           |
     |  insights + next   |   + anomaly detection    |                          |
     |  steps             |                          |                          |


- **🔍 Searchable Metrics**
  - Autocomplete search bar for key GA4 and business events.
  - Drill into event counts, day-over-day changes, and anomalies.

- **🚦 Anomaly Detection & Suggested Actions**
  - Colour-coded signals:
    - ✅ Green = healthy
    - ⚠️ Orange = warning
    - ⛔ Red = critical
  - Grouped by business domain:
    - Campaigns
    - UX & Conversion
    - Sales (Revenue vs Forecast)
    - Customer Experience
    - Category & SKU Highlights
    - Data Engineering
    - Analytics Ops

- **📦 Category & SKU Highlights**
  - Track top movers and underperformers (e.g. Avocados +15%, Pasta -10%, Milk OOS 7%).

- **📊 Strategic KPIs**
  - **EDR (Everyday Rewards)**: active members, redemption rates.
  - **Cartology**: campaign ROI, media revenue growth.
  - **Weekly Active App Users**: engagement trends and YoY growth.

- **🛠️ Data Engineering Checks**
  - Partition monitoring: detect missing GA4 daily tables.
  - Late-arriving data: flag incomplete days (<100% completeness).
  - Schema drift: detect new event parameters or mismatches.

---

## 🏗️ Tech Stack

- **Frontend**: HTML, CSS, Vanilla JS
- **Data Layer**: Demo `healthData` array (replace with BigQuery MCP integration)
- **LLM Integration**: Simulated responses (replace with MCP → BigQuery → LLM pipeline)

---

## 🚀 Getting Started

### Local
1. Clone the repo
2. Open `index.html` in your browser  
   *(or run a local server with `python3 -m http.server 8000`)*

### GitHub Pages
1. Push to a public repo
2. Enable **Pages** in repo settings
3. Access at `https://your-username.github.io/woogle/`

---

## 🧭 Roadmap

- [ ] Replace demo `healthData` with live BigQuery MCP queries
- [ ] Add dynamic anomaly detection (rolling averages, thresholds)
- [ ] Wire Olive’s chat panel to a real LLM backend
- [ ] Add drill-through links to dashboards
- [ ] Extend SKU/category highlights with live product feeds

---

## 👩‍💻 For Analytics Teams

This prototype is designed to:
- **Democratise insights**: let non-technical users “talk to the data”
- **Catch issues early**: anomalies flagged before they hit dashboards
- **Bridge business & engineering**: campaigns, UX, sales, and data quality in one view
- **Enable action**: every anomaly comes with suggested next steps

---

## ⚠️ Disclaimer

This is a **prototype**. All data shown is simulated for demonstration purposes.  
Replace demo logic with live BigQuery + MCP integrations before production use.
