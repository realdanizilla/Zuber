# Zuber Ride Analysis

## Table of Contents
- [Zuber Ride Analysis](#zuber-ride-analysis)
  - [Table of Contents](#table-of-contents)
  - [Project Objective](#project-objective)
  - [Project Structure](#project-structure)
  - [Tools and Techniques Utilized:](#tools-and-techniques-utilized)
  - [Specific Results and Outcomes](#specific-results-and-outcomes)
  - [What I Have Learned from This Project](#what-i-have-learned-from-this-project)


## Project Objective

This project aims to analyze and identify patterns in the available data for Zuber, a ride-sharing company launching in Chicago. The goal is to understand passenger preferences and the impact of external factors, such as weather, on rides. The project involves working with a database of taxi rides and weather data to test hypotheses and extract actionable insights.

[back to top](#zuber-ride-analysis)

## Project Structure

1. **Data Exploration and Import**
- **Objective**: Understand the data schema and import the necessary files.
- **Actions Taken:**
  - Reviewed the schema of the taxi rides and weather data, which included tables for neighborhoods, cabs, trips, and weather_records.
  - Imported CSV files containing key data: project_sql_result_01.csv for taxi companies and rides, project_sql_result_04.csv for average trips by neighborhood, and project_sql_result_07.csv for trip duration and weather conditions.
- **Outcome**: Ensured that the data was correctly imported and explored for any potential inconsistencies or areas requiring cleaning.

2. **Data Cleaning and Preparation**
- **Objective**: Ensure the dataset is ready for analysis by handling missing values, incorrect data types, and other issues.
- **Actions Taken**:
  - Checked each column for missing values and corrected or filled in these values where necessary.
  - Converted columns to their correct data types (e.g., timestamps, numeric fields).
  - Merged tables where necessary, particularly trips and weather_records, based on the start time of the trip and weather records.
- **Outcome**: A clean, merged dataset was prepared for further analysis and visualization.

3. **Exploratory Data Analysis (EDA)**
- **Objective**: Analyze trends, identify patterns, and visualize the data to gain insights into ride behavior.
- **Actions Taken**:
  - **Company Analysis:**
    - Counted the number of taxi rides for each company over specific dates to understand their market share.
    - Aggregated ride counts for companies with "Yellow" or "Blue" in their names for a comparative analysis.
    - Identified the most popular taxi companies for November 2017, such as Flash Cab and Taxi Affiliation Services, and grouped all other companies as "Other."

  - **Neighborhood Analysis:**
    - Analyzed the top 10 neighborhoods in Chicago where rides ended, based on average trips.
    - Visualized the drop-off locations and compared the distribution of trips across neighborhoods.
- **Outcome**: Provided insights into which taxi companies had the most rides and which neighborhoods were the most popular drop-off points, laying the groundwork for further hypothesis testing.

4. **Weather and Ride Duration Analysis**
- **Objective**: Investigate the relationship between weather conditions and ride duration.
- **Actions Taken:**
  - **Classify Weather Conditions:**
    - Retrieved weather records for each hour, categorizing weather as "Bad" if the description contained "rain" or "storm," and as "Good" otherwise.
  - **Trip Duration and Weather Analysis:**
    - Filtered the dataset to analyze only rides starting in the Loop neighborhood and ending at O'Hare Airport.
    - Linked these trips with weather conditions to see how rainy weather affected ride durations on Saturdays.

- **Outcome**: The merged data allowed for a deeper understanding of how external factors like weather could impact the ride-sharing experience.

5. **Visualizations**
- **Objective**: Create meaningful visualizations to represent data findings.
- **Actions Taken**:
  - Plotted graphs showing the number of rides per company to identify market leaders and compare their performance.
  - Created bar charts and histograms to display the distribution of rides across neighborhoods.
  - Developed scatter plots and line graphs to examine the impact of weather conditions on ride durations.
- **Outcome**: Visualizations helped communicate the data trends clearly and supported the decision-making process.

6. **Hypothesis Testing**
- **Objective**: Test whether weather conditions significantly impact the duration of taxi rides.
- Actions Taken:
  - Hypothesis Testing for Ride Duration:
  - Formulated null and alternative hypotheses to test whether the average duration of rides from the Loop to O'Hare Airport changes on rainy Saturdays.
  - Used appropriate statistical tests (e.g., t-test or Mann-Whitney U test) based on the distribution and normality of the data.
  - Set an alpha level (commonly 0.05) to determine the significance of the test results.
- **Outcome**: The hypothesis test revealed the extent to which weather conditions affect ride durations, providing insights into ride-sharing behavior during different weather scenarios.

[back to top](#zuber-ride-analysis)

## Tools and Techniques Utilized:

- SQL: To query and analyze taxi and weather data, identifying ride patterns and correlations.
- Pandas and NumPy: For data manipulation, cleaning, and transformations.
- Matplotlib and Seaborn: For visualizing data trends, distributions, and relationships.
- Scipy: For statistical analysis and hypothesis testing.
- Beautiful Soup: Utilized for web scraping to retrieve weather data for Chicago in November 2017 from HTML pages. This allowed for further analysis on the impact of weather conditions on ride patterns.

[back to top](#zuber-ride-analysis)

## Specific Results and Outcomes

**Taxi Company Analysis**
- Top Companies for Rides:
  - Flash Cab and Taxi Affiliation Services were found to be the most popular taxi companies in Chicago during November 2017.
  - Flash Cab had the highest number of trips over a two-day period, with a significant gap compared to other companies.
- Companies with "Yellow" or "Blue" in Their Name:
  - Analysis focused on companies with "Yellow" and "Blue" in their names, revealing that these companies accounted for a substantial portion of rides between November 1-7, 2017.
  - This provided insight into branding and ride preferences, showing that taxis branded with colors may have different customer perceptions or market niches.

- Market Share:
  - When grouping all companies except the top two (Flash Cab and Taxi Affiliation Services) as "Other," Flash Cab still led in market share, indicating a possible monopoly or strong brand preference in the taxi market.

**Neighborhood Ride Patterns**
- Top Drop-Off Neighborhoods:
  - Loop, River North, and Streeterville were among the top neighborhoods for ride drop-offs, making them key areas of demand in Chicago.
  - Loop had the highest average drop-offs in November 2017, suggesting that it is a central hub for taxi services, likely due to its commercial and business activity.

- Visualization of Demand:
  - The top 10 neighborhoods showed a clear trend: central areas with business and entertainment activities received more rides compared to residential or outlying neighborhoods.
- Average Trips per Neighborhood:
  - A chart of the average number of trips highlighted that certain neighborhoods consistently receive a high volume of drop-offs, indicating consistent demand throughout November.

**Analysis of Weather Impact on Ride Duration**
- Correlation Between Weather and Rides:
  - Bad weather conditions (e.g., rain or storms) showed a slight increase in ride duration for trips from the Loop to O'Hare International Airport.
- Ride Duration on Saturdays:
  - For Saturdays, ride duration showed some variability when comparing rainy vs. non-rainy conditions, indicating that weather could affect traffic and road conditions, thus extending trip times.
- Hypothesis Testing:
  - The hypothesis test revealed that ride durations were, in fact, longer on rainy Saturdays, indicating that weather does have a statistically significant impact on ride duration. However, the effect size was not very large, implying that while weather impacts ride times, it may not be the only contributing factor.

**Rides by Taxi Company and Neighborhood**
- Flash Cab Dominance:
  - Flash Cab led in the number of rides over a selected two-day period in November, followed closely by Taxi Affiliation Services. Other companies had significantly fewer trips, suggesting strong competition between these two major players.
- Neighborhood Analysis & Popularity:
  - Central business and tourist neighborhoods such as Loop, Near North Side, and River North received the highest number of trips, making them focal points for Zuber to target high demand.

- Consistency of Ride Demand:
  - Most neighborhoods with high drop-off rates had consistent demand throughout November, with very little fluctuation, suggesting stable market demand in these areas.

**Duration Analysis from Loop to O'Hare**
- Trips Duration Consistency:
  - For trips from Loop to O'Hare, average ride durations varied depending on the time of day and weather conditions.
  - On rainy days, rides took slightly longer, which is crucial for estimating travel time for passengers traveling to the airport.

- Analysis of Duration Trends:
  - The average duration of rides from Loop to O'Hare was around 45-55 minutes on non-rainy Saturdays, while on rainy Saturdays, the duration increased to around 55-65 minutes.

**Data Visualization Insights**
- Ride Count by Taxi Company:
  - Bar charts revealed the dominance of Flash Cab and Taxi Affiliation Services over other smaller companies.
- Neighborhood Drop-off Visualization:
  - Bar charts of the top 10 neighborhoods showed clear hotspots of activity where Zuber could concentrate its services.
- Impact of Weather on Ride Duration:
  - Visualizations like boxplots and scatter plots highlighted the difference in ride duration based on weather conditions, clearly showing the impact of rainy weather on extending ride times.

[back to top](#zuber-ride-analysis)

**Key Recommendations for Zuber**
- **Focus on High-Demand Neighborhoods**: Target high-demand neighborhoods like Loop, Near North Side, and River North for ride-sharing services, as they are popular drop-off destinations.
- **Prepare for Weather Variations**: Since ride durations are affected by weather, Zuber can develop strategies like surge pricing, optimized routing, and alerts to customers for better service during adverse weather conditions.
-**Compete with Market Leaders**: Understand the strong market presence of Flash Cab and Taxi Affiliation Services. Zuber should aim to compete on price, service quality, or availability to gain market share in Chicago.
- **Monitor Ride Duration to O'Hare**: Since O'Hare is a popular destination, Zuber can ensure accurate estimated times for airport trips and develop marketing strategies to target passengers traveling from central neighborhoods to the airport.

[back to top](#zuber-ride-analysis)

## What I Have Learned from This Project

- **Data Manipulation and Cleaning**: Gained experience in handling real-world data, including dealing with missing values, data type conversions, and rounding numerical values for analysis.
- **SQL Proficiency**: Improved ability to query large datasets, filter data based on conditions, and perform joins across multiple tables to derive insights.
- **Hypothesis Testing**: Developed skills in forming null and alternative hypotheses, determining appropriate significance levels (alpha), and using statistical methods to test hypotheses.
- **Data Visualization**: Enhanced skills in creating meaningful visualizations that illustrate trends and comparisons across different datasets (e.g., taxi company rides and neighborhood drop-off counts).
- **Exploratory Data Analysis (EDA)**: Applied EDA techniques to uncover patterns in data, understand distributions, and make data-driven decisions.

[back to top](#zuber-ride-analysis)