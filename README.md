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


# Executive Summary

### Overview of Findings

This analysis reveals the urgent need for smarter wildfire prevention strategies in Canada. Although the Northwest Territories experienced the highest area burned, British Columbia faced the most wildfire incidents—over 60,000—resulting in the highest financial losses, even from smaller fires. Across the country, nearly half of all wildfires were caused by human activities, particularly during the high-risk months of May through July.

Additionally, commercial forestry has been significantly affected, with nearly 7 million hectares of commercial wood supply lost to wildfires. Many of these losses occurred in Quebec, Ontario, and British Columbia, stressing the need for better harvesting and supply chain planning.

By analyzing historical fire data alongside seasonal and geographic patterns, this project supports the development of prevention strategies focused on regulation, public awareness, and readiness ahead of the summer fire season.

  <img width="517" alt="image" src="https://github.com/user-attachments/assets/f945d3bf-a822-4dd8-8914-3f895879986d" /> <img width="442" alt="image" src="https://github.com/user-attachments/assets/bf329697-dcbc-42e7-af4c-e22614b95c78" />


# Insights Deep Dive

### Fire Frequency & Regional Impact

* **British Columbia had the highest number of wildfire incidents**, with over 60,000 fires reported historically. Alberta followed with approximately 42,000 fires. This highlights a need for sustained fire prevention and preparedness in these provinces.

* **The Northwest Territories experienced the largest area burned**, with 18.91 million acres impacted, followed by Saskatchewan with 15.97 million acres. Fires in these regions tend to be large in size and harder to contain due to their remote nature.

* **Smaller fires are more frequent but contribute significantly to costs**, especially in populated regions like British Columbia and Ontario. This indicates that even low-scale incidents can create high fiscal burdens if not managed early.

* **Fire activity is not evenly distributed across provinces**, suggesting that localized strategies are required, rather than a one-size-fits-all approach.

   <img width="691" alt="image" src="https://github.com/user-attachments/assets/2a882eab-ec1c-4964-9dad-cecb1f8ab77d" />








### Economic and Environmental Impact

* **Over $119 million in wildfire damages were recorded in British Columbia**, driven largely by high fire frequency and response costs. Ontario also faced major economic losses, even though it had fewer fires overall.

* **Wildfires have destroyed approximately 7 million hectares of commercial wood supply**, directly affecting the forestry economy. Quebec and Ontario lost 2 million hectares each, and British Columbia lost 1 million hectares.

* **Wildfires cause significant disruption to communities**, leading to evacuations, property loss, and interruptions to local economies—particularly in fire-prone rural and semi-urban regions.

* **Environmental degradation from wildfires impacts biodiversity and public health**, especially through air pollution, water contamination, and habitat loss.

  <img width="331" alt="image" src="https://github.com/user-attachments/assets/12ddafda-4188-4352-9743-16771d7f47af" />     <img width="332" alt="image" src="https://github.com/user-attachments/assets/49c33c94-2660-4c0a-af90-fe3c195cf261" />  ![image](https://github.com/user-attachments/assets/af86df1a-2300-4efa-9b99-5b26e9e14a19)






### Human Causes & Policy Gaps

* **48% of all wildfires (111,447 out of 228,402) were caused by human activities**, making human behavior one of the most controllable factors in wildfire prevention.

* **Most human-caused fires occur during the early fire season**, indicating a need for heightened awareness and enforcement in spring and early summer months.

* **Current regulations may not be sufficient to reduce risky behavior**, such as open fires, careless smoking, or recreational negligence in forested areas.

* **Prevention strategies like responsible recreation, designated fire-safe zones, and public education campaigns could drastically reduce fire frequency.**

  <img width="565" alt="image" src="https://github.com/user-attachments/assets/977e57bd-f01d-4241-a55b-811a306e235c" />



### Seasonal Trends & Risk Mitigation

* **Fire activity peaks in May, June, and July**, which together account for over 130,000 fire incidents and more than 62 million hectares burned. This calls for pre-summer preparation strategies.

* **Early hazard assessments and community preparedness can reduce impact**, especially in high-risk zones identified from historical data.

* **Strict fire bans and responsive mobilization during peak months are critical**, particularly in provinces like Alberta, BC, and Saskatchewan.

* **Global best practices such as Australia’s Lightning Detection Network and Mediterranean fire-resistant vegetation offer promising models** that could be adapted for Canada’s needs, especially in lightning-prone regions like the Northwest Territories.

  <img width="537" alt="image" src="https://github.com/user-attachments/assets/0c359112-c2ec-4da0-9821-2cbc47aaaab7" />





