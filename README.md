# tableau (Datacamp)

Tableau is a widely used business intelligence (BI) and analytics software trusted by companies like Amazon, Experian, and Unilever to explore, visualize, and securely share data in the form of Workbooks and Dashboards. With its user-friendly drag-and-drop functionality it can be used by everyone to quickly clean, analyze, and visualize your team’s data. We’ll learn how to navigate Tableau’s interface and connect and present data using easy-to-understand visualizations. By the end of this training, we’ll have the skills we need to confidently explore Tableau and build impactful data dashboards. Let’s dive in.

1. Getting started with Tableau
1.1 Introduction
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/a68da773-9e69-420e-b1b0-e360e57e291a)

   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/90183c46-fda2-4498-a14b-b951c9d2ba08)

1.2 Connecting to data
  1.2.1 Loading Workbooks
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/f32b9103-8760-4a03-af93-563a9bf66de9)

  Question: In which year did mobile games overtake console games in terms of revenue?
  2015

  1.2.2 Loading data
  In this exercise we will start by loading the new_york.csv dataset which we will use throughout this section.
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/5fa93eb5-e983-4b84-8c03-17b5cdfb7e49)
  The dashboard gives us an overview of our data - we can see there are 12 fields or columns and we have different data   types indicated at the top of each column:

  # numerical
  Abc text
  globe geographical
  Note: continuous data is green and categorical data is blue.
  The displayed column names can be changed although their remote field name will remain unchanged.

1.3 Navigating Tableau
  1.3.1 Dimensions and measures
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/e066a83b-6c1d-4c6d-bd8d-03def95e7a8d)

  Now that we have connected our data sources let’s now look at the Worksheets interface, where we will create our     visualizations
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/51773933-3993-4d7f-b954-be323f7a3e25)

  Dimensions positioned at the top of the data pane contain qualitative values such as names or dates - in our example Id Neighborhood Room Type.

  Measures positioned below our dimensions contain numerical, quantitative values that can be measured and aggregated - in our example Days Occupied in 2019 Minimum Nights Price and so on.

  Note that we have Reviews Per Month included here. This data is not qualitative, and should be converted to quantitative as shown below:
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/bf8e63f0-6ef5-40d0-9fa1-419d9c67d5f8)

1.4 A tour of interface
  1.4.1 New York Neighbourhood Prices
  Let’s visualize our data. Start by dragging the Neighborhood field to the Rows shelf :
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/ebeefaff-29cf-4d01-8a22-544ba11c80d0)

  Drag the Price field to the Text Marks card :
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/01e600a1-9a7b-420e-a3fe-efb67137d41a)

  Getting the ‘SUM’ of prices does not make much sense.

  However on SUM(Price) at the bottom of the Marks field, click on the down arrow that appears and instead of SUM select Average as the measure :
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/b7b3e3b2-31c9-4902-b170-03ee141d7812)

  Question: What is the average price of a listing in the Brooklyn Heights neighbourhood?
  367

  1.4.2 Segmenting by room type
  Previously we found the average price of rooms in each neighbourhood. Now, we want to know the average number of days listings were occupied in 2019 segmented first by neighbourhood, but also by room type.

  First we need to replace Price from the Marks field with Days Occupied In 2019. We can do this by dragging Price to the Marks pane (until we see a red cross) and then dropping it, and then dragging in Days Occupied In 2019 :
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/946518c7-2513-4d1b-8cda-b403d1d395b4)

  Then get the AVG instead of the SUM :
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/cf0fde2f-6110-4006-9e8c-2d3775670e49)

  And then segment by room type. We can do this by adding Room Type to the Rows shelf :
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/3f87e471-234c-4c6d-ab71-ea0c775ed09c)

  Question: How many days on average were private rooms occupied in Bayside?
  116.5

1.5 How to create visualization in Tableau
  1.5.1 Creating first visualization
  In the previous section we created a table to find out the number of days listings were occupied in 2019 per neighbourhood and rooom type. However a table is tedious to look at, so we would prefer to visualize the results instead.

  However, there are 100+ neighbourhoods in New York, which can be challenging to visualize, so let’s use a prefiltered workbook focusing on a few popular areas for illustrative purposes:
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/8aeecb8d-40c2-4bd0-a3da-b84581442325)

  Click Show Me in the top right and select the stacked barchart option. Note to show numerical values on the face of the bars, click on the T on the dashboard as highlighted below:
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/b388df58-4645-49e0-9091-3d9a0f8f191d)

  1.5.2 Bringing it all together
  To close this section, we will build a visualization on our own from scratch. We will compare occupancy and average prices for each neighbourhood and room type combinations. This would be excellent information to have to hand when deciding whether an investment may be worthwhile.

  Replace the average Days Occupied In 2019 with Price on the bar chart by:
  - dragging Price on top of AVG([Days Occupied In 2019)] in the Rows section
  - changing the aggregation to Average
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/c70d0052-eb65-4d60-99e4-8e650bea0aea)

  Question: WHat is the highest average price for shared room?
  1250
  This value is suspicious - how can a shared room be that expensive and cost more than six times the price of an entire home? This outlier does not necessarily represent an error within our data, and there may a perfectly legitimate reason for the anomaly, however it must be investigated further.

