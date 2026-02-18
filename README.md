# U.S. Electric Vehicle Market Share Analysis

## 📊 Project Overview
Analysis of alternative fuel vehicle adoption across the United States to support infrastructure planning and EV adoption forecasting for a government transportation board.


## 🎯 Business Questions
1. What percentage of vehicles in each state are EVs, PHEVs, HEVs, and gasoline?
2. Which states have the highest EV adoption rates, and which lag behind?
3. Which alternative fuels (biodiesel, ethanol, hydrogen) are significant vs. niche?
4. Where should policymakers prioritize EV infrastructure investment?

## 🛠️ Technical Skills Demonstrated
- **Data Cleaning**: Handling missing values, type conversions, standardization
- **SQL Analysis**: Complex queries, aggregations, CTEs, ranking functions
- **Python**: pandas, matplotlib, seaborn, plotly, pandasql
- **Visualization**: Bar charts, choropleth maps, pie charts
- **Business Intelligence**: Data-driven recommendations, priority scoring

## 📈 Key Findings
- National EV adoption: 1.24% (3.6M vehicles)
- California leads at 3.41% adoption (1.26M EVs)
- Ethanol is the only significant alternative fuel (7.05% of fleet)
- Top infrastructure priorities: California, Washington, DC, Hawaii

## 📁 Repository Contents
- `EV_Vehicle_Analysis.ipynb` - Main analysis notebook
- `Vehicle_Data.csv` - Dataset (51 U.S. jurisdictions)
- `requirements.txt` - Python dependencies
- `README.md` - This file


## 📊 Analysis Highlights

### Market Share Analysis
- Calculated EV, PHEV, HEV, and gasoline percentages for all 51 states
- Identified top 10 and bottom 10 states by EV adoption
- Compared California vs. Texas, Florida, New York

### Alternative Fuels Classification
- **Significant (>1%)**: Ethanol/E85 (7.05%)
- **Emerging (0.1-1%)**: Biodiesel (0.98%)
- **Niche (<0.1%)**: Hydrogen (0.006%), CNG (0.009%)

### Infrastructure Recommendations
Multi-factor priority scoring based on:
- EV adoption rate
- Absolute EV count
- Total market size

**Tier 1 (High Priority)**: California, Washington, DC, Hawaii  
**Tier 2 (Medium Priority)**: Florida, New York, New Jersey, Oregon

## 💡 Technical Approach

### Data Processing
```python
# Example: Percentage calculation
dataset['EV_Percent'] = (dataset['EV'] / dataset['Total_Vehicles']) * 100
```

### SQL Analysis
```sql
-- Example: Top states query
SELECT state, ev, total_vehicles,
       ROUND(100.0 * ev / total_vehicles, 2) as ev_percent
FROM vehicle_data
ORDER BY ev_percent DESC
LIMIT 10;
```

### Visualizations
- Choropleth map showing EV adoption across U.S. states
- Bar charts for top/bottom state rankings
- Pie charts for fuel type distribution

## 📝 Lessons Learned
- Importance of data cleaning (comma removal, type conversion)
- SQL for complex analytical queries
- Multi-factor scoring for business recommendations
- Data storytelling for executive audiences

## 🚀 How to Run
```bash
# Clone repository
git clone https://github.com/Diksha-Bidikar/ev-vehicle-analysis.git

# Install dependencies
pip install -r requirements.txt

# Run Jupyter notebook
jupyter notebook Copy_of_EV_project.ipynb
```

## 🔗 Connect With Me
- **LinkedIn**: [linkedin.com/in/diksha-bidikar](https://www.linkedin.com/in/diksha-bidikar/)
- **Portfolio**: https://diksha-bidikar.github.io/
- **Email**: bidikar.diksha@gmail.com

## 📄 License
This project is for educational and portfolio purposes.

## 🙏 Acknowledgments
- **Analyst Builder** for providing the project framework and learning platform

---

*This project demonstrates data analysis skills developed through structured learning on the Analyst Builder platform.*