# Renewable-Energy-Project-SQL-
# Global Renewable Energy Asset Intelligence System (GREAIS)

## 📌 Project Overview
The **Global Renewable Energy Asset Intelligence System (GREAIS)** is an enterprise-level SQL analytics engine built to monitor, audit, and optimize renewable energy assets worldwide. 

Rather than relying on basic data filtering, this project treats the relational database as a core analytical processor. It addresses complex operational challenges by tracking real-time asset efficiency, detecting mechanical anomalies through statistical thresholds, identifying grid vulnerabilities, and calculating comprehensive corporate profitability across global operations.

## 🛠️ Advanced SQL Techniques Demonstrated
* **Statistical Process Control:** Using `AVG` and `STDDEV` to calculate $+3\sigma$ (three standard deviations) threshold limits to detect mechanical anomalies.
* **Complex Window Functions:** Applying time-series analysis (`ROWS BETWEEN`), frame specification partitions (`RANGE BETWEEN`), and consecutive event streak tracking (Islands-and-Gaps).
* **Multi-CTE Financial Orchestration:** Structuring layered Common Table Expressions combined with `COALESCE` and `DENSE_RANK()` to aggregate revenue, maintenance liabilities, and grid failure losses into country-wide rankings.
* **Unified Time-Series Aggregations:** Utilizing `EXTRACT` date modifications alongside statistical `CORR` functions to find links between mechanical downtime and corporate financial impacts.

---

## 🗄️ Database Architecture & Schema
The relational model consists of 7 primary tables designed to map the entire operational lifecycle of a global energy provider:

1. **`plant_master`**: Infrastructure details containing location metadata (`plant_id`, `plant_name`, `country`).
2. **`energy_generation`**: High-frequency time-series logging output (`plant_id`, `datetime`, `energy_generated_mwh`, `efficiency_percent`).
3. **`energy_sales`**: Transactional ledger recording income streams (`plant_id`, `sale_date`, `revenue_usd`).
4. **`maintenance_logs`**: Operational upkeep tracking ledger (`plant_id`, `maintenance_type`, `downtime_hours`, `maintenance_cost`).
5. **`grid_failures`**: Systemic grid connection instability logs (`failure_id`, `plant_id`, `failure_date`, `outage_hours`, `financial_loss_usd`).
6. **`carbon_credits`**: Green initiative incentive tracking (`plant_id`, `credits_generated`, `market_price_usd`).
7. **`sensor_readings`**: Internet of Things (IoT) mechanical performance telemetry (`plant_id`, `timestamp`, `temperature`, `vibration_level`).

---

## 📊 Business Insights Uncovered
* **High-Loss Correlation:** Blending maintenance and grid failure datasets revealed a steep, direct correlation between system downtime and actual financial loss, pointing to systemic grid instability rather than regular mechanical degradation.
* **Localized Infrastructure Risk:** Isolated a small cluster of power assets suffering more than 3 grid failures per month, signaling regional infrastructure weaknesses.
* **Asset Performance Divergence:** Successfully distinguished between baseline operations, sharp drops below 60% efficiency, and high-performing assets maintaining strict 30-day efficiency marks above 95%.

---

## 💡 Strategic Business Recommendations
1. **Condition-Based Maintenance:** Deploy the 3-hour rolling telemetry alerts (`High Temp Spike` and `High Vibration Spike`) to shift operations from expensive scheduled maintenance cycles to proactive, predictive fixes.
2. **Grid Reinforcement Prioritization:** Target capital investments directly toward reinforcing regional grid interfaces for assets flagged with more than 3 failures per month to preserve energy capture rates.
3. **Optimized Capital Allocation:** Use the country-level ranking matrix to channel development capital into high-margin zones while divesting from or overhauling chronically low-efficiency facilities.

---

## 🚀 How to Run the Queries
1. Clone this repository to your local workspace:
   ```bash
   git clone https://github.com
   ```
2. Open your preferred SQL database management tool (PostgreSQL recommended).
3. Execute the initial schema setup scripts found within `/Database-Setup`.
4. Run individual queries inside the `/Scripts` folder to verify system outputs, analytical trends, and corporate financial metrics.

---
⭐ **If you find this repository helpful for understanding advanced analytical SQL implementations, please give it a star!**