2.1 Filtering and Sorting
![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/6bac5a67-7c5f-45a6-b8f1-defdc2111d9a)

  2.1.1 The order of filtering
The order of filtering is important when dealing with large datasets. The extract and data source filters are applied prior to loading our data into Tableau but we will focus on the Dimension and Measure filters.
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/7bb9dad5-d0cd-4371-99ef-55c3d5908de8)

  2.2 Sorting and filering through selection
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/92ef51cd-429a-4e04-802e-3c574b4218aa)

  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/6b71ed74-959a-4179-87c6-7c95b133738c)

  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/a14c3201-9603-4ae4-938c-e7b6174a19fc)

    2.2.1 Sorting and excluding multiple fields
    Keep only values for 2017 and sort Country alphabetically :

  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/24309eb9-c4be-4365-bf21-52e5ff586d9c)

    Exclude United Arab Emirates from the list, sort by Cell Phones per 100 people in descending order, and keep only the first 10 countries that are listed:

  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/faf0b3fa-ab34-4314-ab8d-d5f448fe79ce)

    Question: Which country had the highest number of cell phones per 100 people in 2017?
    Maldives

  2.2.2 Comparing G7 countries
  The Group of Seven (G7) is an international organization consisting of Canada, France, Germany, Italy, Japan, the United Kingdom, and the United States. In this exercise we will filter data to look only at countries that are part of the G7 with Broadband Subscribers per 100 people greater than 30.

  Navigate to G7 worksheet:
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/fe208e97-8540-4cc2-b251-a5d17e0411d9)

  Filter Country to show countries that make up the G7:
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/ab54b7f3-f4bf-49aa-915d-4985516ffe4d)

  Filter Broadband Subscribers per 100 ppl to show where the value is at least 30 :
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/d1f3e4ed-5930-400a-af1b-fae6f2dd91de)

  Question: Which G7 countries have consistently had at least a value of 30 for Broadband Subscribers per 100 ppl from 2009 onwards? 
  Canada, France, Germany

2.3 Filtering through the filter shelf
Notice that often our data includes nulls. This is misleading because it makes it look like the values are zero, but this might not be the case.

  2.3.1 Filtering for null values
  Navigate to Cell vs Broadband worksheet:
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/2629867f-78ed-4351-bb7d-b4cd5ebc8596)

  We want to know for which countries we lack values for the measures Cell Phones per 100 People and Broadband Subscribers per 100 ppl

  Add Cell Phones per 100 People to the filters card. Select Next and navigate to the Special option in the pop-u. Select Null Values :
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/253551aa-a546-4157-8fcf-49a20b971ea5)

  Repeat the above instruction with the Broadband Subscribers per 100 ppl field :
  ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/7fe89f2a-0bfa-45ef-aa1f-73c40a164bc0)

  Question: Which country has null values for both 'Cell phones per 100 people' and 'Broadband Subcribers per 100 ppl' in 2010?
  Marshall Islands

  Filtering for null values is a useful feature when cleaning and exploring our data, by identifying missing data for follow up.

  2.3.2 Top filters on Tableau
  Now we want to filter countries on their average Cell Phones per 100 People across years 2006-2015. The sum aggregation is set as the default for measures so we’ll have to look out for this.

   Navigate to the Top Filters worksheet :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/375aadb8-9038-4867-b394-abde69663013)

   Add a filter on Country. Use Tableau’s top filter option on the bottom two countries based on the Cell Phones per 100 People average:
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/a5a50655-d4f9-4975-9ed7-ad5764d9eacb)

   Question: Which country has the second lowest average Cell Phones per 100 People ?
   Cuba.

2.4 Aggregation
![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/43d9a040-76c5-4e2f-a158-04b69b7d5239)

   2.4.1 Aggregating measures and dimensions
   Aggregating can be defined as gathering and summarizing data points for analytics. Aggregating measures is more common, but also some dimensions can be aggregated, depending on your use case.
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/211a6e5d-42b3-4618-9a13-1e5ce27c3868)

   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/4b00c47f-c93c-4beb-9055-579171be82e6)

2.5 Scatter plots and aggregations
   2.5.1 CO2 Emmisions and GDP in Sub Regions
