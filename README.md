# McDonald's European Restaurant Dashboard 📊

A comprehensive Power BI dashboard analyzing the performance of McDonald's restaurants across 13 European countries, providing actionable insights for strategic decision-making.

## 📋 Project Overview

This business intelligence project was developed for McDonald's European division to monitor and analyze restaurant performance across multiple markets. The dashboard delivers key financial metrics, demographic insights, and operational indicators through interactive visualizations.

## 🎯 Business Objective

Enable McDonald's EU management to:
- Monitor revenue and profitability across European markets
- Identify high-performing and underperforming locations
- Analyze customer demographics and purchasing behavior
- Track theft incidents and operational risks
- Make data-driven decisions for resource allocation

## 📸 Dashboard Preview

### Financial Overview Page
<img width="1372" height="771" alt="image" src="https://github.com/user-attachments/assets/ab3e74ae-b1d5-4df5-bc19-e07254e9931b" />


The Financial Overview page provides a comprehensive view of performance across all 13 European markets, featuring:
- Country-level performance table with revenue, gross profit percentages, and theft amounts
- Interactive European map visualization with bubble indicators for market presence
- General manager gender distribution analysis
- Customer demographic insights by age group
- Theft pattern analysis across different age segments

### Country Breakdown Page
<img width="1372" height="778" alt="image" src="https://github.com/user-attachments/assets/58568170-7526-42a6-a92f-e8290e9d9aed" />


The Country Breakdown page enables deep-dive analysis into sales performance:
- Product category filtering (Beverages, Burgers, Chicken Sandwiches, Fries, Sides & Other)
- Purchase method distribution with visual pie chart
- Monthly revenue and gross profit trend analysis
- Aggregate KPI metrics prominently displayed

## 🔍 Key Insights & Findings

### Financial Performance
- **Total Revenue**: $25.4M across 13 European countries
- **Total Gross Profit**: $18.1M with an average margin of 71.4%
- **Top 3 Markets by Revenue**:
  1. 🇮🇹 Italy: $2.69M (10.58%)
  2. 🇨🇿 Czech Republic: $2.53M (9.97%)
  3. 🇫🇷 France: $2.51M (9.86%)

### Operational Insights
- **Critical Risk Alert**: United Kingdom shows disproportionately high theft amounts ($6,900) - requiring immediate investigation and security measures
- **Spain** demonstrates strong performance with $2.43M revenue but elevated theft ($2,504), suggesting operational challenges
- **Product Performance**: When scaled to country-level view, total revenue reaches $180M with 32M units sold, indicating robust sales volume

### Customer Demographics
- **Highest Revenue Age Group**: 50+ customers generate approximately $400 in average revenue
- **Primary Customer Base**: 30-39 and 40-49 age groups show strong engagement
- **Theft Patterns**: 20-29 age group shows highest theft incidents, requiring targeted loss prevention strategies

### Payment & Purchase Behavior
- **Credit Cards dominate**: 80.7% of all transactions ($26M)
- **Cash transactions**: 16.64% ($5M) - declining trend
- **Gift Cards**: 2.67% ($1M) - opportunity for promotional growth

### Seasonal Trends
- **Consistent Growth**: Revenue shows steady upward trajectory throughout the year
- **Peak Performance**: December shows highest revenue and gross profit
- **Stable Margins**: Gross profit maintains consistent gap above revenue across all months

### Management Insights
- **Gender Disparity**: 76.92% male vs 23.08% female general managers - diversity opportunity
- **Geographic Distribution**: 10 male managers across 13 locations, with 3 female managers

## 📊 Dashboard Features

### Financial Overview Page
- **Country-level Performance**: Revenue, gross profit, and theft amounts by country
- **Geographic Visualization**: Interactive map showing restaurant locations and performance
- **Manager Gender Distribution**: Insights into management diversity (76.92% Male, 23.08% Female)
- **Revenue by Age Demographics**: Understanding customer segments (20-29, 30-39, 40-49, 50+)
- **Theft Analysis by Age**: Identifying risk patterns across customer demographics

