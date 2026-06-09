# Sales Performance Analysis & Reporting System (SPAR)

## 📊 Executive Summary
A retail business was operating with 305 raw transactional records spread across inconsistent formats with no structured reporting infrastructure. There was zero visibility into which products, regions, or sales reps were driving or destroying revenue. 

I managed the end-to-end delivery of an automated reporting system across **3 Agile sprints**—transforming raw data into an executive-ready dashboard with actionable strategic recommendations.

### 🖥️ Executive Sales Dashboard 
<img width="1136" height="713" alt="E2E_Sales_Dashboard" src="https://github.com/user-attachments/assets/347270e8-63c1-4880-842d-44de76e40899" />


---

## 🛠️ Tech Stack & Tools
* **Project Management & Governance:** Jira Cloud (Scrum), Confluence Cloud
* **Data Engineering & BI:** Microsoft Excel (Power Query, Pivot Tables, Interactive Slicers)
* **Stakeholder Delivery:** Microsoft PowerPoint

---

## 🔍 1. The Problem
The business lacked a reliable reporting layer. Raw data contained duplicate records, broken date formats, and inconsistent casing, making any historical analysis untrustworthy. Consequently, leadership had no clear view of where revenue was concentrated, why orders were being returned, or which territories were severely underperforming.

---

## ⚙️ 2. Agile Project Management & Governance
Rather than treating this as a simple, one-off analysis, I structured the initiative as a formal project delivery to ensure transparency and repeatability.

* **Sprint Execution:** Managed all deliverables under Epic **SPAR-1** across 3 timeboxed sprints, achieving a **79% sprint velocity closure rate** (11 of 14 tickets marked *Done*).
* **Documentation:** Authored a comprehensive **Project Charter** in Confluence, defining scope, constraints, assumptions, and success criteria prior to kick-off.
* **Issue Tracking:** Maintained full sprint backlog visibility by tracking user stories, bugs, and sub-tasks in Jira (see `/jira_screenshots`).
* **Artifact Delivery:** Compiled a final stakeholder-facing PowerPoint presentation and PDF report as formal project closeout artifacts.

---

## 🧼 3. Data Engineering & Governance (Power Query ETL)
To ensure the insights could be trusted by leadership, I developed a robust ETL pipeline focused on strict data governance:

1.  **ETL Pipeline:** Built a 6-step Power Query transformation pipeline to resolve duplicate records, broken date formats, and inconsistent text casing.
2.  **Data Governance Decision:** Formally documented a **15% data reduction** (305 raw $\rightarrow$ 240 clean records) in a **Data Loss Statement**. This was reviewed and formally accepted by stakeholders. 
    > *PM Note: Dropping corrupted records without stakeholder sign-off is a data governance failure, not just a cleaning step.*

---

## 📈 4. Business Intelligence & Key Findings
Data was modeled across 5 analytical dimensions: *Revenue by Month, Revenue by Product, Revenue by Region, Sales Rep Performance,* and *Order Status Breakdown*. 

Three critical insights emerged, each mapping directly to a strategic recommendation:

| Finding | Impact & Context | Actionable Recommendation |
| :--- | :--- | :--- |
| **1. Revenue Concentration Risk** | A single product (**Laptop Pro**) generates **72%** of total revenue ($265,422 of $366,751). This poses a severe business continuity risk. | Diversify the product mix to bring single-product dependency **below 50%**. |
| **2. Abnormal Return Rate** | The order return rate sits at **26%** (74 orders)—nearly **3× the retail industry average** (~10%), representing massive lost margin. | Launch an immediate root-cause audit of the 74 returned orders before the next sales cycle. |
| **3. Territory Disparity** | The **South** region leads at $122,091, while the **East** territory lags at $55,907—a **2.2× gap** with no structural explanation. | Audit East region account coverage and implement a cross-territory mentorship pairing program. |

---

## 💡 PM Lessons Learned
* **Scope Data Governance Upfront:** The Data Loss Statement was not an afterthought; it was treated as a formal change request. Skipping this step in a real-world enterprise environment creates severe audit risks.
* **Velocity is an Accountability Metric:** A 79% sprint closure rate is good, but not perfect. The 3 unclosed tickets were documented in the sprint retrospective with root causes identified (scope creep regarding complex dashboard slicer logic).
* **No Recommendations Without Owners:** A dashboard that highlights a problem without pointing to a decision framework is just a report. Every finding must map directly to an actionable next step.

---

## 🗂️ Repository Structure
```micro
├── /data                # Raw and cleaned transactional datasets (240 clean records)
├── /dashboard           # Interactive Excel MVP dashboard with cross-linked slicers
├── /confluence_report   # Project Charter, Data Dictionary, and Data Cleaning logs
├── /jira_screenshots    # Sprint backlogs, user story mapping, and bug tickets
├── /presentation        # Stakeholder PowerPoint deliverable
└── /project_final_report# Executive summary + finalized PDF report