In this exercise we will create a scatter plot comparing GDP per Capita and CO2 Emissions per Person. The data points in the scatter plot should represent Sub Regions.

   Open the workbook 2_5_co2emissions_and_gdp_in_sub_regions.twbx and ensure you are in the CO2 and GDP worksheet :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/6bb4d5e1-c709-426c-8cca-d55ef9f5c3b6)

   Create a scatter plot with average GDP per Capita on the x-axis and the average CO2 Emissions per Person on the y-axis :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/ef9b094d-36c1-4243-8cce-7c53ddc1db1c)

   Colour the points based on Sub Regions :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/2e10cc14-b50d-482b-a669-82bcf3fa8d78)

   Question: Based on our scatter plot the values for Eastern Asia and Caribbean sub regions are very different. True or False ?
   False, the values are very similar, the data points overlap on the scatterplot.

   2.5.2 Counting on GDP per capita
   The aggregation options Count and Count (Distinct) are useful for analyzing dimensions and whether they have reached certain dimensions.

   Open the workbook 2_6_counting_on_gdp_per_capita.twbx and navigate to the GDP per Capita :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/c9bde446-be64-4a3a-96db-e53914ad1b9b)

   Create a chart with GDP per Capita (Grouped) as rows and the distinct count of GDP per Capita (Grouped) as columns :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/6a0f5e18-f2ec-4c6b-abda-fe251de2eb29)

   Colour the bars based on Sub Region :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/12fbf29b-808a-4cf8-a452-5479a8eac7bc)

   Question: Which sub-region has been in all six GDP per Capita (Grouped) categories ?
   Western Asia

   2.5.3 Standard deviation of life expectancy
   Standard deviation is a useful aggregation for analyzing how much data varies. In this exercise we will use standard deviation to see how much life expectancy has varied across the years for different countries.

   Load the workbook 2_7_std_dev_of_life_expectancy.twbx and navigate to the Life Expectancy worksheet :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/d49af048-cf1f-482c-bc33-fea8900b0ce7)

   Create a bar chart with the bars representing each country’s standard deviation of life expectancy :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/a917d964-c097-463c-8e4f-cd2252ddd889)

   Consider only the years from 1980 to 2000 :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/7aa70395-59f7-49bd-b03a-8d260029c2ac)

   Question: Which country has the highest standard deviation on the Life Expectancy measure? 
   Lebanon

   Lebanon has the highest standard deviation between the years 1980 to 2000. We would have to analyze further if this relatively large variation was due to increased or decreased quality of life.

   2.6 Calculated fields
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/33037a1a-b538-413d-8ec8-c2ff8dd74ead)

   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/a350d73a-a4c1-41d4-b416-02795dc537b8)

   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/3829268b-7d08-4619-8165-c7754333c5c7)

   There’s no need to memorize all of the functions because of Tableau’s handy built-in documentation :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/784e4adf-e78e-4a61-b3de-ffaafe8eb29d)

   2.7 Creating calculated fields
      2.7.1 Calculated field for rounding
      Open the workbook 2_8_calculated_field_for_rounding.twbx and navigate to the Rounding worksheet :
      ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/910353e6-b312-4dd2-b59a-d90de693be91)

      Create a new calculated field called Rounded Women 25-34 - use the built-in documentation and look up ROUND() and round the new column to whole numbers (0 decimal points) :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/4d04af37-c1ec-4006-9b88-136ea9aca43a)

      Replace Women 25-34 in the Marks field with our newly created field :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/ae0c80e8-b438-42be-b1cc-c38ab97dbf91)

      Remove any existing filters and create new filters for Year = 1976 and >=10 for our newly created field :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/bebb5cef-f988-4f9e-b302-68d31e9dc061)

      Question: How many countries in 1976 had women in the 25-34 age range spending, on average, ten years or more in school ?
      4

   2.7.2 Ratio between genders
   Another useful calculated field to make is a ratio. Ratios are ana excellent way to compare two values. In our case, we can compare the mean years of education between men and women using a ratio. The closer the ratio is to one, the more equal levels of education are between women and men.

   Load the workbook 2_9_ratio_between_genders.twbx and navigate to the Ratio worksheet :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/cb3a7f8b-186e-4837-9705-9e4ad202013e)

   Create a calculated field called Men:Women (25-34) which calculates the men:women ratio for years spent in school in the 25-34 age group. Add this new field as a column to the table by dragging it to the Text card and change the aggregation from sum to average :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/ccc9eaa0-0523-4f9d-952a-9004f7dd7719)

   Question: What is Russia's Men:Women (25-34) ration for years spent in school? 
   0.9821

   Russia has a ratio of ~ 0.98 which means that Russian men have an average of 0.98 years of schooling for every year of schooling that Russian women receive.

   Let’s now create a field for the average across women and women in the age group 25-34.

   Navigate to the Average worksheet:
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/01440934-c68c-4e13-b2bd-837d8d56df25)

   Create a new field called 25-34 that sums the values for men and women in the 25-34 age group and divides them by 2 to get the average:
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/72594304-0ebf-45b8-8348-886645b6e34a)

   Add the new field to the table. Make sure to change the aggregation from SUM to AVG :
   ![image](https://github.com/AIPracticeUser/tableau.io/assets/100339175/c10744ec-a11e-4a5d-865d-167db490909e)

   Question: What is the highest 25-34 average for a country?
   13.40

   Remember, this isn’t a weighted average. To make this calculation more accurate, we could add the country’s population data for each gender and age group. Then we could alter the calculated field’s formula to have weighted proportions.

   

      

   





   


   



   






   




  







  

    




  



  











  