**Key Metrics:**
- Total Revenue: $25.4M
- Total Gross Profit: $18.1M
- Total Theft Amount: $12,376

### Country Breakdown Page
- **Product Category Analysis**: Performance metrics for Beverages, Burgers, Chicken Sandwiches, Fries, and Sides & Other
- **Purchase Method Distribution**: Credit Card (80.7%), Cash (16.64%), Gift Card (2.67%)
- **Time Series Analysis**: Revenue and gross profit trends across 12 months
- **Dynamic Filtering**: Interactive product selection for detailed analysis

**Aggregate Metrics:**
- Total Revenue: $180M
- Total Gross Profit: $5M
- Total Quantity Sold: 32M units

## 🎯 Strategic Recommendations

Based on the dashboard insights:

1. **Security Enhancement**: Prioritize theft prevention measures in UK and Spain locations
2. **Market Expansion**: Leverage success factors from top-performing markets (Italy, Czech Republic, France)
3. **Demographic Targeting**: Develop marketing campaigns for 50+ demographic given their high revenue contribution
4. **Payment Innovation**: Capitalize on credit card dominance while exploring digital payment integrations
5. **Management Diversity**: Implement initiatives to improve gender balance in general manager positions
6. **Loss Prevention**: Focus on 20-29 age group with enhanced monitoring and staff training

## 🗂️ Data Model

The project utilizes a star schema with four main tables:

### Fact Tables
- **SaleTransactions**: Transaction-level sales data including product, price, quantity, costs, and revenue
- **Thefts**: Theft incidents with amounts, dates, and store locations

### Dimension Tables
- **StoreDetails**: Store information including location, manager demographics, and regional data
- **DateTable**: Time intelligence table for temporal analysis

### Lookup Table
- **Table**: Age group rankings for demographic segmentation

### Key Relationships
```
DateTable (1) ──→ (*) SaleTransactions
DateTable (1) ──→ (*) Thefts
StoreDetails (1) ──→ (*) SaleTransactions
StoreDetails (1) ──→ (*) Thefts
Table (1) ──→ (*) StoreDetails
```

## 🔧 Technical Implementation

### Data Preparation
- Data cleaning and standardization
- Date dimension creation with quarter and month hierarchies
- Age group segmentation and ranking

### DAX Calculations
```DAX
Rank = RELATED('Table'[Rank])
```

### Key Features
- **Conditional Formatting**: Visual indicators for performance thresholds (red bars for high theft amounts)
- **Interactive Slicers**: Product, country, and time-based filtering
- **Map Visualizations**: Geospatial analysis using Bing Maps integration
- **KPI Cards**: Key performance indicators with clear visual hierarchy
- **Drill-through Capabilities**: Navigate from overview to detailed country analysis

## 🛠️ Technologies Used

- **Power BI Desktop**: Dashboard development and visualization
- **DAX**: Data Analysis Expressions for calculated columns and measures
- **Power Query**: Data transformation and cleaning
- **Bing Maps**: Geographic visualization integration

## 📁 Project Structure
```
├── pbix/Data Model/Dashboard
│   └── Mc Donalds EU Dashboard.pbix
├── Data Sources/
│   ├── DateTable.csv
│   ├── SaleTransactions.csv
│   ├── StoreDetails.csv
│   ├── Table.csv
│   └── Thefts.csv
└── README.md
```

## 🚀 How to Use

1. Download the Power BI (.pbix) file
2. Open with Power BI Desktop (latest version recommended)
3. Refresh data connections if needed
4. Navigate between dashboard pages using the navigation buttons
5. Use slicers and filters to drill down into specific markets or time periods
6. Hover over visualizations for detailed tooltips
7. Click on map bubbles or table rows for cross-filtering

## 📊 Data Coverage

