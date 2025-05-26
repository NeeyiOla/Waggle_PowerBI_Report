# Building a PowerBI Report for Waggle

## Waggle Pet Device Company: Comparitive Performance of Lapdog and Lapcat Smart device

![Waggle Lapdog and Lapcat Logos](

# Table of Content
- [Project Title](#project-title)
- [My Role](#my-role)
- [Project Overvies](#project-overview)
- [Problem Statement](#problem-statement)
- [Stakeholder Engagement](#stakeholder-engagement)
  - [Target stakeholder](#target-stakeholder)
  - [Use Cases](#use-cases)
  - [Stakeholder Stories](#stakeholder-stories)
  - [Acceptance-Criteria](#acceptance-criteria)
  - [Success Criteria](#success-criteria)
- [Data Source](#data-source)
  - [Dataset](#dataset)
  - [Data model stucture](#data-model-structure)
- [Methodolody](#methodology)
  - [Tool Used](#tool-used)
  - [Development](#development)
    - [Project Planning & Requirement gathering](#project-planning--requirement-gathering)
    - [Data Exploration & Profiling](#data-exploration--profiling)
    - [ETL Process Using Power Query and Data modeling](#etl-process-using-power-query-and-data-modeling)
    - [Measures Developmenr Using DAX](#measures-development-using-dax)
    - [Dashboard Design & Visualisation](#dashboard-design--visualisation)
    - [Plushing and Collaboration](#publishing-and-collaboration)
    - [Documentation & Version control](#documentation--version-control)
    - [Review & Iteration](#review--iteration)
- [Detailed Insights and Recommendation](#detailed-insights-and-recommendations)
  - [CEO Executive Summary](#ceo-executive-summary)
  - [Pet Comaprison (Dogs vs Cats)](#pet-comparison-(dogs-vs-cats))
  - [Household & Demographic Inisghts](#household--demograhpic-insights)

# Project Title
Lapcat vs Lapdog - Performance & Viability Report for Smart Pet De

# My Role
**Business Intelligence Analyst/Power BI Developer**

- Analysed Lapcat prototype vs Lapdog product data.
- Created engaging, executive-level dashboard using Power BI.
- Applied Waggle brand guidelines including logo, color palette, and iconography.
- Built interactive filters, navigation buttons, and bookmarks to enhance exploration.
- Delivered insights to inform product strategy, marketing, and go-to-marketing decisions



# Project Overview 
As a **Business Intelligence Analyst** for **Waggle*, a startup that makes smart devices for pets. Recently, Waggle has been thrilled by the success of their Lapdog device, a **fitness collar that lets owners track their dog's steps, alerts them when it's time for a walk, and even repels fleas**! Reviewa have been fantastic, Sales are growing, and-best of all-the product really works!  


This success has led Waggle's CEO to push for feline version but there are concerns about its viability. For this reason, the product team distributed 1,000 Lapcat prototypes for field testing. Now, after months of data collection, **I have been tasked with delivering a boardroom-ready PowerBI report that tells the story of how the Lapcat data compares to finding from the dog collar Lapdog devices**. I am excited for the fact that my work will be presented at the highest levels of the company and will either help conince the CEO that Lapcat is the next big thing or a costly mistake to be avoided.


# Problem Statement 

The CEO needs eveidence that the Laptcat device improves cat activity levels and provides owner satifaction on par with Lapdog. The CEO, Product and Marketing teams requires as follow:

- The CEO is curious about the following questions:
  - Did the average daily steps ibrease for cats wearing the as they did for dogs?
  - Were ownera of Lapcat devices as satifies with the product as Lapdog owners?
- The chief Marketing officer would like your report to be "on-brand" by including only colors from the waggle color palatte, the waggle logo, and other approved logos and icons.
- The product team trusts ypu tp incorporate other visuals and insights as you see fit but is most interested in demoprahic comparision between the dogs and cats using Waggle devices as well as any information about the families who own the pets. They would also like slicers to help them filter and explore  on their own.

# Stakeholder Engagement 
## Target Stakeholder

- **CEO** (Strategic Decision Making)
- **Chief Marketing Officer** (Brand & Visuals)
- **Product Development Team (Demographic & Performance Analytics)

## Use Caes

- Determine whether Lapcat improves pet fitness like Lapdog.
- Assess owner satifaction and feedback.
- Compare cat vs dog activity by demographic (age,weight, breed).
- Evaluate if specific household types engage more with one product.
- Empower team exploration with branded, interactive visuals.


## Stakeholder Stories

- "As the **CEO**, I want to know if cats wearing Lapcat increased daily steps, so i can justify investment.2
- "As the **CMO**, I want brand consistency in visuals to maintain Marketing intergrity."
- "As the **Product Development Team**, We want to compare pet activity, satifaction, and demographics to tailor future prototypes."

## Acceptance Criteria

- Executive report dashboard or summary page answering CEO questions
- At least 7 different Power BI visuals accross report
- At least 5 slicers per page (dropdown, slider, search, hierachy, select all)
- Use of company colors, logos, icons
- Bookmark features:
  - One to switch between visuals
  - One to reset all filters
- Interactive buttons with hover effect for navigation

## Success Criteria
- Strategic clarity on Lapcat Viability
- Enhanced team understanding of pet demographic behavior
- High executive engagment through interactivity
- Visual appeal reflecting Waggle's branding


# Data Structure 

In support of this project a data model was already provided in a Power BI file by the former Business intelligence analyst which make the success of this project a step closer to the success of this project, the dataset for this project and how it been model to build a successful semantic data model is demostrated below.

## Dataset

#### FACT TABLE:  

**Tracker_Data:**  

| Column Name | Data Type | Description |
| --- | --- | --- |
| Activity_Date | Date | Date of pet activity |
| Activity_Minutes | Whole number | minutes per activities |
| Daily_Steps | Whole number | count of steps for each pet daily |
| Family_ID | whole number | Unique Identifier (Foreign Key) for the Family_data table |
| Heartrate_BPM | Whole number | Heartrate vitals record |
| Pet_ID | Whole number | Unique identifier (foriegn Key) for Pet_Data table |
| Tracker_ID | Whole number | Unique identifier (Primary Key) for each record in the Tracker table |


#### DIMENSION TABLE:

**Family_Data**  

| Column Name | Data Type | Description |
| --- | --- | --- |
| Annual Pet Expenses | Whole Number | Cost of maintaining a pet anually |
| City | Text | City of residence |
| Country | Text | Country of residence |
| Email | Text | Email address of each family |
| Family_ID | Whole Number | Unique identifier each record in the Family data table |
| Family_Name | Text | name of family owning a pet device |
| Household_Income | Decimal Number | Total income made by each family |
| Hoiusehold_Size | Whole Number | Total count of individual in the family |
| State | Text | State of residence |
| Total_Pets | Whole Number | number of pet own by each family |
| Years_Of_Ownership | Whole Number | Count total of years of owning  pet |
| Zip | Whole Number | Country Zip code |


**Pet_Data**  

| Column Name | Data Type | Description |
| --- | --- | --- |
| Age | Whole Number | pet age (lat updated life cylce) |
| Breed | Text | breed group of each pet |
| Dog/Cat | Text | type of pet |
| Gender | Text | sexual orentation of pet |
| Name | Text | Pet name |
| Pet_ID | Whole Number | Unique identifier for each pet in the Pet Data |
| Weight | Whole Number | Measurement of each pet body mass |


**Rating_Data**  

| Column Name | Data Type | Description |
| --- | --- | --- |
| Comments | Text | decsriptions for row |
| Device | Text | type of device  |
| Rating | Whole Number | Rating satifaction from each customer tracker |
| Review_Date | Date | Date when the rating data table was review or updated |
| Tracker_ID | Whole Number | Unique identifier for each tracker device in rating table |
| Where Product was bought | Text | Feedback on a survey question |
| Would you Recommend | Text | feedback on a survey question |


#### DATE TABLE:

| Column Name | Data Type | Description |
| --- | --- | --- |
| Date | Date | Date |
| Day | Whole Number | Day nunbering throughout the year |
| Day_of_Week | Text | Days of the week name in full |
| Month | Text | Month name in full |
| Month_Num | Text | Numbering of Months accordingly |
| Month_Short | Text | Short hand form of a month in words |
| Month_Year | Text | Date period with the combination of Month first and then year |
| Weekday | Whole Number | Days number in a week |
| Year | Text | Year of a Date |
| Year_Month | Text | Date period with the combination Year and month |

## Data model Structure

With the Tracker_Data table being the fact table and the like of Rating_Data, Pet_Data, Family_Data, and Date_table being the dimension tabless, a many-to
-one (*:1) relationship is establish from the Tracker_Data (Fact) table to the Dimension tables which is known as a **Star Schema** data model. the below image demostrate how the dataset is being model in the Model view Pane of power BI desktop.

![Waggle Data model](asset/Images/Star_Schema_data_model.png)

# Methodology 
## Tool Used

- **Power BI Desktop** - Modeling, DAX, report design
- **Power Query** - Data cleaning, ETL
- **Power BI Service** - Collaboration, sharing, Security Level role, and bookmarking
- **Figma** or **Mokkup** - Mockup and layout design planning
- **GitHub** - Version control and documentation

## Development

General Approach to creating the Solution:

### Project Planning & Requirement Gathering

- Met with Waggle Stakeholder to gather business questions and branding requirements.
1. Understanding the data: 
Reviewed the included data model and business questions and identify which fields can be used to design metrics that answer the CEO's questions. (That's all, just understand the data!)
- Scoped key deliverables, visuals, and interactivity features.

### Data Exploration & Profiling
- Profiles tables for nulls, duplicates, and data types
- Checked devices usage consistency and rating completness

### ETL Process Using Power Query and Data modeling (wasn't needed)

### Measures Development Using DAX

### Dashboard Design & Visualisation
- Developed one or more visulisations that specifically address the CEO's question about whether there was a difference in average daily steps over time between the two devices and how Lapcat owners rated their device compared to Lapdog owners.
- Address the product  team's  request for demographic insights, using each of the following visuals at least once, Bar chart, Line chart, Table/Matrix, scatter plot, bubble map, and card.
- Making sure my data visualisations and design an appropriate layout that emphasises the most important fings first, with the CEO's questions answered on the first page, insights about the differences between dogs and cats on the second, and insights about the families who own the pets on the third
- In my data visualisation, incorperatebthe branding elements requested by the Chief Marketing Officer.
- Incorporated at least five slicers on each page with at least one example of a drop-down slicer, at least one example of a slider slicer, at least one example of a hierarchy slicer, at least one example of a slicer with "Select All" enabled, and one example of  a slicer with the search box enabled.
- Created at least two bookmark features. One must allow users to dynamically swap one visual out with different one and another must reset all applied filters on the page/
- Created buttons that help the users navigate the created report. Buttons must respond when users hover them by changing color size.

### Publishing and Collaboration
- Uploaded to Power BI service for real-time sharing
- Enabled usage metric and filter reset bookmark
- Enables Role Level Security (RLS)


### Documentation & Version Control
- README.md and Power BI documentation hosted on GitHub
- PBIX file versioned for feedback cycles

## Review & Iteration
- Conducted dry-run with Stakeholder
- Updated layout and labels for clarity
- Refined slicer configuration based on user testing


# Detailed Insights and Recommendations 
### DASHBOARD 1: CEP Executive Summary

### DASHBOARD 2: Pet Comparison (Dogs VS Cats)
Visuals  

- Donut chart: Device usage by pet gender
- Martix: Avg daily steps by breed and age group
- Scatter Plot: Weight vs Activity correlation
- Bubble map: Pet Concentration by region


### DASHBOARD 3: Household & Demographic Insights 
Visuals:  
- Bar chart: satifaction by owner age group
- Table: Avg steps by household size
- Card: % multi-pet households
- Bubble map: Regional rating variation














