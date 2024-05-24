 # Portfolio: Data Professionals Survey

## Power BI project

![powerbi_image](assets/images/powerbi_icon.gif.gif)

This project was developed using raw data collected from social meadia following a survey conducted among professionals in the field of data. The data was transformed using Power Query, and visualizations were created and finalized in a dashboard using Power BI
# Table of contents

- [Objective](#objective)
- [Data source](#data_source)
- [Stages](#stages)
- [Design](#design)
- [Development](#development)
  -  [Data exploration notes](data_exploration_notes)
  - [Data_cleaning](#data_cleaning)
- [DAX_meausres](#dax_measures)
- [Visualization](#visualization)
 
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
   6. How difficult was it to break into the data field (ranked from "ea
   7. What is the average salary per gender?
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
   2. The "Which Title Best Fits Your Current Role?" column contains numerous similar options, making it less clear. 
   3. The "Favorite Programming Language?" column contains many similar entries under the "Other" options, particularly for SQL, which appears in various forms and some other options. 
   4. The "Current Yearly Salary" column needs to be standardized, as it currently contains salary ranges in text format. We require these salaries to be in numerical values and represented by a single number rather than a range. 
   5. The "What Industry do you work in?" column also has so many Countries repeated and writen in different forms under the "Other" option. 
   6. The "Which Country do you live in?" column also has so many Countries repeated and writen in different forms under the "Other" option. 
## Data cleaning
   * What do we expect the clean data to look like? (What should it contain? What contraints should we apply to it?
The aim is to refine our dataset to ensure it is structured and ready for analysis.

The cleaned data should meet the following criteria and constraints:

   *  Only relevant columns should be retained.
   *  All data types should be appropriate for the contents of each column.
   *  No column should contain null values, indicating complete data for all records.
     
What steps are needed to clean and shape the data into the desired format?
   *  Remove unnecessary columns by deleting the ones we don't need
   *  Simplify some columns and reduce the number of options by condesing categories
   *  Delete some characters and letters that are not needed
Below are some steps that were taken in order work on the issues mentioned [here](#data_exploration_notes);

#### "Which Title Best Fits Your Current Role?" column
   * To simplify this column and reduce the number of options, we will standardize and condense the categories. Specifically, we will split the column where there 
      are parentheses (indicating "Other" options). By doing this, we can create separate columns and subsequently delete the unnecessary one.
     ![splitting_the_title_column](assets/images/split_the_title_column.png)
#### "Favorite Programming Language?" column
    * To address the issues found in this column, we will split the column at the colon using the colon delimiter. This will 
      allow us to create separate columns and then delete the unnecessary one.
   ![splitting_the_favourite_language_column](assets/images/split_the_favourite_language_column.png)
      
#### "Current Yearly Salary" column
   *  To achieve what was mentioned regarding the issues found in this column, we will split the salary ranges into two separate columns.To split the columns, we will use the 'Digit to Non-Digit' option. We will then delete the unnecessary column containing only the letter 
      'k'. For the other column with "k" and "-", we will replace them with nothing(leave black), and '+' with '225' for the ones that earn 225 plus. Finally, we will create a new column for the 
      average salary and remove the intermediate columns used for this calculation.. Then, we will create an additional column that calculates the average of these two numbers by summing them and dividing by two. This will 
      provide a more usable, rounded figure instead of the given ranges.

      a.
      ![splitting_the_yearly_salary_column](assets/images/split_the_yearly_salary_1.png)
      b.
      ![replacing_k](assets/images/replace_k_.png)
      c.
      ![replacing_minus](assets/images/replace_minus.png)
      d.
      ![replacing_plus_with_225](assets/images/replacing_plus_with_225.png)
      
#### "What Industry do you work in?" column 
   *  We will split column where there are parenthesis (indicating "Other" options). By doing this, we can create separate columns and subsequently delete the unnecessary ones.
      ![plitting_the_industry_column_image](assets/images/split_the_industry_column.png)
#### "Which Country do you live in?" column
   *  We will split column where there are parenthesis (indicating "Other" options). By doing this, we can  By doing this, we can create 
      separate columns and subsequently delete the unnecessary ones.
     ![splitting_countries_column5](assets/images/split_countries.png)
     

# Visualization
![the_dashboard](assets/images/the_dashboard.gif)
  
    
      

      
      
                                          
                                                                                                                                                                                      

                                                                                                                                                                                                                                                                                                                                   



                                                                     

Write the documentation + commentary
Publish the data to GitHub Pages