- **Countries**: 13 European markets (UK, Spain, France, Germany, Italy, Poland, Portugal, Hungary, Czech Republic, Slovakia, Croatia, Austria, Switzerland)
- **Time Period**: Full year of data (2021-2022)
- **Transactions**: 32M+ units sold
- **Stores**: 13 restaurant locations (one per country)
- **General Managers**: 13 store managers tracked with demographic data

## 🔍 Future Enhancements

- Real-time data integration via Power BI Service
- Predictive analytics for sales forecasting using ML models
- Mobile-optimized dashboard version for field managers
- Drill-through pages for individual store analysis
- Cost optimization recommendations engine
- Competitive benchmarking against industry standards
- Customer satisfaction score integration
- Employee performance metrics dashboard

## 📋 Next Steps

### Immediate Actions (1-2 Weeks)
- [ ] **Security Audit**: Conduct comprehensive security review of UK and Spain locations
- [ ] **Stakeholder Presentation**: Present dashboard findings to EU leadership team
- [ ] **Data Validation**: Verify theft data accuracy with local store managers
- [ ] **User Training**: Schedule Power BI training sessions for regional managers
- [ ] **Dashboard Deployment**: Publish dashboard to Power BI Service for organization-wide access

### Short-term Goals (1-3 Months)
- [ ] **Historical Data Integration**: Import 2-3 years of historical data for trend analysis
- [ ] **Automated Refresh**: Set up scheduled data refresh (daily/weekly)
- [ ] **Additional Metrics**: Incorporate labor costs, inventory turnover, and customer satisfaction scores
- [ ] **Store Manager Page**: Create dedicated page for individual store deep-dives
- [ ] **Alert System**: Implement automated alerts for abnormal theft patterns or revenue drops
- [ ] **Mobile App**: Deploy Power BI mobile app for on-the-go access

### Mid-term Objectives (3-6 Months)
- [ ] **Predictive Modeling**: Develop ML models for sales forecasting and demand prediction
- [ ] **Competitive Analysis**: Integrate market share and competitor data
- [ ] **Customer Segmentation**: Advanced RFM (Recency, Frequency, Monetary) analysis
- [ ] **Product Mix Optimization**: Analyze product performance by country and recommend menu adjustments
- [ ] **Diversity Initiative**: Launch management diversity program based on dashboard insights
- [ ] **API Integration**: Connect to point-of-sale systems for real-time data

### Long-term Vision (6-12 Months)
- [ ] **Enterprise Rollout**: Extend dashboard framework to global McDonald's operations
- [ ] **Advanced Analytics**: Implement AI-driven insights and recommendations
- [ ] **Supply Chain Integration**: Connect with inventory and supplier data
- [ ] **Customer Loyalty Program**: Integrate loyalty card data for personalized insights
- [ ] **Sustainability Metrics**: Add environmental and sustainability KPIs
- [ ] **Benchmarking Portal**: Create peer comparison capabilities across regions

### Continuous Improvement
- [ ] **Monthly Review Meetings**: Establish regular dashboard review cadence with stakeholders
- [ ] **User Feedback Loop**: Collect and implement user feedback for dashboard enhancements
- [ ] **Performance Monitoring**: Track dashboard usage and engagement metrics
- [ ] **Documentation Updates**: Maintain up-to-date user guides and technical documentation
- [ ] **Data Governance**: Ensure data quality, security, and compliance standards

### Success Metrics
Track the following KPIs to measure dashboard impact:
- Dashboard adoption rate (% of managers using weekly)
- Time saved on manual reporting (hours per month)
- Theft reduction in high-risk locations (% decrease)
- Revenue growth in underperforming markets (% increase)
- Decision-making speed improvement (days to action)

## 👤 Author

**European Store Analyst**  
McDonald's EU Division

## 📝 License

This project is proprietary and confidential. For internal McDonald's use only.

---

*"Make a dashboard to see how restaurants in Europe are performing"* - Manager

**Last Updated**: November 2025
