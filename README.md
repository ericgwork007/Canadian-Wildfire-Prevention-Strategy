# Canadian-Wildfire-Prevention-Strategy
This is a dashboard that visualizes Canadian wildfire data extracted from the National Forestry Database.

# Project Background

As part of my portfolio, I explored wildfire prevention strategies in Canada using data from the **National Forestry Database (NFD)**.

The NFD is Canada’s central source of forest management data. It is managed by the Canadian Forest Service (CFS) under Natural Resources Canada, with oversight from the Canadian Council of Forest Ministers (CCFM). The database brings together information from provincial, territorial, and federal resource management organizations to track how forests are managed and how policies affect forest resources across the country.

I approached this project from the perspective of a data analyst working with Natural Resources Canada. My goal was to use historical wildfire and forestry data to identify patterns, understand wildfire risks across different regions, and suggest practical strategies that could help prevent wildfires or minimize their impact.

Insights and recommendations are provided on the following key areas:

- **Wildfire Occurrence Patterns**  
- **Forest Area Burned Trends**  
- **Fire Suppression Costs**  
- **Prevention Strategy Optimization**

An interactive PowerBI dashboard that visualizes wildfire trends and supports decision-making can be found here: <a href = "https://app.powerbi.com/view?r=eyJrIjoiM2Y4NmE3NTMtZjFhZi00MmY1LTkyYTctODMzODYwNjEwZGM0IiwidCI6IjgyOTllMzkwLWI3MjItNDQ2NS1hMmYyLTc2YzlhMzc4NzI3MCJ9">[Link]</a>


# Data Structure & Initial Checks

To begin the analysis, I worked with multiple datasets from the **National Forestry Database** related to wildfires, forest management, and wood supply in Canada. These datasets capture both operational statistics and long-term trends across provinces and territories.

The core of my data model includes the following fact tables:

- **Property losses from fires (in dollars)**  
- **Area burned by fire size class**  
- **Area burned by cause class**  
- **Number of fires by fire size class**  
- **Number of fires by cause class**  
- **Area burned by month**  
- **Number of fires by month**  
- **Wood supply estimates by ownership**  
- **Area harvested by ownership and harvesting methods**  
- **Net merchantable volume of roundwood harvested by category and ownership**

  <img width="652" alt="image" src="https://github.com/user-attachments/assets/41dc61b7-9be8-4deb-b268-00e39fb7ce0d" />


To improve performance and create a cleaner analytical model, I used Power BI’s Power Query Editor to extract and normalize key attributes into separate **dimension tables**, each connected to the main fact tables using numeric surrogate keys. This dimensional modelling allowed me to build a **star schema**, making the model easier to query and more efficient for aggregations and dashboard visualizations.

The dimension tables I created include:

- **Geography** (Province or Territory)  
- **Year**  
- **Month**  
- **Cause of Fire**  
- **Fire Size Class**

This structure helped standardize repeated fields across different datasets and made the data model more scalable. Initial checks involved verifying data consistency across time periods, ensuring there were no missing or duplicate records in key fields, and cleaning column names for better readability.
