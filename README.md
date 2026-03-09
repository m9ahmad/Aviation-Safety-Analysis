# Airplane Crash Data Analysis Since 1908

> Add blockquote



## Project Overview
This project performs an exploratory data analysis (EDA) on airplane crash data since 1908 to uncover patterns, risks, and trends over time. The analysis covers various aspects, including survivability rates, common causes of accidents, operator performance, and third-party risks.

## Data Source
The dataset used for this analysis is `Airplane_Crashes_and_Fatalities_Since_1908_20190820105639.csv`, downloaded from KaggleHub. It contains detailed records of aviation incidents, including date, location, operator, aircraft type, and fatality counts.

## Key Analyses and Findings

### 1. Data Loading and Initial Inspection
- The raw CSV data was loaded into a pandas DataFrame.
- Initial inspection revealed columns such as 'Date', 'Time', 'Location', 'Operator', 'AC Type', 'Fatalities', and 'Aboard'.

### 2. Survivability Rate Calculation
- A new column, `Survival_Rate`, was calculated as `(Aboard - Fatalities) / Aboard` to provide a more insightful metric than raw counts.

### 3. Crew vs. Passenger Risk Analysis
- Analyzed average 'Fatalities Crew' and 'Fatalities Passangers' by 'AC Type' to determine relative risks.
- **Finding**: Certain AC Types showed discrepancies, with some exhibiting higher crew fatality rates compared to passenger fatality rates (e.g., Hawker Siddeley HS-125).

### 4. Temporal Risk: Accidents in 2019 ('The Safety Paradox')
- 'Year' and 'Month' were extracted from the 'Date' column.
- Analysis focused on 2019 to investigate if accidents are decreasing in frequency but increasing in 'Mass Fatality' potential.
- **Finding**: While the total number of accidents in 2019 was relatively low (9 incidents), a significant proportion (6 out of 9) were mass fatality events (>=10 fatalities), notably including the Boeing 737 Max 8 crash, supporting the 'Mass Fatality' potential aspect of 'The Safety Paradox'.

### 5. Keyword Extraction from Summaries ('The Why')
- Top trigrams (3-word phrases) were extracted from the 'Summary' column using `CountVectorizer` and NLTK stopwords.
- **Finding**: Common themes identified included 'cargo plane crashed', 'poor weather conditions', 'adverse weather conditions', and 'make emergency landing', indicating prevalent causes and scenarios.

### 6. Third-Party Risk (Ground Fatalities)
- Incidents causing fatalities to people not on the plane (`Ground` column) were analyzed.
- **Finding**: 242 incidents resulted in ground fatalities, totaling 8513. The highest ground fatalities were tragically linked to the 9/11 attacks in New York City and Arlington, highlighting severe third-party risks in urban areas.

### 7. Decadal Trends in Fatalities-to-Aboard Ratio
- A 'Decade' column was created, and the 'Fatalities-to-Aboard Ratio' was calculated for each decade.
- **Finding**: The ratio showed high fatality rates in early aviation, a gradual decline through the mid-20th century (lowest in the 1980s-1990s), and a slight increase in the 2000s-2010s, reflecting improvements but also the impact of high-casualty events in recent times.

### 8. Operator vs. Incident Type Heatmap ('Competitive Intelligence')
- Top 20 operators were identified, and their incident summaries were analyzed for keywords like 'Engine', 'Weather', 'Pilot', and 'Landing/Takeoff'.
- A heatmap was generated to visualize the frequency of these incident types per operator.
- **Finding**: Aeroflot showed notably higher frequencies across all analyzed incident types (Engine, Weather, Pilot, Landing) compared to other top operators, providing insights into operator-specific risk profiles.

### 9. Aircraft Types with Lowest Survivability Rates
- Mean `Fatalities / Aboard` (Fatality Rate Per Incident) was calculated for AC Types with more than 10 incidents.
- **Finding**: Several older or specialized aircraft types (e.g., De Havilland DH-4, Breguet 14, various Curtiss and Douglas variants, Mil Mi-8 helicopter) exhibited very high average fatality rates, suggesting inherent risks or challenging operational contexts.

### 10. Crew vs. Passenger Fatality Rate Scatter Plot
- An interactive Plotly scatter plot was created to compare `Crew_Fatality_Rate` against `Passenger_Fatality_Rate` by AC Type.
- **Finding**: The plot visually highlights aircraft types where one group (crew or passengers) is statistically more protected or at higher risk than the other, deviating from the 1:1 diagonal line. This can indicate specific vulnerabilities or design considerations related to survivability for different roles aboard an aircraft.
