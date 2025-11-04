1. Project Overview
  The Paris 2024 Olympics Dashboard is an interactive Power BI project designed to analyze and visualize the performance of countries, athletes, and sports events in the 2024      Olympic Games.
  The goal is to transform raw sports performance data into meaningful insights for performance tracking, medal analysis, and country-wise comparison.

2. Objectives
  Analyze overall medal distribution across participating countries.
  Identify top-performing athletes and sports disciplines.
  Explore regional or continent-wise participation and performance trends.
  Enable interactive exploration of Olympic statistics using Power BI visuals.

3. Data Description
  Dataset Components:
  Country: Name of the participating nation
  Athlete: Athlete name and gender
  Sport / Event: Type of sport or discipline
  Medal Type: Gold, Silver, Bronze, or None
  Total Medals: Sum of medals won per athlete or country
  Continent / Region: Grouped by geography for global comparisons
  Data Source:
  Dataset imported from Excel or CSV and transformed in Power Query.

4. Data Cleaning & Transformation
  Performed in Power Query Editor:
  Standardized column names (Country, Medal, Event).
  Removed duplicates and invalid entries.
  Created calculated columns for:
  Total Medals per Country
  Medal Rank
  Medal Percentage Contribution
  Built relationships between tables (Countries, Sports, Athletes).

5. Dashboard Design
The dashboard was organized into three analytical views:
Page 1: Global Medal Overview
  KPIs: Total Medals, Golds, Silvers, Bronzes
  Visuals: Donut chart (medal share by type), stacked column (country ranking), KPI cards
Page 2: Country-Wise Insights
  Bar charts for top 10 countries by medals
  Slicers for continent, medal type, and sport
  Tooltip visuals showing country-specific medal breakdown
Page 3: Sport & Athlete Performance
  Table of top-performing athletes by medals
  Sports-wise medal trend chart
  Filterable visual to explore gender-based performance

6. DAX Measures Used
  Total Medals = COUNTROWS(Filtered Medal Table)
  Gold Medals = CALCULATE(COUNTROWS(Medals), Medals[Type] = "Gold")
  Silver Medals = CALCULATE(COUNTROWS(Medals), Medals[Type] = "Silver")
  Bronze Medals = CALCULATE(COUNTROWS(Medals), Medals[Type] = "Bronze")
  Medal Rank = RANKX(ALL(Medals[Country]), [Total Medals], , DESC)
  These measures enable dynamic ranking, filtering, and KPI visualizations in Power BI.

7. Key Insights
  The top 5 countries account for nearly 70% of total medals.
  Certain sports (e.g., athletics and swimming) dominate medal counts.
  A strong performance correlation was observed between participation rate and medal wins.
  Gender participation ratios improved compared to previous Olympics.

8. Business / Analytical Impact
  Enables stakeholders and sports analysts to track medal performance trends efficiently.
  Improves visibility into country, sport, and gender-based achievements.
  Facilitates historical comparison and strategic planning for future events.

9. Tools & Technologies
  Category	Tools Used
  Data Visualization	Power BI
  Data Cleaning	Power Query
  Data Modeling	DAX, Relationships
  Source Data	Excel / CSV
  Documentation	Markdown, PowerPoint

10. Author
  Vijay Kumar S G
  viji03662@gmail.com

11. Future Enhancements
  Add year-over-year analysis comparing multiple Olympics editions.
  Integrate interactive forecasting for future medal trends.
  Include athlete age, training data, and record-breaking statistics.
