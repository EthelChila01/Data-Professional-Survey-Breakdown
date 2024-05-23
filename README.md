# Portfolio: Data Professionals Survey

## Power BI project

![powerbi_image](assets/images/powerbi_icon.gif.gif)

This project was developed using raw data collected from social meadia following a survey conducted among professionals in the field of data. The data was transformed using Power Query, and visualizations were created and finalized in a dashboard using Power BI
# Table of contents

- [Objective](#objective)
- [Data source](#data_source)
- [Stages](#stages)
- [Design](#design)
 
# Objective:

## Key Pain Point:
The Head of Human Resources wants to understand the demographics and satisfaction levels of data professionals to enhance recruitment and retention strategies.

### Ideal Solution:
To create a dashboard that provides comprehensive insights into the survey data of data professionals, including their:

   * Countries 
   * Salaries
   * Job titles
   * Ages
   * Gender
   * Programming languages

This dashboard will assist the Human Resources team in making informed decisions to improve recruitment processes, tailor professional development programs, and enhance overall employee satisfaction and retention.

# Data source

The Social Media Department conducted a survey on Twitter, Instagram, Facebook, and LinkedIn, and provided us with [ths resulting raw data](https://github.com/EthelChila01/Data-Professional-Survey-Breakdown/tree/main/assets/dataset)

# Stages

* Design
* Data cleaning
* Analysis
* Visualization

# Design
   *  Dashboard components required
To understand what it should contain, we need to figure out what questions we need the dashboard to answer:
   1. Which countries took part in the survey?
   2. How many people took part in the survey?
   3. What are their average salaries respective of their jobtitles
   4. What is the avarage age of the survey takers?
   5. What is the most their favourite programming language?
   6. How difficult was it to break into the data field (ranked from "easy", "difficult", "Very difficult", "neither easy nor difficult"?
   7. How satisfied are they with their salaries (ranked from 0 to 10)?
   8. How happy are they with their Work-life balance (ranked from 0 to 10)?
For now, these are some of the questions we need to answer, this may change as we progress down our analysis.

## Dashboard mockup
   *  What should it look like?
Some of the data visuals that may be appropriate in answering our questions include:
   1.  A tree map
   2.  Card
   3.  stacked bar chart
   4.  Stacked column chart
   5.  Guage
   6.  Pie chart
![dashboard_mockup](assets/images/data_proffesionals_mockup.png)

# Tools
Tool        | Purpose                                         |
----------- | ------------------------------------------------|
Power query | Exploring,cleaning and transforming the data    | 
Power BI    | Visualizing the data via interactive dashboards |
Mockup AI   | Designing the wireframe/mockup of the dashboard |

# Development                                                                                                                                                                                                                          
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
### Pseudocode
   *  What's the general approach in creating this solution from start to finish?

   1. Import the data to power BI 
   2. Explore the data in power query
   3. Clean the data with power query
   4. Transform the data in power query
   5. Visualize the data in Power BI
   6. Generate the findings based on the insights

## Data exploration notes
This is the stage where you have a scan of what's in the data, errors, inconcsistencies, bugs, weird and corrupted characters etc
Additionally, ensure that you identify the specific columns required for the project. 
   *  What are your initial observations with this dataset? What's caught your attention so far?
      1. Alot of columns are unnecesary for the project and can be deleted
      2. The "Which Title Best Fits Your Current Role" column contains numerous similar options, making it less clear. To simplify this column and reduce the number of options, we will standardize and condense the categories. Specifically, we will split the column where there 
        are parentheses (indicating "Other" options). By doing this, we can create separate columns and subsequently delete the unnecessary one.
      3. The "Favorite Programming Language" column contains many similar entries under the "Other" options, particularly for SQL, which appears in various forms and some other options. To address this, we will split the column at the colon using the colon delimiter. This will 
        allow us to create separate columns and then delete the unnecessary one.
      4. The "Current Yearly Salary" column has to be worked on too because the salaries included in it are in ranges. We need to have the salaries in numerical values because they are in text and at least just one salary instaed of a ranage. What we will do is break up the 
         numbers and put them in two seperate columns using th and then create another column that will give us an avearge for those two numbers by adding them then diving by two. This will at least give us a rounded number, making it more usable instead of the ranges given. 
        To split the columns we will use the 'Digit to Non Digit' option, then delete the unnecessary column with only k,then for the other column replace 'k', '-' and '+'                                                                                                           
                                                                                                                                                                                      with nothing.

                                                                                                                                                                                                                                                                                                                                   






Write the documentation + commentary
Publish the data to GitHub Pages




