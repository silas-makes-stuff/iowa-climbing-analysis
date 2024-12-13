# iowa-climbing-analysis

## **Goal**
Examined
1. What are the average quality and difficulty ratings of routes by location? What are the average quality and difficulty ratings by type of route (sport, trad, TR)?
2. Where is the best location for beginner, intermediate, and advanced climbers to find the most amount of high quality routes? At which climbing walls are they located?

## Description
This project uses data sourced from Mountain Project to explore the available rock climbing routes in Iowa, their types, subtypes, wall locations, safety ratings, and average climber reviews. The analysis aimed to extract relevant insights on climb quality, grade, and location. Key tasks included data extraction, data cleaning and refining, exploratory data analysis, and data visualization using Excel and Tableau. 

## Skills
Data cleaning, data visualization, Exploratory data analysis (EDA)

## Technology
Excel, Tableau

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

## Calculations

| Figure        |    Overall    |     Sport     |      TR       |     Trad      |
| ------------- | ------------- | ------------- | ------------- | ------------- |
|Total Routes   |      138      |      85       |      23       |      30       |
|Quality Rating |     2.8/5     |      2.9      |       3       |      2.5      |
|IRCRA Rating   |     10.8      |      12       |       9       |      9        |

<img
  src="https://github.com/user-attachments/assets/cddc043d-551c-4c3d-ab15-d02b34f1ad19"
  alt="The image is a table summarizing statistical data for Route Quality /5 stars,'Route Difficulty,' and 'Route Height, ft.' Route Quality /5 stars; Mean: 2.84; Max: 4.0; Min: 1.0; Median: 2.80; Mode: 3.0; Standard Deviation: 0.67; High; Frequency Range: 2.5, 3.0; Low Frequency Range: 1.0, 1.5; Route Difficulty; Mean: 10.88; Max: 17.0; Min: 7.0; Median: 10.0; Mode: 10.0; Standard Deviation: 3.20; High Frequency Range: 7, 9; Low Frequency Range: 11, 14; Route Height, ft, mean: 41, Max: 85, Min: 20, Median: 40, Mode: 30, Standard Deviation: 14.85, High Frequency Range: 20, 30, Low frequency range: 80, 90. R squared Difficulty/Height, 0.0097; R squared Quality/Difficulty, 0.0534; R squared quality height 0.0005"
  width="500"
  height="300" />

<img
  src="https://github.com/user-attachments/assets/6f7b5b49-85cb-4edc-9f33-ad49e7a1dc01"
  alt="The image is a bar chart titled 'Quality Rating Frequency.' The x axis displays the frequency of quality ratings within specified intervals of 5 stars. The y-axis displays the frequency count. The intervals have the following approximate counts: 1.0, 1.5, Around 5; 1.5, 2.0: Around 15; 2.0, 2.5: Around 20; 2.5, 3.0: Around 55 (highest frequency); 3.0, 3.5: Around 10; 3.5, 4.0: Around 20; The chart shows that the most frequent ratings fall in the 2.5, 3.0 interval"
  width="500"
  height="300" />

  <img
  src="https://github.com/user-attachments/assets/17d87f3d-42b7-4506-988a-6c5aca954bee"
  alt="It shows the frequency of route heights within specified intervals on the x-axis and the frequency count on the y-axis. The intervals are as follows, with approximate frequencies: 30, 40: ~35; 40, 50: ~20; 50, 60: ~10; 60, 70: ~10; 70, 80: ~5; 80, 90: ~2. The chart highlights that the most common route height falls in the 20, 30 interval, with a significant decline in frequency as the height increases."
  width="500"
  height="300" />

  <img
  src="https://github.com/user-attachments/assets/a18f0b35-cb4f-44ee-b3e0-7cdb769eadf2"
  alt="The image is a bar chart titled Difficulty Frequency. It displays the frequency of route difficulties within specific intervals on the x-axis and the frequency count on the y-axis. The intervals and approximate frequencies are: 9, 11: ~35; 11, 14: ~10; 14, 16: ~20; 16, 18: ~10. The chart indicates that the majority of routes fall within the difficulty range of 7, 9, with a notable decrease in frequency as the difficulty increases."
  width="500"
  height="300" />

  <img
  src="https://github.com/user-attachments/assets/619f97d2-7c9b-494a-9abe-716e88c09d3f"
  alt="The image is a scatter plot titled Difficulty/Quality with an R squared value of 0.0534. It displays the relationship between route quality (x-axis) and route difficulty (y-axis). The x-axis ranges from 0.0 to 4.5, representing route quality ratings. The y-axis ranges from 6 to 18, representing route difficulty levels. The data points are scattered, showing a weak positive trend. A dotted trend line is included, indicating a slight upward slope. The low value of 0.0534 suggests a weak correlation between difficulty and quality."
  width="500"
  height="300" />

  # Dashboards

  ## Excel
  Excel dashboard can be accessed [here](Climbing_Iowa_Dashboard.xlsx). 

  ## Tableau
  Tableau dashboard can be accessed [here](https://public.tableau.com/shared/5FDZSPRFP?:display_count=n&:origin=viz_share_link) or [here as a .twbx](https://public.tableau.com/shared/HPMX24W5Z?:display_count=n&:origin=viz_share_link) 


