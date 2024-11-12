# iowa-climbing-analysis

## **Goal**
Examined
1. What are the average quality and difficulty ratings of routes by location? What are the average quality and difficulty ratings by type of route (sport, trad, TR)?
2. Where is the best location for beginner, intermediate, and advanced climbers to find the most amount of high quality routes? At which climbing walls are they located?

## Description
This project uses data sourced from Mountain Project to explore the available rock climbing routes in Iowa, their types, subtypes, wall locations, safety ratings, and average climber reviews. The analysis aimed to extract relevant insights on climb quality, grade, and location. Key tasks included data extraction, data cleaning and refining, exploratory data analysis, and data visualization. 

## Skills
Data cleaning, data visualization, Exploratory data analysis (EDA)

# Cleaning and Refining

## Blanks, Duplicates, Spaces, Formatting
- **Filtered** for blank cells and removed rows with missing data.
- Used **Conditional formatting** to highlight and remove duplicates.
- Used **TRIM() function** to find and remove extra spaces in cells.
- Used **Format as number** for Avg Rating to one decimal point.
- Reviewed for consistent naming conventions (e.g. 5.10a, not 5.10A).
- Used **Text to Column** to separate...
-    Location - Wall Name, Geographic Location, and Nearest City. Added nearest city as necessary. 
-    Type - Route Type (Sport, Trad, or Toprope), Top Rope (TR) Access, and Aid (Y/N).
-    Rating - Yosemite Decimal System, V-scale, and Safety Ratings. (If more than one rating was listed, the higher difficulty or higher risk rating was kept).
- Used **VLOOKUP** to convert grades from the Yosemite Decimal System to the [IRCRA recommended universal scale](https://www.ircra.rocks/single-post/2016/09/12/reporting-grades-in-climbing-research) (see image below). This eliminated issues with analyzing grades with subdivisions (i.e. 5.10c or 5.8+)

## Relevance and Accuracy
- Cross-referenced state park and climbing databases.
- Added nearest city to missing fields. 
- Removed rows with routes under 20ft. 
- Removed Bouldering routes not listed concurrently with Sport, TR, or Trad.
-    Moved bouldering routes and ratings to separate sheet (lost during program crash).

# Exploratory Data Analysis (EDA)

## Overall
- EDA revealed 138 routes across Iowa, 85 sport, 30 trad, and 23 TR.
- Average route quality rating was 2.8/5 stars, with ratings ranging from -1/5 stars to 4/5 stars.
-   Calculated Z-Value to determine outliers, removed -1/5 as an outlier.
- Average IRCRA difficulty rating was 10.8 (5.10b), with ratings ranging from 7 (5.7) to 17 (5.11d).
- Average route height was 41ft.
- ANOVA revealed a statistically significant relationship between Route Quality and Route Difficulty (p = 0.0066), although the model explains only a small portion of the variance (R² = 0.053). The coefficients for the model are estimated with 95% confidence intervals that suggest the relationship is statistically significant.

## Calculations and Tests
![image](https://github.com/user-attachments/assets/758f2302-b8f6-41d8-acaf-23ad05ec4031)

![image](https://github.com/user-attachments/assets/cddc043d-551c-4c3d-ab15-d02b34f1ad19)

![image](https://github.com/user-attachments/assets/6f7b5b49-85cb-4edc-9f33-ad49e7a1dc01)

![image](https://github.com/user-attachments/assets/17d87f3d-42b7-4506-988a-6c5aca954bee)

![image](https://github.com/user-attachments/assets/a18f0b35-cb4f-44ee-b3e0-7cdb769eadf2)

![image](https://github.com/user-attachments/assets/619f97d2-7c9b-494a-9abe-716e88c09d3f)



