# Exploration-of-The-Data-Finding-Patterns-Trends-Regarding-Chipotle-Telelink-locations
This project focuses on understanding customer churn for Telelink by analyzing trends in cities with and without Chipotle locations. 

. Data was prepared using PostgreSQL (pgAdmin) to clean and combine datasets, while Tableau was used to create interactive visualizations. 
The dashboard highlights churn rates, customer demographics, and income levels, providing actionable insights for stakeholders to develop targeted 
marketing strategies and improve retention. This analysis demonstrates how data visualization and SQL-based preparation can uncover meaningful
patterns to drive decision-making.

SQL code or other code supporting the dashboard
● To Create Table
■ CREATE TABLE chipotle_locations(
states VARCHAR,state VARCHAR,location VARCHAR,address VARCHAR,
latitude NUMERIC,longitude NUMERIC
● To import the dataset
■ Right Click on the chipotle_locations table and click on import/export.
--command " "\\copy public.chipotle_locations (states, state, location, address, latitude, longitude) FROM 'C:/Users/LabUser/DOWNLO~1/CHIPOT~1.CSV' DELIMITER ',' CSV HEADER QUOTE '\"' ESCAPE '''';""
● Make sure columns exist
■ SELECT *
FROM customer LIMIT 10;
■ SELECT *
FROM chipotle_locations LIMIT 10;
■ SELECT *
FROM location LIMIT 10;
● Check Count
■ SELECT COUNT (*)
FROM chipotle_locations;
■ SELECT COUNT (*)
FROM customer;
■ SELECT COUNT (*)
FROM location;
● Create Calculated Fields on Tableau
■ Chipotle City Exists
● [Location] THEN “Has Chipotle” ELSE “ No Chipotle” END
■ AVGage
● AVG ([Age])
■ Avg Churn
● AVG(IF [Churn]=’Yes’ THEN 1 ELSE 0 END)
■ Income segments
● IF [Age]<30 AND [Income]<50000 THEN “ Young & Low
Income”
     
Part 2: Demonstration
ELSEIF [Age]<30 AND [Income]>=50000 THEN “Young & High Income”
ELSEIF [Age]>=30 AND [Income]<50000 THEN “ Middle-aged & Low Income”
ELSEIF [Age]>=30 AND [Income]>=50000 THEN “ Middle-aged & High Income” END


4. SQL code or other code supporting the dashboard
● To Create Table
■ CREATE TABLE chipotle_locations(
states VARCHAR,state VARCHAR,location VARCHAR,address VARCHAR,
latitude NUMERIC,longitude NUMERIC
● To import the dataset
■ Right Click on the chipotle_locations table and click on import/export.
--command " "\\copy public.chipotle_locations (states, state, location, address, latitude, longitude) FROM 'C:/Users/LabUser/DOWNLO~1/CHIPOT~1.CSV' DELIMITER ',' CSV HEADER QUOTE '\"' ESCAPE '''';""
● Make sure columns exist
■ SELECT *
FROM customer LIMIT 10;
■ SELECT *
FROM chipotle_locations LIMIT 10;
■ SELECT *
FROM location LIMIT 10;
● Check Count
■ SELECT COUNT (*)
FROM chipotle_locations;
■ SELECT COUNT (*)
FROM customer;
■ SELECT COUNT (*)
FROM location;
● Create Calculated Fields on Tableau
■ Chipotle City Exists
● [Location] THEN “Has Chipotle” ELSE “ No Chipotle” END
■ AVGage
● AVG ([Age])
■ Avg Churn
● AVG(IF [Churn]=’Yes’ THEN 1 ELSE 0 END)
■ Income segments
● IF [Age]<30 AND [Income]<50000 THEN “ Young & Low
Income”
     
 Part 2: Demonstration
ELSEIF [Age]<30 AND [Income]>=50000 THEN “Young & High Income”
ELSEIF [Age]>=30 AND [Income]<50000 THEN “ Middle-aged & Low Income”
ELSEIF [Age]>=30 AND [Income]>=50000 THEN “ Middle-aged & High Income” END
B.https://wgu.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=a7756d0f-de58-42e8-bfcf -b1e901554506
Part 3: Report
C. Exploration of the data
1. My goal was to bring awareness to the Telelink stakeholders in understanding
customer churn in regards to Chipotle locations. I achieved this by finding patterns and trends that could help with brainstorming any marketing strategies. The Tableau dashboard includes visuals of churn rates in cities with and without Chipotle locations, customer details, and income levels. The visuals I have included such as pie charts, bar charts help stakeholders make decisions based on the data shown to reduce churn.
2. I chose Tableau for this project because it is a user-friendly tool that allows for easy data visualization. Tableau’s interactive features make it easy to explore different aspects of the data as well.
3. Explain the steps used to clean and prepare the data for the analysis.
To prepare for my dashboard, I decided to use pgAdmin because it is a great tool for managing and querying PostgreSQL databases. It allows you to write SQL queries, which is needed for preparing and cleaning the data before analysis. Additionally, it makes it possible to combine multiple datasets and perform detailed analysis, making it a strong complement to Tableau for data visualization.
  1.
2.
Table Creation:
a. Created a new table in PostgreSQL to hold the Chipotle locations data with the following command, using the query tool:
i. CREATE TABLE chipotle_locations(states VARCHAR,state VARCHAR,location VARCHAR,address VARCHAR,latitude NUMERIC,longitude NUMERIC);
Data Import:

 a. Imported the dataset into the newly created table using the COPY command
i. \copy public.chipotle_locations (states, state, location, address, latitude, longitude) FROM 'C:/Users/LabUser/DOWNLO~1/CHIPOT~1.CSV' DELIMITER ',' CSV HEADER QUOTE '\"' ESCAPE '''';
3. Verification:
a. Checked that the columns existed and data was correctly imported by previewing a sample of the data:
i. SELECT * FROM customer LIMIT 10;
ii. SELECT * FROM chipotle_locations LIMIT 10;
iii. SELECT * FROM location LIMIT 10;
4. Data Validation:
a. Checked the total number of records in each table to ensure completeness:
i. SELECT COUNT(*) FROM chipotle_locations;
ii. SELECT COUNT(*) FROM customer;
iii. SELECT COUNT(*) FROM location;
5. Handling Null Values:
a. I ensured there were no null values to maintain data integrity.
b. To ensure data integrity, I used pgAdmin to check for NULL values. I
opened the table view and used the filter icon to identify any NULL values present in the columns.
6. Transition to Tableau:
a. After preparing the data in pgAdmin, I imported the datasets into Tableau for visualization and further analysis.
4. Summarize the steps used to create the dashboard.
➔ Step 1: Import Data into Tableau: I connected Tableau to the datasets by
importing the tables from PostgreSQL, including customer, location, and
chipotle_locations.
➔ Step2:JoinDataSources:Tojointhedata,Iperformedtablejoinswithin
Tableau. I connected the customer table to the location table and the location

 table to the chipotle_locations table using relevant fields such as Location Id,
and City( chipotles city column named under Location).
➔ Step3:CreateVisualizations:Icreatedvariousvisualizationstoanalyzeand better understand the data.This included maps showing customer and Chipotle locations, bar charts depicting churn rates, pie charts of customer demographics such as gender, and other visuals for average age and income segments. I also thought it was important to include the avg age, avg income,avg churn and income segments to analyze the data with more depth.
➔ Step4:DesignDashboards:Iorganizedthevisualizationsintodashboards. Each dashboard focused on different aspects of the data, such as churn rates, customer demographics, and income analysis. I ensured that the dashboards were interactive and easy to navigate.
➔ Step5:AddFilters:Iaddedfiltersandinteractiveelementstothedashboards, allowing users to explore different parts of the data and view important details based on their selections.Additionally, I implemented the colorblind option to improve accessibility.
➔ Step6:Story:Afterfinalizingthedashboards,Icreatedthestoryandsavedmy workbook to my desktop.
5. The analysis revealed that Telelink customers are spread across the United States, including Alaska, Hawaii, and Puerto Rico. However, Chipotle locations are only present on the mainland U.S., with no representation in Alaska, Hawaii, or Puerto Rico. This could impact marketing strategies.
Analysis Results
● Churn Rates: Telelink customers in cities without Chipotle locations had
an average churn rate of 0.266, while in cities with Chipotle, the churn rate was slightly lower at 0.260. This shows a minor difference in customer churn between these areas. Overall, 2,650 customers churned in the US, while 7,350 did not.
● Gender Distribution: There were slightly more female Telelink customers than males in cities with Chipotle locations. The count was 1,382 females and 1,313 males, with a few customers not specifying their gender. Specifically, 169 customers who didn't answer the gender question were from cities without Chipotle, while 62 were from cities with Chipotle.
● Age: The average age of Telelink customers in cities without Chipotle was 53 years old, compared to 52 years in cities where Chipotle is present.
 
● Income: The average income in cities where Chipotle exists was $40,000, slightly higher than the $39,000 average in cities without Chipotle locations.
● Customer Segments: The largest customer segment for Telelink was middle-aged, low-income customers, followed by middle-aged, high-income, then young, low-income, and lastly, young, high-income.
These results support the dashboard's purpose by offering a broad view of how customer churn, demographics, and income levels relate to where Chipotle locations are. The data shows that there are small differences in churn rates and customer details between cities with and without Chipotle. But this information can still help create strategies to keep more customers, especially middle-aged, low-income customers, who are the biggest group.
6. Discuss the limitation(s) of your data analysis:
The analysis may show patterns, but it doesn't necessarily prove that one factor causes another. For example, just because churn rates are lower in cities with Chipotle, it doesn't mean Chipotle directly impacts churn.
The data for chipotle also does not include certain regions like Alaska, Hawaii, and Puerto Rico, which limits your ability to analyze customer behavior in those areas.
The analysis shows us the current situation but doesn't consider how future changes, like new Chipotle locations or shifts in customer demographics, could affect churn rates.
The analysis provides insights for enhancing customer satisfaction. For example, it suggests focusing on middle-aged, low-income customers who represent a significant segment. Additionally, developing age-specific products or tailored advertising strategies could further improve engagement and satisfaction.


Create a Dashboard. Tableau. (n.d.). https://help.tableau.com/current/pro/desktop/en-gb/dashboards_create.htm
GeeksforGeeks. (2022, October 2). How to create a story in tableau? http://www.geeksforgeeks.org/how-to-create-a-story-in-tableau
Import/Export Data dialog¶. Import/Export Data Dialog - pgAdmin 4 8.11 documentation. (n.d.). https://www.pgadmin.org/docs/pgadmin4/development/import_export_data.html



Braun, J. (2020, July 28). Chipotle locations. Kaggle. https://www.kaggle.com/datasets/jeffreybraun/chipotle-locations/data
Codecademy. (n.d.). SQL commands. https://www.codecademy.com/article/sql-commands
Download magnifying glass clock stopwatch royalty-free stock illustration image - pixabay. Pixabay. (2019, November). https://pixabay.com/illustrations/magnifying-glass-clock-stopwatch-4664710/
Download smileys emotions smartphone royalty-free stock illustration image - pixabay. Pixabay. (2020, November). https://pixabay.com/illustrations/smileys-emotions-smartphone-person-5776137/
Sewell, W. (2024, August). Churn customer data. D211 Advanced Data Acquisition. Western Governor’s University ; Western Governor’s University .
