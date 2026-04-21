# NGO-Program-Analysis
Generated NGO dataset cleaned with Power Query and analyzed via PivotTables to answer five guiding questions on reach, effectiveness, water access, activity, and underperformance. Includes transparent cleaning steps, added columns, and ready documentation.
# NGO Program Analysis (Generated Dataset)

##  Project Overview
This project demonstrates how to clean, analyze, and visualize community program data using **Excel Power Query** and **PivotTables**.  

>  Note: The dataset used here is **generated for demonstration purposes** and does not represent actual NGO records.

The analysis answers five guiding questions:
1. How many people are we reaching?  
2. Which programs are most effective?  
3. Do we have water access gaps?  
4. Which community is most active?  
5. Are certain communities underperforming?

---

##  Data Cleaning (Power Query)

### Steps Taken
1. **Fixed Column Types**  
   - Dates → Date type  
   - Text fields → Text type  
   - Numeric fields → Decimal/Whole Number  
   - Ensures calculations and grouping work correctly.

2. **Handled Missing Values**  
   - Replaced `null` with `0` for numeric fields (Participants, Water Access, Outcome Rate).  
   - Preserves transparency while avoiding calculation errors.

3. **Standardized Community Names**  
   - Corrected spelling inconsistencies (e.g., *Keriocho → Kericho*).  
   - Ensures accurate grouping in analysis.

4. **Capped Outliers (Winsorizing)**  
   - `Waste (kg)` capped at 1000.  
   - `Outcome Rate (%)` capped at 100.  
   - Added **new columns** (`Waste Cleaned`, `Outcome Rate Cleaned`) to preserve raw data.  
   - Shows recruiters you handled data quality responsibly.

5. **Added Flags**  
   - `Outlier Flag` column marks extreme values.  
   - Demonstrates transparency in cleaning.

6. **Removed Duplicates**  
   - Used composite key (`Date + Community + Activity Type`).  
   - Ensures unique records.

7. **Added Date Columns**  
   - `Year`, `Month`, and combined `Year-Month` (e.g., `2023-07`).  
   - Enables time‑based analysis and chronological sorting.

---

##  Final Dataset Columns
- **Date, Year, Month, Year-Month** → for time analysis  
- **Community, Program Area, Activity Type** → categorical fields  
- **Participants** → raw participant counts  
- **Waste (kg), Waste (kg) Cleaned** → raw + capped values  
- **Outcome Rate (%), Outcome Rate (%) Cleaned** → raw + capped values  
- **Water Access (%)** → cleaned percentages  
- **Outlier Flag** → Yes/No indicator  

---

##  Findings (PivotTables)

### Q1: How many people are we reaching?
PivotTable shows total participants by Community and Year-Month.

- **Overall Reach:** 62,058 participants across all communities.  
- **Top Community:** Kericho (19,007 participants).  
- **Lowest Community:** Kipkelion (12,828 participants).  
- **Peak Month:** June 2023 (5,888 participants).  
- **Lowest Month:** August 2023 (3,723 participants).  

**Outcome:** Our programs consistently reach thousands monthly, with Kericho leading in participant engagement.

---

### Q2: Which programs are most effective?
PivotTable shows average Outcome Rate (%) Cleaned by Program Area.

- **Most Effective Program:** Economic Empowerment (72.3% average).  
- **Overall Average Effectiveness:** 69.8%.  
- **Peak Month:** August 2023 (80.2% average across all programs).  
- **Lowest Month:** January 2024 (63.1% average).  

**Observation:** Education and Health show high variability, while Economic Empowerment remains consistently strong.

---

### Q3: Do we have water access gaps?
PivotTable shows average Water Access (%) by Community.

- **Overall Average Access:** 52.4%.  
- **Lowest Community:** Kipkelion (51.8% average, dipping to 35.9% in Apr 2023).  
- **Highest Community:** Chepseon (53.5% average, peaking at 66.7% in Apr 2023).  

**Observation:** All communities remain near 50%, indicating widespread gaps. Seasonal dips (e.g., Kipkelion in Apr, Londiani in Jul) highlight vulnerabilities.

---

### Q4: Which community is most active?
PivotTable shows count of Activity Type by Community.

- **Most Active Community:** Kericho (154 activities).  
- **Least Active Community:** Londiani (119 activities).  
- **Overall Activity Count:** 534 activities across all communities.  

**Observation:** Kericho leads in activity engagement, while Londiani lags slightly behind.

---

### Q5: Are certain communities underperforming?
PivotTable compares Sum of Participants vs Average Outcome Rate (%) Cleaned.

- **Kericho:** Largest reach (19,007) but lowest effectiveness (66.5%) → underperformance risk.  
- **Kipkelion:** Smallest reach (12,828) but highest effectiveness (73.3%) → strong outcomes despite scale.  
- **Chepseon:** Balanced (14,805 participants, 70.7% effectiveness).  
- **Londiani:** Moderate reach (15,418) with average effectiveness (69.6%).  

**Observation:** Bigger programs like Kericho reach more people but deliver weaker outcomes, while smaller programs like Kipkelion achieve stronger results. This highlights the need to balance scale with quality.

---

##  Conclusion
This project demonstrates:
- **Data cleaning transparency** (raw + cleaned columns side by side).  
- **Recruiter‑ready documentation** (every step explained).  
- **Actionable insights** tied directly to guiding questions.  

The workflow shows how Power Query + PivotTables can transform messy data into clear, decision‑ready analysis.

Analyst- Sagambor

