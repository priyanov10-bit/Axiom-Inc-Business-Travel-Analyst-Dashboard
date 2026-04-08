# Axiom-Inc-Business-Travel-Analyst-Dashboard
As Finance Office Manager Ms. priya is responsible for both business travel budget approvals and employee travel audit tasks while establishing cost-control measures. To perform effectively in this role she must know all about travel costs together with booking behavior patterns and industry trends that help follow Axiom Inc.'s financial rules.
Business Intelligence
Axiom Inc, Business Travel Analyst Dashboard

1. User Requirements and Scenario
Company: Axiom Inc.
User: Finance Office Manager
Strategic Goals:
•	The system should maximize staff expenditure across airline options and fares types.
•	An organization should motivate customers to schedule appointments in advance since it generates discounts.
•	The evaluation of airline usage patterns supports corporate rate negotiations and helps contract better price agreements with airlines.
•	Managerial oversight of travel patterns through time enables better preparation of future policies and partnership development.
User Role:
As Finance Office Manager Ms. priya is responsible for both business travel budget approvals and employee travel audit tasks while establishing cost-control measures. To perform effectively in this role she must know all about travel costs together with booking behavior patterns and industry trends that help follow Axiom Inc.'s financial rules.
Selected KPIs:
KPI 1: Ticket Sales by Airline and Fare Type
•	The organization will aim to understand fare type expenditures throughout credit spreads to reveal expensive segments.
•	Total ticket cost divided by airline and fare type classification include Economy and First Class among others.
•	Measurement: SUM(Ticket Price) per Airline and Fare Type
•	This metric reveals which airlines together with their fare types consume the most budget due to its importance.
KPI 2: Total Travel Cost by Airline
•	Strategic Goal: Track and compare airline-wise cost allocation
•	The variable sums the total costs of tickets which are organized based on airlines.
•	Measurement: SUM(Ticket Price) per Airline
•	The identification of high-cost airlines serves as an essential purpose because it allows organizations to focus their cost reduction efforts and renegotiation attempts on these carriers.
KPI 3: Average Lead Time per Airline
•	The strategic goal aims to encourage early booking periods in order to decrease expenses.
•	Definition: Average number of days between ticket purchase and travel date
•	The Airline-specific measurement consists of AVG(DATEDIFF('day', [Purchase Date], [Travel Date])).
•	The ratio demonstrates if employees make their bookings before or after the deadline
KPI 4: Ticket Sales Trends by Airline (2016-2019)
•	Strategic Goal: Detect historical trends in employee airline usage
•	The ticketer tracks the yearly ticket sales according to airline types.
•	Measurement: Number of records(Bookings) by Airline and Year
•	Evaluation of historical airline choices provides data that can help planning strategies for the future.
2. Data Preparation in Tableau Prep Builder
Files Used:
•	Employee_airline_travel.xls
•	Oceanic2016.csv, Oceanic2017.csv, Oceanic2018.csv, Oceanic2019.csv
•	US_Airports.hyper (used later in Tableau Desktop)
Data Preparation Steps:
 
Combine Data:
  - Union 1: Merge Oceanic_2016.csv and Oceanic_2017.csv.
  - Union 5: Add Union 1  and Union3 result.
  - Union 3: Merge Oceanic_2019.csv with Oceanic_2018.csv.
  - Union 7: Combine Union 5 and employee flights.xlsx

Clean Data:
  - Clean 1: Fix inconsistencies in Union 5 result.
  - Clean 2: Fix Employee_airline_transfers.xlsx before Union 3.
  - Clean 3: Fix Union 7 result.
  - Clean 5: Final cleanup after joining.

Transform Data:
  - Extract: Pull data from US_Airports_hypermart_extract.
  - Clean 4: Fix extracted US_Airports_hypermart_extract data.

- Join Data:
  - Join 1: Combine Clean 3 result with Clean 4 result.

- Export:
  - Saved final cleaned and joined data as output.
Screenshot of Tableau Prep Flow:
 

3. Dashboard Design and Visualisation Strategy
Approach: Hybrid (Explanatory + Exploratory)
The dashboard is designed to allow both high-level summaries and deep-dive filtering by Fare Type, Airline, and Year. Each visual supports strategic questions relevant to the Finance Office Manager.
Visual Components:
•	Bar Chart (KPI 1): Ticket sales by airline and fare type, highlighting revenue contribution by cabin class
•	Bar Chart (KPI 2): Total cost per airline, to visualize cost concentration
•	Bar Chart (KPI 3): Average lead time per airline, used to detect booking behavior patterns
•	Line Chart (KPI 4): Ticket trends from 2016 to 2019 per airline, identifying changes in usage
Interactivity:
•	Filters: Year, Fare Type, Airline
•	Highlight actions: Clicking a bar filters related views
•	Tooltip popups show precise values and KPI breakdowns
Design Elements:
•	Consistent color palette (economy vs. first class)
•	Horizontal and vertical containers used for clean layout
•	Labels and axis titles improved for clarity
Screenshot of Final Dashboard:
 

4. Insights and Recommendations
•	Economy tickets account for 45% of total spend on some airlines.
•	American Airlines had the highest total cost, followed closely by Delta Airlines
•	Over 30% of bookings are made with less than 3 days lead time, leading to higher costs
•	American Airlines saw the largest year-on-year growth in ticket count from 2016 to 2019
Recommendations:
•	Encourage employees to book at least 7 days in advance
•	Review corporate contracts with high-cost airlines
•	Introduce fare type restrictions for short-haul travel
•	Focus negotiations on airlines with increasing use year-on-year


